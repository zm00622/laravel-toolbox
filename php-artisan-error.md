Script @php artisan package:discover --ansi handling the post-autoload-dump event returned with error code 1

This error is caused by not using full path in API. You should change your links in API from relative path to full. This should resolve the problem.
