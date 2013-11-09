![logo](../img/CRPLogo.png)

# CRP crypt Doc EN

CRP is a cryptographic function available in php and jQuery. You can use it in a chat, an exchange of information between a server and a client, for a secure connection… You can encrypt with one language and decrypt with the other.

Encrypt and decrypt texts given as a parameter with the private key. It manages a random key internally. The same text encrypted at different time with the same private key will provide different results.

CRP-securitis-connexion do not send the password to the server at each connection, but will get an encrypted message from the server, thanks to the password, and decrypt the message before sending it back to the server.

***
***
***

> # ![icone](../img/php.png)
Class de cryptage et décryptage static pour php.

####Package
* php
	* `crp.php`

#### Import
```php
require_once 'php/crp.php';
```

#### Usage
***
> #### `crp::crypte('TEXT', 'KEY');`
Fonction de cryptage.

**Paramètre**
* **TEXT** Text to be encrypted.
* **KEY** Key used to encrypt the text.

**Return**
* a base64 string.

**Exemple d'utilisation**
```php
$message = 'Hello World';
$key = '123456789';

$tmp = crp::crypte($message, $key);
// $tmp = bDpiamM6cTtkYyA6O3MgY2p2ZHNramhzZGJxcyx2Yyw=
```

***

> #### `crp::decrypte('TEXT', 'KEY');`
Fonction de décryptage.

**Paramètre**
* **TEXT** Text to be decrypted.
* **KEY** Key used to decrypt the text.

**Return**
* The text decrypted.

**Exemple d'utilisation**

```php
$message = 'bDpiamM6cTtkYyA6O3MgY2p2ZHNramhzZGJxcyx2Yyw=';
$key = '123456789';
	
$tmp = crp::decrypte($message, $key);
// $tmp = Hello World
```
***
***
***

> #![icone](../img/jquery.png) 
Plugin de cryptage et décryptage pour jQuery

####Package
* jQuery
	* `jquery.crp.min.js`
	* `jquery.md5.min.js`
	* `jquery.base64.min.js`

#### Import
Import all the files in your folder.
```js
<script type="text/javascript" src="js/lib/jquery.crp.min.js"></script>
<script type="text/javascript" src="js/lib/jquery.md5.min.js"></script>
<script type="text/javascript" src="js/lib/jquery.base64.min.js"></script>
```

#### Usage

***

> #### `$.crp.crypte('TEXT', 'KEY');`
Fonction de cryptage.

**Paramètre**
* **TEXT** Text to be encrypted.
* **KEY** Key used to encrypt the text.

**Return**
* A base64 string.

**Exemple d'utilisation**
```js
var message = 'Hello World';
var key = '123456789';
	
var tmp = $.crp.crypte(message, key);
// tmp = bDpiamM6cTtkYyA6O3MgY2p2ZHNramhzZGJxcyx2Yyw=
```

***

> #### `$.crp.decrypte('TEXT', 'KEY');`
Fonction de decrypage.

**Paramètre**
* **TEXT** Text to be decrypted.
* **KEY** Key used to decrypt the text.

**Return**
* The decrypted message.

**Exemple d'utilisation**
```js
var message = 'bDpiamM6cTtkYyA6O3MgY2p2ZHNramhzZGJxcyx2Yyw=';
var key = '123456789';
	
var tmp = $.crp.decrypte(message,key);
// tmp = Hello World
```
