---
title: La fonction imbriquée n'a pas une signature compatible avec le délégué '<delegatename>'.
ms.date: 07/20/2015
f1_keywords:
- vbc36532
- bc36532
helpviewer_keywords:
- BC36532
ms.assetid: 493f292c-d81e-40ef-8b47-61f020571829
ms.openlocfilehash: ea6f230715520cb35809d57db76b300da326ec9a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283463"
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
  
-   Ajustez la définition du délégué ou l’expression lambda assignée afin que les signatures sont compatibles.  
  
## <a name="see-also"></a>Voir aussi
- [Conversion simplifiée des délégués](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
- [Expressions lambda](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
