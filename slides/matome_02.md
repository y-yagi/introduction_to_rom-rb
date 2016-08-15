
## まとめ

* `rom-sql`と同じ使い方で他のdatastoreに対して処理が行えるかと思ったが、割と駄目
  * gem側で機能が足りてない事が多い
    * `Command`が実装されてないとか、`Schemas`が実装されてないとか割とある
      * Readは出来るが、Writingが出来ないgemとかある
  * まともに開発がされているadapter、`rom-sql`だけなのでは感が
