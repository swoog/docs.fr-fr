---
title: --, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- --_CSharpKeyword
helpviewer_keywords:
- -- operator [C#]
- decrement operator (--) [C#]
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
ms.openlocfilehash: 615b100447233856ab3740d075d69e3ae19285fd
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44210427"
---
# <a name="---operator-c-reference"></a>--, opérateur (référence C#)
L’opérateur de décrémentation (`--`) décrémente son opérande de 1. L’opérateur de décrémentation peut figurer avant ou après son opérande : `--variable` et `variable--`. La première forme est une opération de décrément préfixé. Le résultat de l’opération est la valeur de l’opérande « après » sa décrémentation. La deuxième forme est une opération de décrément suffixé. Le résultat de l’opération est la valeur de l’opérande « avant » sa décrémentation.  
  
## <a name="remarks"></a>Notes  
 Les types numériques et d’énumération ont des opérateurs de décrémentation prédéfinis.  
  
 Les types définis par l’utilisateur peuvent surcharger l’opérateur `--` (voir [operator](../../../csharp/language-reference/keywords/operator.md)). Les opérations sur les types intégraux sont en général autorisées sur l’énumération.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#8](../../../csharp/language-reference/operators/codesnippet/CSharp/decrement-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
