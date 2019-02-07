---
title: 'Procédure : Lire les caractères d’une chaîne'
ms.date: 01/21/2019
ms.technology: dotnet-standard
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
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 01d5fb2e4f785a4a510715b58e95d310a6ffa4e2
ms.sourcegitcommit: b8ace47d839f943f785b89e2fff8092b0bf8f565
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2019
ms.locfileid: "55675346"
---
# <a name="how-to-read-characters-from-a-string"></a><span data-ttu-id="83a3a-102">Procédure : Lire les caractères d’une chaîne</span><span class="sxs-lookup"><span data-stu-id="83a3a-102">How to: Read characters from a string</span></span>
<span data-ttu-id="83a3a-103">Les exemples de code suivants montrent comment lire des caractères de façon synchrone et asynchrone à partir d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="83a3a-103">The following code examples show how to read characters synchronously or asynchronously from a string.</span></span>  
  
## <a name="example-read-characters-synchronously"></a><span data-ttu-id="83a3a-104">Exemple : Lire des caractères de façon synchrone</span><span class="sxs-lookup"><span data-stu-id="83a3a-104">Example: Read characters synchronously</span></span> 
 <span data-ttu-id="83a3a-105">Cet exemple lit 13 caractères de façon synchrone à partir d’une chaîne, les stocke dans un tableau, puis les affiche.</span><span class="sxs-lookup"><span data-stu-id="83a3a-105">This example reads 13 characters synchronously from a string, stores them in an array, and displays them.</span></span> <span data-ttu-id="83a3a-106">Ensuite, l’exemple lit les caractères restants de la chaîne, les stocke dans le tableau à partir du sixième élément, puis affiche le contenu du tableau.</span><span class="sxs-lookup"><span data-stu-id="83a3a-106">The example then reads the rest of the characters in the string, stores them in the array starting at the sixth element, and displays the contents of the array.</span></span>  
  
 [!code-csharp[Conceptual.StringReader#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source.cs#1)]
 [!code-vb[Conceptual.StringReader#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source.vb#1)]  
  
## <a name="example-read-characters-asynchronously"></a><span data-ttu-id="83a3a-107">Exemple : Lire des caractères de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="83a3a-107">Example: Read characters asynchronously</span></span>  
 <span data-ttu-id="83a3a-108">L’exemple suivant montre le code-behind d’une application WPF.</span><span class="sxs-lookup"><span data-stu-id="83a3a-108">The next example is the code behind a WPF app.</span></span> <span data-ttu-id="83a3a-109">Au chargement de la fenêtre, l’exemple lit tous les caractères de façon asynchrone à partir d’un contrôle <xref:System.Windows.Controls.TextBox> et les stocke dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="83a3a-109">On window load, the example asynchronously reads all characters from a <xref:System.Windows.Controls.TextBox> control and stores them in an array.</span></span> <span data-ttu-id="83a3a-110">Ensuite, il écrit de façon asynchrone chaque lettre ou espace blanc sur une ligne distincte d’un contrôle <xref:System.Windows.Controls.TextBlock>.</span><span class="sxs-lookup"><span data-stu-id="83a3a-110">It then asynchronously writes each letter or white-space character to a separate line of a <xref:System.Windows.Controls.TextBlock> control.</span></span>  
  
 [!code-csharp[Conceptual.StringReader#2](../../../samples/snippets/csharp/VS_Snippets_Wpf/StringReaderWriter/MainWindow.xaml.cs)]
 [!code-vb[Conceptual.StringReader#2](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/StringReaderWriter/MainWindow.xaml.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="83a3a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83a3a-111">See also</span></span>

- <xref:System.IO.StringReader>  
- <xref:System.IO.StringReader.Read%2A?displayProperty=nameWithType>  
- [<span data-ttu-id="83a3a-112">E/S sur fichier asynchrones</span><span class="sxs-lookup"><span data-stu-id="83a3a-112">Asynchronous file I/O</span></span>](../../../docs/standard/io/asynchronous-file-i-o.md)  
- [<span data-ttu-id="83a3a-113">Guide pratique pour créer une liste de répertoires</span><span class="sxs-lookup"><span data-stu-id="83a3a-113">How to: Create a directory listing</span></span>](https://msdn.microsoft.com/library/4d2772b1-b991-4532-a8a6-6ef733277e69)  
- [<span data-ttu-id="83a3a-114">Guide pratique pour lire et écrire dans un fichier de données créé récemment</span><span class="sxs-lookup"><span data-stu-id="83a3a-114">How to: Read and write to a newly created data file</span></span>](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)  
- [<span data-ttu-id="83a3a-115">Guide pratique pour ouvrir un fichier journal et y ajouter des éléments</span><span class="sxs-lookup"><span data-stu-id="83a3a-115">How to: Open and append to a log file</span></span>](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)  
- [<span data-ttu-id="83a3a-116">Guide pratique pour lire le texte d’un fichier</span><span class="sxs-lookup"><span data-stu-id="83a3a-116">How to: Read text from a file</span></span>](../../../docs/standard/io/how-to-read-text-from-a-file.md)  
- [<span data-ttu-id="83a3a-117">Guide pratique pour écrire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="83a3a-117">How to: Write text to a file</span></span>](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
- [<span data-ttu-id="83a3a-118">Guide pratique pour écrire des caractères dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="83a3a-118">How to: Write characters to a string</span></span>](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
- [<span data-ttu-id="83a3a-119">E/S de fichier et de flux</span><span class="sxs-lookup"><span data-stu-id="83a3a-119">File and stream I/O</span></span>](../../../docs/standard/io/index.md)
