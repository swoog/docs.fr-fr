---
title: 'Comment : énumérer des répertoires et des fichiers'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- I/O [.NET Framework], enumerating directories and files
ms.assetid: 86b69a08-3bfa-4e5f-b4e1-3b7cb8478215
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3de83395df9e8c89a92e85b96ddd15e9f0be6ad5
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44207692"
---
# <a name="how-to-enumerate-directories-and-files"></a><span data-ttu-id="1f697-102">Comment : énumérer des répertoires et des fichiers</span><span class="sxs-lookup"><span data-stu-id="1f697-102">How to: Enumerate Directories and Files</span></span>
<span data-ttu-id="1f697-103">Vous pouvez énumérer des répertoires et des fichiers à l’aide de méthodes qui retournent une collection énumérable de chaînes de leurs noms.</span><span class="sxs-lookup"><span data-stu-id="1f697-103">You can enumerate directories and files by using methods that return an enumerable collection of strings of their names.</span></span> <span data-ttu-id="1f697-104">Vous pouvez également utiliser des méthodes qui retournent une collection énumérable d’objets <xref:System.IO.DirectoryInfo>, <xref:System.IO.FileInfo> ou <xref:System.IO.FileSystemInfo>.</span><span class="sxs-lookup"><span data-stu-id="1f697-104">You can also use methods that return an enumerable collection of <xref:System.IO.DirectoryInfo>, <xref:System.IO.FileInfo>, or <xref:System.IO.FileSystemInfo> objects.</span></span> <span data-ttu-id="1f697-105">Les collections énumérables offrent de meilleures performances que les tableaux lorsque vous travaillez avec collections volumineuses de fichiers et de répertoires.</span><span class="sxs-lookup"><span data-stu-id="1f697-105">Enumerable collections provide better performance than arrays when you work with large collections of directories and files.</span></span>  
  
 <span data-ttu-id="1f697-106">Vous pouvez également utiliser les collections énumérables obtenues à partir de ces méthodes pour fournir le paramètre <xref:System.Collections.Generic.IEnumerable%601> pour les constructeurs de classes de collection, comme la classe <xref:System.Collections.Generic.List%601>.</span><span class="sxs-lookup"><span data-stu-id="1f697-106">You can also use enumerable collections obtained from these methods to supply the <xref:System.Collections.Generic.IEnumerable%601> parameter for constructors of collection classes such as the <xref:System.Collections.Generic.List%601> class.</span></span>  
  
 <span data-ttu-id="1f697-107">Si vous souhaitez obtenir uniquement les noms des répertoires ou des fichiers, utilisez les méthodes d’énumération de la classe <xref:System.IO.Directory>.</span><span class="sxs-lookup"><span data-stu-id="1f697-107">If you want to obtain only the names of directories or files, use the enumeration methods of the <xref:System.IO.Directory> class.</span></span> <span data-ttu-id="1f697-108">Si vous souhaitez obtenir d’autres propriétés des répertoires ou des fichiers, utilisez les classes <xref:System.IO.DirectoryInfo> et <xref:System.IO.FileSystemInfo>.</span><span class="sxs-lookup"><span data-stu-id="1f697-108">If you want to obtain other properties of directories or files, use the <xref:System.IO.DirectoryInfo> and <xref:System.IO.FileSystemInfo> classes.</span></span>  
  
 <span data-ttu-id="1f697-109">Le tableau suivant fournit un guide sur les méthodes qui retournent des collections énumérables.</span><span class="sxs-lookup"><span data-stu-id="1f697-109">The following table provides a guide to the methods that return enumerable collections.</span></span>  
  
