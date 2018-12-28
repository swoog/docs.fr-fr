---
title: "'ReDim' ne peut pas changer le nombre de dimensions"
ms.date: 07/20/2015
f1_keywords:
- vbrArray_RankMismatch
ms.assetid: 52505298-9985-4682-8f6e-ff7d56077f34
ms.openlocfilehash: ba3e389e3732d39f16e2c8ae884fae4e935e6ac9
ms.sourcegitcommit: 0888d7b24f475c346a3f444de8d83ec1ca7cd234
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/22/2018
ms.locfileid: "53778721"
---
# <a name="redim-cannot-change-the-number-of-dimensions"></a>'ReDim' ne peut pas changer le nombre de dimensions
Une opération tente d’utiliser l’instruction `ReDim` pour modifier le rang (nombre de dimensions) d’un tableau. L’instruction`ReDim` peut modifier la taille d’une ou plusieurs dimensions d’un tableau qui a déjà été déclaré en bonne et due forme, mais elle ne peut pas modifier le rang d’un tableau.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Assurez-vous de bien vouloir modifier le rang du tableau et non la taille de ses dimensions et, si possible, utilisez `Dim` pour déclarer un nouveau tableau avec le rang souhaité.  
  
## <a name="see-also"></a>Voir aussi  
 [Tableaux en Visual Basic](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)  
 [Dimensions du tableau en Visual Basic](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)  
 [ReDim (instruction)](../../visual-basic/language-reference/statements/redim-statement.md)  
 [Dim (instruction)](../../visual-basic/language-reference/statements/dim-statement.md)
