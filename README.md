# laravel-notes
Commands and notes for Laravel

##### Link storage on server with no SSH
```
Route::get('/foo', function () {
    Artisan::call('storage:link');
});
```
Alternative #2
```
<?php
symlink(__DIR__ . '/../laravel-core/storage/app/', 'storage');
```

Alternative #3
```
App::make('files')->link(storage_path('app/public'), public_path('storage'));
```
