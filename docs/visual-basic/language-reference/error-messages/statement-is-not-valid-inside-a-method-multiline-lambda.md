---
title: Instruction n’est pas valide à l’intérieur d’une expression lambda multiligne (méthode)
ms.date: 07/20/2015
f1_keywords:
- vbc30024
- bc30024
helpviewer_keywords:
- BC30024
ms.assetid: 758e7a8f-429b-42c1-9a78-778e5b480e04
ms.openlocfilehash: 994cafc44a37d16d0f70caec560f530c6a836ec0
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58841561"
---
# <a name="statement-is-not-valid-inside-a-methodmultiline-lambda"></a>Instruction non valide dans une méthode ou une expression lambda multiligne
L’instruction n’est pas valide dans un `Sub`, `Function`, propriété `Get`, ou une propriété `Set` procédure. Certaines instructions peuvent être placées au niveau du module ou de la classe. D’autres, tels que `Option Strict`, doit être au niveau de l’espace de noms et précéder toutes les autres déclarations.  
  
 **ID d’erreur :** BC30024  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Supprimez l’instruction de la procédure.  
  
## <a name="see-also"></a>Voir aussi

- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)
- [Get (instruction)](../../../visual-basic/language-reference/statements/get-statement.md)
- [Set (instruction)](../../../visual-basic/language-reference/statements/set-statement.md)
