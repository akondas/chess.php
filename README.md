# Chess.php

chess.php is a PHP chess library that is used for chess move
generation/validation, piece placement/movement, and check/checkmate/stalemate
detection - basically everything but the AI. 

NOTE: this is a port of [chess.js](https://github.com/jhlywa/chess.js) for php, froked from [ryanhs/chess.php](https://github.com/ryanhs/chess.php)

[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.2-8892BF.svg)](https://php.net/)
[![Latest Stable Version](https://poser.pugx.org/akondas/chess.php/v/stable)](https://packagist.org/akondas/ryanhs/chess.php)
[![Build Status](https://travis-ci.org/akondas/chess.php.svg?branch=master)](https://travis-ci.org/akondas/chess.php)
[![MIT License](https://poser.pugx.org/ryanhs/chess.php/license)](https://packagist.org/packages/ryanhs/chess.php)  

## Installation

use composer with `composer require akondas/chess.php`   
or put in your composer.json  
```
"require": {
	"ryanhs/chess.php": "^1.0"
}
```

## Example Code
The code below plays a complete game of chess ... randomly.

```php
<?php

require 'vendor/autoload.php';
use \Ryanhs\Chess\Chess;

$chess = new Chess();
while (!$chess->gameOver()) {
	$moves = $chess->moves();
	$move = $moves[mt_rand(0, count($moves) - 1)];
	$chess->move($move);
}

echo $chess->ascii() . PHP_EOL;
```

```
   +------------------------+
 8 | .  .  .  .  .  .  .  . |
 7 | .  .  .  .  r  .  .  . |
 6 | .  .  .  .  .  .  .  . |
 5 | .  .  .  .  .  .  .  . |
 4 | k  .  .  .  .  .  .  . |
 3 | .  .  .  .  .  .  K  . |
 2 | .  .  .  n  .  .  .  . |
 1 | .  .  .  .  .  .  .  . |
   +------------------------+
     a  b  c  d  e  f  g  h
```

## Chess.php documentation

you can check it here: [https://ryanhs.github.io/chess.php](https://ryanhs.github.io/chess.php)
