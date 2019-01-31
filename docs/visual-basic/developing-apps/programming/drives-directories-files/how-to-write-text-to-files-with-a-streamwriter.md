---
title: 'Procédure : écrire du texte dans des fichiers à l’aide de StreamWriter dans Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], writing to
- text, writing to files
- writing to files [Visual Basic], StreamWriter
ms.assetid: 99762e57-ef46-4dcc-8959-a8f79c22f067
ms.openlocfilehash: 39c6ad59ad965f566c77f72dd4a97335494d6382
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678523"
---
# <a name="how-to-write-text-to-files-with-a-streamwriter-in-visual-basic"></a>Procédure : écrire du texte dans des fichiers à l’aide de StreamWriter dans Visual Basic
Cet exemple ouvre un objet <xref:System.IO.StreamWriter> avec la méthode `My.Computer.FileSystem.OpenTextFileWriter` et l’utilise pour écrire une chaîne dans un fichier texte avec la méthode <xref:System.IO.TextWriter.WriteLine%2A> de la classe <xref:System.IO.StreamWriter>.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbFileIOWrite#5](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-write-text-to-files-with-a-streamwriter_1.vb)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   Le fichier existe et est en lecture seule (<xref:System.IO.IOException>).  
  
-   Le disque est plein (<xref:System.IO.IOException>).  
  
-   Le nom du chemin est trop long (<xref:System.IO.PathTooLongException>).  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Cet exemple crée un fichier s’il n’existe pas déjà. Si une application doit créer un fichier, elle doit disposer de l’autorisation `Create` pour accéder au dossier. Si le fichier existe déjà, l’application a uniquement besoin de l’autorisation `Write`, qui est une autorisation de niveau inférieur. Quand cela est possible, il est plus sûr de créer le fichier au cours du déploiement et de n’accorder l’autorisation `Read` que sur un seul fichier, plutôt que l’autorisation `Create` sur un dossier.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.IO.StreamWriter>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.OpenTextFileWriter%2A>
- [Guide pratique pour lire des fichiers texte](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-text-files.md)
- [Écriture dans des fichiers](../../../../visual-basic/developing-apps/programming/drives-directories-files/writing-to-files.md)
