---
title: value (référence C#)
ms.date: 07/20/2015
f1_keywords:
- value_CSharpKeyword
helpviewer_keywords:
- value keyword [C#]
ms.assetid: c99d6468-687f-4a46-89b4-a95e1b00bf6d
ms.openlocfilehash: 1e120d68fc4a42f24feb225f652c14525fde3d71
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42931940"
---
# <a name="value-c-reference"></a>value (référence C#)
Le mot clé contextuel `value` est utilisé dans l’accesseur set de déclarations de propriété ordinaires. Il est similaire à un paramètre d’entrée sur une méthode. Le mot `value` fait référence à la valeur que le code client tente d’assigner à la propriété. Dans l’exemple suivant, `MyDerivedClass` a une propriété appelée `Name` qui utilise le paramètre `value` pour assigner une nouvelle chaîne au `name` du champ de stockage. Du point de vue du code client, l’opération est écrite comme une assignation simple.  
  
 [!code-csharp[csrefKeywordsModifiers#26](../../../csharp/language-reference/keywords/codesnippet/CSharp/value_1.cs)]  
  
 Pour plus d’informations sur l’utilisation de `value`, consultez [Propriétés](../../../csharp/programming-guide/classes-and-structs/properties.md).  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)
