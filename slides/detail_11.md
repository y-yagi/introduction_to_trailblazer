## View Model

* [cells: View components for Ruby and Rails.](https://github.com/apotonick/cells)

```ruby
class Comment::Cell < Cell::ViewModel
  property :body
  property :author

  def show
    render
  end

  private
    def author_link
      link_to "#{author.email}", author
    end
end
```

```erb
<div class="comment">
  <%= body %>
  By <%= author_link %>
</div>
```
