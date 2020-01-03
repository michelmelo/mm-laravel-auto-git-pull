# mm-laravel-auto-git-pull
MM Laravel auto git pull
```code
composer require michelmelo/mm-laravel-auto-git-pull
```


## https://packagist.org/packages/michelmelo/mm-laravel-auto-git-pull

## .env Variables
```code
AUTO_PULL_SECRET=xxxxxxxxxxxxxxxxxx
AUTO_PULL_DIR=/var/www/site.com
AUTO_PULL_SERVER_IP=111.11.111.111
AUTO_PULL_SSH_USER=root
AUTO_PULL_SSH_PRIVATE_KEY=storage/app/id_rsa
AUTO_PULL_SSH_USER_PASS=
```

## Add Route in api.php
```code
Route::any('/auto-git-pull', '\MichelMelo\MMAutoGitPull\MMAutoGitPullController@pull');
```

## Create Webhook Url on github.com
```code
http://site.com/api/auto-git-pull?secret=xxxxxxxxxxxxxxxxxx
```

## Result
```json
{
    "status": true,
    "message": "Success!",
    "data": [
        "No local changes to save",
        "Already up-to-date."
    ],
    "errors": [
        
    ]
}
```
