FILED WITH GRAMMAR MISTAKES, TO FIX AT FINAL VERSION

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

   Comme toute convention C++, tous les fichiers `.cpp` devraient être accommodés d'un fichier `.h` / header. Encore, tout autre extension de fichier que `.h` doit être évité (comme `.hpp`) L'utilisation de fichiers header seul (non accommodé par un `.cpp`) est permis.

### Header Guards

(TO MAKE FULLY FRENCH (WITH ACCENTS ETC) LATER
   Comme toujours les headers doivent avoir un header guard et le nomage de ceux-ci doit suivre ce pattern: `|NOM_DU_RPOJET|_|NOM_DU_FICHER|_H_` (`|` sont seulement presents pour specifier que leur contenu ne fait que decrire ce qui devrait etre present). `|NOM_DU_PROJET|` n'est pas necessaire si vos fichiers sont dans les limites d'une source qui n'a pas pour objectif d'etre inclue en tant que dependence de quelconque facon dans d'autre projet.

### Ordre d'inclusion 

L'ordre d'inclusion devrait etre comme cela (chacun separe par un line feed):
1. Le fichier `.h` accomodé
2. Les headers standards de C++
3. Les headers standards de C
  a. AVERTISSEMENT: Ne jamais utiliser les `.h` de headers de la librairie standard C, utilisez plutôt ceux préfixés d'un "c"
5. Dependences (tout ce qui est externe au projet)
6. Headers de projet
