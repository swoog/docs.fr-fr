---
title: Guide pratique pour écrire dans des fichiers binaires en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], binary access
- WriteAllBytes method [Visual Basic]
- binary files [Visual Basic], writing in Visual Basic
ms.assetid: 59fae125-de5b-4c96-883c-209f4a55112c
ms.openlocfilehash: 59edf84c1addd287eb1d1615c46258f329b1c7e2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33587200"
---
# <a name="how-to-write-to-binary-files-in-visual-basic"></a><span data-ttu-id="6f55d-102">Guide pratique pour écrire dans des fichiers binaires en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6f55d-102">How to: Write to Binary Files in Visual Basic</span></span>
<span data-ttu-id="6f55d-103">La méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllBytes%2A> écrit des données dans un fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="6f55d-103">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllBytes%2A> method writes data to a binary file.</span></span> <span data-ttu-id="6f55d-104">Si le paramètre `append` est `True`, elle ajoute les données au fichier ; sinon, les données dans le fichier sont remplacées.</span><span class="sxs-lookup"><span data-stu-id="6f55d-104">If the `append` parameter is `True`, it will append the data to the file; otherwise data in the file is overwritten.</span></span>  
  
 <span data-ttu-id="6f55d-105">Si le chemin spécifié (nom de fichier exclu) n’est pas valide, une exception <xref:System.IO.DirectoryNotFoundException> est levée.</span><span class="sxs-lookup"><span data-stu-id="6f55d-105">If the specified path excluding the file name is not valid, a <xref:System.IO.DirectoryNotFoundException> exception will be thrown.</span></span> <span data-ttu-id="6f55d-106">Si le chemin est valide mais que le fichier n’existe pas, le fichier est créé.</span><span class="sxs-lookup"><span data-stu-id="6f55d-106">If the path is valid but the file does not exist, the file will be created.</span></span>  
  
### <a name="to-write-to-a-binary-file"></a><span data-ttu-id="6f55d-107">Pour écrire dans un fichier binaire</span><span class="sxs-lookup"><span data-stu-id="6f55d-107">To write to a binary file</span></span>  
  
-   <span data-ttu-id="6f55d-108">Utilisez la méthode `WriteAllBytes` en fournissant le chemin et le nom du fichier, ainsi que les octets à écrire.</span><span class="sxs-lookup"><span data-stu-id="6f55d-108">Use the `WriteAllBytes` method, supplying the file path and name and the bytes to be written.</span></span> <span data-ttu-id="6f55d-109">Cet exemple ajoute le tableau de données `CustomerData` au fichier nommé `CollectedData.dat`.</span><span class="sxs-lookup"><span data-stu-id="6f55d-109">This example appends the data array `CustomerData` to the file named `CollectedData.dat`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#27](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-write-to-binary-files_1.vb)]  
  
## <a name="robust-programming"></a><span data-ttu-id="6f55d-110">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="6f55d-110">Robust Programming</span></span>  
 <span data-ttu-id="6f55d-111">Les conditions ci-dessous peuvent générer une exception :</span><span class="sxs-lookup"><span data-stu-id="6f55d-111">The following conditions may create an exception:</span></span>  
  
-   <span data-ttu-id="6f55d-112">Le chemin n’est pas valide pour l’une des raisons suivantes : il s’agit d’une chaîne de longueur nulle, il ne contient que des espaces blancs ou il contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="6f55d-112">The path is not valid for one of the following reasons: it is a zero-length string; it contains only white space; or it contains invalid characters.</span></span> <span data-ttu-id="6f55d-113">(<xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="6f55d-113">(<xref:System.ArgumentException>).</span></span>  
  
-   <span data-ttu-id="6f55d-114">Le chemin n’est pas valide, car il a la valeur `Nothing` (<xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="6f55d-114">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
-   <span data-ttu-id="6f55d-115">`File` pointe vers un chemin qui n’existe pas (<xref:System.IO.FileNotFoundException> ou <xref:System.IO.DirectoryNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="6f55d-115">`File` points to a path that does not exist (<xref:System.IO.FileNotFoundException> or <xref:System.IO.DirectoryNotFoundException>).</span></span>  
  
-   <span data-ttu-id="6f55d-116">Le fichier est utilisé par un autre processus, ou une erreur E/S se produit (<xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="6f55d-116">The file is in use by another process, or an I/O error occurs (<xref:System.IO.IOException>).</span></span>  
  
-   <span data-ttu-id="6f55d-117">Le chemin dépasse la longueur maximale définie par le système (<xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="6f55d-117">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
-   <span data-ttu-id="6f55d-118">Un nom de fichier ou de répertoire du chemin contient un signe deux-points (:) ou n'a pas un format correct (<xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="6f55d-118">A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
-   <span data-ttu-id="6f55d-119">L'utilisateur n'a pas les autorisations nécessaires pour afficher le chemin d'accès (<xref:System.Security.SecurityException>).</span><span class="sxs-lookup"><span data-stu-id="6f55d-119">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f55d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f55d-120">See Also</span></span>  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllBytes%2A>  
 [<span data-ttu-id="6f55d-121">Guide pratique : insérer du texte dans des fichiers</span><span class="sxs-lookup"><span data-stu-id="6f55d-121">How to: Write Text to Files</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-write-text-to-files.md)
