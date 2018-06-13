---
title: Le codage ne peut pas avoir la valeur Nothing
ms.date: 07/20/2015
ms.assetid: 59f7c731-8291-4a85-bf51-c225e48cdc84
ms.openlocfilehash: 05f64dfe9610f679986040ec87e6287caac9bd08
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33638117"
---
# <a name="encoding-cannot-be-set-to-nothing"></a>Le codage ne peut pas avoir la valeur Nothing
Une tentative de lecture ou d’écriture dans un fichier a échoué, car le paramètre `encoding` a la valeur `Nothing` , mais requiert une valeur valide.  
  
 <xref:System.Text.Encoding> est utilisé pour déterminer le codage à utiliser lors de l’écriture dans un fichier. La valeur par défaut est UTF-8.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Fournissez une valeur valide pour le paramètre `encoding` .  
  
## <a name="see-also"></a>Voir aussi  
 [Codages de fichiers](../../visual-basic/developing-apps/programming/drives-directories-files/file-encodings.md)  
 [Lecture à partir de fichiers](../../visual-basic/developing-apps/programming/drives-directories-files/reading-from-files.md)  
 [Écriture dans des fichiers](../../visual-basic/developing-apps/programming/drives-directories-files/writing-to-files.md)  
 [My.Computer.FileSystem.ReadAllText](xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A)  
 [My.Computer.FileSystem.WriteAllText](xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A)
