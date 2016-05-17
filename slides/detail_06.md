## Operation

* ビジネスロジックを定義する(service object)
* modelを保存する処理を定義するのはOperationだけ
* validation / callback / authorizationもOperationに含まれる

```ruby
class Comment::Create < Trailblazer::Operation
  contract do
    property :body
    validates :body, length: {maximum: 160}
  end

  def process(params)
    if validate(params)
      ...
    else
      ...
    end
  end
end
```
