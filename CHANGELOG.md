# Change Log

All notable changes to this project will be documented in this file.

## Unreleased

## [0.1.3] - 2015-06-19

### Added

* You can now change the configuration at runtime. Example:

```ruby
UserImport.new(file: csv_file) do
  after_build do
    user.import_by_user = current_user
  end
end
```

* Add `after_build` hooks to perform arbitrary operations on a model
before saving it.

* `identifier` does not have to be a required attribute anymore. That
  enables you to use `id` as an identifier and import new entries
without having to provide an `id`

## [0.1.2] - 2015-06-15

### Fixed

* `run!` was not *returning* a report object when the header was invalid.

## [0.1.1] - 2015-06-12

### Changed

* When calling `run!` on an import with invalid header we update the
report object instead of raising an exception.

## [0.1.0] - 2015-06-11

* Initial Release
