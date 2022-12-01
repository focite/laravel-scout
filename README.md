# Laravel Scout Elasticsearch Driver

This package provides a [Elasticsearch](https://www.elastic.co/products/elasticsearch) driver for Laravel Scout.

## Installation

You can install the package via composer:

```bash
composer require jaravel/laravel-scout-elastic
```

Laravel will automatically register the driver service provider.

### Setting up Elasticsearch configuration

After you've published the Laravel Scout package configuration, you need to set your driver to `elasticsearch` and add its configuration:

```php
// config/scout.php
...
    // Set your driver to elasticsearch
    'driver' => env('SCOUT_DRIVER', 'elasticsearch'),
...
    /*
    |--------------------------------------------------------------------------
    | Elasticsearch Configuration
    |--------------------------------------------------------------------------
    |
    | Here you may configure your Elasticsearch settings.
    |
    */
    'elasticsearch' => [
        'hosts' => [
            env('ELASTICSEARCH_HOST', 'localhost'),
            // [
            //     'host'   => env('ELASTICSEARCH_HOST', 'localhost'),
            //     'port'   => env('ELASTICSEARCH_PORT', '9200'),
            //     'scheme' => env('ELASTICSEARCH_SCHEME', 'https'),
            //     'path'   => env('ELASTICSEARCH_PATH', '/elastic'),
            //     'user'   => env('ELASTICSEARCH_USER', 'username'),
            //     'pass'   => env('ELASTICSEARCH_PASS', 'password'),
            // ]
        ],
    ]
...
```

For host configuration you can refer to the official [Elasticsearch documentation](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)

## Usage

Now you can use Laravel Scout as described in the [Laravel Scout official documentation](https://laravel.com/docs/8.x/scout)

## License

The MIT License (MIT).
