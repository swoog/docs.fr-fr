---
title: Composition de flux
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- streams, base streams
- I/O [.NET Framework], composing streams
- Stream class, composing streams
- base streams
- streams, backing stores
ms.assetid: da761658-a535-4f26-a452-b30df47f73d5
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1f2aa68822dd14b4cb81b48598faa6bdb4c71a13
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544352"
---
# <a name="composing-streams"></a><span data-ttu-id="4455b-102">Composition de flux</span><span class="sxs-lookup"><span data-stu-id="4455b-102">Composing Streams</span></span>
<span data-ttu-id="4455b-103">Un magasin de stockage est un support de stockage, comme un disque ou de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4455b-103">A backing store is a storage medium, such as a disk or memory.</span></span> <span data-ttu-id="4455b-104">Chaque magasin de stockage implémente son propre flux en tant qu’implémentation de la classe <xref:System.IO.Stream>.</span><span class="sxs-lookup"><span data-stu-id="4455b-104">Each different backing store implements its own stream as an implementation of the <xref:System.IO.Stream> class.</span></span> <span data-ttu-id="4455b-105">Chaque type de flux lit et écrit des octets depuis et vers le magasin de stockage donné.</span><span class="sxs-lookup"><span data-stu-id="4455b-105">Each stream type reads and writes bytes from and to its given backing store.</span></span> <span data-ttu-id="4455b-106">Les flux qui se connectent aux magasins de stockage sont appelés des flux de base.</span><span class="sxs-lookup"><span data-stu-id="4455b-106">Streams that connect to backing stores are called base streams.</span></span> <span data-ttu-id="4455b-107">Les flux de base possèdent des constructeurs qui ont les paramètres requis pour connecter le flux au magasin de stockage.</span><span class="sxs-lookup"><span data-stu-id="4455b-107">Base streams have constructors that have the parameters necessary to connect the stream to the backing store.</span></span> <span data-ttu-id="4455b-108">Par exemple, <xref:System.IO.FileStream> possède des constructeurs qui spécifient un paramètre de chemin d’accès, qui indique la façon dont le fichier est partagé par les processus, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="4455b-108">For example, <xref:System.IO.FileStream> has constructors that specify a path parameter, which specifies how the file will be shared by processes, and so on.</span></span>  
  
 <span data-ttu-id="4455b-109">La conception des classes <xref:System.IO> fournit une composition simplifiée des flux.</span><span class="sxs-lookup"><span data-stu-id="4455b-109">The design of the <xref:System.IO> classes provides simplified stream composing.</span></span> <span data-ttu-id="4455b-110">Les flux de base peuvent être joints à un ou plusieurs flux directs qui fournissent la fonctionnalité souhaitée.</span><span class="sxs-lookup"><span data-stu-id="4455b-110">Base streams can be attached to one or more pass-through streams that provide the functionality you want.</span></span> <span data-ttu-id="4455b-111">Un lecteur ou un writer peut être joint à la fin de la chaîne afin que les types préférés puissent être lus ou écrits facilement.</span><span class="sxs-lookup"><span data-stu-id="4455b-111">A reader or writer can be attached to the end of the chain so that the preferred types can be read or written easily.</span></span>  
  
 <span data-ttu-id="4455b-112">L’exemple de code suivant crée un **FileStream** autour du fichier `MyFile.txt` existant afin de placer `MyFile.txt` dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4455b-112">The following code example creates a **FileStream** around the existing `MyFile.txt` in order to buffer `MyFile.txt`.</span></span> <span data-ttu-id="4455b-113">(Notez que les **FileStreams** sont mis en mémoire tampon par défaut.) Ensuite, un <xref:System.IO.StreamReader> est créé pour lire les caractères à partir du **FileStream**, qui est transmis à **StreamReader** en tant qu’argument de son constructeur.</span><span class="sxs-lookup"><span data-stu-id="4455b-113">(Note that **FileStreams** are buffered by default.) Next, a <xref:System.IO.StreamReader> is created to read characters from the **FileStream**, which is passed to the **StreamReader** as its constructor argument.</span></span> <span data-ttu-id="4455b-114"><xref:System.IO.StreamReader.ReadLine%2A> lit jusqu’à ce que <xref:System.IO.StreamReader.Peek%2A> ne détecte plus aucun caractère.</span><span class="sxs-lookup"><span data-stu-id="4455b-114"><xref:System.IO.StreamReader.ReadLine%2A> reads until <xref:System.IO.StreamReader.Peek%2A> finds no more characters.</span></span>  
  
 [!code-cpp[System.IO.StreamReader#20](../../../samples/snippets/cpp/VS_Snippets_CLR_System/system.IO.StreamReader/CPP/source2.cpp#20)]
 [!code-csharp[System.IO.StreamReader#20](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.IO.StreamReader/CS/source2.cs#20)]
 [!code-vb[System.IO.StreamReader#20](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.IO.StreamReader/VB/source2.vb#20)]  
  
 <span data-ttu-id="4455b-115">L’exemple de code suivant crée un **FileStream** autour du fichier `MyFile.txt` existant afin de placer `MyFile.txt` dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4455b-115">The following code example creates a **FileStream** around the existing `MyFile.txt` in order to buffer `MyFile.txt`.</span></span> <span data-ttu-id="4455b-116">(Notez que les **FileStreams** sont mis en mémoire tampon par défaut.) Ensuite, un **BinaryReader** est créé pour lire les octets à partir du **FileStream**, qui est transmis à **BinaryReader** en tant qu’argument de son constructeur.</span><span class="sxs-lookup"><span data-stu-id="4455b-116">(Note that **FileStreams** are buffered by default.) Next, a **BinaryReader** is created to read bytes from the **FileStream**, which is passed to the **BinaryReader** as its constructor argument.</span></span> <span data-ttu-id="4455b-117"><xref:System.IO.BinaryReader.ReadByte%2A> lit jusqu’à ce que <xref:System.IO.BinaryReader.PeekChar%2A> ne détecte plus aucun octet.</span><span class="sxs-lookup"><span data-stu-id="4455b-117"><xref:System.IO.BinaryReader.ReadByte%2A> reads until <xref:System.IO.BinaryReader.PeekChar%2A> finds no more bytes.</span></span>  
  
 [!code-cpp[System.IO.StreamReader#21](../../../samples/snippets/cpp/VS_Snippets_CLR_System/system.IO.StreamReader/CPP/source3.cpp#21)]
 [!code-csharp[System.IO.StreamReader#21](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.IO.StreamReader/CS/source3.cs#21)]
 [!code-vb[System.IO.StreamReader#21](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.IO.StreamReader/VB/source3.vb#21)]  
  
## <a name="see-also"></a><span data-ttu-id="4455b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4455b-118">See also</span></span>

- <xref:System.IO.StreamReader>
- <xref:System.IO.StreamReader.ReadLine%2A?displayProperty=nameWithType>
- <xref:System.IO.StreamReader.Peek%2A?displayProperty=nameWithType>
- <xref:System.IO.FileStream>
- <xref:System.IO.BinaryReader>
- <xref:System.IO.BinaryReader.ReadByte%2A?displayProperty=nameWithType>
- <xref:System.IO.BinaryReader.PeekChar%2A?displayProperty=nameWithType>
