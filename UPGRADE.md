### Renamed classes:

    October\Rain\Support\Yaml -> Yaml
    October\Rain\Support\Markdown -> Markdown
    System\Classes\ApplicationException -> ApplicationException
    System\Classes\SystemException -> SystemException
    October\Rain\Support\ValidationException -> ValidationException

### File system changes

    [MOVE] /app/config -> /config
    [MOVE] /app/storage -> /storage
    [CREATE] /storage/framework
    [DELETE] /bootstrap/start.php
    [DELETE] /bootstrap/autoload.php
    [SPAWN] /bootstrap/app.php
    [SPAWN] /bootstrap/autoload.php

*SPAWN* means to create a file using the git source.

### Clean up

Optional things you can delete, if they do not contain anything custom.

    [DELETE] /app/start/artisan.php
    [DELETE] /app/start/global.php
    [DELETE] /app/filters.php
    [DELETE] /app/routes.php
    [DELETE] /app
    [DELETE] /storage/cache

### Breaking code changes

**Model->remember() has been removed**
**App::make('paginator')->setCurrentPage(5);** should no longer be used

##### Paginator API changes

    getTotal() -> total()
    getCurrentPage() -> currentPage()
    getLastPage() -> lastPage()
    getFrom() -> firstItem()
    getTo() -> lastItem()

### Things to do

- Does config still inherit?
- Does translation still inherit? Switch to our own?
- Model->remember() replacement usage is buggy/broken
- Custom Exception Handler needs attention
- `laravel.log` should be renamed to system.log
- Search for `@todo L5`