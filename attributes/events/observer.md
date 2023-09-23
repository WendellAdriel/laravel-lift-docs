# Observer

The `Observer` attribute allows you to register a observer class for model events.

This is used to register a Observer Class with a model explained in more detail here: (Laravel Docs: Eloquent Observers)[https://laravel.com/docs/10.x/eloquent#observers]

## Usage

```php
use Illuminate\Database\Eloquent\Model;
use WendellAdriel\Lift\Attributes\Events\Observer;
use WendellAdriel\Lift\Lift;


#[Observer(ProductObserver::class)]
final class Product extends Model
{
    use Lift;

}
```

## API

```php
#[Observer(string $observer)]
```

Properties:

1. observer | string | (Observer class)[https://laravel.com/docs/10.x/eloquent#observers]