|<span data-ttu-id="1f697-110">Pour énumérer</span><span class="sxs-lookup"><span data-stu-id="1f697-110">To enumerate</span></span>|<span data-ttu-id="1f697-111">Collection énumérable à retourner</span><span class="sxs-lookup"><span data-stu-id="1f697-111">Enumerable collection to return</span></span>|<span data-ttu-id="1f697-112">Méthode à utiliser</span><span class="sxs-lookup"><span data-stu-id="1f697-112">Method to use</span></span>|  
|------------------|-------------------------------------|-------------------|  
|<span data-ttu-id="1f697-113">Répertoires</span><span class="sxs-lookup"><span data-stu-id="1f697-113">Directories</span></span>|<span data-ttu-id="1f697-114">Noms de répertoires</span><span class="sxs-lookup"><span data-stu-id="1f697-114">Directory names</span></span>|<xref:System.IO.Directory.EnumerateDirectories%2A?displayProperty=nameWithType>|  
||<span data-ttu-id="1f697-115">Informations sur le répertoire (<xref:System.IO.DirectoryInfo>)</span><span class="sxs-lookup"><span data-stu-id="1f697-115">Directory information (<xref:System.IO.DirectoryInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="1f697-116">Fichiers</span><span class="sxs-lookup"><span data-stu-id="1f697-116">Files</span></span>|<span data-ttu-id="1f697-117">Noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="1f697-117">File names</span></span>|<xref:System.IO.Directory.EnumerateFiles%2A?displayProperty=nameWithType>|  
||<span data-ttu-id="1f697-118">Informations sur le fichier (<xref:System.IO.FileInfo>)</span><span class="sxs-lookup"><span data-stu-id="1f697-118">File information (<xref:System.IO.FileInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="1f697-119">Informations sur le système de fichiers</span><span class="sxs-lookup"><span data-stu-id="1f697-119">File system information</span></span>|<span data-ttu-id="1f697-120">Entrées du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="1f697-120">File system entries</span></span>|<xref:System.IO.Directory.EnumerateFileSystemEntries%2A?displayProperty=nameWithType>|  
||<span data-ttu-id="1f697-121">Informations sur le système de fichiers (<xref:System.IO.FileSystemInfo>)</span><span class="sxs-lookup"><span data-stu-id="1f697-121">File system information (<xref:System.IO.FileSystemInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateFileSystemInfos%2A?displayProperty=nameWithType>|  
  
 <span data-ttu-id="1f697-122">Bien que vous puissiez énumérer immédiatement tous les fichiers dans les sous-répertoires d’un répertoire parent à l’aide de l’option de recherche <xref:System.IO.SearchOption.AllDirectories> fournie par l’énumération <xref:System.IO.SearchOption>, les exceptions d’accès non autorisé (<xref:System.UnauthorizedAccessException>) peuvent entraîner une énumération non terminée.</span><span class="sxs-lookup"><span data-stu-id="1f697-122">Although you can immediately enumerate all the files in the subdirectories of a parent directory by using the <xref:System.IO.SearchOption.AllDirectories> search option provided by the <xref:System.IO.SearchOption> enumeration, unauthorized access exceptions (<xref:System.UnauthorizedAccessException>) may cause the enumeration to be incomplete.</span></span> <span data-ttu-id="1f697-123">Si ces exceptions sont possibles, vous pouvez les intercepter et continuer en commençant par énumérer les répertoires, puis les fichiers.</span><span class="sxs-lookup"><span data-stu-id="1f697-123">If these exceptions are possible, you can catch them and continue by first enumerating directories and then enumerating files.</span></span>  
  
### <a name="to-enumerate-directory-names"></a><span data-ttu-id="1f697-124">Pour énumérer les noms de répertoires</span><span class="sxs-lookup"><span data-stu-id="1f697-124">To enumerate directory names</span></span>  
  
-   <span data-ttu-id="1f697-125">Utilisez la méthode <xref:System.IO.Directory.EnumerateDirectories%28System.String%29?displayProperty=nameWithType> pour obtenir une liste des noms de répertoires de niveau supérieur dans un chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="1f697-125">Use the <xref:System.IO.Directory.EnumerateDirectories%28System.String%29?displayProperty=nameWithType> method to obtain a list of the top-level directory names in a specified path.</span></span>  
  
     [!code-csharp[System.IO.EnumDirs1#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.enumdirs1/cs/program.cs#1)]
     [!code-vb[System.IO.EnumDirs1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.enumdirs1/vb/program.vb#1)]  
  
### <a name="to-enumerate-file-names-in-a-directory-and-subdirectories"></a><span data-ttu-id="1f697-126">Pour énumérer les noms de fichiers dans un répertoire et des sous-répertoires</span><span class="sxs-lookup"><span data-stu-id="1f697-126">To enumerate file names in a directory and subdirectories</span></span>  
  
-   <span data-ttu-id="1f697-127">Utilisez la méthode <xref:System.IO.Directory.EnumerateFiles%28System.String%2CSystem.String%2CSystem.IO.SearchOption%29?displayProperty=nameWithType> pour rechercher un répertoire et (éventuellement) ses sous-répertoires, et obtenir une liste de noms de fichiers qui correspondent à un modèle de recherche spécifié.</span><span class="sxs-lookup"><span data-stu-id="1f697-127">Use the <xref:System.IO.Directory.EnumerateFiles%28System.String%2CSystem.String%2CSystem.IO.SearchOption%29?displayProperty=nameWithType> method to search a directory and (optionally) its subdirectories, and to obtain a list of file names that match a specified search pattern.</span></span>  
  
     [!code-csharp[System.IO.Directory.EnumerateFiles#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directory.enumeratefiles/cs/program.cs#1)]
     [!code-vb[System.IO.Directory.EnumerateFiles#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directory.enumeratefiles/vb/program.vb#1)]  
  
### <a name="to-enumerate-a-collection-of-directoryinfo-objects"></a><span data-ttu-id="1f697-128">Pour énumérer une collection d’objets DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1f697-128">To enumerate a collection of DirectoryInfo objects</span></span>  
  
-   <span data-ttu-id="1f697-129">Utilisez la méthode <xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType> pour obtenir une collection de répertoires de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="1f697-129">Use the <xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType> method to obtain a collection of top-level directories.</span></span>  
  
     [!code-csharp[System.IO.DirectoryInfo.EnumDirs#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directoryinfo.enumdirs/cs/program.cs#1)]
     [!code-vb[System.IO.DirectoryInfo.EnumDirs#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directoryinfo.enumdirs/vb/module1.vb#1)]  
  
### <a name="to-enumerate-a-collection-of-fileinfo-objects-in-all-directories"></a><span data-ttu-id="1f697-130">Pour énumérer une collection d’objets FileInfo dans tous les répertoires</span><span class="sxs-lookup"><span data-stu-id="1f697-130">To enumerate a collection of FileInfo objects in all directories</span></span>  
  
-   <span data-ttu-id="1f697-131">Utilisez la méthode <xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType> pour obtenir une collection de fichiers qui correspondent à un modèle de recherche spécifié dans tous les répertoires.</span><span class="sxs-lookup"><span data-stu-id="1f697-131">Use the <xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType> method to obtain a collection of files that match a specified search pattern in all directories.</span></span> <span data-ttu-id="1f697-132">Cet exemple énumère d’abord les répertoires de niveau supérieur pour intercepter les éventuelles exceptions d’accès non autorisé, puis énumère les fichiers.</span><span class="sxs-lookup"><span data-stu-id="1f697-132">This example first enumerates the top-level directories to catch possible unauthorized access exceptions, and then enumerates the files.</span></span>  
  
     [!code-csharp[System.IO.DirectoryInfo.EnumerateDirectories#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directoryinfo.enumeratedirectories/cs/program.cs#1)]
     [!code-vb[System.IO.DirectoryInfo.EnumerateDirectories#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directoryinfo.enumeratedirectories/vb/program.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="1f697-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f697-133">See also</span></span>

- [<span data-ttu-id="1f697-134">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="1f697-134">File and Stream I/O</span></span>](../../../docs/standard/io/index.md)
