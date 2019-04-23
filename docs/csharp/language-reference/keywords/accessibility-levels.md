---
title: Niveaux d’accessibilité - Référence C#
ms.custom: seodec18
ms.date: 12/06/2017
helpviewer_keywords:
- access modifiers [C#], accessibility levels
- accessibility levels
ms.assetid: dc083921-0073-413e-8936-a613e8bb7df4
ms.openlocfilehash: da49c6f0b44ab0eefbd338963a744a11502f75da
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59130466"
---
# <a name="accessibility-levels-c-reference"></a>Niveaux d’accessibilité (référence C#)

Utilisez les modificateurs d’accès `public`, `protected`, `internal` ou `private` pour spécifier l’un des niveaux d’accessibilité déclarés ci-dessous pour les membres.  
  
|Accessibilité déclarée|Signification|  
|----------------------------|-------------|  
|[`public`](public.md)|L’accès n’est pas limité.|  
|[`protected`](protected.md)|L’accès est limité à la classe conteneur ou aux types dérivés de la classe conteneur.|  
|[`internal`](internal.md)|L’accès est limité à l’assembly actuel.|  
|[`protected internal`](protected-internal.md)|L’accès est limité à l’assembly actuel ou aux types dérivés de la classe conteneur.|  
|[`private`](private.md)|L’accès est limité au type conteneur.|  
|[`private protected`](private-protected.md)|L’accès est limité à la classe conteneur ou aux types dérivés de la classe conteneur dans l’assembly actuel. Disponible depuis C# 7.2. |  
  
 Vous ne pouvez spécifier qu’un seul modificateur d’accès pour un membre ou un type, sauf si vous utilisez les combinaisons `protected internal` ou `private protected`.  
  
 Les modificateurs d’accès ne sont pas autorisés sur les espaces de noms. Les espaces de noms ne présentent aucune limitation d’accès.  
  
 Selon le contexte dans lequel une déclaration de membre est effectuée, seules certaines accessibilités déclarées sont autorisées. Si aucun modificateur d’accès n’est spécifié dans une déclaration de membre, une accessibilité par défaut est utilisée.  
  
 Les types de premier niveau, qui ne sont pas imbriqués dans d’autres types, peuvent uniquement avoir une accessibilité `internal` ou `public`. L’accessibilité par défaut de ces types est `internal`.  
  
 Les types imbriqués, qui sont membres d’autres types, peuvent avoir les accessibilités déclarées indiquées dans le tableau suivant.  
  
|Membres de|Accessibilité par défaut du membre|Accessibilité déclarée du membre autorisée|  
|----------------|----------------------------------|--------------------------------------------------|  
|`enum`|`public`|Aucun.|  
|`class`|`private`|`public`<br /><br /> `protected`<br /><br /> `internal`<br /><br /> `private`<br /><br /> `protected internal` <br /><br />`private protected`|  
|`interface`|`public`|Aucun.|  
|`struct`|`private`|`public`<br /><br /> `internal`<br /><br /> `private`|  
  
 L’accessibilité d’un type imbriqué dépend de son [domaine d’accessibilité](../../../csharp/language-reference/keywords/accessibility-domain.md), qui est déterminé à la fois par l’accessibilité déclarée du membre et par le domaine d’accessibilité du type conteneur immédiat. Toutefois, le domaine d'accessibilité d'un type imbriqué ne peut pas dépasser celui du type conteneur.  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)
- [Modificateurs d’accès](../../../csharp/language-reference/keywords/access-modifiers.md)
- [Domaine d’accessibilité](../../../csharp/language-reference/keywords/accessibility-domain.md)
- [Limitations sur l’utilisation des niveaux d’accessibilité](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md)
- [Modificateurs d’accès](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)
- [public](../../../csharp/language-reference/keywords/public.md)
- [private](../../../csharp/language-reference/keywords/private.md)
- [protected](../../../csharp/language-reference/keywords/protected.md)
- [internal](../../../csharp/language-reference/keywords/internal.md)
