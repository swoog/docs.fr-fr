---
title: '&#39;ReDim&#39; ne pouvez modifier la dimension la plus à droite'
ms.date: 07/20/2015
f1_keywords:
- vbrArray_TypeMismatch
ms.assetid: d53cf41b-7a7a-466c-a29a-920d99698fa9
ms.openlocfilehash: 94e0fe81f7e750a67943b68f2db700e3a7831da1
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482715"
---
# <a name="39redim39-can-only-change-the-right-most-dimension"></a>&#39;ReDim&#39; ne pouvez modifier la dimension la plus à droite
Une instruction `ReDim` a tenté d’utiliser le mot clé `Preserve` pour modifier une dimension d’un tableau qui n’est pas la dernière dimension. Lors de l’utilisation de `Preserve`, vous pouvez redimensionner uniquement la dernière dimension d’un tableau. Pour toutes les autres dimensions, vous devez spécifier la même taille que pour le tableau existant.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Supprimez le mot clé `Preserve` .  
  
## <a name="see-also"></a>Voir aussi  
 [Tableaux en Visual Basic](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)  
 [Dimensions du tableau en Visual Basic](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)  
 [ReDim (instruction)](../../visual-basic/language-reference/statements/redim-statement.md)  
 [Dim (instruction)](../../visual-basic/language-reference/statements/dim-statement.md)  
 [Conserver - supprimer](https://msdn.microsoft.com/library/91badeab-b4e0-48b6-92c9-9f0c8f995d81)
