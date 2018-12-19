---
title: 'Procédure : Copier, supprimer et déplacer des fichiers et dossiers - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- I/O [C#]
ms.assetid: 62e52cd7-9597-4e4a-acf9-1315f5cdbf05
ms.openlocfilehash: 498f266597032a4c35dbc8783994095b5c08fc3d
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240240"
---
# <a name="how-to-copy-delete-and-move-files-and-folders-c-programming-guide"></a><span data-ttu-id="1c8ba-102">Procédure : Copier, supprimer et déplacer des fichiers et dossiers (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="1c8ba-102">How to: Copy, Delete, and Move Files and Folders (C# Programming Guide)</span></span>
<span data-ttu-id="1c8ba-103">Les exemples suivants montrent comment copier, déplacer et supprimer des fichiers et dossiers de manière synchrone à l’aide des classes <xref:System.IO.File?displayProperty=nameWithType>, <xref:System.IO.Directory?displayProperty=nameWithType>, <xref:System.IO.FileInfo?displayProperty=nameWithType> et <xref:System.IO.DirectoryInfo?displayProperty=nameWithType> à partir de l’espace de noms <xref:System.IO?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-103">The following examples show how to copy, move, and delete files and folders in a synchronous manner by using the <xref:System.IO.File?displayProperty=nameWithType>, <xref:System.IO.Directory?displayProperty=nameWithType>, <xref:System.IO.FileInfo?displayProperty=nameWithType>, and <xref:System.IO.DirectoryInfo?displayProperty=nameWithType> classes from the <xref:System.IO?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="1c8ba-104">Ces exemples ne fournissent pas de barre de progression ou autre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-104">These examples do not provide a progress bar or any other user interface.</span></span> <span data-ttu-id="1c8ba-105">Si vous souhaitez fournir une boîte de dialogue de progression standard, consultez [Guide pratique pour fournir une boîte de dialogue de progression pour les opérations sur les fichiers](how-to-provide-a-progress-dialog-box-for-file-operations.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ba-105">If you want to provide a standard progress dialog box, see [How to: Provide a Progress Dialog Box for File Operations](how-to-provide-a-progress-dialog-box-for-file-operations.md).</span></span>  
  
 <span data-ttu-id="1c8ba-106">Utilisez <xref:System.IO.FileSystemWatcher?displayProperty=nameWithType> pour fournir des événements qui vous permettent de calculer la progression quand vous travaillez sur plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-106">Use <xref:System.IO.FileSystemWatcher?displayProperty=nameWithType> to provide events that will enable you to calculate the progress when operating on multiple files.</span></span> <span data-ttu-id="1c8ba-107">Une autre approche consiste à utiliser l’appel de code non managé pour appeler les méthodes pertinentes relatives aux fichiers dans le shell Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-107">Another approach is to use platform invoke to call the relevant file-related methods in the Windows Shell.</span></span> <span data-ttu-id="1c8ba-108">Pour plus d’informations sur la façon d’effectuer ces opérations sur les fichiers de façon asynchrone, consultez [E/S de fichiers asynchrones](../../../standard/io/asynchronous-file-i-o.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ba-108">For information about how to perform these file operations asynchronously, see [Asynchronous File I/O](../../../standard/io/asynchronous-file-i-o.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1c8ba-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="1c8ba-109">Example</span></span>  
 <span data-ttu-id="1c8ba-110">L’exemple suivant montre comment copier des fichiers et des répertoires.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-110">The following example shows how to copy files and directories.</span></span>  
  
 [!code-csharp[csFilesandFolders#7](../../../csharp/programming-guide/file-system/codesnippet/CSharp/how-to-copy-delete-and-move-files-and-folders_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="1c8ba-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="1c8ba-111">Example</span></span>  
 <span data-ttu-id="1c8ba-112">L’exemple suivant montre comment déplacer des fichiers et des répertoires.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-112">The following example shows how to move files and directories.</span></span>  
  
 [!code-csharp[csFilesandFolders#8](../../../csharp/programming-guide/file-system/codesnippet/CSharp/how-to-copy-delete-and-move-files-and-folders_2.cs)]  
  
## <a name="example"></a><span data-ttu-id="1c8ba-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="1c8ba-113">Example</span></span>  
 <span data-ttu-id="1c8ba-114">L’exemple suivant montre comment supprimer des fichiers et des répertoires.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-114">The following example shows how to delete files and directories.</span></span>  
  
 [!code-csharp[csFilesandFolders#9](../../../csharp/programming-guide/file-system/codesnippet/CSharp/how-to-copy-delete-and-move-files-and-folders_3.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="1c8ba-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c8ba-115">See Also</span></span>

- <xref:System.IO?displayProperty=nameWithType>  
- [<span data-ttu-id="1c8ba-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1c8ba-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="1c8ba-117">Système de fichiers et Registre (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="1c8ba-117">File System and the Registry (C# Programming Guide)</span></span>](index.md)  
- [<span data-ttu-id="1c8ba-118">Guide pratique pour fournir une boîte de dialogue de progression pour les opérations sur les fichiers</span><span class="sxs-lookup"><span data-stu-id="1c8ba-118">How to: Provide a Progress Dialog Box for File Operations</span></span>](how-to-provide-a-progress-dialog-box-for-file-operations.md)  
- [<span data-ttu-id="1c8ba-119">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="1c8ba-119">File and Stream I/O</span></span>](../../../standard/io/index.md)  
- [<span data-ttu-id="1c8ba-120">Tâches d’E/S courantes</span><span class="sxs-lookup"><span data-stu-id="1c8ba-120">Common I/O Tasks</span></span>](../../../standard/io/common-i-o-tasks.md)
