# 現場Railsの勉強用リポジトリ
このリポジトリは現場で使えるRuby on Rails5 速習実践ガイドの勉強リポジトリです。


#### simple_format
- 使用例：`simple_format(h(@task.description), {}, sanitize: false, wrapper_tag: "div")`

ブラウザ場では改行しているように表示されない。そのため、文字列内の改行を<br>タグなどに変換する必要がある。
そのような場合に簡単に使える便利メソッド、simple_formatがデフォルトで用意されている。詳しくはAPIリファレンス..

### 登録・更新操作

|  メソッド  |  メソッドの説明  | 検証を行うか　 |
| ---- | ---- | ---- |
| #save<br>#save! | オブジェクトの現状通りに登録・更新を行う。 | ◯ |
| #update<br>#update!<br>#update_attributes<br>#update_attributes! | 変更内容を引数に指定して更新を行う。<br>save, save!を更新用途に便利にしたもの。 | ◯ |
| #updated_attribute | 1つの属性の変更を行う。検証は行わないがその他の点はsaveと同様 | x |
| #update_column<br>#update_columns | 変更内容を引数で指定して更新を行うが、モデルに実装された検証や次節で説明するコールバックなどを実行せず、直接的に更新SQLを更新する。 | x |
| .create<br>.create! | オブジェクトを生成してsave/save!を実行する | ◯ |
| .update_all | 更新SQLを実行する。検証やコールバックは実行されない | x |

