---
title: "Comment : lire les caractères d'une chaîne"
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology: dotnet-standard
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- reading characters from strings
- data streams, reading characters from string
- I/O [.NET Framework], reading characters from strings
- reading data, strings
- streams, reading characters from string
ms.assetid: 27ea5e52-6db8-42d8-980a-50bcfc7fd270
caps.latest.revision: 13
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: c4023d8e801da542414aac1fddaf7aef5bf1e98f
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="how-to-read-characters-from-a-string"></a><span data-ttu-id="f6f13-102">Comment : lire les caractères d'une chaîne</span><span class="sxs-lookup"><span data-stu-id="f6f13-102">How to: Read Characters from a String</span></span>
<span data-ttu-id="f6f13-103">Les exemples de code suivants montrent comment lire des caractères de façon synchrone et asynchrone à partir d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f6f13-103">The following code examples show how to read characters synchronously and asynchronously from a string.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f6f13-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f6f13-104">Example</span></span>  
 <span data-ttu-id="f6f13-105">Cet exemple lit 13 caractères de façon synchrone à partir d’une chaîne, les stocke dans un tableau et les affiche.</span><span class="sxs-lookup"><span data-stu-id="f6f13-105">This example reads 13 characters synchronously from a string, stores them in an array, and displays those characters.</span></span> <span data-ttu-id="f6f13-106">Ensuite, il lit les caractères restants de la chaîne, les stocke dans le tableau à partir du sixième élément et affiche le contenu du tableau.</span><span class="sxs-lookup"><span data-stu-id="f6f13-106">It then reads the remaining characters in the string, stores them in the array starting at the sixth element, and displays the contents of the array.</span></span>  
  
 [!code-cpp[Conceptual.StringReader#1](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.stringreader/cpp/source.cpp#1)]
 [!code-csharp[Conceptual.StringReader#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source.cs#1)]
 [!code-vb[Conceptual.StringReader#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="f6f13-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="f6f13-107">Example</span></span>  
 <span data-ttu-id="f6f13-108">L’exemple suivant lit tous les caractères de façon asynchrone à partir d’un contrôle <xref:System.Windows.Controls.TextBox> et les stocke dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="f6f13-108">The next example reads all the characters asynchronously from a <xref:System.Windows.Controls.TextBox> control, and stores them in an array.</span></span> <span data-ttu-id="f6f13-109">Ensuite, il écrit de façon asynchrone chaque lettre ou espace blanc sur une ligne distincte, suivie d’un saut de ligne dans un contrôle <xref:System.Windows.Controls.TextBlock>.</span><span class="sxs-lookup"><span data-stu-id="f6f13-109">It then asynchronously writes each letter or white space character on a separate line followed by a line break to a <xref:System.Windows.Controls.TextBlock> control.</span></span>  
  
 [!code-csharp[Conceptual.StringReader#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source2.cs#2)]
 [!code-vb[Conceptual.StringReader#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="f6f13-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6f13-110">See Also</span></span>  
 <xref:System.IO.StringReader>  
 <xref:System.IO.StringReader.Read%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="f6f13-111">E/S sur fichier asynchrones</span><span class="sxs-lookup"><span data-stu-id="f6f13-111">Asynchronous File I/O</span></span>](../../../docs/standard/io/asynchronous-file-i-o.md)  
 [<span data-ttu-id="f6f13-112">NIB : Guide pratique : créer un listing de répertoires</span><span class="sxs-lookup"><span data-stu-id="f6f13-112">NIB: How to: Create a Directory Listing</span></span>](https://msdn.microsoft.com/library/4d2772b1-b991-4532-a8a6-6ef733277e69)  
 [<span data-ttu-id="f6f13-113">Comment : lire et écrire dans un fichier de données créé récemment</span><span class="sxs-lookup"><span data-stu-id="f6f13-113">How to: Read and Write to a Newly Created Data File</span></span>](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)  
 [<span data-ttu-id="f6f13-114">Comment : ouvrir un fichier journal et y ajouter des éléments</span><span class="sxs-lookup"><span data-stu-id="f6f13-114">How to: Open and Append to a Log File</span></span>](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)  
 [<span data-ttu-id="f6f13-115">Comment : lire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="f6f13-115">How to: Read Text from a File</span></span>](../../../docs/standard/io/how-to-read-text-from-a-file.md)  
 [<span data-ttu-id="f6f13-116">Comment : écrire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="f6f13-116">How to: Write Text to a File</span></span>](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
 [<span data-ttu-id="f6f13-117">Comment : écrire des caractères dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="f6f13-117">How to: Write Characters to a String</span></span>](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
 [<span data-ttu-id="f6f13-118">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="f6f13-118">File and Stream I-O</span></span>](../../../docs/standard/io/index.md)
