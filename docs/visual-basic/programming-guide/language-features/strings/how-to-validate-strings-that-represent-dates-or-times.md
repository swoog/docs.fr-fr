---
title: 'Comment : valider des chaînes qui représentent des dates ou des heures (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], validating
- String data type [Visual Basic], validation
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
ms.openlocfilehash: 411c8517783421b2472c3e4aa77287f8252f179b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647860"
---
# <a name="how-to-validate-strings-that-represent-dates-or-times-visual-basic"></a>Comment : valider des chaînes qui représentent des dates ou des heures (Visual Basic)
Le code suivant exemple définit un `Boolean` valeur qui indique si une chaîne représente une date ou heure valide.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbcnRegEx#2](../../../../visual-basic/programming-guide/language-features/strings/codesnippet/VisualBasic/how-to-validate-strings-that-represent-dates-or-times_1.vb)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Remplacez `("01/01/03")` et `"9:30 PM"` avec la date et l’heure que vous souhaitez valider. Vous pouvez remplacer la chaîne par une autre chaîne codée en dur, avec un `String` ou variable, avec une méthode qui retourne une chaîne, telle que `InputBox`.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Utilisez cette méthode pour valider la chaîne avant d’essayer de convertir le `String` à un `DateTime` variable. En vérifiant tout d’abord la date ou l’heure, vous pouvez éviter de générer une exception au moment de l’exécution.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.Information.IsDate%2A>  
 <xref:Microsoft.VisualBasic.Interaction.InputBox%2A>  
 [Validation de chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
