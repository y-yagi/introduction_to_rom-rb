
## `Command`

`rom-sql`の[`Create Command`](https://github.com/rom-rb/rom-sql/blob/master/lib/rom/sql/commands/create.rb)

```ruby
require 'rom/sql/commands/error_wrapper'
require 'rom/sql/commands/transaction'

module ROM
  module SQL
    module Commands
      # SQL create command
      #
      # @api public
      class Create < ROM::Commands::Create
        adapter :sql

        include Transaction
        include ErrorWrapper

        use :associates
        use :schema

        # Inserts provided tuples into the database table
        #
        # @api public
        def execute(tuples)
          insert_tuples = with_input_tuples(tuples) do |tuple|
            attributes = input[tuple]
            validator.call(attributes)
            attributes.to_h
          end

          if insert_tuples.length > 1
            multi_insert(insert_tuples)
          else
            insert(insert_tuples)
          end
        end

        private

        # Executes insert statement and returns inserted tuples
        #
        # @api private
        def insert(tuples)
          pks = tuples.map { |tuple| relation.insert(tuple) }
          relation.where(relation.primary_key => pks).to_a
        end

        # Executes multi_insert statement and returns inserted tuples
        #
        # @api private
        def multi_insert(tuples)
          pks = relation.multi_insert(tuples, return: :primary_key)
          relation.where(relation.primary_key => pks).to_a
        end

        # Yields tuples for insertion or return an enumerator
        #
        # @api private
        def with_input_tuples(tuples)
          input_tuples = Array([tuples]).flatten.map
          return input_tuples unless block_given?
          input_tuples.each { |tuple| yield(tuple) }
        end
      end
    end
  end
end
```
