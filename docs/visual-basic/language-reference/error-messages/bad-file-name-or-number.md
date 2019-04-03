---
title: Nom ou numéro de fichier incorrect
ms.date: 07/20/2015
f1_keywords:
- vbrID52
ms.assetid: d0e96aea-7621-48f6-a78b-5d37d18aaa4e
ms.openlocfilehash: b6da1031b60a4cd73c53588cf18992797c3fddab
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58839065"
---
# <a name="bad-file-name-or-number"></a>Nom ou numéro de fichier incorrect
Une erreur s’est produite lors de la tentative d’accès au fichier spécifié. Parmi les causes possibles de cette erreur sont :  
  
-   Une instruction fait référence à un fichier avec un nom de fichier ou d’un nombre qui n’a pas été spécifié dans le `FileOpen` instruction ou qui a été spécifié dans un `FileOpen` instruction mais elle était par la suite fermé.  
  
-   Une instruction fait référence à un fichier avec un nombre qui est en dehors de la plage de numéros de fichier.  
  
-   Une instruction fait référence à un nom de fichier ou un nombre qui n’est pas valide.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous que le nom de fichier est spécifié dans un `FileOpen` instruction. Notez que si vous avez appelé la `FileClose` instruction sans arguments, vous avez peut-être fermé accidentellement tous les fichiers ouverts.  
  
2.  Si votre code génère des numéros de fichier par algorithme, assurez-vous que les nombres sont valides.  
  
3.  Vérifiez les noms de fichier pour vous assurer qu’elles sont conformes aux conventions du système d’exploitation.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
- [Conventions d’affectation de noms de Visual Basic](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
