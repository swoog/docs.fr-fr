---
title: Types F#
description: En savoir plus sur les types qui sont utilisés dans F# et comment F# sont nommés et décrits.
ms.date: 05/16/2016
ms.openlocfilehash: bdbb89dc751970ac31fe102df009f0bff6388e52
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "33565583"
---
# <a name="f-types"></a>Types F#

Cette rubrique décrit les types qui sont utilisés dans F# et comment F# sont nommés et décrits.


## <a name="summary-of-f-types"></a>Résumé de F# Types
Certains types sont considérés comme *types primitifs*, telles que le type booléen `bool` et les types intégraux et à virgule flottante de différentes tailles, qui incluent les types pour les octets et les caractères. Ces types sont décrits dans [Types primitifs](primitive-types.md).

Les autres types qui sont intégrées au langage incluent les tuples, des listes, des tableaux, des séquences, des enregistrements et les unions discriminées. Si vous disposez d’expérience avec d’autres langages .NET et learning F#, vous devez lire les rubriques pour chacun de ces types. Des liens vers plus d’informations sur ces types sont inclus dans le [rubriques connexes](https://msdn.microsoft.com/library/#rel) section de cette rubrique. Ces F#-types spécifiques prennent en charge les styles de programmation qui sont communes aux langages de programmation fonctionnelle. La plupart de ces types sont associés à des modules dans le F# bibliothèque qui prennent en charge les opérations courantes sur ces types.

Le type d’une fonction inclut des informations sur les types de paramètres et type de retour.

Le .NET Framework est la source des types d’objets, les types d’interface, les types délégués et d’autres. Vous pouvez définir vos propres types d’objet comme vous le faites dans n’importe quel autre langage .NET.

En outre, F# code peut définir des alias, qui sont nommés *abréviations de types*, qui sont d’autres noms pour les types. Vous pouvez utiliser les abréviations de type lorsque le type peut changer à l’avenir et que vous souhaitez éviter de modifier le code qui dépend du type. Ou bien, vous pouvez utiliser une abréviation de type comme un nom convivial pour un type qui peut rendre le code plus facile à lire et à comprendre.

F#Fournit des types de collection utiles qui sont conçues avec la programmation fonctionnelle à l’esprit. À l’aide de ces types de collection vous permet d’écrire du code qui ne fonctionne plus dans le style. Pour plus d’informations, consultez [ F# Types de collections](fsharp-collection-types.md).


## <a name="syntax-for-types"></a>Syntaxe pour les Types
Dans F# code, vous devez souvent écrire les noms des types. Chaque type a une forme syntaxique, et vous utilisez ces formes syntaxiques dans les annotations de type, les déclarations de méthode abstraite, les déclarations de délégué, signatures et d’autres constructions. Chaque fois que vous déclarez une nouvelle construction de programme dans l’interpréteur, l’interpréteur imprime le nom de la construction et la syntaxe pour son type. Cette syntaxe peut être simplement un identificateur pour un type défini par l’utilisateur ou un identificateur intégré tel que pour `int` ou `string`, mais pour des types plus complexes, la syntaxe est plus complexe.

Le tableau suivant présente les aspects de la syntaxe de type pour F# types.



