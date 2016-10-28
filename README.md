# heroku-buildpack-apt

Add support for apt-based dependencies during both compile and runtime.

This project is a fork of the deprecated [ddollar/heroku-buildpack-apt](https://github.com/ddollar/heroku-buildpack-apt) repository. Please consider this to be completely separate from the originating project.

## Usage

This buildpack is not meant to be used on its own, and instead should be in used in combination with Heroku's [multiple buildpack support](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app).

Include a list of apt package names to be installed in a file named `Aptfile`

## Example

#### Command-line

    heroku buildpacks:add --index 1 https://github.com/kckrinke/heroku-buildpack-apt

#### .buildpacks

    https://github.com/kckrinke/heroku-buildpack-apt
    https://github.com/heroku/heroku-buildpack-ruby

#### Aptfile

    libpq-dev
    http://downloads.sourceforge.net/project/wkhtmltopdf/0.12.1/wkhtmltox-0.12.1_linux-precise-amd64.deb

## License

MIT
