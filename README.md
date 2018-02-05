# Code Sniffer

The coding standards that have been set and agreed by the development team.

## Licence

Copyright &copy; 2018 GatenbySanderson Ltd.

This project is open source software released under the terms of the MIT licence: see [LICENCE.md](LICENCE.md).

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* PHP >=5.6

As this is a private repo, when using composer to require this package - it is assumed your SSH key has already been added to GitHub to authenticate.

### Installing

Start by adding this repo to your projects `composer.json` file:

```json
{
  "repositories": [
    {
        "type": "vcs",
        "url":  "git@github.com:gatenbysanderson/code-sniffer.git",
        "no-api": true
    }
  ]
}
```

You can then simply require the package as with any other:

```
$ composer require --dev gatenbysanderson/code-sniffer
```

### Running the Sniffer

To run the sniffer, you can either call the command in full:

```
$ vendor/bin/phpcs --standard=vendor/gatenbysanderson/code-sniffer/src/phpcs.xml directory1 [directory2 ...]
```

Or create a composer script to make life easier:

```json
{
  "scripts": {
    "gscs": "phpcs --standard=vendor/gatenbysanderson/code-sniffer/src/phpcs.xml directory1 [directory2 ...]"
  }
}
```

This allows you to then run:

```
$ composer gscs
```

## Built With

* [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) - The code sniffer
* [Composer](https://getcomposer.org/) - Dependency management

## Contributing

All changes must be made through the medium of a pull request.

1. Create a feature branch off of the `develop` branch: `feature/my-awesome-feature`
2. Push your commits to the feature branch
3. Submit a pull request to merge the feature into `develop`
4. Once accepted, `develop` should then be merged into `master`
5. `master` should then be tagged with a new release

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/gatenbysanderson/code-sniffer/tags). 

## License

This project is licensed under the proprietary License.
