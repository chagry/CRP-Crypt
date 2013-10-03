# CRP crypt V 0.1 FR

CRP est une fonction de cryptage decliner pour php et jQuery. Vous pouvez l'utiliser dans un chat, un echange d'information entre le serveur et le client, securisation de connexion… Vous pouvez crypter avec un langage est decrypter avec un autre langage.

Crypte et décrypte les texte passer en paramètre avec la clé secret. Intègre en interne une clés secondaire, le même texte crypté à des moments différents avec la même clé secret donnera des résultats différents.

CRP securitie connexion conciste a ne pas envoier le password au serveur a chaque connexion mais plus tot, recuperer un message crypter de la pare du serveur est utiliser votre password pour decrypter le message avant de le renvoyer au serveur. Votre password a etais envoier une seule foit au serveur au moment de l'enregistrement, est plus jamais il sera renvoier au serveur.

***
***
***

> # ![icone](img/php.png)
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
* **TEXT** Le texte a crypter.
* **KEY** La cles a utiliser pour crypter le texte.

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
Fonction de decrypage.

**Paramètre**
* **TEXT** Le texte a decrypter.
* **KEY** La cles a utiliser pour decrypter le texte.

**Return**
* Le message decrypter.

**Exemple d'utilisation**
```php
$message = 'bDpiamM6cTtkYyA6O3MgY2p2ZHNramhzZGJxcyx2Yyw=';
$key = '123456789';
	
$tmp = crp::decrypte($message, $key);
// $tmp = Hello World
```
Merci à [info-3000](http://www.info-3000.com/) pour les fonction de cryptage et décryptage en php.
***
***
***


> #![icone](img/jquery.png) 
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
* **TEXT** Le texte a crypter.
* **KEY** La cles a utiliser pour crypter le texte.

**Return**
* Une chaine de caracter base64.

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
* **TEXT** Le texte a decrypter.
* **KEY** La cles a utiliser pour decrypter le texte.

**Return**
* Le message decrypter.

**Exemple d'utilisation**
```js
var message = 'bDpiamM6cTtkYyA6O3MgY2p2ZHNramhzZGJxcyx2Yyw=';
var key = '123456789';
	
var tmp = $.crp.decrypte(message,key);
// tmp = Hello World
```
