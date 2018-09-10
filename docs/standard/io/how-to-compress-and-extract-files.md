---
title: Guide pratique pour compresser et extraire des fichiers
ms.date: 06/06/2018
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
ms.openlocfilehash: 669936d15cfe1ea125ed36ffdfcfd093b6aacbe1
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44225079"
---
# <a name="how-to-compress-and-extract-files"></a><span data-ttu-id="00833-102">Guide pratique pour compresser et extraire des fichiers</span><span class="sxs-lookup"><span data-stu-id="00833-102">How to: Compress and extract files</span></span>

<span data-ttu-id="00833-103">L'espace de noms <xref:System.IO.Compression> contient les types suivants pour la compression et la décompression de fichiers et de flux.</span><span class="sxs-lookup"><span data-stu-id="00833-103">The <xref:System.IO.Compression> namespace contains the following types for compressing and decompressing files and streams.</span></span> <span data-ttu-id="00833-104">Vous pouvez également utiliser ces types pour lire et modifier le contenu d’un fichier compressé :</span><span class="sxs-lookup"><span data-stu-id="00833-104">You can also use these types to read and modify the contents of a compressed file:</span></span>

- <xref:System.IO.Compression.ZipFile>

- <xref:System.IO.Compression.ZipArchive>

- <xref:System.IO.Compression.ZipArchiveEntry>

- <xref:System.IO.Compression.DeflateStream>

- <xref:System.IO.Compression.GZipStream>

<span data-ttu-id="00833-105">Les exemples suivants présentent certaines des fonctions disponibles quand vous travaillez avec des fichiers compressés.</span><span class="sxs-lookup"><span data-stu-id="00833-105">The following examples show some of the functions you can perform when working with compressed files.</span></span>

## <a name="example-1---create-and-extract-a-zip-file"></a><span data-ttu-id="00833-106">Exemple 1 : Créer et extraire un fichier .zip</span><span class="sxs-lookup"><span data-stu-id="00833-106">Example 1 - Create and extract a .zip file</span></span>

<span data-ttu-id="00833-107">L’exemple suivant montre comment créer et extraire un fichier compressé ayant une extension de nom de fichier .zip à l’aide de la classe <xref:System.IO.Compression.ZipFile>.</span><span class="sxs-lookup"><span data-stu-id="00833-107">The following example shows how to create and extract a compressed file that has a .zip file name extension by using the <xref:System.IO.Compression.ZipFile> class.</span></span> <span data-ttu-id="00833-108">Il compresse le contenu d’un dossier dans un nouveau fichier .zip, puis extrait ce contenu dans un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="00833-108">It compresses the contents of a folder into a new .zip file and then extracts that content to a new folder.</span></span> <span data-ttu-id="00833-109">Pour utiliser la classe <xref:System.IO.Compression.ZipFile>, vous devez référencer l’assembly `System.IO.Compression.FileSystem` dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="00833-109">To use the <xref:System.IO.Compression.ZipFile> class, you must reference the `System.IO.Compression.FileSystem` assembly in your project.</span></span>