|Type|Syntaxe de type|Exemples|
|----|-----------|--------|
|type primitif|*type-name*|`int`<br /><br />`float`<br /><br />`string`|
|type d’agrégat (classe, structure, union, enregistrement, enum et ainsi de suite)|*type-name*|`System.DateTime`<br /><br />`Color`|
|abréviation de type|*nom de l’abréviation de type*|`bigint`|
|type qualifié complet|*Namespaces.type-nom*<br /><br />ou<br /><br />*modules.type-nom*<br /><br />ou<br /><br />*Namespaces.modules.type-nom*|`System.IO.StreamWriter`|
|array|*nom de type*[] ou<br /><br />*nom de type* tableau|`int[]`<br /><br />`array<int>`<br /><br />`int array`|
|tableau à deux dimensions|*nom de type*[,]|`int[,]`<br /><br />`float[,]`|
|tableau tridimensionnel|*nom de type*[,]|`float[,,]`|
|tuple|*type-name1* &#42; *type-nom2* ...|Par exemple, `(1,'b',3)` a le type `int * char * int`|
|type générique|*paramètre de type* *nom de type générique*<br /><br />ou<br /><br />*nom de type générique*&lt;*liste de paramètres de type*&gt;|`'a list`<br /><br />`list<'a>`<br /><br />`Dictionary<'key, 'value>`|
|type (un type générique qui a un argument de type spécifique fourni) construit|*argument de type* *nom de type générique*<br /><br />ou<br /><br />*nom de type générique*&lt;*liste d’arguments type*&gt;|`int option`<br /><br />`string list`<br /><br />`int ref`<br /><br />`option<int>`<br /><br />`list<string>`<br /><br />`ref<int>`<br /><br />`Dictionary<int, string>`|
|type de fonction qui a un paramètre unique|*paramètre-type1*  - &gt; *type de retour*|Une fonction qui accepte un `int` et retourne un `string` a le type `int -> string`|
|type de fonction qui a plusieurs paramètres|*paramètre-type1*  - &gt; *paramètre-type2*  - &gt; ... -&gt; *type de retour*|Une fonction qui accepte un `int` et un `float` et retourne un `string` a le type `int -> float -> string`|
|fonction d’ordre supérieur en tant que paramètre|(*type de fonction*)|`List.map` a le type `('a -> 'b) -> 'a list -> 'b list`|
|délégué|délégué de *type de fonction*|`delegate of unit -> int`|
|type flexible|#*nom de type*|`#System.Windows.Forms.Control`<br /><br />`#seq<int>`|

## <a name="related-topics"></a>Rubriques connexes


|Rubrique|Description|
|-----|-----------|
|[Types primitifs](primitive-types.md)|Décrit les types simples intégrés tels que les types intégraux, le type booléen et les types de caractères.|
|[Type d’unité](unit-type.md)|Décrit le `unit` type, un type qui a une valeur et qui est indiqué par () ; équivalent au `void` dans C# et `Nothing` en Visual Basic.|
|[Tuples](tuples.md)|Décrit le type de tuple, un type qui se compose de valeurs associées de n’importe quel type groupées en paires, triples, quadruples et ainsi de suite.|
|[Options](options.md)|Décrit le type d’option, un type qui peut avoir une valeur ou être vide.|
|[Listes](lists.md)|Décrit les listes, qui sont des séries immuables et ordonnée d’éléments tous du même type.|
|[Tableaux](arrays.md)|Décrit les tableaux, qui sont des jeux ordonnés d’éléments mutables du même type qui occupent un bloc contigu de mémoire et qui sont de taille fixe.|
|[Séquences](sequences.md)|Décrit le type de séquence, ce qui représente une série logique de valeurs ; les valeurs individuelles sont calculées uniquement si nécessaire.|
|[Enregistrements](records.md)|Décrit le type d’enregistrement, un petit agrégat de valeurs nommées.|
|[Unions discriminées](discriminated-unions.md)|Décrit le type d’union discriminée, un type dont les valeurs peuvent être l’un d’un ensemble de types possibles.|
|[Fonctions](functions/index.md)|Décrit les valeurs de fonction.|
|[Classes](classes.md)|Décrit le type de classe, un type d’objet qui correspond à un type référence .NET. Types classe peuvent contenir des membres, les propriétés, les interfaces implémentées et un type de base.|
|[Structures](structures.md)|Décrit le `struct` type, un type d’objet qui correspond à un type valeur .NET. Le `struct` type représente généralement un petit agrégat de données.|
|[Interfaces](interfaces.md)|Décrit les types d’interface, qui sont des types qui représentent un jeu de membres qui fournissent certaines fonctionnalités, mais qui ne contiennent aucune donnée. Un type d’interface doit être implémenté par un type d’objet pour être utile.|
|[Délégués](delegates.md)|Décrit le type délégué, qui représente une fonction en tant qu’objet.|
|[Énumérations](enumerations.md)|Décrit les types d’énumération, dont les valeurs appartiennent à un ensemble de valeurs nommées.|
|[Attributs](attributes.md)|Décrit les attributs, qui sont utilisés pour spécifier des métadonnées pour un autre type.|
|[Types d'exceptions](exception-handling/exception-types.md)|Décrit les exceptions, qui spécifient des informations sur l’erreur.|
