---
title: 'Procédure : énumérer des répertoires et des fichiers'
ms.date: 12/27/2018
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- I/O [.NET Framework], enumerating directories and files
ms.assetid: 86b69a08-3bfa-4e5f-b4e1-3b7cb8478215
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 863335cf080dbccd76b38c7222b74637b99ae2f0
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758662"
---
# <a name="how-to-enumerate-directories-and-files"></a><span data-ttu-id="f5db7-102">Procédure : énumérer des répertoires et des fichiers</span><span class="sxs-lookup"><span data-stu-id="f5db7-102">How to: Enumerate directories and files</span></span>
<span data-ttu-id="f5db7-103">Les collections énumérables offrent de meilleures performances que les tableaux lorsque vous travaillez avec collections volumineuses de fichiers et de répertoires.</span><span class="sxs-lookup"><span data-stu-id="f5db7-103">Enumerable collections provide better performance than arrays when you work with large collections of directories and files.</span></span> <span data-ttu-id="f5db7-104">Pour énumérer des répertoires et des fichiers, utilisez des méthodes qui retournent une collection énumérable de noms de répertoire ou de fichier ou leurs objets <xref:System.IO.DirectoryInfo>, <xref:System.IO.FileInfo> ou <xref:System.IO.FileSystemInfo>.</span><span class="sxs-lookup"><span data-stu-id="f5db7-104">To enumerate directories and files, use methods that return an enumerable collection of directory or file names, or their <xref:System.IO.DirectoryInfo>, <xref:System.IO.FileInfo>, or <xref:System.IO.FileSystemInfo> objects.</span></span>  
  
<span data-ttu-id="f5db7-105">Si vous souhaitez parcourir et retourner uniquement les noms des répertoires ou des fichiers, utilisez les méthodes d’énumération de la classe <xref:System.IO.Directory>.</span><span class="sxs-lookup"><span data-stu-id="f5db7-105">If you want to search and return only the names of directories or files, use the enumeration methods of the <xref:System.IO.Directory> class.</span></span> <span data-ttu-id="f5db7-106">Si vous souhaitez parcourir et retourner d’autres propriétés des répertoires ou des fichiers, utilisez les classes <xref:System.IO.DirectoryInfo> et <xref:System.IO.FileSystemInfo>.</span><span class="sxs-lookup"><span data-stu-id="f5db7-106">If you want to search and return other properties of directories or files, use the <xref:System.IO.DirectoryInfo> and <xref:System.IO.FileSystemInfo> classes.</span></span>  
  
<span data-ttu-id="f5db7-107">Vous pouvez utiliser les collections énumérables issues de ces méthodes en tant que paramètre <xref:System.Collections.Generic.IEnumerable%601> pour les constructeurs de classes de collection, comme <xref:System.Collections.Generic.List%601>.</span><span class="sxs-lookup"><span data-stu-id="f5db7-107">You can use enumerable collections from these methods as the <xref:System.Collections.Generic.IEnumerable%601> parameter for constructors of collection classes like <xref:System.Collections.Generic.List%601>.</span></span>  
  
<span data-ttu-id="f5db7-108">Le tableau suivant récapitule les méthodes qui retournent des collections énumérables de fichiers et de répertoires .</span><span class="sxs-lookup"><span data-stu-id="f5db7-108">The following table summarizes the methods that return enumerable collections of files and directories:</span></span>  
  
