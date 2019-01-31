---
title: 'Procédure : rechercher des sous-répertoires avec un modèle spécifique en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- pattern matching
- folders, finding
ms.assetid: c9265fd1-7483-4150-8b7f-ff642caa939d
ms.openlocfilehash: 32b0f5c1052d45e9c068d291f8e6efaf6dfbf906
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54677691"
---
# <a name="how-to-find-subdirectories-with-a-specific-pattern-in-visual-basic"></a>Procédure : rechercher des sous-répertoires avec un modèle spécifique en Visual Basic
La méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetDirectories%2A> retourne une collection en lecture seule de chaînes représentant les noms de chemin des sous-répertoires d’un répertoire. Vous pouvez utiliser le paramètre `wildCards` pour indiquer un modèle spécifique. Si vous souhaitez inclure le contenu des sous-répertoires dans la recherche, affectez la valeur `SearchOption.SearchAllSubDirectories` au paramètre `searchType`.  
  
 Une collection vide est retournée si aucun répertoire correspondant au modèle spécifié n’est détecté.  
  
### <a name="to-find-subdirectories-with-a-specific-pattern"></a>Pour rechercher des sous-répertoires avec un modèle spécifique  
  
-   Utilisez la méthode `GetDirectories`, en fournissant le nom et le chemin du répertoire à rechercher. L’exemple suivant retourne tous les répertoires dans la structure de répertoires dont le nom contient le mot « Logs », et il les ajoute à `ListBox1`.  
  
     [!code-vb[VbVbcnFileAccess#1](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-find-subdirectories-with-a-specific-pattern_1.vb)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   Le chemin n’est pas valide pour l’une des raisons suivantes : il s’agit d’une chaîne de longueur nulle, il ne contient que des espaces blancs, il contient des caractères non valides ou il s’agit d’un chemin d’appareil (il commence par \\\\.\\) (<xref:System.ArgumentException>).  
  
-   Le chemin n’est pas valide, car il a la valeur `Nothing` (<xref:System.ArgumentNullException>).  
  
-   Un ou plusieurs des caractères génériques spécifiés sont `Nothing`, une chaîne vide ou contiennent uniquement des espaces (<xref:System.ArgumentNullException>).  
  
-   `directory` n'existe pas (<xref:System.IO.DirectoryNotFoundException>).  
  
-   `directory` pointe vers un fichier existant (<xref:System.IO.IOException>).  
  
-   Le chemin dépasse la longueur maximale définie par le système (<xref:System.IO.PathTooLongException>).  
  
-   Un nom de fichier ou de dossier dans le chemin contient un signe deux-points (:) ou n’a pas un format correct (<xref:System.NotSupportedException>).  
  
-   L'utilisateur n'a pas les autorisations nécessaires pour afficher le chemin d'accès (<xref:System.Security.SecurityException>).  
  
-   L'utilisateur ne dispose pas des autorisations nécessaires (<xref:System.UnauthorizedAccessException>).  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetDirectories%2A>
- [Guide pratique pour rechercher des fichiers avec un modèle spécifique](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-find-files-with-a-specific-pattern.md)
