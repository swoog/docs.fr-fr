---
title: 'Comment : déclarer une variable objet et lui affecter un objet dans Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], declaring
- declaring object variables [Visual Basic]
ms.assetid: 2fa77dde-1fb2-439a-80d4-3e9787649fad
ms.openlocfilehash: 1f38c90f0571b3fc73c4c89812092cdada936d84
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33648874"
---
# <a name="how-to-declare-an-object-variable-and-assign-an-object-to-it-in-visual-basic"></a>Comment : déclarer une variable objet et lui affecter un objet dans Visual Basic
Vous déclarez une variable de la [Type de données d’objet](../../../../visual-basic/language-reference/data-types/object-data-type.md) en spécifiant `As Object` dans un [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md). Vous assignez un objet à cette variable en plaçant l’objet après le signe égal (`=`) dans une clause d’instruction ou d’initialisation d’attribution.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déclare une `Object` variable et assigne actuel d’instance.  
  
```  
      Dim thisObject As Object  
thisObject = "This is an Object"  
```  
  
 Vous pouvez combiner la déclaration et l’assignation en initialisant la variable dans le cadre de sa déclaration. L’exemple suivant est équivalent à l’exemple précédent.  
  
```  
Dim thisObject As Object= "This is an Object"  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   une référence à l'espace de noms <xref:System>.  
  
-   Une classe, une structure ou un module dans lequel placer la `Dim` instruction.  
  
-   Une procédure dans laquelle placer l’instruction d’assignation.  
  
## <a name="see-also"></a>Voir aussi  
 [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)  
 [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)  
 [Déclaration des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)  
 [Object (type de données)](../../../../visual-basic/language-reference/data-types/object-data-type.md)  
 [Dim (instruction)](../../../../visual-basic/language-reference/statements/dim-statement.md)  
 [Inférence de type local](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)  
 [Option Strict (instruction)](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
