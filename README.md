# Coffeebox

This is an opinionated rewrite of [Facebox](http://defunkt.github.com/facebox/).

## Features

1. Everything is converted to coffescript
2. Shipped as a Rails 3.2/4.0 asset pipeline compatible gem
3. Zero images: Includes [spin.js](http://fgnass.github.io/spin.js/) instead of a gif preloader, and uses &times; (&amp;times;) as a close button
4. Preloads displayed images with [imgpreload](https://github.com/farinspace/jquery.imgpreload)
5. Built-in support for turbolinks
6. Does not stay in DOM when closed
7. Proper show/hide of overlay (no blinking when loading -> loaded)
8. Configurable SASS styling

## List of removed Facebox features:

1. Overlay opacity setting - please use CSS instead

## Installation

Add this line to your application's Gemfile:

    gem 'coffeebox'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install coffeebox

## Loading

Require it in application.js

    //= require coffeebox

Or in in application.js.coffe

    #= require coffeebox

and in application.css.sass:

    //= require coffeebox

or import SASS file directly (from sass\scss only)

    // Set some options
    $facebox-background: #fff
    $facebox-close-color: #000
    $facebox-close-hover: #333
    $facebox-close-size: 25px
    $facebox-border: 3px solid rgba(0, 0, 0, 0)
    $facebox-border-radius: 25px

    // Then import
    @import coffeebox

## Usage

    $.coffeebox('test <b>html</b>')
    $.coffeebox(image: 'http:://...')
    $.cbox.loading()
    $.cbox.close()

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
