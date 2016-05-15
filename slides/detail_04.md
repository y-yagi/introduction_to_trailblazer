## Controller

* HTTPのエンドポイントとしての処理のみを書く
  * リダイレクトやviewのrenderなど
* 当然ビジネスロジックは書かない

```ruby
class CommentsController < ApplicationController
  def new
    form Comment::Update
  end

  def create
    run Comment::Update do |op|
      return redirect_to comments_path(op.model)
    end

    render :new
  end
end
```
