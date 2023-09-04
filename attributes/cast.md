# Cast

The `Cast` attribute allows you to cast your model's **public properties** to a specific type and also to type your public properties. It works the same way as it would be using the `casts` property on your model, but you can set it directly on your **public properties**.

```php
use Carbon\CarbonImmutable;
use Illuminate\Database\Eloquent\Model;
use WendellAdriel\Lift\Attributes\Cast;
use WendellAdriel\Lift\Lift;

final class Product extends Model
{
    use Lift;

    public string $name;

    #[Cast('float')]
    public float $price;

    #[Cast('int')]
    public int $category_id;

    #[Cast('boolean')]
    public bool $is_active;

    #[Cast('immutable_datetime')]
    public CarbonImmutable $promotion_expires_at;
}
```
