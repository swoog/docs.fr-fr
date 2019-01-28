---
title: 'Procédure : Obtenir des informations sur les fichiers, dossiers et lecteurs - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- files [C#], getting information about
ms.assetid: 22fc2da6-5494-405b-995e-c0b99142a93e
ms.openlocfilehash: 7c122f0d342acb3708072be89e08c7465a654815
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54660383"
---
# <a name="how-to-get-information-about-files-folders-and-drives--c-programming-guide"></a><span data-ttu-id="168f2-102">Procédure : Obtenir des informations sur les fichiers, dossiers et lecteurs (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="168f2-102">How to: Get Information About Files, Folders, and Drives  (C# Programming Guide)</span></span>
<span data-ttu-id="168f2-103">Dans le .NET Framework, vous pouvez accéder aux informations sur le système de fichiers en utilisant les classes suivantes :</span><span class="sxs-lookup"><span data-stu-id="168f2-103">In the .NET Framework, you can access file system information by using the following classes:</span></span>  
  
-   <xref:System.IO.FileInfo?displayProperty=nameWithType>  
  
-   <xref:System.IO.DirectoryInfo?displayProperty=nameWithType>  
  
-   <xref:System.IO.DriveInfo?displayProperty=nameWithType>  
  
-   <xref:System.IO.Directory?displayProperty=nameWithType>  
  
-   <xref:System.IO.File?displayProperty=nameWithType>  
  
 <span data-ttu-id="168f2-104">Les classes <xref:System.IO.FileInfo> et <xref:System.IO.DirectoryInfo> représentent un fichier ou un répertoire. Elles contiennent des propriétés qui exposent une grande partie des attributs de fichiers pris en charge par le système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="168f2-104">The <xref:System.IO.FileInfo> and <xref:System.IO.DirectoryInfo> classes represent a file or directory and contain properties that expose many of the file attributes that are supported by the NTFS file system.</span></span> <span data-ttu-id="168f2-105">Elles contiennent également des méthodes pour ouvrir, fermer, déplacer et supprimer des fichiers et dossiers.</span><span class="sxs-lookup"><span data-stu-id="168f2-105">They also contain methods for opening, closing, moving, and deleting files and folders.</span></span> <span data-ttu-id="168f2-106">Vous pouvez créer des instances de ces classes en passant une chaîne qui représente le nom du fichier, dossier ou lecteur dans le constructeur :</span><span class="sxs-lookup"><span data-stu-id="168f2-106">You can create instances of these classes by passing a string that represents the name of the file, folder, or drive in to the constructor:</span></span>  
  
```csharp  
System.IO.DriveInfo di = new System.IO.DriveInfo(@"C:\");  
```  
  
 <span data-ttu-id="168f2-107">Vous pouvez aussi obtenir les noms des fichiers, dossiers ou lecteurs en appelant <xref:System.IO.DirectoryInfo.GetDirectories%2A?displayProperty=nameWithType>, <xref:System.IO.DirectoryInfo.GetFiles%2A?displayProperty=nameWithType> et <xref:System.IO.DriveInfo.RootDirectory%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="168f2-107">You can also obtain the names of files, folders, or drives by using calls to <xref:System.IO.DirectoryInfo.GetDirectories%2A?displayProperty=nameWithType>, <xref:System.IO.DirectoryInfo.GetFiles%2A?displayProperty=nameWithType>, and <xref:System.IO.DriveInfo.RootDirectory%2A?displayProperty=nameWithType>.</span></span>  
  
 <span data-ttu-id="168f2-108">Les classes <xref:System.IO.Directory?displayProperty=nameWithType> et <xref:System.IO.File?displayProperty=nameWithType> fournissent des méthodes statiques pour récupérer des informations sur les répertoires et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="168f2-108">The <xref:System.IO.Directory?displayProperty=nameWithType> and <xref:System.IO.File?displayProperty=nameWithType> classes provide static methods for retrieving information about directories and files.</span></span>  
  
## <a name="example"></a><span data-ttu-id="168f2-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="168f2-109">Example</span></span>  
 <span data-ttu-id="168f2-110">L’exemple suivant illustre différentes manières d’accéder aux informations sur les fichiers et dossiers.</span><span class="sxs-lookup"><span data-stu-id="168f2-110">The following example shows various ways to access information about files and folders.</span></span>  
  
 [!code-csharp[csFilesandFolders#6](../../../csharp/programming-guide/file-system/codesnippet/CSharp/how-to-get-information-about-files-folders-and-drives_1.cs)]  
  
## <a name="robust-programming"></a><span data-ttu-id="168f2-111">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="168f2-111">Robust Programming</span></span>  
 <span data-ttu-id="168f2-112">Quand vous traitez des chaînes de chemin spécifiées par l’utilisateur, vous devez également gérer les exceptions dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="168f2-112">When you process user-specified path strings, you should also handle exceptions for the following conditions:</span></span>  
  
-   <span data-ttu-id="168f2-113">Le nom de fichier est mal formé.</span><span class="sxs-lookup"><span data-stu-id="168f2-113">The file name is malformed.</span></span> <span data-ttu-id="168f2-114">Par exemple, il contient des caractères non valides ou uniquement des espaces blancs.</span><span class="sxs-lookup"><span data-stu-id="168f2-114">For example, it contains invalid characters or only white space.</span></span>  
  
-   <span data-ttu-id="168f2-115">Le nom de fichier est null.</span><span class="sxs-lookup"><span data-stu-id="168f2-115">The file name is null.</span></span>  
  
-   <span data-ttu-id="168f2-116">Le nom de fichier est plus long que la longueur maximale définie par le système.</span><span class="sxs-lookup"><span data-stu-id="168f2-116">The file name is longer than the system-defined maximum length.</span></span>  
  
-   <span data-ttu-id="168f2-117">Le nom de fichier contient un signe deux-points (:).</span><span class="sxs-lookup"><span data-stu-id="168f2-117">The file name contains a colon (:).</span></span>  
  
 <span data-ttu-id="168f2-118">Si l’application ne dispose pas des autorisations suffisantes pour lire le fichier spécifié, la méthode `Exists` retourne `false` indépendamment de l’existence d’un chemin. La méthode ne lève pas d’exception.</span><span class="sxs-lookup"><span data-stu-id="168f2-118">If the application does not have sufficient permissions to read the specified file, the `Exists` method returns `false` regardless of whether a path exists; the method does not throw an exception.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="168f2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="168f2-119">See also</span></span>

- <xref:System.IO?displayProperty=nameWithType>
- [<span data-ttu-id="168f2-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="168f2-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="168f2-121">Système de fichiers et Registre (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="168f2-121">File System and the Registry (C# Programming Guide)</span></span>](../../../csharp/programming-guide/file-system/index.md)
