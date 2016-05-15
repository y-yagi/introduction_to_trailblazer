## Form

* [reform: Form objects decoupled from models.](https://github.com/apotonick/reform)
* form object
* validationはここに定義する
* operationクラスに直接定義しても良いし、当然別ファイルに分けても良い

```ruby
contract do
  property :body
  validates :body, length: {maximum: 160}

  property :author do
    property :email
    validates :email, email: true
  end
end
```
