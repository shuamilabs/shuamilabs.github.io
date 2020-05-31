# my-lab

Welcome to simple plain my-lab theme! In this directory, you'll find the files you need to be able to package up your theme into a gem. Put your layouts in `_layouts`, your includes in `_includes`, your sass files in `_sass` and any other assets in `assets`.

To experiment with this code, add some sample content and run `bundle exec jekyll serve`


## Installation

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "my-lab"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: my-lab
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install my-lab

## Image
![main page](/assets/images/my_lab01.jpg)
![post page](/assets/images/my_lab02.jpg)

## Usage
### default layouts files
- category.html
- default.html
- page.html
- post.html

### includes files
- discussion.html
- footer.html
- header.html
- navigation.html

### pages

Create about.md, categories.md, contact.md and index.html in your root directory (if not exist).

__index.html__

```
---
layout: default
title: Posts
pagination: 
  enabled: true
---
Index page
```

__about.md__

```
---
layout: page
title: About
permalink: /about/
---
About page
```

__categories.md__

```
---
layout: page
title: Categories
permalink: /categories/
---
{% for category in site.categories %}
  - [{{category | first}}]({{site.url}}{{site.baseurl}}{{page.url}}{{category | first}})
{% endfor %}
```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/shuamilabs/mylab-jekyll. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

