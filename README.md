# Code Sniffer

The coding standards set by the company

## Examples

You can run the following command in full:

```
$ phpcs --standard=vendor/gatenbysanderson/code-sniffer/src/phpcs.xml
```

Or you can add this to your `composer.json` file which allows you to run `composer gscs`:

```json
{
  //...
  
  "scripts": {
    "gscs": "phpcs --standard=vendor/gatenbysanderson/code-sniffer/src/phpcs.xml"
  }
  
  //...
}
```
