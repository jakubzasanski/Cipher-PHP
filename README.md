# Cipher-PHP

Simple cipher class

## Usage

#### Hash password to storage

```php
# Include class file
require_once "Cipher.php";

# Create Cipher object 
$cipher = new Cipher(APP_PRIV_KEY);

# Hash password
$hashed_password = $cipher->HashPassword($plaintext);
```

#### Compare password and hash

```php
$cipher = new Cipher(APP_PRIV_KEY);

if ($cipher->VerifyPassword($plaintext, $hashed_password)) {
    echo 'Success!';
} else {
    echo 'Failed!';
}
```

#### Encrypt/decrypt string

```php
$cipher = new Cipher(APP_PRIV_KEY);

$string = 'example';

$encrypted = $cipher->Encrypt($string);
$decrypted = $cipher->Decrypt($encrypted);
```