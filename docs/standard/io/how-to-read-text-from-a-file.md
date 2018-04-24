---
title: 'Comment : lire du texte dans un fichier'
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
helpviewer_keywords:
- streams, reading text from files
- reading text files
- reading data, text files
- data streams, reading text from files
- I/O [.NET Framework], reading text from files
ms.assetid: ed180baa-dfc6-4c69-a725-46e87edafb27
caps.latest.revision: 23
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: e1058879d4af8aac12baf24d10a0c22894351e6f
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="how-to-read-text-from-a-file"></a><span data-ttu-id="291ce-102">Comment : lire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="291ce-102">How to: Read Text from a File</span></span>
<span data-ttu-id="291ce-103">Les exemples suivants montrent comment lire le texte de façon synchrone et asynchrone à partir d’un fichier texte à l’aide du .NET pour les applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="291ce-103">The following examples show how to read text synchronously and asynchronously from a text file using .NET for desktop apps.</span></span> <span data-ttu-id="291ce-104">Dans les deux exemples, lorsque vous créez l'instance de la classe <xref:System.IO.StreamReader>, vous fournissez le chemin d'accès relatif ou absolu au fichier.</span><span class="sxs-lookup"><span data-stu-id="291ce-104">In both examples, when you create the instance of the <xref:System.IO.StreamReader> class, you provide the relative or absolute path to the file.</span></span> <span data-ttu-id="291ce-105">Les exemples suivants supposent que le fichier nommé TestFile.txt se trouve dans le même dossier que l'application.</span><span class="sxs-lookup"><span data-stu-id="291ce-105">The following examples assume that the file named TestFile.txt is in the same folder as the application.</span></span>  
  
 <span data-ttu-id="291ce-106">Ces exemples de code ne s'appliquent pas à développer des applications Windows Store car le Windows Runtime fournit différents types de flux de lecture et d'écriture aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="291ce-106">These code examples do not apply developing for Windows Store Apps because the Windows Runtime provides different streams types reading and writing to files.</span></span> <span data-ttu-id="291ce-107">Vous trouverez un exemple montrant comment lire le texte d'un fichier dans le contexte d'une application Windows Store sur la page [Démarrage rapide : lire et écrire dans des fichiers](http://msdn.microsoft.com/library/windows/apps/hh758325.aspx).</span><span class="sxs-lookup"><span data-stu-id="291ce-107">For an example that shows how to read text from a file within the context of a Windows Store app, see [Quickstart: Reading and writing files](http://msdn.microsoft.com/library/windows/apps/hh758325.aspx).</span></span> <span data-ttu-id="291ce-108">Vous trouverez des exemples montrant comment effectuer une conversion entre des flux .NET Framework et des flux Windows Runtime sur la page [Guide pratique pour effectuer une conversion entre des flux .NET Framework et des flux Windows Runtime](../../../docs/standard/io/how-to-convert-between-dotnet-streams-and-winrt-streams.md).</span><span class="sxs-lookup"><span data-stu-id="291ce-108">For examples that show how to convert between .NET Framework streams and Windows runtime streams see [How to: Convert Between .NET Framework Streams and Windows Runtime Streams](../../../docs/standard/io/how-to-convert-between-dotnet-streams-and-winrt-streams.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="291ce-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="291ce-109">Example</span></span>  
 <span data-ttu-id="291ce-110">Le premier exemple montre une opération synchrone de lecture dans une application console.</span><span class="sxs-lookup"><span data-stu-id="291ce-110">The first example shows a synchronous read operation within a console application.</span></span> <span data-ttu-id="291ce-111">Dans cet exemple, le fichier texte est ouvert à l'aide d'un lecteur de flux, le contenu est copié dans une chaîne et la chaîne est affichée dans la console.</span><span class="sxs-lookup"><span data-stu-id="291ce-111">In this example, the text file is opened using a stream reader, the contents are copied to a string and string is output to the console.</span></span>  
  
 [!code-csharp[Conceptual.BasicIO.TextFiles#3](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.basicio.textfiles/cs/source3.cs#3)]
 [!code-vb[Conceptual.BasicIO.TextFiles#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.basicio.textfiles/vb/source3.vb#3)]  
  
## <a name="example"></a><span data-ttu-id="291ce-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="291ce-112">Example</span></span>  
 <span data-ttu-id="291ce-113">Le deuxième exemple présente une opération asynchrone de lecture dans une application Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="291ce-113">The second example shows an asynchronous read operation within a Windows Presentation Foundation (WPF) application.</span></span>  
  
 [!code-csharp[Conceptual.BasicIO.TextFiles#6](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.basicio.textfiles/cs/source6.cs#6)]
 [!code-vb[Conceptual.BasicIO.TextFiles#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.basicio.textfiles/vb/source6.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="291ce-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="291ce-114">See Also</span></span>  
 <xref:System.IO.StreamReader>  
 <xref:System.IO.File.OpenText%2A?displayProperty=nameWithType>  
 <xref:System.IO.StreamReader.ReadLine%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="291ce-115">E/S sur fichier asynchrones</span><span class="sxs-lookup"><span data-stu-id="291ce-115">Asynchronous File I/O</span></span>](../../../docs/standard/io/asynchronous-file-i-o.md)  
 [<span data-ttu-id="291ce-116">NIB : Guide pratique : créer un listing de répertoires</span><span class="sxs-lookup"><span data-stu-id="291ce-116">NIB: How to: Create a Directory Listing</span></span>](https://msdn.microsoft.com/library/4d2772b1-b991-4532-a8a6-6ef733277e69)  
 [<span data-ttu-id="291ce-117">Démarrage rapide : lire et écrire dans des fichiers</span><span class="sxs-lookup"><span data-stu-id="291ce-117">Quickstart: Reading and writing files</span></span>](http://msdn.microsoft.com/library/windows/apps/hh758325.aspx)  
 [<span data-ttu-id="291ce-118">Guide pratique pour effectuer une conversion entre les flux .NET Framework et les flux Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="291ce-118">How to: Convert Between .NET Framework Streams and Windows Runtime Streams</span></span>](../../../docs/standard/io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)  
 [<span data-ttu-id="291ce-119">Comment : lire et écrire dans un fichier de données créé récemment</span><span class="sxs-lookup"><span data-stu-id="291ce-119">How to: Read and Write to a Newly Created Data File</span></span>](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)  
 [<span data-ttu-id="291ce-120">Comment : ouvrir un fichier journal et y ajouter des éléments</span><span class="sxs-lookup"><span data-stu-id="291ce-120">How to: Open and Append to a Log File</span></span>](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)  
 [<span data-ttu-id="291ce-121">Comment : écrire du texte dans un fichier</span><span class="sxs-lookup"><span data-stu-id="291ce-121">How to: Write Text to a File</span></span>](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
 [<span data-ttu-id="291ce-122">Comment : lire les caractères d’une chaîne</span><span class="sxs-lookup"><span data-stu-id="291ce-122">How to: Read Characters from a String</span></span>](../../../docs/standard/io/how-to-read-characters-from-a-string.md)  
 [<span data-ttu-id="291ce-123">Comment : écrire des caractères dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="291ce-123">How to: Write Characters to a String</span></span>](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
 [<span data-ttu-id="291ce-124">Fichier et flux de données E/S</span><span class="sxs-lookup"><span data-stu-id="291ce-124">File and Stream I-O</span></span>](../../../docs/standard/io/index.md)
