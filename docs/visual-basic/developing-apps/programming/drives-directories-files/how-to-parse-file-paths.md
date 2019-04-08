---
title: 'Procédure : analyser des chemins d’accès dans Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- file names [Visual Basic], parsing [Visual Basic]
- parsing, file paths [Visual Basic]
ms.assetid: c1bd99c9-8160-456a-b5ab-60a49139b923
ms.openlocfilehash: c089910e3fd5d02b674cfed3062fb15275d91486
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834606"
---
# <a name="how-to-parse-file-paths-in-visual-basic"></a><span data-ttu-id="fc609-102">Procédure : analyser des chemins d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fc609-102">How to: Parse File Paths in Visual Basic</span></span>
<span data-ttu-id="fc609-103">L’objet <xref:Microsoft.VisualBasic.FileIO.FileSystem> fournit plusieurs méthodes qui facilitent l’analyse des chemins de fichier.</span><span class="sxs-lookup"><span data-stu-id="fc609-103">The <xref:Microsoft.VisualBasic.FileIO.FileSystem> object offers a number of useful methods when parsing file paths.</span></span>  
  
-   <span data-ttu-id="fc609-104">La méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.CombinePath%2A> combine deux chemins et affiche un chemin combiné au format correct.</span><span class="sxs-lookup"><span data-stu-id="fc609-104">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.CombinePath%2A> method takes two paths and returns a properly formatted combined path.</span></span>  
  
-   <span data-ttu-id="fc609-105">La méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetParentPath%2A> retourne le chemin absolu du parent du chemin fourni.</span><span class="sxs-lookup"><span data-stu-id="fc609-105">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetParentPath%2A> method returns the absolute path of the parent of the provided path.</span></span>  
  
-   <span data-ttu-id="fc609-106">La méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFileInfo%2A> retourne un objet <xref:System.IO.FileInfo> qui peut être interrogé pour déterminer les propriétés du fichier, telles que son nom et son chemin.</span><span class="sxs-lookup"><span data-stu-id="fc609-106">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFileInfo%2A> method returns a <xref:System.IO.FileInfo> object that can be queried to determine the file's properties, such as its name and path.</span></span>  
  
 <span data-ttu-id="fc609-107">Ne vous basez pas sur l’extension de nom de fichier pour déterminer le contenu d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="fc609-107">Do not make decisions about the contents of the file based on the file name extension.</span></span> <span data-ttu-id="fc609-108">Par exemple, le fichier Form1.vb peut ne pas être un fichier source Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fc609-108">For example, the file Form1.vb may not be a Visual Basic source file.</span></span>  
  
### <a name="to-determine-a-files-name-and-path"></a><span data-ttu-id="fc609-109">Pour déterminer le nom et le chemin d’un fichier</span><span class="sxs-lookup"><span data-stu-id="fc609-109">To determine a file's name and path</span></span>  
  
-   <span data-ttu-id="fc609-110">Utilisez les propriétés <xref:System.IO.FileInfo.DirectoryName%2A> et <xref:System.IO.FileInfo.Name%2A> de l’objet <xref:System.IO.FileInfo> pour déterminer le nom et le chemin d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="fc609-110">Use the <xref:System.IO.FileInfo.DirectoryName%2A> and <xref:System.IO.FileInfo.Name%2A> properties of the <xref:System.IO.FileInfo> object to determine a file's name and path.</span></span> <span data-ttu-id="fc609-111">Cet exemple détermine le nom et le chemin d’un fichier, puis les affiche.</span><span class="sxs-lookup"><span data-stu-id="fc609-111">This example determines the name and path and displays them.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#54](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#54)]  
  
### <a name="to-combine-a-files-name-and-directory-to-create-the-full-path"></a><span data-ttu-id="fc609-112">Pour combiner le nom et le répertoire d’un fichier en un chemin complet</span><span class="sxs-lookup"><span data-stu-id="fc609-112">To combine a file's name and directory to create the full path</span></span>  
  
-   <span data-ttu-id="fc609-113">Utilisez la méthode `CombinePath` , en spécifiant le répertoire et le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="fc609-113">Use the `CombinePath` method, supplying the directory and name.</span></span> <span data-ttu-id="fc609-114">Cet exemple combine les chaînes `folderPath` et `fileName` créées dans l’exemple précédent, puis affiche le résultat.</span><span class="sxs-lookup"><span data-stu-id="fc609-114">This example takes the strings `folderPath` and `fileName` created in the previous example, combines them, and displays the result.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#55](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#55)]  
  
## <a name="see-also"></a><span data-ttu-id="fc609-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc609-115">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CombinePath%2A>
- <xref:System.IO.FileInfo>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFileInfo%2A>
- [<span data-ttu-id="fc609-116">Guide pratique pour placer la collection de fichiers dans un répertoire</span><span class="sxs-lookup"><span data-stu-id="fc609-116">How to: Get the Collection of Files in a Directory</span></span>](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-get-the-collection-of-files-in-a-directory.md)
