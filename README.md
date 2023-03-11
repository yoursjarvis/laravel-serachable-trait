<img src="https://i.imgur.com/cZO9N5D.png" alt="Build Status">

# Laravel Searchable Trait

A laravel package to implement search functionality easily in any model in your project just using a `trait` .

installation :

`composer require yoursjarvis/laravel-searchable-trait`

Usage :

- use `Searchable` trait in your model
- Define `$searchable` property in your model to select which columns to search in

Example :

```php
use YoursJarvis\LaravelSearchableTrait\Searchable;

class User extends Model {

  use Searchable ;

  protected $searchable = ['name', 'posts.title'];

  public function posts(){
    return $this->hasMany(Post::class);
  }
```
