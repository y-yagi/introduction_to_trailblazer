## Policy

* 認可処理
* [pundit](https://github.com/elabs/pundit)っぽく書ける
  * "policy class is heavily inspired by the excellent Pundit gem"との事
* punditで書いたpolicy classをそのまま使う事も可能

```ruby
class Thing::Policy
  def initialize(user, thing)
    @user, @thing = user, thing
  end

  def create?
    admin?
  end

  def admin?
    @user.admin == true
  end
  # ..
end
```
