---
title: extern alias (référence C#)
ms.date: 07/20/2015
f1_keywords:
- alias_CSharpKeyword
helpviewer_keywords:
- extern alias keyword [C#]
- aliases [C#], extern keyword
- aliases, extern keyword
ms.assetid: f487bf4f-c943-4fca-851b-e540c83d9027
ms.openlocfilehash: 66210bc1a84e2c3239dcac72cdc194b14dcccf30
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405445"
---
# <a name="extern-alias-c-reference"></a>extern alias (référence C#)
Il se peut que vous deviez référencer deux versions d’assemblys qui ont le même nom de type qualifié complet. Par exemple, vous pourriez avoir à utiliser plusieurs versions d’un assembly dans la même application. En utilisant un alias d’assembly externe, vous pouvez encapsuler les espaces de noms de chaque assembly dans des espaces de noms racines nommés par l’alias, ce qui permet de les utiliser dans le même fichier.  
  
> [!NOTE]
>  Le mot clé [extern](../../../csharp/language-reference/keywords/extern.md) est également utilisé comme modificateur de méthode, déclarant une méthode écrite en code non managé.  
  
 Pour référencer deux assemblys portant le même nom de type qualifié complet, vous devez spécifier un alias à l’invite de commandes, comme suit :  
  
 `/r:GridV1=grid.dll`  
  
 `/r:GridV2=grid20.dll`  
  
 Cela crée les alias externes `GridV1` et `GridV2`. Pour utiliser ces alias à partir d’un programme, référencez-les en utilisant le mot clé `extern`. Exemple :  
  
 `extern alias GridV1;`  
  
 `extern alias GridV2;`  
  
 Chaque déclaration d’alias externe introduit un espace de noms racine supplémentaire qui est parallèle à l’espace de noms global (mais n’est pas compris dedans). Ainsi, vous pouvez référencer les types de chaque assembly sans ambiguïté en utilisant leur nom qualifié complet, enraciné dans l’alias d’espace de noms approprié.  
  
 Dans l’exemple précédent, `GridV1::Grid` serait le contrôle de grille de `grid.dll`, et `GridV2::Grid` serait le contrôle de grille de `grid20.dll`.  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [Mots clés d’espaces de noms](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [:: (opérateur)](../../../csharp/language-reference/operators/namespace-alias-qualifer.md)  
- [/reference (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/reference-compiler-option.md)
