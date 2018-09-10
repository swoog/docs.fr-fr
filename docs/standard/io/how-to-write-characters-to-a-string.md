---
title: 'Comment : écrire des caractères dans une chaîne'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data streams, writing characters to string
- writing characters to strings
- streams, writing characters to strings
- I/O [.NET Framework], writing characters to strings
ms.assetid: 1222cbeb-0760-44bf-9888-914a2a37174b
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bea51eaf11bd9d73d5a68eb09795bd9f9f143f95
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44214470"
---
# <a name="how-to-write-characters-to-a-string"></a><span data-ttu-id="d49e3-102">Comment : écrire des caractères dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="d49e3-102">How to: Write Characters to a String</span></span>
<span data-ttu-id="d49e3-103">Les exemples de code suivants écrivent des caractères de façon synchrone et asynchrone à partir d’un tableau de caractères dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d49e3-103">The following code examples write characters synchronously and asynchronously from a character array into a string.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d49e3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="d49e3-104">Example</span></span>  
 <span data-ttu-id="d49e3-105">L’exemple suivant écrit 5 caractères de façon synchrone à partir d’un tableau dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d49e3-105">The following example writes 5 characters synchronously from an array to a string.</span></span>  
  
 [!code-csharp[Conceptual.StringBuilder#9](../../../samples/snippets/csharp/VS_Snippets_CLR/Conceptual.StringBuilder/cs/example2.cs#9)]
 [!code-vb[Conceptual.StringBuilder#9](../../../samples/snippets/visualbasic/VS_Snippets_CLR/Conceptual.StringBuilder/vb/example2.vb#9)]  
  
## <a name="example"></a><span data-ttu-id="d49e3-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="d49e3-106">Example</span></span>  
 <span data-ttu-id="d49e3-107">L’exemple suivant lit tous les caractères de façon asynchrone à partir d’un contrôle <xref:System.Windows.Controls.TextBox> et les stocke dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="d49e3-107">The next example reads all the characters asynchronously from a <xref:System.Windows.Controls.TextBox> control, and stores them in an array.</span></span> <span data-ttu-id="d49e3-108">Ensuite, il écrit de façon asynchrone chaque lettre ou espace blanc sur une ligne distincte, suivie d’un saut de ligne dans un contrôle <xref:System.Windows.Controls.TextBlock>.</span><span class="sxs-lookup"><span data-stu-id="d49e3-108">It then asynchronously writes each letter or white space character on a separate line followed by a line break to a <xref:System.Windows.Controls.TextBlock> control.</span></span>  
  
 [!code-csharp[Conceptual.StringReader#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source2.cs#2)]
 [!code-vb[Conceptual.StringReader#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="d49e3-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d49e3-109">See also</span></span>

- <xref:System.IO.StringWriter>  
- <xref:System.IO.StringWriter.Write%2A?displayProperty=nameWithType>  
- <xref:System.Text.StringBuilder>  
- [<span data-ttu-id="d49e3-110">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="d49e3-110">File and Stream I/O</span></span>](../../../docs/standard/io/index.md)  
- [<span data-ttu-id="d49e3-111">E/S sur fichier asynchrones</span><span class="sxs-lookup"><span data-stu-id="d49e3-111">Asynchronous File I/O</span></span>](../../../docs/standard/io/asynchronous-file-i-o.md)  
- [<span data-ttu-id="d49e3-112">Guide pratique pour énumérer des répertoires et des fichiers</span><span class="sxs-lookup"><span data-stu-id="d49e3-112">How to: Enumerate Directories and Files</span></span>](../../../docs/standard/io/how-to-enumerate-directories-and-files.md)  
- [<span data-ttu-id="d49e3-113">Comment : lire et écrire dans un fichier de données créé récemment</span><span class="sxs-lookup"><span data-stu-id="d49e3-113">How to: Read and Write to a Newly Created Data File</span></span>](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)  
- [<span data-ttu-id="d49e3-114">Comment : ouvrir un fichier journal et y ajouter des éléments</span><span class="sxs-lookup"><span data-stu-id="d49e3-114">How to: Open and Append to a Log File</span></span>](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)  
- [<span data-ttu-id="d49e3-115">Comment : lire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="d49e3-115">How to: Read Text from a File</span></span>](../../../docs/standard/io/how-to-read-text-from-a-file.md)  
- [<span data-ttu-id="d49e3-116">Comment : écrire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="d49e3-116">How to: Write Text to a File</span></span>](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
- [<span data-ttu-id="d49e3-117">Comment : lire les caractères d’une chaîne</span><span class="sxs-lookup"><span data-stu-id="d49e3-117">How to: Read Characters from a String</span></span>](../../../docs/standard/io/how-to-read-characters-from-a-string.md)
