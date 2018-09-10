---
title: Espaces de noms (Guide de programmation C#)
ms.date: 08/21/2018
helpviewer_keywords:
- C# language, namespaces
- namespaces [C#]
ms.assetid: b1c4ab46-3fad-4ffa-9deb-dd50a2d8c65a
ms.openlocfilehash: c4011092a6c605137053b544d4b9f14cce2fdb4c
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44211994"
---
# <a name="namespaces-c-programming-guide"></a>Espaces de noms (Guide de programmation C#)

Les espaces de noms sont largement utilisés de deux façons dans la programmation avec C#. Premièrement, le .NET Framework utilise des espaces de noms pour organiser ses nombreuses classes, comme suit :  
  
[!code-csharp[csProgGuide#22](../inside-a-program/codesnippet/CSharp/index_1.cs)]  
  
`System` est un espace de noms et `Console` est une classe de cet espace de noms. Vous pouvez utiliser le mot clé `using`. Ainsi, le nom complet n’est pas obligatoire, comme dans l’exemple suivant :  
  
[!code-csharp[csProgGuide#1](../inside-a-program/codesnippet/CSharp/index_2.cs)]  
  
[!code-csharp[csProgGuide#25](../inside-a-program/codesnippet/CSharp/index_3.cs)]  
  
Pour plus d’informations, consultez [Directive using](../../language-reference/keywords/using-directive.md).  
  
Deuxièmement, la déclaration de vos propres espaces de noms peut vous aider à contrôler l’étendue des noms de classes et de méthodes dans les projets de programmation plus vastes. Utilisez le mot clé [namespace](../../language-reference/keywords/namespace.md) pour déclarer un espace de noms, comme dans l’exemple suivant :  
  
[!code-csharp[csProgGuideNamespaces#6](codesnippet/CSharp/index_4.cs)]

Le nom de l’espace de noms doit être un [nom d’identificateur](../inside-a-program/identifier-names.md) C# valide.

## <a name="namespaces-overview"></a>Vue d'ensemble des espaces de noms  

Les espaces de noms ont les propriétés suivantes :  
  
- Ils organisent les projets de code de taille importante.  
- Ils sont délimités à l’aide de l’opérateur `.`.  
- La `using directive` évite de devoir spécifier le nom de l’espace de noms pour chaque classe.  
- L’espace de noms `global` est l’espace de noms « racine » : `global::System` fait toujours référence à l’espace de noms `System` du .NET Framework.  

## <a name="c-language-specification"></a>Spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation d’espaces de noms](using-namespaces.md)
- [Comment : utiliser l’alias d’espace de noms global](how-to-use-the-global-namespace-alias.md)
- [Comment : utiliser l’espace de noms My](how-to-use-the-my-namespace.md)
- [Guide de programmation C#](../index.md)  
- [Noms d’identificateur](../inside-a-program/identifier-names.md)
- [Mots clés d’espaces de noms](../../language-reference/keywords/namespace-keywords.md)  
- [using, directive](../../language-reference/keywords/using-directive.md)  
- [:: (opérateur)](../../language-reference/operators/namespace-alias-qualifer.md)  
- [. Opérateur](../../language-reference/operators/member-access-operator.md)
>>>>>>> ajouter des règles de nommage d’identificateur
