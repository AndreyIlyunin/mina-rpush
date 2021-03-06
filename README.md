# mina-rpush

Mina tasks for [rpush](https://github.com/rpush/rpush) deployment.

This version of gem is compatible with Mina 1.x, [check out older version for 0.3 support](https://github.com/d4rky-pl/mina-rpush/tree/mina-0.3)

## Installation

```ruby
# Gemfile
gem 'mina-rpush', require: false
```

## Usage

```ruby
# config/deploy.rb

require 'mina/rpush'

task deploy: :environment do
  deploy do
    ...

    on :launch do
      ...
      invoke 'rpush:restart'
    end
  end
end
```

## Tasks

```
mina rpush:restart  # Restart rpush (stop + start)
mina rpush:start    # Start rpush
mina rpush:stop     # Stop rpush
mina rpush:push     # Deliver all pending notifications
mina rpush:status   # Shows status of the running Rpush instance
```

## Thanks

Thanks to the author of [mina-clockwork](https://github.com/907th/mina-clockwork) for giving me a starting point in developing this gem.

## Contributing

Feel free to contribute!
