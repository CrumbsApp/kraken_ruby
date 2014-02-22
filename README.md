# KrakenRuby

This gem is a wrapper for the [Kraken Digital Asset Trading Platform](https://www.kraken.com). 

The current version (0.1.0) can only be used for querying public market information. The next version of the gem will allow for access to private account information.

Below are the instructions for installing and using the gem.

## Installation

Add this line to your application's Gemfile:

    gem 'kraken_ruby'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install kraken_ruby

## Usage

Create a Kraken client:

```ruby
API_KEY = '3bH+M/nLp......'
API_SECRET = 'wQG+7Lr9b.....'

kraken = Kraken::Client.new(API_KEY, API_SECRET)

time = kraken.server_time
time.unixtime #=> 1393056191
```

### Public Data Methods

#### Server Time

This functionality is provided by Kraken to to aid in approximating the skew time between the server and client.

```ruby
time = kraken.server_time

time.unixtime #=> 1393056191
time.rfc1123 #=> "Sat, 22 Feb 2014 08:28:04 GMT"
```

#### Asset Info

Returns the assets that can be traded on the exchange. This method can be passed ```info```, ```aclass``` (asset class), and ```asset``` options. An example below is given for each:

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
