---
title: Convention d’appel de DLL incorrecte
ms.date: 07/20/2015
f1_keywords:
- vbrID49
ms.assetid: 7c7def45-b0ab-450f-ad3f-4383dfd9aed7
ms.openlocfilehash: d8c7f7aea46162215115689305f4010cb513b020
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33583836"
---
# <a name="bad-dll-calling-convention"></a>Convention d’appel de DLL incorrecte
Arguments passés à une bibliothèque de liens dynamiques (DLL) doivent correspondre exactement à ceux attendus par la routine. Conventions d’appel traitent nombre, type et ordre des arguments. Votre programme peut appeler une routine dans une DLL qui est passée du type incorrect ou le nombre d’arguments.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous que tous les types d’argument correspondent à ceux spécifiés dans la déclaration de la routine que vous appelez.  
  
2.  Vérifiez que vous passez le même nombre d’arguments indiqué dans la déclaration de la routine que vous appelez.  
  
3.  Si la routine DLL attend des arguments par valeur, vérifiez que `ByVal` est spécifié pour ces arguments dans la déclaration de la routine.  
  
## <a name="see-also"></a>Voir aussi  
 [Types d’erreurs](../../../visual-basic/programming-guide/language-features/error-types.md)  
 [Call (instruction)](../../../visual-basic/language-reference/statements/call-statement.md)  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
