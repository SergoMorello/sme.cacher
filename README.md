<h1>
  <span>Cacher</span>
</h1>

##	Простой класс для кэширования данных

[Cacher](#cacher)   

###

<h3 id="cacher">Cacher:</h3>

#### В кэше можно хранить любые данные и файлы от одной секунды до бесконечности

##### Установить директорию куда будет сохраняться весь кэш `по умолчанию это __DIR__.'/.cache/`

```php
Cacher::setDir(__DIR__.'/.cache/');
```

##### Сохранить данные в кэше put(`ключ`, `данные`, `время хранения в секундах`)

```php
Cacher::put('message', 'Hello World!', 60);
```

##### Получить данные

```php
Cacher::get('message');
```

###### или получить и сразу удалить

```php
Cacher::pull('message');
```

##### Удалить

```php
Cacher::forget('message');
```

##### Проверить существование по ключу

```php
Cacher::has('message');
```

##### Так же можно выполнять все действия с классом с помощью хелпера

```php
cacher()->put('message2', 'world hello', 180);

cacher()->get('message2');
```