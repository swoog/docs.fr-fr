---
title: 'Comment : ouvrir un fichier journal et y ajouter des éléments'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- log files, opening
- streams, opening and appending to log file
- log files, appending to
- I/O [.NET Framework], log files
ms.assetid: 74423362-1721-49cb-aa0a-e04005f72a06
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 35a7d481cf82818054a852f7c2e142f615022fcb
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2018
ms.locfileid: "46695804"
---
# <a name="how-to-open-and-append-to-a-log-file"></a>Comment : ouvrir un fichier journal et y ajouter des éléments
<xref:System.IO.StreamWriter> et <xref:System.IO.StreamReader> écrivent des caractères dans et lisent des caractères à partir des flux. L’exemple de code suivant ouvre le fichier `log.txt` pour l’entrée, ou crée le fichier s’il n’existe pas déjà, et ajoute les informations à la fin du fichier. Le contenu du fichier est ensuite écrit vers la sortie standard pour affichage. Comme alternative à cet exemple, les informations peuvent être stockées en tant que chaîne unique ou tableau de chaînes et la méthode <xref:System.IO.File.WriteAllText%2A> ou <xref:System.IO.File.WriteAllLines%2A> peut être utilisée pour obtenir la même fonctionnalité.  
  
> [!NOTE]
>  Les utilisateurs Visual Basic peuvent choisir d’utiliser les méthodes et les propriétés fournies par la classe <xref:Microsoft.VisualBasic.Logging.Log> ou la classe <xref:Microsoft.VisualBasic.FileIO.FileSystem> pour la création ou l’écriture dans des fichiers journaux.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[Conceptual.BasicIO.TextFiles#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.basicio.textfiles/cs/source2.cs#2)]
 [!code-vb[Conceptual.BasicIO.TextFiles#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.basicio.textfiles/vb/source2.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO.StreamWriter>  
- <xref:System.IO.StreamReader>  
- <xref:System.IO.File.AppendText%2A?displayProperty=nameWithType>  
- <xref:System.IO.File.OpenText%2A?displayProperty=nameWithType>  
- <xref:System.IO.StreamReader.ReadLine%2A?displayProperty=nameWithType>  
- [Guide pratique pour énumérer des répertoires et des fichiers](../../../docs/standard/io/how-to-enumerate-directories-and-files.md)  
- [Comment : lire et écrire dans un fichier de données créé récemment](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)  
- [Comment : lire du texte dans un fichier](../../../docs/standard/io/how-to-read-text-from-a-file.md)  
- [Comment : écrire du texte dans un fichier](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
- [Comment : lire les caractères d’une chaîne](../../../docs/standard/io/how-to-read-characters-from-a-string.md)  
- [Comment : écrire des caractères dans une chaîne](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
- [Fichier et flux de données E/S](../../../docs/standard/io/index.md)
