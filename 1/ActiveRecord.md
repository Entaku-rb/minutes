# Entaku.rb#1

## ActiveRecord

### メンバー

* @osyo
* @s4na
* @ima1zumi

### 話したいこと

* どういう SQL が裏で発行されているのか
  * rails cで見る

* explainを見る
* `.to_sql`
    * ActiveRecord_Relationクラス

* scopeとは
    * DRY
    * ActiveRecord_Relationのままメソッドチェーンできるようになる
        * クラスメソッドだと返り値がオブジェクトのインスタンスになる
    * 複雑なクエリを名前付けできる
    * ActiveRecord_Relationが返る


* Hoge has_many foo
  * Hoge.find_by(foos: nil)
  * Hoge.where.not(ids: Foo.where.not(hoge_id: nil))
* Bug report
  * https://qiita.com/QUANON/items/eda79c2b32fba99215ce


#### ActiveRecordで遊びたい

https://github.com/rails/rails/blob/master/guides/bug_report_templates/active_record_gem.rb