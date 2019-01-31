---
title: 'Procédure : obtenir la collection de fichiers d’un répertoire en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- folders, working with
- files [Visual Basic], accessing
ms.assetid: 6c8ba7e8-dd37-4853-92bf-762b67c98160
ms.openlocfilehash: a708d9cfd7b1a5ded3088ee567660bd0b3a5423f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54731931"
---
# <a name="how-to-get-the-collection-of-files-in-a-directory-in-visual-basic"></a>Procédure : obtenir la collection de fichiers d’un répertoire en Visual Basic
Les surcharges de la méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%2A?displayProperty=nameWithType> retournent une collection en lecture seule de chaînes représentant les noms des fichiers contenus dans un répertoire :  
  
-   Utilisez la surcharge <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%28System.String%29> pour effectuer une recherche de fichier simple dans un répertoire spécifié, sans rechercher dans les sous-répertoires.  
  
-   Utilisez la surcharge <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles(System.String,Microsoft.VisualBasic.FileIO.SearchOption,System.String[])> pour spécifier des options supplémentaires pour votre recherche. Vous pouvez utiliser le paramètre `wildCards` pour spécifier un modèle de recherche. Pour inclure des sous-répertoires dans la recherche, affectez la valeur `searchType` au paramètre <xref:Microsoft.VisualBasic.FileIO.SearchOption.SearchAllSubDirectories?displayProperty=nameWithType>.  
  
 Une collection vide est retournée si aucun fichier correspondant au modèle spécifié n'est détecté.  
  
### <a name="to-list-files-in-a-directory"></a>Pour énumérer les fichiers contenus dans un répertoire  
  
-   Utilisez l'une des surcharges de méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%2A?displayProperty=nameWithType>, en fournissant le nom et le chemin d'accès au répertoire dans lequel effectuer la recherche dans le paramètre `directory`. L’exemple suivant retourne tous les fichiers contenus dans le répertoire et les ajoute à `ListBox1`.  
  
     [!code-vb[VbVbcnMyFileSystem#32](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-get-the-collection-of-files-in-a-directory_1.vb)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   Le chemin n’est pas valide pour l’une des raisons suivantes : il s’agit d’une chaîne de longueur nulle, il ne contient que des espaces blancs, il contient des caractères non valides ou il s’agit d’un chemin d’appareil (il commence par \\\\.\\) (<xref:System.ArgumentException>).  
  
-   Le chemin n’est pas valide, car il a la valeur `Nothing` (<xref:System.ArgumentNullException>).  
  
-   `directory` n'existe pas (<xref:System.IO.DirectoryNotFoundException>).  
  
-   `directory` pointe vers un fichier existant (<xref:System.IO.IOException>).  
  
-   Le chemin dépasse la longueur maximale définie par le système (<xref:System.IO.PathTooLongException>).  
  
-   Un nom de fichier ou de répertoire du chemin contient un signe deux-points (:) ou n'a pas un format correct (<xref:System.NotSupportedException>).  
  
-   L'utilisateur n'a pas les autorisations nécessaires pour afficher le chemin (<xref:System.Security.SecurityException>).  
  
-   L'utilisateur ne dispose pas des autorisations nécessaires (<xref:System.UnauthorizedAccessException>).  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%2A>
- [Guide pratique pour rechercher des fichiers avec un modèle spécifique](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-find-files-with-a-specific-pattern.md)
- [Guide pratique pour rechercher des sous-répertoires avec un modèle spécifique](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-find-subdirectories-with-a-specific-pattern.md)
