---
description: Take your Eloquent Models to the next level
---

# 🏋 Lift for Laravel

<figure><img src=".gitbook/assets/laravel-lift-banner.png" alt=""><figcaption></figcaption></figure>

**Lift** is a package that boosts your Eloquent Models in Laravel.

It lets you create public properties in Eloquent Models that match your table schema. This makes your models easier to read and work with in any IDE.

The package intelligently uses PHP 8’s attributes, and gives you complete freedom in setting up your models. For instance, you can put validation rules right into your models - a simple and easy-to-understand arrangement compared to a separate request class. Plus, all these settings are easily reachable through handy new methods.

With a focus on simplicity, **Lift** depends on **Eloquent Events** to work. This means the package fits easily into your project, without needing any major changes (unless you’ve turned off event triggering).

To start using **Lift**, you just need to add the `Lift` trait to your Eloquent Models, and you're ready to go.

```php
use Illuminate\Database\Eloquent\Model;
use WendellAdriel\Lift\Lift;

final class Product extends Model
{
    use Lift;
}
```

### Credits <a href="#credits" id="credits"></a>

* [Wendell Adriel](https://github.com/WendellAdriel)
* [All Contributors](https://github.com/WendellAdriel/laravel-lift/graphs/contributors)

### Contributing <a href="#contributing" id="contributing"></a>

Check the [**Contributing Guide**](https://github.com/WendellAdriel/laravel-lift/blob/main/CONTRIBUTING.md).
