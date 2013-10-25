![logo](../img/CRPLogo.png)

# CRP crypt Doc FR

CRP est une fonction de cryptage decliné pour php et jQuery. Vous pouvez l'utiliser dans un chat, un échange d'information entre le serveur et le client, sécurisation de connexion… Vous pouvez crypter avec une langue et decrypter avec une autre.

Crypte et décrypte les textes passés en paramètre avec la clé secrète. Intègre en interne une clé aléatoire, le même texte crypté à des moments différents avec la même clé secrète donnera des résultats différents.

CRP-securitis-connexion consiste à ne pas envoyer le password au serveur a chaque connexion mais plustôt, récupérer un message crypté de la part du serveur, grâce à votre password, decrypter le message avant de le renvoyer au serveur.

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
* **TEXT** Le texte à crypter.
* **KEY** La clé à utiliser pour crypter le texte.

**Return**
* Une chaine de caracter base64.

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
* **TEXT** Le texte à decrypter.
* **KEY** La clé à utiliser pour décrypter le texte.

**Return**
* Le message décrypté.

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
Importer les fichiers depuis votre dossier.
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
* **TEXT** Le texte à crypter.
* **KEY** La clé à utiliser pour crypter le texte.

**Return**
* Une chaine de caractère base64.

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
* **TEXT** Le texte à décrypter.
* **KEY** La clé à utiliser pour décrypter le texte.

**Return**
* Le message décrypté.

**Exemple d'utilisation**
```js
var message = 'bDpiamM6cTtkYyA6O3MgY2p2ZHNramhzZGJxcyx2Yyw=';
var key = '123456789';
	
var tmp = $.crp.decrypte(message,key);
// tmp = Hello World
```
