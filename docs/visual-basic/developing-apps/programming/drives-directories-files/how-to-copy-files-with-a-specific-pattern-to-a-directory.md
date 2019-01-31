---
title: 'Procédure : copier des fichiers avec un modèle spécifique dans un répertoire en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- My.Computer.FileSystem.CopyFile method, copying files [Visual Basic]
- files [Visual Basic], copying
- CopyFile method [Visual Basic], copying files in Visual Basic
- I/O [Visual Basic], copying files
ms.assetid: f205d2ad-bbe5-4d55-8a40-acda21aa82dd
ms.openlocfilehash: 9c2ed926d21bf73b9b93863e5c3a3ed9ccc950aa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634075"
---
# <a name="how-to-copy-files-with-a-specific-pattern-to-a-directory-in-visual-basic"></a><span data-ttu-id="7b9ef-102">Procédure : copier des fichiers avec un modèle spécifique dans un répertoire en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7b9ef-102">How to: Copy Files with a Specific Pattern to a Directory in Visual Basic</span></span>
<span data-ttu-id="7b9ef-103">La méthode <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles%2A> retourne une collection en lecture seule de chaînes représentant les noms de chemin des fichiers.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-103">The <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles%2A> method returns a read-only collection of strings representing the path names for the files.</span></span> <span data-ttu-id="7b9ef-104">Vous pouvez utiliser le paramètre `wildCards` pour indiquer un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-104">You can use the `wildCards` parameter to specify a specific pattern.</span></span>  
  
 <span data-ttu-id="7b9ef-105">Une collection vide est retournée si aucun fichier correspondant n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-105">An empty collection is returned if no matching files are found.</span></span>  
  
 <span data-ttu-id="7b9ef-106">Vous pouvez utiliser la méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile%2A> pour copier les fichiers dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-106">You can use the <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile%2A> method to copy the files to a directory.</span></span>  
  
### <a name="to-copy-files-with-a-specific-pattern-to-a-directory"></a><span data-ttu-id="7b9ef-107">Pour copier des fichiers avec un modèle spécifique dans un répertoire</span><span class="sxs-lookup"><span data-stu-id="7b9ef-107">To copy files with a specific pattern to a directory</span></span>  
  
1.  <span data-ttu-id="7b9ef-108">Utilisez la méthode `GetFiles` pour retourner la liste des fichiers.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-108">Use the `GetFiles` method to return the list of files.</span></span> <span data-ttu-id="7b9ef-109">Cet exemple retourne tous les fichiers .rtf qui se trouvent dans le répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-109">This example returns all .rtf files in the specified directory.</span></span>  
  
     [!code-vb[VbFileIOMisc#36](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-copy-files-with-a-specific-pattern-to-a-directory_1.vb)]  
  
2.  <span data-ttu-id="7b9ef-110">Utilisez la méthode `CopyFile` pour copier les fichiers.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-110">Use the `CopyFile` method to copy the files.</span></span> <span data-ttu-id="7b9ef-111">Cet exemple copie les fichiers dans le répertoire nommé `testdirectory`.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-111">This example copies the files to the directory named `testdirectory`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#88](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-copy-files-with-a-specific-pattern-to-a-directory_2.vb)]  
  
3.  <span data-ttu-id="7b9ef-112">Terminez l’instruction `For` par une instruction `Next` .</span><span class="sxs-lookup"><span data-stu-id="7b9ef-112">Close the `For` statement with a `Next` statement.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#89](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-copy-files-with-a-specific-pattern-to-a-directory_3.vb)]  
  
## <a name="example"></a><span data-ttu-id="7b9ef-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="7b9ef-113">Example</span></span>  
 <span data-ttu-id="7b9ef-114">L’exemple suivant, qui présente les extraits de code ci-dessus dans leur intégralité, copie tous les fichiers .rtf du répertoire spécifié dans le répertoire nommé `testdirectory`.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-114">The following example, which presents the above snippets in complete form, copies all .rtf files in the specified directory to the directory named `testdirectory`.</span></span>  
  
 [!code-vb[VbFileIOMisc#37](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-copy-files-with-a-specific-pattern-to-a-directory_4.vb)]  
  
## <a name="net-framework-security"></a><span data-ttu-id="7b9ef-115">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="7b9ef-115">.NET Framework Security</span></span>  
 <span data-ttu-id="7b9ef-116">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="7b9ef-116">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="7b9ef-117">Le chemin n’est pas valide pour l’une des raisons suivantes : il s’agit d’une chaîne de longueur nulle, il ne contient que des espaces blancs, il contient des caractères non valides ou il s’agit d’un chemin d’appareil (il commence par \\\\.\\) (<xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="7b9ef-117">The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException>).</span></span>  
  
-   <span data-ttu-id="7b9ef-118">Le chemin n’est pas valide, car il a la valeur `Nothing` (<xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="7b9ef-118">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
-   <span data-ttu-id="7b9ef-119">Le répertoire n’existe pas (<xref:System.IO.DirectoryNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="7b9ef-119">The directory does not exist (<xref:System.IO.DirectoryNotFoundException>).</span></span>  
  
-   <span data-ttu-id="7b9ef-120">Le répertoire pointe vers un fichier existant (<xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="7b9ef-120">The directory points to an existing file (<xref:System.IO.IOException>).</span></span>  
  
-   <span data-ttu-id="7b9ef-121">Le chemin dépasse la longueur maximale définie par le système (<xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="7b9ef-121">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
-   <span data-ttu-id="7b9ef-122">Un nom de fichier ou de répertoire du chemin contient un signe deux-points (:) ou n'a pas un format correct (<xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="7b9ef-122">A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
-   <span data-ttu-id="7b9ef-123">L'utilisateur n'a pas les autorisations nécessaires pour afficher le chemin (<xref:System.Security.SecurityException>).</span><span class="sxs-lookup"><span data-stu-id="7b9ef-123">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span> <span data-ttu-id="7b9ef-124">L'utilisateur ne dispose pas des autorisations nécessaires (<xref:System.UnauthorizedAccessException>).</span><span class="sxs-lookup"><span data-stu-id="7b9ef-124">The user lacks necessary permissions (<xref:System.UnauthorizedAccessException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b9ef-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b9ef-125">See also</span></span>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile%2A>
- <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles%2A>
- [<span data-ttu-id="7b9ef-126">Guide pratique pour rechercher des sous-répertoires avec un modèle spécifique</span><span class="sxs-lookup"><span data-stu-id="7b9ef-126">How to: Find Subdirectories with a Specific Pattern</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-find-subdirectories-with-a-specific-pattern.md)
- [<span data-ttu-id="7b9ef-127">Résolution des problèmes : lecture et écriture dans des fichiers texte</span><span class="sxs-lookup"><span data-stu-id="7b9ef-127">Troubleshooting: Reading from and Writing to Text Files</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)
- [<span data-ttu-id="7b9ef-128">Guide pratique pour placer la collection de fichiers dans un répertoire</span><span class="sxs-lookup"><span data-stu-id="7b9ef-128">How to: Get the Collection of Files in a Directory</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-get-the-collection-of-files-in-a-directory.md)
