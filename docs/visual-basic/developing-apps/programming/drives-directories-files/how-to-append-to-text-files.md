---
title: 'Procédure : effectuer un ajout à des fichiers texte en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- I/O [Visual Basic], appending to files
- I/O [Visual Basic], My.Computer.FileSystem.WriteAllText method
- I/O [Visual Basic], WriteAllText method
ms.assetid: bbbd7fb5-f169-41a9-b53f-520ea9613913
ms.openlocfilehash: e855293ac3636049520a85abdf685091d437bb60
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64628904"
---
# <a name="how-to-append-to-text-files-in-visual-basic"></a><span data-ttu-id="4f5f2-102">Procédure : effectuer un ajout à des fichiers texte en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4f5f2-102">How to: Append to Text Files in Visual Basic</span></span>
<span data-ttu-id="4f5f2-103">Vous pouvez utiliser la méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A> pour ajouter un fichier texte en spécifiant que le paramètre `append` est défini avec la valeur `True`.</span><span class="sxs-lookup"><span data-stu-id="4f5f2-103">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A> method can be used to append to a text file by specifying that the `append` parameter is set to `True`.</span></span>  
  
### <a name="to-append-to-a-text-file"></a><span data-ttu-id="4f5f2-104">Pour effectuer un ajout à un fichier texte</span><span class="sxs-lookup"><span data-stu-id="4f5f2-104">To append to a text file</span></span>  
  
- <span data-ttu-id="4f5f2-105">Utilisez la méthode `WriteAllText`, en spécifiant le fichier cible et la chaîne à ajouter, et en affectant la valeur `True` au paramètre `append`.</span><span class="sxs-lookup"><span data-stu-id="4f5f2-105">Use the `WriteAllText` method, specifying the target file and string to be appended and setting the `append` parameter to `True`.</span></span>  
  
     <span data-ttu-id="4f5f2-106">Cet exemple écrit la chaîne `"This is a test string."` dans le fichier nommé `Testfile.txt`.</span><span class="sxs-lookup"><span data-stu-id="4f5f2-106">This example writes the string `"This is a test string."` to the file named `Testfile.txt`.</span></span>  
  
     [!code-vb[VbFileIOWrite#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOWrite/VB/Class1.vb#6)]  
  
## <a name="robust-programming"></a><span data-ttu-id="4f5f2-107">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="4f5f2-107">Robust Programming</span></span>  
 <span data-ttu-id="4f5f2-108">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="4f5f2-108">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="4f5f2-109">Le chemin n’est pas valide pour l’une des raisons suivantes : il s’agit d’une chaîne de longueur nulle, il ne contient que des espaces blancs, il contient des caractères non valides ou il s’agit d’un chemin d’appareil (il commence par \\\\.\\) (<xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="4f5f2-109">The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="4f5f2-110">Le chemin n’est pas valide, car il a la valeur `Nothing` (<xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="4f5f2-110">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="4f5f2-111">`File` pointe vers un chemin qui n’existe pas (<xref:System.IO.FileNotFoundException> ou <xref:System.IO.DirectoryNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="4f5f2-111">`File` points to a path that does not exist (<xref:System.IO.FileNotFoundException> or <xref:System.IO.DirectoryNotFoundException>).</span></span>  
  
- <span data-ttu-id="4f5f2-112">Le fichier est utilisé par un autre processus, ou une erreur E/S se produit (<xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="4f5f2-112">The file is in use by another process, or an I/O error occurs (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="4f5f2-113">Le chemin dépasse la longueur maximale définie par le système (<xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="4f5f2-113">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
- <span data-ttu-id="4f5f2-114">Un nom de fichier ou de répertoire du chemin contient un signe deux-points (:) ou n'a pas un format correct (<xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="4f5f2-114">A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
- <span data-ttu-id="4f5f2-115">L'utilisateur n'a pas les autorisations nécessaires pour afficher le chemin d'accès (<xref:System.Security.SecurityException>).</span><span class="sxs-lookup"><span data-stu-id="4f5f2-115">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f5f2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f5f2-116">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- [<span data-ttu-id="4f5f2-117">Écriture dans des fichiers</span><span class="sxs-lookup"><span data-stu-id="4f5f2-117">Writing to Files</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/writing-to-files.md)
