# Dispatches

The `Dispatches` attribute allows you to dispatch custom (Laravel Events)[https://laravel.com/docs/10.x/events#defining-events].


## Usage

```php
use Illuminate\Database\Eloquent\Model;
use WendellAdriel\Lift\Attributes\Events\Observer;
use WendellAdriel\Lift\Lift;


#[Dispatches(ProductSaved::class)]
#[Dispatches(ProductHasBeenSetup::class, 'created')]
final class Product extends Model
{
    use Lift;

}
```

## API

```php
#[Dispatches(string $eventClass, string $event = '')]
```

Properties:

1. eventClass | string | (Event class)[https://laravel.com/docs/10.x/events#defining-events]
2. event | string | model event string e.g. 'created', only needed if this string isn't in the event class name.
