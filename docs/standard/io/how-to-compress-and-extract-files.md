---
title: 'Comment : compresser et extraire des fichiers'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- I/O [.NET Framework], compression
- compression
- compress files
ms.assetid: e9876165-3c60-4c84-a272-513e47acf579
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 33c9249692998aea8c22ddbf75a5a9b7bdf28708
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="how-to-compress-and-extract-files"></a><span data-ttu-id="a2cdc-102">Comment : compresser et extraire des fichiers</span><span class="sxs-lookup"><span data-stu-id="a2cdc-102">How to: Compress and Extract Files</span></span>
<span data-ttu-id="a2cdc-103">L'espace de noms <xref:System.IO.Compression> contient les types suivants pour la compression et la décompression de fichiers et de flux.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-103">The <xref:System.IO.Compression> namespace contains the following types for compressing and decompressing files and streams.</span></span> <span data-ttu-id="a2cdc-104">Vous pouvez également utiliser ces types pour lire et modifier le contenu d’un fichier compressé :</span><span class="sxs-lookup"><span data-stu-id="a2cdc-104">You can also use these types to read and modify the contents of a compressed file:</span></span>  
  
-   <xref:System.IO.Compression.ZipFile>  
  
-   <xref:System.IO.Compression.ZipArchive>  
  
-   <xref:System.IO.Compression.ZipArchiveEntry>  
  
-   <xref:System.IO.Compression.DeflateStream>  
  
