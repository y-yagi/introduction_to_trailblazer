## Views

* view層はそのまま使える
* ただ、パーツ毎にcellを使い、viewはシンプルな状態のままにしておくことが推奨されている

```erb
<h1>Comments for <%= @thing.name %></h1>

 This was created <%= @thing.created_at %>

   <%= concept("comment/cell",
   collection: @thing.comments) %>
```
