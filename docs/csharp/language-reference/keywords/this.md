---
title: this (référence C#)
description: this, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- this
- this_CSharpKeyword
helpviewer_keywords:
- this keyword [C#]
ms.assetid: d4f827fe-4710-410b-89b8-867dad44b8a3
ms.openlocfilehash: df1bf6a3e6d24b231bf5e3c7a960f49084c4e53a
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46577358"
---
# <a name="this-c-reference"></a>this (référence C#)
Le mot clé `this` fait référence à l’instance actuelle de la classe et est également utilisé comme modificateur du premier paramètre d’une méthode d’extension.  
  
> [!NOTE]
>  Cet article traite de l’utilisation de `this` avec des instances de classe. Pour plus d’informations sur son utilisation dans les méthodes d’extension, consultez [Méthodes d’extension](../../../csharp/programming-guide/classes-and-structs/extension-methods.md).  
  
 Voici quelques utilisations courantes de `this` :  
  
-   Pour qualifier des membres masqués par des noms similaires, par exemple :  
  
 [!code-csharp[csrefKeywordsAccess#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_1.cs)]  
  
-   Pour passer un objet comme paramètre à d’autres méthodes, par exemple :  
  
    ```csharp  
    CalcTax(this);  
    ```  
  
-   Pour déclarer des indexeurs, par exemple :  
  
 [!code-csharp[csrefKeywordsAccess#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_2.cs)]  
  
 Les fonctions membres statiques, car ils existent au niveau de la classe et non comme faisant partie d’un objet, n’ont pas de pointeur `this`. Une erreur consiste à faire référence à `this` dans une méthode statique.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, `this` est utilisé pour qualifier les membres de la classe `Employee`, `name` et `alias`, qui sont masqués par des noms similaires. Il est également utilisé pour passer un objet à la méthode `CalcTax`, qui appartient à une autre classe.  
  
 [!code-csharp[csrefKeywordsAccess#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_3.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [base](../../../csharp/language-reference/keywords/base.md)  
- [Méthodes](../../../csharp/programming-guide/classes-and-structs/methods.md)
