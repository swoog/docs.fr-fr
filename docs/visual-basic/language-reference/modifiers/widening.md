---
title: Widening (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.widening
helpviewer_keywords:
- conversions [Visual Basic], type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- Widening keyword [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: 646ae263-94d3-40a2-b0cc-64f619292f56
ms.openlocfilehash: d7d43d4f5f931881d5c8b663c719fe7f92559799
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778662"
---
# <a name="widening-visual-basic"></a>Widening (Visual Basic)
Indique qu’un opérateur de conversion (`CType`) convertit une classe ou structure à un type qui peut contenir toutes les valeurs possibles de la classe ou la structure d’origine.  
  
## <a name="converting-with-the-widening-keyword"></a>Conversion avec le mot clé étendu  
 La procédure de conversion doit spécifier `Public Shared` outre `Widening`.  
  
 Les conversions étendues aboutissent toujours en cours d’exécution et sans jamais aucune perte de données. Sont des exemples `Single` à `Double`, `Char` à `String`et un type dérivé à son type de base. Cette dernière conversion est étendue, car le type dérivé contient tous les membres du type de base et est donc une instance du type de base.  
  
 Le code de consommation n’a pas d’utiliser `CType` pour les conversions étendues, même si `Option Strict` est `On`.  
  
 Le `Widening` mot clé peut être utilisé dans ce contexte :  
  
 [Operator (instruction)](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 Par exemple des définitions d’étendues et restrictives des opérateurs de conversion, consultez [Comment : Définir un opérateur de Conversion](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).  
  
## <a name="see-also"></a>Voir aussi

- [Operator (instruction)](../../../visual-basic/language-reference/statements/operator-statement.md)
- [Narrowing](../../../visual-basic/language-reference/modifiers/narrowing.md)
- [Conversions étendues et restrictives](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Guide pratique pour Définir un opérateur](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [CType (fonction)](../../../visual-basic/language-reference/functions/ctype-function.md)
- [Option Strict (instruction)](../../../visual-basic/language-reference/statements/option-strict-statement.md)
- [Guide pratique pour Définir un opérateur de Conversion](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
