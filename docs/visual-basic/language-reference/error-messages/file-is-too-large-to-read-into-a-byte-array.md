---
title: Le fichier est trop volumineux pour être lu dans un tableau d'octets
ms.date: 07/20/2015
ms.assetid: 686630a6-a439-46c7-8d7b-34613ae4c5d8
ms.openlocfilehash: 1b04d47cab77269a0ce84ef77c162a4401d99d9e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33585923"
---
# <a name="file-is-too-large-to-read-into-a-byte-array"></a>Le fichier est trop volumineux pour être lu dans un tableau d'octets
La taille du fichier que vous tentez de lire dans un tableau d’octets dépasse 4 Go. Le `My.Computer.FileSystem.ReadAllBytes` méthode ne peut pas lire un fichier qui dépasse cette taille.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Utilisez un <xref:System.IO.StreamReader> pour lire le fichier. Pour plus d’informations, consultez [principes de base de .NET Framework fichier e/s et le système de fichiers (Visual Basic)](../../../visual-basic/developing-apps/programming/drives-directories-files/basics-of-net-framework-file-io-and-the-file-system.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllBytes%2A>  
 <xref:System.IO.StreamReader>  
 [Accès au fichier avec Visual Basic](../../../visual-basic/developing-apps/programming/drives-directories-files/file-access.md)  
 [Guide pratique : lire le texte des fichiers avec un StreamReader](../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-text-from-files-with-a-streamreader.md)
