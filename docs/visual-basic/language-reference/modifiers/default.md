---
title: Default (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Default
helpviewer_keywords:
- defaults, properties
- properties [Visual Basic], default
- default properties, in Visual Basic
- Default keyword [Visual Basic]
- default properties
ms.assetid: 45fce9b9-d212-4b2d-ab86-6e359b8b57af
ms.openlocfilehash: f78ffe42a9d618d44da2a50c0de831396576430c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58836725"
---
# <a name="default-visual-basic"></a>Default (Visual Basic)
Identifie une propriété comme la propriété par défaut de sa classe, une structure ou une interface.  
  
## <a name="remarks"></a>Notes  
 Une classe, une structure ou une interface peut désigner au plus une de ses propriétés comme le *propriété par défaut*, à condition que la propriété prend au moins un paramètre. Si le code fait référence à une classe ou structure sans spécifier un membre, Visual Basic résout qu’une référence à la propriété par défaut.  
  
 Propriétés par défaut peuvent entraîner une légère réduction dans les caractères de code source, mais ils peuvent rendre votre code plus difficile à lire. Si le code appelant n’est pas familiarisé avec votre classe ou structure, lorsqu’il fait référence au nom de classe ou structure il ne peut pas être certains que cette référence accède à la classe ou structure lui-même ou une propriété par défaut. Cela peut entraîner des erreurs du compilateur ou des erreurs de logique d’exécution subtiles.  
  
 Vous pouvez légèrement réduire les risques d’erreurs de propriété par défaut en utilisant toujours la [Option Strict, instruction](../../../visual-basic/language-reference/statements/option-strict-statement.md) pour définir le contrôle de type du compilateur `On`.  
  
 Si vous envisagez d’utiliser une classe prédéfinie ou une structure dans votre code, vous devez déterminer s’il possède une propriété par défaut et si c’est le cas, ce que son nom est.  
  
 En raison de ces inconvénients, vous devez envisager de ne pas définir les propriétés par défaut. Pour la lisibilité du code, vous devez également envisager de toujours faire explicitement référence à toutes les propriétés, même les propriétés par défaut.  
  
 Le `Default` modificateur peut être utilisé dans ce contexte :  
  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Déclarer et appeler une propriété par défaut en Visual Basic](../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-and-call-a-default-property.md)
- [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
