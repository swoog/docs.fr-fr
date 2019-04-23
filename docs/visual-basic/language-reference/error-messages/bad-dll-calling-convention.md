---
title: Convention d’appel de DLL incorrecte
ms.date: 07/20/2015
f1_keywords:
- vbrID49
ms.assetid: 7c7def45-b0ab-450f-ad3f-4383dfd9aed7
ms.openlocfilehash: f7b0c3a6edbe0b950195306fa66287ff9b209bfe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59306623"
---
# <a name="bad-dll-calling-convention"></a>Convention d’appel de DLL incorrecte
Arguments passés à une bibliothèque de liens dynamiques (DLL) doivent correspondre exactement à ceux attendus par la routine. Conventions d’appel traitent nombre, type et ordre des arguments. Votre programme peut appeler une routine dans une DLL qui lui est passée le type incorrect ou le nombre d’arguments.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Assurez-vous que tous les types d’argument correspondent à ceux spécifiés dans la déclaration de la routine que vous appelez.  
  
2. Vérifiez que vous passez le même nombre d’arguments indiqué dans la déclaration de la routine que vous appelez.  
  
3. Si la routine DLL attend des arguments par valeur, assurez-vous que `ByVal` est spécifié pour ces arguments dans la déclaration de la routine.  
  
## <a name="see-also"></a>Voir aussi

- [Types d’erreurs](../../../visual-basic/programming-guide/language-features/error-types.md)
- [Call (instruction)](../../../visual-basic/language-reference/statements/call-statement.md)
- [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
