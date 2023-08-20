# CXX

## Introduction

   L'honneur de la meilleure convention d'écriture pour le C++ peut être sans aucune hésitation honoré à <a href="https://google.github.io/styleguide/cppguide.html#General_Naming_Rules">Google C++ Style Guide</a>, mais elle n'atteint tout de même pas nos attentes personnelles. C'est pourquoi avec une grande influence de celle-ci et de notre expérience, nous avons decidé de créer la nôtre. Nous n'avons pas pour objectif de la standardiser au monde entier, vous pouvez donc la considérer comme n'était rien de plus qu'une convention personnelle.
   
## Version C++

   Toute fonctionalité dans C++17 sera considéré, mais aucune provenant de versions supérieures. La convention devrait cependant être respectée pour les nouvelles versions a l'exception de cas d'obsolescence (Ce qui ne devrait certainement pas arriver pour des raisons évidentes).

## Nomage

### Nomage de fichiers

   Les fichiers headers et sources C++ devraient seulement avoir une terminaison `.cpp` ou `.h`, donc pas de `.cc` ou `.hpp`. Tout nom de fichier devrait soit inclure aucunes majuscules ou une au début de son nom et de chaque mot dans son nom. Examples valides: `test.h`, `VulkanLib.h`, `vulkanlib.h`. Les `-` et `_` sont interdits dans le nom des fichiers sauf s'il y a une raison spécifique de faire ainsi autre que "c'est beau".

### Nomage de fonctions / methodes et variables

Toutes fonctions, methodes et variables doivent utiliser la convention camel case.

### Nomage de déclarations de type et de namespaces 

Toutes déclarations de type et namespace doit utiliser la convetion pascal case.

## Styles de base

### Brackets

Aucune `{` ne devrait être sur la même ligne que son parent. Exemple:

```C++
// !! INVALIDE !!
void test() {
}

// VALIDE
void test()
{
}
```

(La même chose s'applique aux classes, namespaces, enums, etc a l'exception des lambdas)

## Headers

### Header Guards

### Ordre d'inclusion 
