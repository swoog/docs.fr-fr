---
title: Le codage ne peut pas avoir la valeur Nothing
ms.date: 07/20/2015
ms.assetid: 59f7c731-8291-4a85-bf51-c225e48cdc84
ms.openlocfilehash: 492db7755e8b2b75ea8c60d7f4e1ccc1a5ded865
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64598362"
---
# <a name="encoding-cannot-be-set-to-nothing"></a>Le codage ne peut pas avoir la valeur Nothing
Une tentative de lecture ou d’écriture dans un fichier a échoué, car le paramètre `encoding` a la valeur `Nothing` , mais requiert une valeur valide.  
  
 <xref:System.Text.Encoding> est utilisé pour déterminer le codage à utiliser lors de l’écriture dans un fichier. La valeur par défaut est UTF-8.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Fournissez une valeur valide pour le paramètre `encoding` .  
  
## <a name="see-also"></a>Voir aussi

- [Codages de fichiers](../../visual-basic/developing-apps/programming/drives-directories-files/file-encodings.md)
- [Lecture à partir de fichiers](../../visual-basic/developing-apps/programming/drives-directories-files/reading-from-files.md)
- [Écriture dans des fichiers](../../visual-basic/developing-apps/programming/drives-directories-files/writing-to-files.md)
- [My.Computer.FileSystem.ReadAllText](xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A)
- [My.Computer.FileSystem.WriteAllText](xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A)
