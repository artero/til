# Create a single-file executable with dependencies

Bundle has an option that allows loading dependencies when you execute a file
[require 'bundler/inline'](https://bundler.io/v2.0/guides/bundler_in_a_single_file_ruby_script.html)

When executing a file with this code the script will automatically install any missing gems. 

An example using [Thor](http://whatisthor.com/):

```ruby
#!/usr/bin/env ruby

require 'bundler/inline'

gemfile do
  source 'https://rubygems.org'
  gem 'thor'
end

class MyCLI < Thor
  desc "hello NAME", "say hello to NAME"
  def hello(name)
    puts "Hello #{name}"
  end
end

MyCLI.start(ARGV)
```
