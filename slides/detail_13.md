## Representer

* [representable: Maps representation documents from and to Ruby objects. Includes JSON, XML and YAML support, plain properties and compositions.](https://github.com/apotonick/representable)
* RubyオブジェクトをJSONやXMLに変換する為の処理を定義する箇所

```ruby
class SongRepresenter < Representable::Decorator
  include Representable::JSON

  property :title
  property :track
end
```

```
SongRepresenter.new(song).to_json
#=> {"title":"Fallout","track":1}
```
