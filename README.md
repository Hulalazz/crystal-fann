# crystal-fann

Crystal bindings for the FANN C lib

## Installation

Add this to your application's `shard.yml`:

```yaml
dependencies:
  crystal-fann:
    github: bararchy/crystal-fann
```

## Usage

Look at the spec for most functions

```crystal
require "crystal-fann"
ann = Crystal::Fann::Network.new(2, [2], 1)
500.times do
  ann.train_single([1.0_f32, 0.1_f32], [0.5_f32])
end
result = ann.run([1.0_f32, 0.1_f32])
# Remmber to close the network when done to free allocated C mem
ann.close
```

TODO: Write usage instructions here

## Development

TODO: Write development instructions here

## Contributing

1. Fork it ( https://github.com/bararchy/crystal-fann/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [bararchy](https://github.com/bararchy) - creator, maintainer
