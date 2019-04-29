---
title: L’opérande 'ReDim' ne peut pas être Nothing
ms.date: 07/20/2015
ms.assetid: b857f313-3fc2-4262-a577-88df1718b811
ms.openlocfilehash: 0f2354cdf52c65eb3ce387933ebfc825c80e6bad
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61613325"
---
# <a name="redim-preserve-operand-cannot-be-nothing"></a>L’opérande 'ReDim' ne peut pas être Nothing
Une instruction `ReDim` tente d’utiliser le mot clé `Preserve` pour modifier une dimension d’un tableau qui n’est pas la dernière dimension, mais elle ne fournit pas de valeur valide pour son opérande.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Remplacez l’opérande `Preserve` par une valeur valide.  
  
## <a name="see-also"></a>Voir aussi

- [Tableaux en Visual Basic](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)
- [Dimensions du tableau en Visual Basic](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)
- [ReDim (instruction)](../../visual-basic/language-reference/statements/redim-statement.md)
- [Dim (instruction)](../../visual-basic/language-reference/statements/dim-statement.md)
