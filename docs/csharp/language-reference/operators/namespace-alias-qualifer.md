---
title: ::, opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 324f6711cdec478e5647b05d84c281f79e95f036
ms.sourcegitcommit: 4c10802ad003374641a2c2373b8a92e3c88babc8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2019
ms.locfileid: "65452364"
---
# <a name="-operator-c-reference"></a>::, opérateur (référence C#)

Le qualificateur d’alias d’espace de noms (`::`) s’utilise pour rechercher les identificateurs. Il se place toujours entre deux identificateurs, comme dans cet exemple :

[!code-csharp[csRefOperators#27](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#27)]

L’opérateur `::` peut également être utilisé avec une *directive d’alias using* :

```csharp
// using Col=System.Collections.Generic;
var numbers = new Col::List<int> { 1, 2, 3 };
```

## <a name="remarks"></a>Remarques

Le qualificateur d’alias d’espace de noms peut être `global`. Il appelle alors une recherche dans l’espace de noms global, plutôt que dans un espace de noms avec alias.

## <a name="for-more-information"></a>Pour plus d'informations

Pour obtenir un exemple d’utilisation de l’opérateur `::`, consultez la section suivante :

- [Guide pratique pour utiliser l’alias d’espace de noms global](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Mots clés d’espaces de noms](../keywords/namespace-keywords.md)
- [., opérateur](member-access-operators.md#member-access-operator-)
- [extern alias](../keywords/extern-alias.md)