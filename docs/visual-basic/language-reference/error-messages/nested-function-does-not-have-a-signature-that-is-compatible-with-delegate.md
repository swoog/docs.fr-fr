---
title: La fonction imbriquée n'a pas une signature compatible avec le délégué '<delegatename>'.
ms.date: 07/20/2015
f1_keywords:
- vbc36532
- bc36532
helpviewer_keywords:
- BC36532
ms.assetid: 493f292c-d81e-40ef-8b47-61f020571829
ms.openlocfilehash: 912962e2ab39c4811294ccc225814b230100e12a
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64592012"
---
# <a name="nested-function-does-not-have-a-signature-that-is-compatible-with-delegate-delegatename"></a>Fonction imbriquée n’a pas une signature qui est compatible avec le délégué '\<nom_délégué >'
Une expression lambda a été assignée à un délégué qui a une signature incompatible. Par exemple, dans le code suivant, le délégué `Del` a deux paramètres entiers.  
  
```vb  
Delegate Function Del(ByVal p As Integer, ByVal q As Integer) As Integer  
```  
  
 L’erreur est générée si une expression lambda avec un argument est déclarée comme type `Del`:  
  
```vb  
' Neither of these is valid.   
' Dim lambda1 As Del = Function(n As Integer) n + 1  
' Dim lambda2 As Del = Function(n) n + 1  
```  
  
 **ID d’erreur :** BC36532  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Ajustez la définition du délégué ou l’expression lambda assignée afin que les signatures sont compatibles.  
  
## <a name="see-also"></a>Voir aussi

- [Conversion simplifiée des délégués](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
- [Expressions lambda](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
