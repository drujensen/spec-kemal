# spec-kemal

Kemal helpers to Crystal's `spec` for easy testing.

## Installation

Add it to your `shard.yml`.

```yaml
name: your-kemal-app
version: 0.1.0

dependencies:
  spec-kemal:
    github: sdogruyol/spec-kemal
    branch: master
  kemal:
    github: sdogruyol/kemal
    branch: master
```

## Usage

Just require it before your files in your `spec/spec_helper.cr`

```crystal
require "spec-kemal"
require "../src/your-kemal-app"
```

Now you can access your `Kemal` application in your `spec`s.

```crystal
# spec/your-kemal-app-spec.cr

describe "Your::Kemal::App" do

  it "renders #index" do
    response = HTTP::Client.get "http://localhost:3000/"
    response.body.should eq "Hello World!"
  end

end
```

## Contributing

1. Fork it ( https://github.com/sdogruyol/spec-kemal/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [sdogruyol](https://github.com/sdogruyol) Sdogruyol - creator, maintainer