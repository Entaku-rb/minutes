# Entaku.rb #2: gemのデバッグ


## 参加者

* okuramasafumi
* ima1zumi
* osyo
* s4na


## テーマ

* gemのデバッグ/リーディング方法
    * binding.pryは神だけどそれだけではわからない
* 起点を探して読む
    * activerecordならhas_oneとか
* 全体を掴むのは難しい
    * 疎結合な設計であるなら全体を掴む必要はない
* 全体がどういう機能で分かれているのか意識する必要はありそう
    * 調べたい機能がどの機能に所属しているのか
* どこで実装されているのは意識する必要はある
    * irb なら https://github.com/ruby/irb
    * reline なら https://github.com/ruby/reline
* 設計そのものが変化するばあい 
    * 設計をメタ知識として習得する必要がある？
* ドキュメントを読んで見る
    * https://api.rubyonrails.org/
    * https://api.rubyonrails.org/classes/ActiveRecord/Core.html#method-i-slice
    * 定義元とか書いてあることがある
* 自分が思っている箇所とは違う場所で実装されていることはままある
    * ActiveRecord で実装されていると思ったら実は ActiveModel だったり
* Rubyの世界だと素直にgrepしても実装が見つからないときがある（メタプログラミング）
    * `class_eval`や`define_method`で調べると見つかるかも、という知識が重要
* メソッドの定義元を調べるのに Ruby の機能を使う
    * `obj.method(:hoge).source_location` や `obj.instance_method(:hoge).source_location`
* 一人でコードを読むのは大変
    * みんなでコードを読もう
    * twitter で実況
    * 解説記事


