---
title: L’opérande 'ReDim' ne peut pas être Nothing
ms.date: 07/20/2015
ms.assetid: b857f313-3fc2-4262-a577-88df1718b811
ms.openlocfilehash: a4153795bc72e831d9f4bb0814df0c410cf67ab8
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738836"
---
# <a name="redim-preserve-operand-cannot-be-nothing"></a>L’opérande 'ReDim' ne peut pas être Nothing
Une instruction `ReDim` tente d’utiliser le mot clé `Preserve` pour modifier une dimension d’un tableau qui n’est pas la dernière dimension, mais elle ne fournit pas de valeur valide pour son opérande.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Remplacez l’opérande `Preserve` par une valeur valide.  
  
## <a name="see-also"></a>Voir aussi
- [Tableaux en Visual Basic](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)
- [Dimensions du tableau en Visual Basic](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)
- [ReDim (instruction)](../../visual-basic/language-reference/statements/redim-statement.md)
- [Dim (instruction)](../../visual-basic/language-reference/statements/dim-statement.md)
