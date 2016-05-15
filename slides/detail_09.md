## Callback

* operationクラスで実行するCallback処理を定義する
* operationクラスに直接定義しても良いし、当然別ファイルに分けても良い

```ruby
class Comment::Create < Trailblazer::Operation
  callback :after_save do
    # this is a Disposable::Callback::Group class.
  end
end
```

```ruby
class AfterSave < Disposable::Callback::Group
  on_change :notify!
end
```
