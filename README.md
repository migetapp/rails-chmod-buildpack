# `miget/rails-chmod-buildpack`

The Rails Chmod Buildpack is a [Miget](https://miget.com) Buildpack (for Paketo-based applications) designed to address an issue with certain Rails apps running on Jammy stacks: [paketo-buildpacks/ruby#889](https://github.com/paketo-buildpacks/ruby/issues/889).

It is optimized for use with the [Miget Ubuntu 22 Full Builder](https://github.com/migetapp/builder-ubuntu22-full).

Generally, it should work with `paketobuildpacks/builder-jammy-full`, but unfortunately, `paketobuildpacks/builder-jammy-full` is currently experiencing an issue documented in [Issue 556](https://github.com/paketo-buildpacks/builder-jammy-full/issues/556).


## Behavior
This buildpack performs the following action:
* Changes the permission of the `./tmp` directory from `744` to `775` in the root directory of the Rails application.

## Bindings
This buildpack does not include any Paketo Bindings.

## License
This buildpack is released under version 2.0 of the [Apache License][a].

[a]: http://www.apache.org/licenses/LICENSE-2.0
