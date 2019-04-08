---
title: 'Procédure : renommer un fichier en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- I/O [Visual Basic], renaming files
- files [Visual Basic], renaming
ms.assetid: 0ea7e0c8-2cb2-4bf5-a00d-7b6e3c08a3bc
ms.openlocfilehash: b86797018e1471590fd4c89848921e696afbc819
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58814147"
---
# <a name="how-to-rename-a-file-in-visual-basic"></a><span data-ttu-id="25eac-102">Procédure : renommer un fichier en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="25eac-102">How to: Rename a File in Visual Basic</span></span>
<span data-ttu-id="25eac-103">Utilisez la méthode `RenameFile` de l’objet `My.Computer.FileSystem` pour renommer un fichier en fournissant l’emplacement actuel, le nom actuel du fichier et le nouveau nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="25eac-103">Use the `RenameFile` method of the `My.Computer.FileSystem` object to rename a file by supplying the current location, file name, and the new file name.</span></span> <span data-ttu-id="25eac-104">Cette méthode ne peut pas être utilisée pour déplacer un fichier. Utilisez la méthode `MoveFile` pour déplacer et renommer le fichier.</span><span class="sxs-lookup"><span data-stu-id="25eac-104">This method cannot be used to move a file; use the `MoveFile` method to move and rename the file.</span></span>  
  
### <a name="to-rename-a-file"></a><span data-ttu-id="25eac-105">Pour renommer un fichier</span><span class="sxs-lookup"><span data-stu-id="25eac-105">To rename a file</span></span>  
  
-   <span data-ttu-id="25eac-106">Pour renommer un fichier, utilisez la méthode `My.Computer.FileSystem.RenameFile`.</span><span class="sxs-lookup"><span data-stu-id="25eac-106">Use the `My.Computer.FileSystem.RenameFile` method to rename a file.</span></span> <span data-ttu-id="25eac-107">Dans cet exemple, le nom de fichier `Test.txt` est remplacé par `SecondTest.txt`.</span><span class="sxs-lookup"><span data-stu-id="25eac-107">This example renames the file named `Test.txt` to `SecondTest.txt`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#9)]  
  
 <span data-ttu-id="25eac-108">Cet exemple de code est également disponible sous la forme d’un extrait de code IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="25eac-108">This code example is also available as an IntelliSense code snippet.</span></span> <span data-ttu-id="25eac-109">Dans le sélecteur d’extraits de code, il se trouve dans **Système de fichiers - Traitement des lecteurs, dossiers et fichiers**.</span><span class="sxs-lookup"><span data-stu-id="25eac-109">In the code snippet picker, the snippet is located in **File system - Processing Drives, Folders, and Files**.</span></span> <span data-ttu-id="25eac-110">Pour plus d’informations, consultez [Extraits de code](/visualstudio/ide/code-snippets).</span><span class="sxs-lookup"><span data-stu-id="25eac-110">For more information, see [Code Snippets](/visualstudio/ide/code-snippets).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="25eac-111">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="25eac-111">Robust Programming</span></span>  
 <span data-ttu-id="25eac-112">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="25eac-112">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="25eac-113">Le chemin n’est pas valide pour l’une des raisons suivantes : il s’agit d’une chaîne de longueur nulle, il ne contient que des espaces blancs, il contient des caractères non valides ou il s’agit d’un chemin d’appareil (il commence par \\\\.\\) (<xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-113">The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException>).</span></span>  
  
-   <span data-ttu-id="25eac-114">`newName` contient des informations de chemin (<xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-114">`newName` contains path information (<xref:System.ArgumentException>).</span></span>  
  
-   <span data-ttu-id="25eac-115">Le chemin n’est pas valide, car il a la valeur `Nothing` (<xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-115">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
-   <span data-ttu-id="25eac-116">`newName` est `Nothing` ou une chaîne vide (<xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-116">`newName` is `Nothing` or an empty string (<xref:System.ArgumentNullException>).</span></span>  
  
-   <span data-ttu-id="25eac-117">Le fichier source n’est pas valide ou n’existe pas (<xref:System.IO.FileNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-117">The source file is not valid or does not exist (<xref:System.IO.FileNotFoundException>).</span></span>  
  
-   <span data-ttu-id="25eac-118">Un fichier ou un répertoire porte déjà le nom spécifié dans `newName` (<xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-118">There is an existing file or directory with the name specified in `newName` (<xref:System.IO.IOException>).</span></span>  
  
-   <span data-ttu-id="25eac-119">Le chemin dépasse la longueur maximale définie par le système (<xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-119">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
-   <span data-ttu-id="25eac-120">Un nom de fichier ou de répertoire du chemin contient un signe deux-points (:) ou n'a pas un format correct (<xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-120">A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
-   <span data-ttu-id="25eac-121">L'utilisateur n'a pas les autorisations nécessaires pour afficher le chemin d'accès (<xref:System.Security.SecurityException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-121">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>  
  
-   <span data-ttu-id="25eac-122">L’utilisateur ne dispose pas de l’autorisation nécessaire (<xref:System.UnauthorizedAccessException>).</span><span class="sxs-lookup"><span data-stu-id="25eac-122">The user does not have the required permission (<xref:System.UnauthorizedAccessException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25eac-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25eac-123">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem.RenameFile%2A>
- [<span data-ttu-id="25eac-124">Guide pratique pour déplacer un fichier</span><span class="sxs-lookup"><span data-stu-id="25eac-124">How to: Move a File</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-move-a-file.md)
- [<span data-ttu-id="25eac-125">Création, suppression et déplacement de fichiers et de répertoires</span><span class="sxs-lookup"><span data-stu-id="25eac-125">Creating, Deleting, and Moving Files and Directories</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/creating-deleting-and-moving-files-and-directories.md)
- [<span data-ttu-id="25eac-126">Guide pratique pour créer une copie d’un fichier dans le même répertoire</span><span class="sxs-lookup"><span data-stu-id="25eac-126">How to: Create a Copy of a File in the Same Directory</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-create-a-copy-of-a-file-in-the-same-directory.md)
- [<span data-ttu-id="25eac-127">Guide pratique pour créer une copie d’un fichier dans un autre répertoire</span><span class="sxs-lookup"><span data-stu-id="25eac-127">How to: Create a Copy of a File in a Different Directory</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-create-a-copy-of-a-file-in-a-different-directory.md)
