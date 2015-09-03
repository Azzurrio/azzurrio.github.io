---
layout:     post
title:      "Hello World"
subtitle:   "It all start with a big bang"
date:       2015-09-04 12:00:00
author:     "Karim El-Husseiny"
header-img: "img/hello-world.jpg"
---
#Code Example
That's just a example of my custom code highlighting
{% highlight ruby %}
  def parse_body(body, tokens)
    body.parse(tokens, parse_context) do |end_tag_name, end_tag_params|
      @blank &&= body.blank?

      return false if end_tag_name == block_delimiter
      unless end_tag_name
        raise SyntaxError.new(parse_context.locale.t("errors.syntax.tag_never_closed".freeze, block_name: block_name))
      end

      # this tag is not registered with the system
      # pass it to the current block for special handling or error reporting
      unknown_tag(end_tag_name, end_tag_params, tokens)
    end

    true
  end
{% endhighlight %}