[!code-csharp[System.IO.Compression.ZipFile#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.zipfile/cs/program1.cs#1)]
[!code-vb[System.IO.Compression.ZipFile#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.zipfile/vb/program1.vb#1)]

## <a name="example-2---extract-specific-file-extensions"></a><span data-ttu-id="00833-110">Exemple 2 : Extraire des extensions de fichier spécifiques</span><span class="sxs-lookup"><span data-stu-id="00833-110">Example 2 - Extract specific file extensions</span></span>

<span data-ttu-id="00833-111">L’exemple suivant montre comment itérer au sein du contenu d’un fichier .zip existant et en extraire les fichiers ayant une extension .txt.</span><span class="sxs-lookup"><span data-stu-id="00833-111">The next example shows how to iterate through the contents of an existing .zip file and extract files that have a .txt extension.</span></span> <span data-ttu-id="00833-112">Il utilise la classe <xref:System.IO.Compression.ZipArchive> pour accéder à un fichier .zip existant, et la classe <xref:System.IO.Compression.ZipArchiveEntry> pour inspecter les entrées individuelles du fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="00833-112">It uses the <xref:System.IO.Compression.ZipArchive> class to access an existing .zip file, and the <xref:System.IO.Compression.ZipArchiveEntry> class to inspect the individual entries in the compressed file.</span></span> <span data-ttu-id="00833-113">Il utilise une méthode d’extension (<xref:System.IO.Compression.ZipFileExtensions.ExtractToFile%2A>) pour l’objet <xref:System.IO.Compression.ZipArchiveEntry>.</span><span class="sxs-lookup"><span data-stu-id="00833-113">It uses an extension method (<xref:System.IO.Compression.ZipFileExtensions.ExtractToFile%2A>) for the <xref:System.IO.Compression.ZipArchiveEntry> object.</span></span> <span data-ttu-id="00833-114">La méthode d’extension est disponible dans la classe <xref:System.IO.Compression.ZipFileExtensions?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="00833-114">The extension method is available in the <xref:System.IO.Compression.ZipFileExtensions?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="00833-115">Pour utiliser la classe <xref:System.IO.Compression.ZipFileExtensions>, vous devez référencer l’assembly `System.IO.Compression.FileSystem` dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="00833-115">To use the <xref:System.IO.Compression.ZipFileExtensions> class, you must reference the `System.IO.Compression.FileSystem` assembly in your project.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00833-116">Lors de la décompression des fichiers, vous devez rechercher des chemins d’accès malveillants qui risquent de sortir du répertoire dans lequel vous souhaitez décompresser les fichiers.</span><span class="sxs-lookup"><span data-stu-id="00833-116">When unzipping files, you must look for malicious file paths which can escape out of the directory where you want to unzip into.</span></span> <span data-ttu-id="00833-117">Il s’agit d’une attaque par chemin transversal.</span><span class="sxs-lookup"><span data-stu-id="00833-117">This is known as a path traversal attack.</span></span>

<span data-ttu-id="00833-118">L’exemple suivant montre comment rechercher les chemins d’accès malveillants et garantir une décompression sûre :</span><span class="sxs-lookup"><span data-stu-id="00833-118">The following example demonstrates how to check for malicious file paths and provides a safe way to unzip:</span></span>

[!code-csharp[System.IO.Compression.ZipArchive#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.ziparchive/cs/program1.cs#1)]
[!code-vb[System.IO.Compression.ZipArchive#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.ziparchive/vb/program1.vb#1)]

## <a name="example-3---add-a-new-file-to-an-existing-zip-file"></a><span data-ttu-id="00833-119">Exemple 3 : Ajouter un nouveau fichier à un fichier .zip existant</span><span class="sxs-lookup"><span data-stu-id="00833-119">Example 3 - Add a new file to an existing .zip file</span></span>

<span data-ttu-id="00833-120">L’exemple suivant utilise la classe <xref:System.IO.Compression.ZipArchive> pour accéder à un fichier .zip existant, puis ajoute un nouveau fichier au fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="00833-120">The following example uses the <xref:System.IO.Compression.ZipArchive> class to access an existing .zip file, and adds a new file to the compressed file.</span></span> <span data-ttu-id="00833-121">Le nouveau fichier est compressé quand vous l’ajoutez au fichier .zip existant.</span><span class="sxs-lookup"><span data-stu-id="00833-121">The new file gets compressed when you add it to the existing .zip file.</span></span>

[!code-csharp[System.IO.Compression.ZipArchiveMode#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.compression.ziparchivemode/cs/program1.cs#1)]
[!code-vb[System.IO.Compression.ZipArchiveMode#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.compression.ziparchivemode/vb/program1.vb#1)]

## <a name="example-4---compress-and-decompress-a-directory-of-gz-files"></a><span data-ttu-id="00833-122">Exemple 4 : Compresser et décompresser un répertoire de fichiers .gz</span><span class="sxs-lookup"><span data-stu-id="00833-122">Example 4 - Compress and decompress a directory of .gz files</span></span>

<span data-ttu-id="00833-123">Vous pouvez également utiliser les classes <xref:System.IO.Compression.GZipStream> et <xref:System.IO.Compression.DeflateStream> pour compresser et décompresser des données.</span><span class="sxs-lookup"><span data-stu-id="00833-123">You can also use the <xref:System.IO.Compression.GZipStream> and <xref:System.IO.Compression.DeflateStream> classes to compress and decompress data.</span></span> <span data-ttu-id="00833-124">Elles utilisent le même algorithme de compression.</span><span class="sxs-lookup"><span data-stu-id="00833-124">They use the same compression algorithm.</span></span> <span data-ttu-id="00833-125">Les objets <xref:System.IO.Compression.GZipStream> compressés qui sont écrits dans un fichier ayant une extension .gz peuvent être décompressés à l’aide de nombreux outils courants en plus des méthodes fournies par <xref:System.IO.Compression.GZipStream>.</span><span class="sxs-lookup"><span data-stu-id="00833-125">Compressed <xref:System.IO.Compression.GZipStream> objects that are written to a file that has an extension of .gz can be decompressed by using many common tools in addition to the methods provided by <xref:System.IO.Compression.GZipStream>.</span></span> <span data-ttu-id="00833-126">L’exemple suivant montre comment compresser et décompresser un répertoire de fichiers à l’aide de la classe <xref:System.IO.Compression.GZipStream> :</span><span class="sxs-lookup"><span data-stu-id="00833-126">The following example shows how to compress and decompress a directory of files by using the <xref:System.IO.Compression.GZipStream> class:</span></span>

[!code-csharp[IO.Compression.GZip1#1](../../../samples/snippets/csharp/VS_Snippets_CLR/IO.Compression.GZip1/CS/gziptest.cs#1)]
[!code-vb[IO.Compression.GZip1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/IO.Compression.GZip1/VB/gziptest.vb#1)]

## <a name="see-also"></a><span data-ttu-id="00833-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00833-127">See also</span></span>

- <xref:System.IO.Compression.ZipArchive>  
- <xref:System.IO.Compression.ZipFile>  
- <xref:System.IO.Compression.ZipArchiveEntry>  
- <xref:System.IO.Compression.DeflateStream>  
- <xref:System.IO.Compression.GZipStream>  
- [<span data-ttu-id="00833-128">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="00833-128">File and Stream I/O</span></span>](../../../docs/standard/io/index.md)
