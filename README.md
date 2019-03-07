# 現場Railsの勉強用リポジトリ
このリポジトリは現場で使えるRuby on Rails5 速習実践ガイドの勉強リポジトリです。


#### simple_format
- 使用例：`simple_format(h(@task.description), {}, sanitize: false, wrapper_tag: "div")`

ブラウザ場では改行しているように表示されない。そのため、文字列内の改行を<br>タグなどに変換する必要がある。
そのような場合に簡単に使える便利メソッド、simple_formatがデフォルトで用意されている。詳しくはAPIリファレンス..

