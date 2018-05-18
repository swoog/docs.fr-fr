---
title: 'Comment : compresser et extraire des fichiers'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- I/O [.NET Framework], compression
- compression
- compress files
ms.assetid: e9876165-3c60-4c84-a272-513e47acf579
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f3e535e13fe91e1a5cb9c868428f5edbb9eac03f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-compress-and-extract-files"></a>Comment : compresser et extraire des fichiers
L'espace de noms <xref:System.IO.Compression> contient les types suivants pour la compression et la décompression de fichiers et de flux. Vous pouvez également utiliser ces types pour lire et modifier le contenu d’un fichier compressé :  
  
-   <xref:System.IO.Compression.ZipFile>  
  
-   <xref:System.IO.Compression.ZipArchive>  
  
-   <xref:System.IO.Compression.ZipArchiveEntry>  
  
-   <xref:System.IO.Compression.DeflateStream>  
  
-   <xref:System.IO.Compression.GZipStream>  
  
 Les exemples suivants présentent certaines des fonctions disponibles quand vous travaillez avec des fichiers compressés.  
  
## <a name="example"></a>Exemple  
 Cet exemple montre comment créer et extraire un fichier compressé ayant une extension de nom de fichier .zip à l’aide de la classe <xref:System.IO.Compression.ZipFile>. Il compresse le contenu d’un dossier dans un nouveau fichier .zip, puis extrait ce contenu dans un nouveau dossier. Pour utiliser la classe <xref:System.IO.Compression.ZipFile>, vous devez référencer l’assembly `System.IO.Compression.FileSystem` dans votre projet.  
  
 [!code-csharp[System.IO.Compression.ZipFile#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.zipfile/cs/program1.cs#1)]
 [!code-vb[System.IO.Compression.ZipFile#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.zipfile/vb/program1.vb#1)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment itérer au sein du contenu d’un fichier .zip existant et en extraire les fichiers ayant une extension .txt. Il utilise la classe <xref:System.IO.Compression.ZipArchive> pour accéder à un fichier .zip existant, et la classe <xref:System.IO.Compression.ZipArchiveEntry> pour inspecter les entrées individuelles du fichier compressé. Il utilise une méthode d’extension (<xref:System.IO.Compression.ZipFileExtensions.ExtractToFile%2A>) pour l’objet <xref:System.IO.Compression.ZipArchiveEntry>. La méthode d’extension est disponible dans la classe <xref:System.IO.Compression.ZipFileExtensions?displayProperty=nameWithType>. Pour utiliser la classe <xref:System.IO.Compression.ZipFileExtensions>, vous devez référencer l’assembly `System.IO.Compression.FileSystem` dans votre projet.  
  
 [!code-csharp[System.IO.Compression.ZipArchive#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.ziparchive/cs/program1.cs#1)]
 [!code-vb[System.IO.Compression.ZipArchive#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.ziparchive/vb/program1.vb#1)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise la classe <xref:System.IO.Compression.ZipArchive> pour accéder à un fichier .zip existant, puis ajoute un nouveau fichier au fichier compressé. Le nouveau fichier est compressé quand vous l’ajoutez au fichier .zip existant.  
  
 [!code-csharp[System.IO.Compression.ZipArchiveMode#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.ziparchivemode/cs/program1.cs#1)]
 [!code-vb[System.IO.Compression.ZipArchiveMode#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.ziparchivemode/vb/program1.vb#1)]  
  
## <a name="example"></a>Exemple  
 Vous pouvez également utiliser les classes <xref:System.IO.Compression.GZipStream> et <xref:System.IO.Compression.DeflateStream> pour compresser et décompresser des données. Elles utilisent le même algorithme de compression. Les objets <xref:System.IO.Compression.GZipStream> compressés qui sont écrits dans un fichier ayant une extension .gz peuvent être décompressés à l’aide de nombreux outils courants en plus des méthodes fournies par <xref:System.IO.Compression.GZipStream>. Cet exemple montre comment compresser et décompresser un répertoire de fichiers à l’aide de la classe <xref:System.IO.Compression.GZipStream>.  
  
 [!code-csharp[IO.Compression.GZip1#1](../../../samples/snippets/csharp/VS_Snippets_CLR/IO.Compression.GZip1/CS/gziptest.cs#1)]
 [!code-vb[IO.Compression.GZip1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/IO.Compression.GZip1/VB/gziptest.vb#1)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.IO.Compression.ZipArchive>  
 <xref:System.IO.Compression.ZipFile>  
 <xref:System.IO.Compression.ZipArchiveEntry>  
 <xref:System.IO.Compression.DeflateStream>  
 <xref:System.IO.Compression.GZipStream>  
 [Fichier et flux de données E/S](../../../docs/standard/io/index.md)
