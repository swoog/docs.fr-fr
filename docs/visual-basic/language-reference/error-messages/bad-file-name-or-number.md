---
title: Nom ou numéro de fichier incorrect
ms.date: 07/20/2015
f1_keywords:
- vbrID52
ms.assetid: d0e96aea-7621-48f6-a78b-5d37d18aaa4e
ms.openlocfilehash: 903be68e71ad590b4b669545afd077175534ef4d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33585565"
---
# <a name="bad-file-name-or-number"></a>Nom ou numéro de fichier incorrect
Une erreur s’est produite lors de la tentative d’accès au fichier spécifié. Parmi les causes possibles de cette erreur sont :  
  
-   Une instruction fait référence à un fichier avec un nom de fichier ou d’un nombre qui n’a pas été spécifié dans le `FileOpen` instruction ou qui a été spécifié dans un `FileOpen` instruction mais a ensuite fermé.  
  
-   Une instruction fait référence à un fichier avec un nombre qui est en dehors de la plage des numéros de fichier.  
  
-   Une instruction fait référence à un nom de fichier ou un nombre qui n’est pas valide.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous que le nom de fichier est spécifié dans un `FileOpen` instruction. Notez que si vous avez appelé la `FileClose` instruction sans arguments, vous avez peut-être fermé accidentellement tous les fichiers ouverts.  
  
2.  Si votre code génère des nombres de fichier par algorithme, vérifiez que les nombres sont valides.  
  
3.  Vérifiez les noms de fichiers pour vous assurer qu’elles sont conformes aux conventions du système d’exploitation.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>  
 [Conventions d’affectation de noms de Visual Basic](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
