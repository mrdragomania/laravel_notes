# laravel-notes
Commands and notes for Laravel

##### Link storage on server with no SSH
```
Route::get('/foo', function () {
    Artisan::call('storage:link');
});
```
