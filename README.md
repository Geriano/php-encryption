# php-encryption
PHP Encryption Manager

Usage:
```php
<?php

require 'path/to/composer/autoload.php';

use Geriano\Encryption\Encryptor;

// if use AES-256-CBC cipher
$cipher = 'AES-256-CBC';
// key string must have 32 length
$key    = 'YOUR_SECRET_KEY';

// if use AES-128-CBC
$cipher = 'AES-128-CBC';
// key string must have 16 length
$key    = 'YOUR_SECRET_KEY';

$encryptor = new Encryptor($key, $cipher);

$encrypted = $encryptor->encrypt('MY_SECRET_PASSWORD');

var_dump($encrypted);
// output: random string never same

$myData = $encryptor->decrypt($encrypted);

var_dump($myData);
// output: 'MY_SECRET_PASSWORD'
```
