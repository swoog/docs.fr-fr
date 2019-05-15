---
title: Nothing et les chaînes en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], Nothing
ms.assetid: 261380af-2024-4ecf-823b-43b1034d92cd
ms.openlocfilehash: f5c1ea8cc0728b25e8e874963967aed504e466d7
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591346"
---
# <a name="nothing-and-strings-in-visual-basic"></a>Nothing et les chaînes en Visual Basic
Le runtime Visual Basic et .NET Framework évaluent `Nothing` différemment lorsqu’il s’agit de chaînes.  
  
## <a name="visual-basic-runtime-and-the-net-framework"></a>Runtime Visual Basic et .NET Framework  
 Prenons l'exemple suivant :  
  
 [!code-vb[VbVbalrStrings#47](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#47)]  
  
 Le runtime Visual Basic prend généralement la valeur `Nothing` comme une chaîne vide ( » »). Le .NET Framework est pas le cas, toutefois et lève une exception chaque fois qu’une tentative est effectuée pour effectuer une opération de chaîne sur `Nothing`.  
  
## <a name="see-also"></a>Voir aussi

- [Introduction aux chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
