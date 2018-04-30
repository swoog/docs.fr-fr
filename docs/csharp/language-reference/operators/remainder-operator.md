---
title: '%, opérateur (référence C#)'
ms.date: 04/04/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '%_CSharpKeyword'
helpviewer_keywords:
- remainder operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
caps.latest.revision: 15
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 796b4a40347fc5881db27a8a8a28404c7c4e8c5b
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="-operator-c-reference"></a>%, opérateur (référence C#)
L’opérateur de reste (`%`) calcule le reste de la division du premier opérande par le deuxième. Tous les types numériques ont des opérateurs de reste prédéfinis. 
  
## <a name="remarks"></a>Notes  
 La formule `a % b` retourne toujours une valeur de la plage `(-b, b)`, de manière exclusive (elle ne retourne jamais `b` ou `-b`), en conservant le signe du dividende. Pour la division entière, l’opérateur de reste applique la règle `a % b = a - (a / b) * b`.
  
 Cela est différent du modulo canonique, qui applique une règle similaire avec une division plancher et retourne des valeurs de la plage `[0, b)`. C# ne fournit pas d’opérateur de modulo canonique. Toutefois, le comportement est le même pour les dividendes positifs.
  
 Les types définis par l’utilisateur peuvent surcharger l’opérateur `%` (voir [operator](../../../csharp/language-reference/keywords/operator.md)). Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#9](../../../csharp/language-reference/operators/codesnippet/CSharp/remainder-operator_1.cs)]  
  
## <a name="comments"></a>Commentaires  
 Notez les erreurs d’arrondi associées au type double.  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
