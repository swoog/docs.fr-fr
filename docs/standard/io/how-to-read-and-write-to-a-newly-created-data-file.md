---
title: 'Comment : lire et écrire dans un fichier de données créé récemment'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- streams, reading and writing data
- BinaryReader class, examples
- I/O [.NET Framework], reading data
- I/O [.NET Framework], writing data
- BinaryWriter class, examples
ms.assetid: e209d949-31e8-44ea-8e38-87f9093f3093
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6b854495a32755b2cbbd0421b1a45458fd2b7863
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-read-and-write-to-a-newly-created-data-file"></a>Comment : lire et écrire dans un fichier de données créé récemment
Les classes <xref:System.IO.BinaryWriter> et <xref:System.IO.BinaryReader?displayProperty=nameWithType> sont utilisées pour écrire et lire des données plutôt que des chaînes de caractères. L’exemple suivant montre comment écrire et lire des données dans un flux de fichier vide nommé `Test.data`. Après avoir créé le fichier de données dans le répertoire actif, les objets <xref:System.IO.BinaryWriter> et <xref:System.IO.BinaryReader> associés sont créés, et l’objet <xref:System.IO.BinaryWriter> est utilisé pour écrire les entiers de 0 à 10 dans `Test.data`, ce qui laisse le pointeur de fichier à la fin du fichier. Après avoir replacé le pointeur de fichier au début, l’objet <xref:System.IO.BinaryReader> lit le contenu spécifié.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.IO.BinaryReaderWriter#7](../../../samples/snippets/cpp/VS_Snippets_CLR_System/system.IO.BinaryReaderWriter/CPP/source6.cpp#7)]
 [!code-csharp[System.IO.BinaryReaderWriter#7](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.IO.BinaryReaderWriter/CS/source6.cs#7)]
 [!code-vb[System.IO.BinaryReaderWriter#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.IO.BinaryReaderWriter/VB/source6.vb#7)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 Si `Test.data` existe déjà dans le répertoire actif, une exception <xref:System.IO.IOException> est levée. Utilisez l’option de mode de fichier <xref:System.IO.FileMode.Create?displayProperty=nameWithType> lors de l’initialisation du flux de fichier pour toujours créer un nouveau fichier sans lever d’exception.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.IO.BinaryReader>  
 <xref:System.IO.BinaryWriter>  
 <xref:System.IO.FileStream>  
 <xref:System.IO.FileStream.Seek%2A?displayProperty=nameWithType>  
 <xref:System.IO.SeekOrigin>  
 [Guide pratique pour énumérer des répertoires et des fichiers](../../../docs/standard/io/how-to-enumerate-directories-and-files.md)  
 [Comment : ouvrir un fichier journal et y ajouter des éléments](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)  
 [Comment : lire du texte dans un fichier](../../../docs/standard/io/how-to-read-text-from-a-file.md)  
 [Comment : écrire du texte dans un fichier](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
 [Comment : lire les caractères d’une chaîne](../../../docs/standard/io/how-to-read-characters-from-a-string.md)  
 [Comment : écrire des caractères dans une chaîne](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
 [Fichier et flux de données E/S](../../../docs/standard/io/index.md)
