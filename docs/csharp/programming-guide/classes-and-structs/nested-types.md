---
title: Types imbriqués (guide de programmation C#)
ms.date: 07/10/2017
helpviewer_keywords:
- nested types [C#]
ms.assetid: f2e1b315-e3d1-48ce-977f-7bae0960ba99
ms.openlocfilehash: 57356fbf4bff218932d1f1b4c62532f10c175757
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33319931"
---
# <a name="nested-types-c-programming-guide"></a>Types imbriqués (guide de programmation C#)
Un type défini dans une [classe](../../../csharp/language-reference/keywords/class.md) ou un [struct](../../../csharp/language-reference/keywords/struct.md) s’appelle un type imbriqué. Exemple :  
  
[!code-csharp[csProgGuideObjects#68](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/nested-types_1.cs)]  
  
Que le type externe soit une classe ou un struct, les types imbriqués sont par défaut [private](../../../csharp/language-reference/keywords/private.md) ; ils sont accessibles uniquement à partir de leur type conteneur. Dans l’exemple précédent, la classe `Nested` est inaccessible aux types externes. 

Vous pouvez aussi spécifier un [modificateur d’accès](../../language-reference/keywords/access-modifiers.md) pour définir l’accessibilité d’un type imbriqué, comme ceci :

- Les types imbriqués d’une **classe** peuvent être [public](../../../csharp/language-reference/keywords/public.md), [protected](../../../csharp/language-reference/keywords/protected.md), [internal](../../../csharp/language-reference/keywords/internal.md), [protected internal](../../../csharp/language-reference/keywords/protected-internal.md), [private](../../../csharp/language-reference/keywords/private.md) ou [private protected](../../../csharp/language-reference/keywords/private-protected.md). 

   Cependant, le fait de définir une classe imbriquée `protected`, `protected internal` ou `private protected` à l’intérieur d’une [classe sealed](../../language-reference/keywords/sealed.md) a pour effet de générer l’avertissement de compilateur [CS0628](../../misc/cs0628.md), « nouveau membre protected déclaré dans une classe sealed ».
  
- Les types imbriqués d’un **struct** peuvent être [public](../../../csharp/language-reference/keywords/public.md), [internal](../../../csharp/language-reference/keywords/internal.md) ou [private](../../../csharp/language-reference/keywords/private.md).
  
L’exemple suivant fait passer le type de la classe `Nested` à public :
  
[!code-csharp[csProgGuideObjects#69](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/nested-types_2.cs)]  
  
 Le type imbriqué (ou interne) peut accéder au type conteneur (ou externe). Pour accéder au type conteneur, passez-le en tant qu’argument au constructeur du type imbriqué. Exemple :  
  
 [!code-csharp[csProgGuideObjects#70](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/nested-types_3.cs)]  
  
 Un type imbriqué a accès à tous les membres qui sont accessibles à son type conteneur. Il peut accéder aux membres privés et protégés du type conteneur, y compris à tous les membres protégés hérités.  
  
 Dans la déclaration précédente, le nom complet de classe `Nested` est `Container.Nested`. Il s'agit du nom utilisé pour créer une instance de la classe imbriquée, comme suit :  
  
 [!code-csharp[csProgGuideObjects#71](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/nested-types_4.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Classes et structs](../../../csharp/programming-guide/classes-and-structs/index.md)  
 [Modificateurs d’accès](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
 [Constructeurs](../../../csharp/programming-guide/classes-and-structs/constructors.md)
