---
title: DataView.prototype.getFloat32()
slug: Web/JavaScript/Reference/Global_Objects/DataView/getFloat32
tags:
  - DataView
  - JavaScript
  - Méthode
  - Prototype
  - Reference
  - TypedArrays
translation_of: Web/JavaScript/Reference/Global_Objects/DataView/getFloat32
original_slug: Web/JavaScript/Reference/Objets_globaux/DataView/getFloat32
---
{{JSRef}}

La méthode **`getFloat32()`** permet de lire un nombre flottant signé sur 32 bits à l'octet donné par rapport au début de {{jsxref("DataView")}}.

{{EmbedInteractiveExample("pages/js/dataview-getfloat32.html")}}

## Syntaxe

    dataview.getFloat32(positionOctet [, littleEndian])

### Paramètres

- `positionOctet`
  - : La position, exprimée en nombre d'octets depuis le début de la vue, à laquelle lire les données.
- `littleEndian`
  - : {{optional_inline}} indique si la valeur sur 32 bits est enregistrée dans l'ordre des octets {{Glossary("Endianness", "de poids faible")}}. Si le paramètre vaut `false` ou `undefined`, la valeur sera lue dans l'ordre des octets de poids forts.

### Valeur de retour

Un nombre flottant signé, sur 32 bits.

### Erreurs renvoyées

- {{jsxref("RangeError")}}
  - : Renvoyée si `positionOctet` est tel qu'il est en dehors de la vue.

## Description

Il n'y a pas de contrainte d'alignement, les valeurs codées sur plusieurs octets peuvent être obtenues depuis n'importe quelle position.

## Exemples

### Utilisation de la méthode `getFloat32`

```js
var buffer = new ArrayBuffer(8);
var dataview = new DataView(buffer);
dataview.getFloat32(1); // 0
```

## Spécifications

| Spécification                                                                                                                | État                             | Commentaires                                    |
| ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- | ----------------------------------------------- |
| {{SpecName('Typed Array')}}                                                                                         | {{Spec2('Typed Array')}} | Remplacée dans ECMAScript 2015.                 |
| {{SpecName('ES2015', '#sec-dataview.prototype.getfloat32', 'DataView.prototype.getFloat32')}} | {{Spec2('ES2015')}}         | Définition initiale au sein d'un standard ECMA. |
| {{SpecName('ESDraft', '#sec-dataview.prototype.getfloat32', 'DataView.prototype.getFloat32')}} | {{Spec2('ESDraft')}}     |                                                 |

## Compatibilité des navigateurs

{{Compat("javascript.builtins.DataView.getFloat32")}}

## Voir aussi

- {{jsxref("DataView")}}
- {{jsxref("ArrayBuffer")}}