-   <xref:System.IO.Compression.GZipStream>  
  
 <span data-ttu-id="a2cdc-105">Les exemples suivants présentent certaines des fonctions disponibles quand vous travaillez avec des fichiers compressés.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-105">The following examples show some of the functions you can perform when working with compressed files.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a2cdc-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2cdc-106">Example</span></span>  
 <span data-ttu-id="a2cdc-107">Cet exemple montre comment créer et extraire un fichier compressé ayant une extension de nom de fichier .zip à l’aide de la classe <xref:System.IO.Compression.ZipFile>.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-107">This example shows how to create and extract a compressed file that has a .zip file name extension by using the <xref:System.IO.Compression.ZipFile> class.</span></span> <span data-ttu-id="a2cdc-108">Il compresse le contenu d’un dossier dans un nouveau fichier .zip, puis extrait ce contenu dans un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-108">It compresses the contents of a folder into a new .zip file and then extracts that content to a new folder.</span></span> <span data-ttu-id="a2cdc-109">Pour utiliser la classe <xref:System.IO.Compression.ZipFile>, vous devez référencer l’assembly `System.IO.Compression.FileSystem` dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-109">To use the <xref:System.IO.Compression.ZipFile> class, you must reference the `System.IO.Compression.FileSystem` assembly in your project.</span></span>  
  
 [!code-csharp[System.IO.Compression.ZipFile#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.zipfile/cs/program1.cs#1)]
 [!code-vb[System.IO.Compression.ZipFile#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.zipfile/vb/program1.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="a2cdc-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2cdc-110">Example</span></span>  
 <span data-ttu-id="a2cdc-111">L’exemple suivant montre comment itérer au sein du contenu d’un fichier .zip existant et en extraire les fichiers ayant une extension .txt.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-111">The next example shows how to iterate through the contents of an existing .zip file and extract files that have a .txt extension.</span></span> <span data-ttu-id="a2cdc-112">Il utilise la classe <xref:System.IO.Compression.ZipArchive> pour accéder à un fichier .zip existant, et la classe <xref:System.IO.Compression.ZipArchiveEntry> pour inspecter les entrées individuelles du fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-112">It uses the <xref:System.IO.Compression.ZipArchive> class to access an existing .zip file, and the <xref:System.IO.Compression.ZipArchiveEntry> class to inspect the individual entries in the compressed file.</span></span> <span data-ttu-id="a2cdc-113">Il utilise une méthode d’extension (<xref:System.IO.Compression.ZipFileExtensions.ExtractToFile%2A>) pour l’objet <xref:System.IO.Compression.ZipArchiveEntry>.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-113">It uses an extension method (<xref:System.IO.Compression.ZipFileExtensions.ExtractToFile%2A>) for the <xref:System.IO.Compression.ZipArchiveEntry> object.</span></span> <span data-ttu-id="a2cdc-114">La méthode d’extension est disponible dans la classe <xref:System.IO.Compression.ZipFileExtensions?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-114">The extension method is available in the <xref:System.IO.Compression.ZipFileExtensions?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="a2cdc-115">Pour utiliser la classe <xref:System.IO.Compression.ZipFileExtensions>, vous devez référencer l’assembly `System.IO.Compression.FileSystem` dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-115">To use the <xref:System.IO.Compression.ZipFileExtensions> class, you must reference the `System.IO.Compression.FileSystem` assembly in your project.</span></span>  
  
 [!code-csharp[System.IO.Compression.ZipArchive#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.ziparchive/cs/program1.cs#1)]
 [!code-vb[System.IO.Compression.ZipArchive#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.ziparchive/vb/program1.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="a2cdc-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2cdc-116">Example</span></span>  
 <span data-ttu-id="a2cdc-117">L’exemple suivant utilise la classe <xref:System.IO.Compression.ZipArchive> pour accéder à un fichier .zip existant, puis ajoute un nouveau fichier au fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-117">The next example uses the <xref:System.IO.Compression.ZipArchive> class to access an existing .zip file, and adds a new file to the compressed file.</span></span> <span data-ttu-id="a2cdc-118">Le nouveau fichier est compressé quand vous l’ajoutez au fichier .zip existant.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-118">The new file gets compressed when you add it to the existing .zip file.</span></span>  
  
 [!code-csharp[System.IO.Compression.ZipArchiveMode#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.ziparchivemode/cs/program1.cs#1)]
 [!code-vb[System.IO.Compression.ZipArchiveMode#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.ziparchivemode/vb/program1.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="a2cdc-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2cdc-119">Example</span></span>  
 <span data-ttu-id="a2cdc-120">Vous pouvez également utiliser les classes <xref:System.IO.Compression.GZipStream> et <xref:System.IO.Compression.DeflateStream> pour compresser et décompresser des données.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-120">You can also use the <xref:System.IO.Compression.GZipStream> and <xref:System.IO.Compression.DeflateStream> classes to compress and decompress data.</span></span> <span data-ttu-id="a2cdc-121">Elles utilisent le même algorithme de compression.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-121">They use the same compression algorithm.</span></span> <span data-ttu-id="a2cdc-122">Les objets <xref:System.IO.Compression.GZipStream> compressés qui sont écrits dans un fichier ayant une extension .gz peuvent être décompressés à l’aide de nombreux outils courants en plus des méthodes fournies par <xref:System.IO.Compression.GZipStream>.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-122">Compressed <xref:System.IO.Compression.GZipStream> objects that are written to a file that has an extension of .gz can be decompressed by using many common tools in addition to the methods provided by <xref:System.IO.Compression.GZipStream>.</span></span> <span data-ttu-id="a2cdc-123">Cet exemple montre comment compresser et décompresser un répertoire de fichiers à l’aide de la classe <xref:System.IO.Compression.GZipStream>.</span><span class="sxs-lookup"><span data-stu-id="a2cdc-123">This example shows how to compress and decompress a directory of files by using the <xref:System.IO.Compression.GZipStream> class.</span></span>  
  
 [!code-csharp[IO.Compression.GZip1#1](../../../samples/snippets/csharp/VS_Snippets_CLR/IO.Compression.GZip1/CS/gziptest.cs#1)]
 [!code-vb[IO.Compression.GZip1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/IO.Compression.GZip1/VB/gziptest.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="a2cdc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2cdc-124">See Also</span></span>  
 <xref:System.IO.Compression.ZipArchive>  
 <xref:System.IO.Compression.ZipFile>  
 <xref:System.IO.Compression.ZipArchiveEntry>  
 <xref:System.IO.Compression.DeflateStream>  
 <xref:System.IO.Compression.GZipStream>  
 [<span data-ttu-id="a2cdc-125">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="a2cdc-125">File and Stream I-O</span></span>](../../../docs/standard/io/index.md)
