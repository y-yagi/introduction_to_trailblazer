## Model

* Modelにはassociaton、scope、finderのみを定義する
* 当然ビジネスロジックは書かない
* callback / validationも書かない

```ruby
class Comment < ActiveRecord::Base
  has_many   :users
  belongs_to :thing

  scope :recent, -> { limit(10) }
end
```
