# StampI18n

[![Build Status](https://secure.travis-ci.org/karpiu/stamp-i18n.png)](http://travis-ci.org/karpiu/stamp-i18n)

Little plugin for 'stamp' gem. It uses I18n locale files to customize date and time stamps.

## Installation

Add this lines to your application's Gemfile:

    gem 'stamp'
    gem 'stamp-i18n'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install stamp
    $ gem install stamp-i18n

## Usage

Same as in [http://rubydoc.info/gems/stamp](http://rubydoc.info/gems/stamp) but instead of using method 'stamp' like this:

    date = Date.new(2011, 6, 9)
    date.stamp("March 1, 1999")         #=> "June  9, 2011"
   
we are using new method 'localize_stamp' like this:

    date = Date.new(2011, 6, 9)
    date.localize_stamp("March 1, 1999")         #=> "junio  9, 2011" if locale is :de
    date.localize_stamp("March 1, 1999")         #=> "czerwiec  9, 2011" if locale is :pl
    
Note that we are still using english names as examples passed to stamp methods.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
