# Twitch-Automatyczne-odbieranie-punktow
Zadaniem skryptu jest automatyczne klikanie przycisku aby odebrać dodatkowe punkty na platformie twitch.

# Instalacja
1. Instalujemy wtyczkę 'Tampermonkey'
1. Przechodzimy do wtyczki
1. Wybieramy 'Panel sterowania'
1. Klikamy w przycisk 'Dodaj nowy skrypt' (+)
1. Uzupełniamy odpowiednio dane tj. name,match,icon itp.
1. Wklejamy skrypt w miejscu '// Your code here...'
1. Zapisujemy i cieszymy się.


# Film
Film z prezentacją skryptu: [Youtube](https://www.youtube.com/@SkryptoweWybryki).

# Kod
```
function odbierzBonus() {
    const element = document.querySelector('[aria-label="Odbierz bonus"]');
    if (element !== null) {
      element.click();
    }
}

setInterval(odbierzBonus, 2000);
```


# Cały kod

```

// ==UserScript==
// @name         Twitch - Automatyczne odbieranie punktów
// @namespace    http://tampermonkey.net/
// @version      v1.0
// @description  Automatyczne odbieranie punktów
// @author       SkryptoweWybryki
// @match        https://www.twitch.tv/*
// @icon         https://www.google.com/s2/favicons?sz=64&domain=twitch.tv
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

function odbierzBonus() {
    const element = document.querySelector('[aria-label="Odbierz bonus"]');
    if (element !== null) {
      element.click();
    }
}

setInterval(odbierzBonus, 2000);

})();
```
