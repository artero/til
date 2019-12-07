# Keynote gem concatenate tags with rumble

Keynote comes with a version of the gem [Rumble](https://github.com/judofyr/rumble),
an HTML markup in Ruby.

You can have problems with some Rails helpers that generate tags, like link_to in
this cases you can use the `text` method followed with the tag helper

```ruby
p.author do
  text 'Written by '
  a 'Bluebie', :href => 'http://creativepony.com/'
  br
  text link_to 'Home', '/'
end
```

* Ref: https://rubydoc.info/gems/keynote/Keynote/Rumble
