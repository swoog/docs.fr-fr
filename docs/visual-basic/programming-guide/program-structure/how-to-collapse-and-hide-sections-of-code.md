---
title: 'Comment : réduire et masquer des sections de code (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic, code collapsing
- Visual Basic, code hiding
- Visual Basic code, collapsing and hiding
ms.assetid: b770e8f5-e07d-491a-ab4b-a977980f9ba2
ms.openlocfilehash: f6c272b7ac016258d99873512cb789bba6739727
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-collapse-and-hide-sections-of-code-visual-basic"></a>Comment : réduire et masquer des sections de code (Visual Basic)
Le `#Region` directive vous permet de réduire et masquer des sections de code dans des fichiers Visual Basic. Le `#Region` directive vous permet de spécifier un bloc de code que vous pouvez développer ou réduire lors de l’utilisation de l’éditeur de code Visual Studio. La possibilité de masquer le code de manière sélective rend vos fichiers plus gérable et plus facile à lire. Pour plus d’informations, voir [Mode Plan](/visualstudio/ide/outlining).  
  
 `#Region` directives prennent en charge une sémantique de bloc de code comme `#If...#End If`. Cela signifie qu’ils ne peuvent pas commencer dans un bloc et se terminer par une autre ; le début et fin doivent être dans le même bloc. `#Region` directives ne sont pas pris en charge dans les fonctions.  
  
### <a name="to-collapse-and-hide-a-section-of-code"></a>Pour réduire et masquer une section de code  
  
-   Placez la section de code entre les `#Region` et `#End Region` instructions, comme dans l’exemple suivant :  
  
     [!code-vb[VbVbalrConditionalComp#6](../../../visual-basic/language-reference/directives/codesnippet/VisualBasic/how-to-collapse-and-hide-sections-of-code_1.vb)]  
  
     Le `#Region` bloc peut être utilisé plusieurs fois dans un fichier de code ; par conséquent, les utilisateurs peuvent définir leurs propres blocs de procédures et des classes qui peuvent, à son tour, être réduits. `#Region` les blocs peuvent également être imbriqués dans d’autres `#Region` blocs.  
  
    > [!NOTE]
    >  Masquage du code n’empêche pas sa compilation et n’affecte pas `#If...#End If` instructions.  
  
## <a name="see-also"></a>Voir aussi  
 [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)  
 [#Region (directive)](../../../visual-basic/language-reference/directives/region-directive.md)  
 [#If...Then...#Else, directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md)  
 [Mode Plan](/visualstudio/ide/outlining)
