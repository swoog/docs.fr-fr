---
title: 'Déclaration d’opérateur doit être une des : +,-, *,-, -, ^, &amp;, Like, Mod et, Or, Xor, pas, &lt; &lt;, &gt; &gt;, =, &lt; &gt;, &lt;, &lt;=, &gt; , &gt;=, CType, IsTrue, IsFalse'
ms.date: 07/20/2015
f1_keywords:
- bc33000
- vbc33000
helpviewer_keywords:
- BC33000
ms.assetid: 15c5d8eb-3a8c-4141-8f41-33151afabf97
ms.openlocfilehash: f32935dd4aaccd3040655b418badc13c1988c1b8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54622271"
---
# <a name="operator-declaration-must-be-one-of----amp-like-mod-and-or-xor-not-ltlt-gtgt"></a>Déclaration d’opérateur doit être une des : +,-, *,\,/, ^, &amp;, Like, Mod et, Or, Xor, pas, &lt; &lt;, &gt; &gt;...
Vous pouvez déclarer uniquement un opérateur qui est éligible pour la surcharge. Le tableau suivant répertorie les opérateurs que vous pouvez déclarer.  
  
|Type|Opérateurs|  
|----------|---------------|  
|Unaire|`+`, `-`, `IsFalse`, `IsTrue`, `Not`|  
|Binaire|`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`|  
|Conversion (unaire)|`CType`|  
  
 Notez que le `=` opérateur dans la liste binaire est l’opérateur de comparaison, pas l’opérateur d’assignation.  
  
 **ID d’erreur :** BC33000  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Sélectionnez un opérateur dans le jeu d’opérateurs surchargeables.  
  
2.  Si vous avez besoin des fonctionnalités de surcharge d’un opérateur que vous ne pouvez pas surcharger directement, créez une procédure `Function` qui accepte les paramètres appropriés et retourne la valeur adéquate.  
  
## <a name="see-also"></a>Voir aussi
- [Operator (instruction)](../../../visual-basic/language-reference/statements/operator-statement.md)
- [Procédures d’opérateur](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)
- [Guide pratique pour Définir un opérateur](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [Guide pratique pour Définir un opérateur de Conversion](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)