|<span data-ttu-id="f5db7-109">Pour parcourir et retourner</span><span class="sxs-lookup"><span data-stu-id="f5db7-109">To search and return</span></span>|<span data-ttu-id="f5db7-110">Utiliser la méthode</span><span class="sxs-lookup"><span data-stu-id="f5db7-110">Use method</span></span>|  
|------------------|-------------------------------------|-------------------|  
|<span data-ttu-id="f5db7-111">Noms de répertoires</span><span class="sxs-lookup"><span data-stu-id="f5db7-111">Directory names</span></span>|<xref:System.IO.Directory.EnumerateDirectories%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="f5db7-112">Informations sur le répertoire (<xref:System.IO.DirectoryInfo>)</span><span class="sxs-lookup"><span data-stu-id="f5db7-112">Directory information (<xref:System.IO.DirectoryInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="f5db7-113">Noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="f5db7-113">File names</span></span>|<xref:System.IO.Directory.EnumerateFiles%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="f5db7-114">Informations sur le fichier (<xref:System.IO.FileInfo>)</span><span class="sxs-lookup"><span data-stu-id="f5db7-114">File information (<xref:System.IO.FileInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="f5db7-115">Noms d’entrée de système de fichiers</span><span class="sxs-lookup"><span data-stu-id="f5db7-115">File system entry names</span></span>|<xref:System.IO.Directory.EnumerateFileSystemEntries%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="f5db7-116">Informations sur les entrées de système de fichiers (<xref:System.IO.FileSystemInfo>)</span><span class="sxs-lookup"><span data-stu-id="f5db7-116">File system entry information (<xref:System.IO.FileSystemInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateFileSystemInfos%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="f5db7-117">Noms de répertoires et de fichiers</span><span class="sxs-lookup"><span data-stu-id="f5db7-117">Directory and file names</span></span> |<xref:System.IO.Directory.EnumerateFileSystemEntries%2A?displayProperty=nameWithType>|  

> [!NOTE]
> <span data-ttu-id="f5db7-118">Bien que vous puissiez énumérer immédiatement tous les fichiers dans les sous-répertoires d’un répertoire parent à l’aide de l’option <xref:System.IO.SearchOption.AllDirectories> de l’énumération <xref:System.IO.SearchOption> facultative, des erreurs <xref:System.UnauthorizedAccessException> peuvent rendre l’énumération incomplète.</span><span class="sxs-lookup"><span data-stu-id="f5db7-118">Although you can immediately enumerate all the files in the subdirectories of a parent directory by using the <xref:System.IO.SearchOption.AllDirectories> option of the optional <xref:System.IO.SearchOption> enumeration, <xref:System.UnauthorizedAccessException> errors may make the enumeration incomplete.</span></span> <span data-ttu-id="f5db7-119">Vous pouvez intercepter ces exceptions en énumérant d’abord les répertoires, puis les fichiers.</span><span class="sxs-lookup"><span data-stu-id="f5db7-119">You can catch these exceptions by first enumerating directories and then enumerating files.</span></span>  
  
## <a name="examples-use-the-directory-class"></a><span data-ttu-id="f5db7-120">Exemples : utiliser la classe Directory</span><span class="sxs-lookup"><span data-stu-id="f5db7-120">Examples: Use the Directory class</span></span>  
  
<span data-ttu-id="f5db7-121">L’exemple suivant utilise la méthode <xref:System.IO.Directory.EnumerateDirectories%28System.String%29?displayProperty=nameWithType> pour obtenir une liste des noms de répertoires de niveau supérieur dans un chemin spécifié.</span><span class="sxs-lookup"><span data-stu-id="f5db7-121">The following example uses the <xref:System.IO.Directory.EnumerateDirectories%28System.String%29?displayProperty=nameWithType> method to get a list of the top-level directory names in a specified path.</span></span>  

[!code-csharp[System.IO.EnumDirs1#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.enumdirs1/cs/program.cs#1)]
[!code-vb[System.IO.EnumDirs1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.enumdirs1/vb/program.vb#1)]  

<span data-ttu-id="f5db7-122">L’exemple suivant utilise la méthode <xref:System.IO.Directory.EnumerateFiles%28System.String%2CSystem.String%2CSystem.IO.SearchOption%29?displayProperty=nameWithType> pour énumérer de manière récursive tous les noms de fichiers dans un répertoire et dans les sous-répertoires qui correspondent à un certain modèle.</span><span class="sxs-lookup"><span data-stu-id="f5db7-122">The following example uses the <xref:System.IO.Directory.EnumerateFiles%28System.String%2CSystem.String%2CSystem.IO.SearchOption%29?displayProperty=nameWithType> method to recursively enumerate all file names in a directory and subdirectories that match a certain pattern.</span></span> <span data-ttu-id="f5db7-123">Il lit chaque ligne de chaque fichier et affiche les lignes qui contiennent la chaîne spécifiée, avec les noms de fichiers et chemins correspondants.</span><span class="sxs-lookup"><span data-stu-id="f5db7-123">It then reads each line of each file and displays the lines that contain a specified string, with their filenames and paths.</span></span>

[!code-csharp[System.IO.Directory.EnumerateFiles#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directory.enumeratefiles/cs/program.cs#1)]
[!code-vb[System.IO.Directory.EnumerateFiles#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directory.enumeratefiles/vb/program.vb#1)]  
  
## <a name="examples-use-the-directoryinfo-class"></a><span data-ttu-id="f5db7-124">Exemples : utiliser la classe DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="f5db7-124">Examples: Use the DirectoryInfo class</span></span>  
  
<span data-ttu-id="f5db7-125">L’exemple suivant utilise la méthode <xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType> pour lister une collection de répertoires de niveau supérieur dont <xref:System.IO.FileSystemInfo.CreationTimeUtc> est antérieur à une certaine valeur <xref:System.DateTime>.</span><span class="sxs-lookup"><span data-stu-id="f5db7-125">The following example uses the <xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType> method to list a collection of top-level directories whose <xref:System.IO.FileSystemInfo.CreationTimeUtc> is earlier than a certain <xref:System.DateTime> value.</span></span>  

[!code-csharp[System.IO.DirectoryInfo.EnumDirs#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directoryinfo.enumdirs/cs/program.cs)]
[!code-vb[System.IO.DirectoryInfo.EnumDirs#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directoryinfo.enumdirs/vb/module1.vb)]  
  
<span data-ttu-id="f5db7-126">L’exemple suivant utilise la méthode <xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType> pour lister tous les fichiers dont <xref:System.IO.FileInfo.Length> dépasse 10 Mo.</span><span class="sxs-lookup"><span data-stu-id="f5db7-126">The following example uses the <xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType> method to list all files whose <xref:System.IO.FileInfo.Length> exceeds 10MB.</span></span> <span data-ttu-id="f5db7-127">Cet exemple énumère d’abord les répertoires de niveau supérieur, pour intercepter les éventuelles exceptions d’accès non autorisé, puis énumère les fichiers.</span><span class="sxs-lookup"><span data-stu-id="f5db7-127">This example first enumerates the top-level directories, to catch possible unauthorized access exceptions, and then enumerates the files.</span></span>  

[!code-csharp[System.IO.DirectoryInfo.EnumerateDirectories#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directoryinfo.enumeratedirectories/cs/program.cs#1)]
[!code-vb[System.IO.DirectoryInfo.EnumerateDirectories#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directoryinfo.enumeratedirectories/vb/program.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="f5db7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5db7-128">See also</span></span>

- [<span data-ttu-id="f5db7-129">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="f5db7-129">File and stream I/O</span></span>](../../../docs/standard/io/index.md)
