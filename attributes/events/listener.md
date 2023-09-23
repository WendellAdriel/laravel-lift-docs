# Listener

The `Listener` attribute allows you to register a listener function for model events.

A more convenient way of registering a listener function "replacing" laravels event closures for eloquent models, more info (Laravel Docs: Eloquent Closures)[https://laravel.com/docs/10.x/eloquent#events-using-closures]

## Usage

```php
use Illuminate\Database\Eloquent\Model;
use WendellAdriel\Lift\Attributes\Events\Listener;
use WendellAdriel\Lift\Lift;

final class Product extends Model
{
    use Lift;


    #[Listener]
    public function onCreated(Product $product) {
    	Log::info("Product {$product->name} has been created.");
    }
}
```

## API

```php
#[Listener(event: 'created', queue: true)]
```

Properties:

1. event | string | one of the laravel model events
2. queue | bool | should this handler be queued
