# laravel-notes
Commands and notes for Laravel

##### Link storage on server with no SSH
###### Option #1
```
Route::get('/foo', function () {
    Artisan::call('storage:link');
});
```
###### Option #2
```
<?php
symlink(__DIR__ . '/../laravel-core/storage/app/', 'storage');
```

###### Option #3
```
App::make('files')->link(storage_path('app/public'), public_path('storage'));
```
