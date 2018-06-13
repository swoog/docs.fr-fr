---
title: 'Comment : lire et écrire dans un fichier de données créé récemment'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- streams, reading and writing data
- BinaryReader class, examples
- I/O [.NET Framework], reading data
- I/O [.NET Framework], writing data
- BinaryWriter class, examples
ms.assetid: e209d949-31e8-44ea-8e38-87f9093f3093
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6b854495a32755b2cbbd0421b1a45458fd2b7863
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33572695"
---
# <a name="how-to-read-and-write-to-a-newly-created-data-file"></a><span data-ttu-id="edcc4-102">Comment : lire et écrire dans un fichier de données créé récemment</span><span class="sxs-lookup"><span data-stu-id="edcc4-102">How to: Read and Write to a Newly Created Data File</span></span>
<span data-ttu-id="edcc4-103">Les classes <xref:System.IO.BinaryWriter> et <xref:System.IO.BinaryReader?displayProperty=nameWithType> sont utilisées pour écrire et lire des données plutôt que des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="edcc4-103">The <xref:System.IO.BinaryWriter> and <xref:System.IO.BinaryReader?displayProperty=nameWithType> classes are used for writing and reading data rather than character strings.</span></span> <span data-ttu-id="edcc4-104">L’exemple suivant montre comment écrire et lire des données dans un flux de fichier vide nommé `Test.data`.</span><span class="sxs-lookup"><span data-stu-id="edcc4-104">The following example demonstrates how to write data to, and read data from, a new, empty file stream called `Test.data`.</span></span> <span data-ttu-id="edcc4-105">Après avoir créé le fichier de données dans le répertoire actif, les objets <xref:System.IO.BinaryWriter> et <xref:System.IO.BinaryReader> associés sont créés, et l’objet <xref:System.IO.BinaryWriter> est utilisé pour écrire les entiers de 0 à 10 dans `Test.data`, ce qui laisse le pointeur de fichier à la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="edcc4-105">After creating the data file in the current directory, the associated <xref:System.IO.BinaryWriter> and <xref:System.IO.BinaryReader> objects are created, and the <xref:System.IO.BinaryWriter> object is used to write the integers 0 through 10 to `Test.data`, which leaves the file pointer at the end of the file.</span></span> <span data-ttu-id="edcc4-106">Après avoir replacé le pointeur de fichier au début, l’objet <xref:System.IO.BinaryReader> lit le contenu spécifié.</span><span class="sxs-lookup"><span data-stu-id="edcc4-106">After setting the file pointer back to the origin, the <xref:System.IO.BinaryReader> object reads out the specified content.</span></span>  
  
## <a name="example"></a><span data-ttu-id="edcc4-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="edcc4-107">Example</span></span>  
 [!code-cpp[System.IO.BinaryReaderWriter#7](../../../samples/snippets/cpp/VS_Snippets_CLR_System/system.IO.BinaryReaderWriter/CPP/source6.cpp#7)]
 [!code-csharp[System.IO.BinaryReaderWriter#7](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.IO.BinaryReaderWriter/CS/source6.cs#7)]
 [!code-vb[System.IO.BinaryReaderWriter#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.IO.BinaryReaderWriter/VB/source6.vb#7)]  
  
## <a name="robust-programming"></a><span data-ttu-id="edcc4-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="edcc4-108">Robust Programming</span></span>  
 <span data-ttu-id="edcc4-109">Si `Test.data` existe déjà dans le répertoire actif, une exception <xref:System.IO.IOException> est levée.</span><span class="sxs-lookup"><span data-stu-id="edcc4-109">If `Test.data` already exists in the current directory, an <xref:System.IO.IOException> exception is thrown.</span></span> <span data-ttu-id="edcc4-110">Utilisez l’option de mode de fichier <xref:System.IO.FileMode.Create?displayProperty=nameWithType> lors de l’initialisation du flux de fichier pour toujours créer un nouveau fichier sans lever d’exception.</span><span class="sxs-lookup"><span data-stu-id="edcc4-110">Use the file mode option <xref:System.IO.FileMode.Create?displayProperty=nameWithType> when you initialize the file stream to always create a new file without throwing an  exception.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="edcc4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edcc4-111">See Also</span></span>  
 <xref:System.IO.BinaryReader>  
 <xref:System.IO.BinaryWriter>  
 <xref:System.IO.FileStream>  
 <xref:System.IO.FileStream.Seek%2A?displayProperty=nameWithType>  
 <xref:System.IO.SeekOrigin>  
 [<span data-ttu-id="edcc4-112">Guide pratique pour énumérer des répertoires et des fichiers</span><span class="sxs-lookup"><span data-stu-id="edcc4-112">How to: Enumerate Directories and Files</span></span>](../../../docs/standard/io/how-to-enumerate-directories-and-files.md)  
 [<span data-ttu-id="edcc4-113">Comment : ouvrir un fichier journal et y ajouter des éléments</span><span class="sxs-lookup"><span data-stu-id="edcc4-113">How to: Open and Append to a Log File</span></span>](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)  
 [<span data-ttu-id="edcc4-114">Comment : lire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="edcc4-114">How to: Read Text from a File</span></span>](../../../docs/standard/io/how-to-read-text-from-a-file.md)  
 [<span data-ttu-id="edcc4-115">Comment : écrire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="edcc4-115">How to: Write Text to a File</span></span>](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
 [<span data-ttu-id="edcc4-116">Comment : lire les caractères d’une chaîne</span><span class="sxs-lookup"><span data-stu-id="edcc4-116">How to: Read Characters from a String</span></span>](../../../docs/standard/io/how-to-read-characters-from-a-string.md)  
 [<span data-ttu-id="edcc4-117">Comment : écrire des caractères dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="edcc4-117">How to: Write Characters to a String</span></span>](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
 [<span data-ttu-id="edcc4-118">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="edcc4-118">File and Stream I/O</span></span>](../../../docs/standard/io/index.md)
