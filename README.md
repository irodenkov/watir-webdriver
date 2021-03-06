watir-webdriver
===============

Watir implementation built on WebDriver's Ruby bindings.
See http://rubyforge.org/pipermail/wtr-development/2009-October/001313.html.

API docs
--------

http://jarib.github.com/watir-webdriver/doc/

Example
-------
```ruby

require 'watir-webdriver'

browser = Watir::Browser.new :firefox
browser.goto "http://google.com"
browser.text_field(:name => 'q').set("WebDriver rocks!")
browser.button(:name => 'btnG').click
puts browser.url
browser.close
```

Description
-----------

The file in lib/watir/elements/generated.rb is autogenerated from the HTML5 spec. This is done by extracting the IDL parts from the spec and processing them with the WebIDL gem (link below).

Specs
-----

watir-webdriver uses the watir2 branch of watirspec for testing. After cloning, you should fetch the submodule:

    git submodule init && git submodule update

Specs specific to watir-webdriver are found in spec/*_spec.rb, with watirspec in spec/watirspec.

See also
--------

* http://github.com/jarib/webidl
* http://github.com/jarib/watirspec/tree/watir2
* http://selenium.googlecode.com

Dependencies
------------

* selenium-webdriver

Note on Patches/Pull Requests
-----------------------------

* Fork the project.
* Make your feature addition or bug fix.
* Add tests for it. This is important so I don't break it in a
  future version unintentionally.
* Commit, do not mess with rakefile, version, or history.
  (if you want to have your own version, that is fine but bump version in a commit by itself I can ignore when I pull)
* Send me a pull request. Bonus points for topic branches.

Copyright
---------

Copyright (c) 2009-2011 Jari Bakken. See LICENSE for details.
