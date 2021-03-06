# Change Log

All notable changes to this project will be documented in this file.

## [1.2.0] - 2020-05-05

### Added

- Added ability to copy link to clipboard through click (thanks to [Rafael Milewski](https://github.com/milewski))
- Added config option to overwrite the Media resource (thanks to [Rafael Milewski](https://github.com/milewski))

### Changed

- Fixed URL field not displaying (thanks to [Rafael Milewski](https://github.com/milewski))

## [1.1.0] - 2020-04-28

### Added

- Added ability to overwrite MediaHandler class (thanks to [Rafael Milewski](https://github.com/milewski))

## [1.0.1] - 2020-04-27

### Changed

- Fixed issue with media not being queried on detail view

## [1.0.0] - 2020-04-24

Initial public release.

### Changed

- Fixed bug where a numeric value would not be queryable
- Updated packages

## 0.1.19 - 2019-10-17

#### Updated

- Field UI when in compact mode + add default thumbnail size
- Media modal UI

## 0.1.17 - 2019-10-16

#### Manual changes required

- run `php artisan migrate` to add columns that are required for WebP

#### Added

- Upload button on resource index page
- Search on upload index page
- WebP support
- Method to modify thumbnail sizes on nova admin
- Method to format Media model serialization

## 0.1.9 - 2019-10-02

#### Updated

- UI changes in media library modal
- Selected files are now rendered at top when opening modal
- Upload Media button added to resource view that opens stripped media modal for file upload
- Custom formatter option for media model to decrease response size

#### Removed

- Media nav item from under nova resource navigation

#### Added

- Custom resource view.
- Blade template for nova navigation
- Display resource view in Nova navigation

##### Display resource view in Nova navigation

In your `NovaServiceProvider` class add or update `tools` method

```
use OptimistDigital\MediaField\NovaMediaLibrary;

public function tools()
{
    return [
        new \OptimistDigital\MediaField\NovaMediaLibrary,
    ];
}
```

## 0.1.0 - 2019-8-28

#### Manual changes required

- run `php artisan migrate` to add the new title field

#### Added

- Pagination
- Title field
- Media edit modal
