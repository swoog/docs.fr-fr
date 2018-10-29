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
ms.openlocfilehash: 5e52b827f337892c33ec61b9affa1cc646a759c5
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48841175"
---
# <a name="composing-streams"></a>Composition de flux
Un magasin de stockage est un support de stockage, comme un disque ou de la mémoire. Chaque magasin de stockage implémente son propre flux en tant qu’implémentation de la classe <xref:System.IO.Stream>. Chaque type de flux lit et écrit des octets depuis et vers le magasin de stockage donné. Les flux qui se connectent aux magasins de stockage sont appelés des flux de base. Les flux de base possèdent des constructeurs qui ont les paramètres requis pour connecter le flux au magasin de stockage. Par exemple, <xref:System.IO.FileStream> possède des constructeurs qui spécifient un paramètre de chemin d’accès, qui indique la façon dont le fichier est partagé par les processus, et ainsi de suite.  
  
 La conception des classes <xref:System.IO> fournit une composition simplifiée des flux. Les flux de base peuvent être joints à un ou plusieurs flux directs qui fournissent la fonctionnalité souhaitée. Un lecteur ou un writer peut être joint à la fin de la chaîne afin que les types préférés puissent être lus ou écrits facilement.  
  
 L’exemple de code suivant crée un **FileStream** autour du fichier `MyFile.txt` existant afin de placer `MyFile.txt` dans la mémoire tampon. (Notez que les **FileStreams** sont mis en mémoire tampon par défaut.) Ensuite, un <xref:System.IO.StreamReader> est créé pour lire les caractères à partir du **FileStream**, qui est transmis à **StreamReader** en tant qu’argument de son constructeur. <xref:System.IO.StreamReader.ReadLine%2A> lit jusqu’à ce que <xref:System.IO.StreamReader.Peek%2A> ne détecte plus aucun caractère.  
  
 [!code-cpp[System.IO.StreamReader#20](../../../samples/snippets/cpp/VS_Snippets_CLR_System/system.IO.StreamReader/CPP/source2.cpp#20)]
 [!code-csharp[System.IO.StreamReader#20](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.IO.StreamReader/CS/source2.cs#20)]
 [!code-vb[System.IO.StreamReader#20](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.IO.StreamReader/VB/source2.vb#20)]  
  
 L’exemple de code suivant crée un **FileStream** autour du fichier `MyFile.txt` existant afin de placer `MyFile.txt` dans la mémoire tampon. (Notez que les **FileStreams** sont mis en mémoire tampon par défaut.) Ensuite, un **BinaryReader** est créé pour lire les octets à partir du **FileStream**, qui est transmis à **BinaryReader** en tant qu’argument de son constructeur. <xref:System.IO.BinaryReader.ReadByte%2A> lit jusqu’à ce que <xref:System.IO.BinaryReader.PeekChar%2A> ne détecte plus aucun octet.  
  
 [!code-cpp[System.IO.StreamReader#21](../../../samples/snippets/cpp/VS_Snippets_CLR_System/system.IO.StreamReader/CPP/source3.cpp#21)]
 [!code-csharp[System.IO.StreamReader#21](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.IO.StreamReader/CS/source3.cs#21)]
 [!code-vb[System.IO.StreamReader#21](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.IO.StreamReader/VB/source3.vb#21)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO.StreamReader>  
- <xref:System.IO.StreamReader.ReadLine%2A?displayProperty=nameWithType>  
- <xref:System.IO.StreamReader.Peek%2A?displayProperty=nameWithType>  
- <xref:System.IO.FileStream>  
- <xref:System.IO.BinaryReader>  
- <xref:System.IO.BinaryReader.ReadByte%2A?displayProperty=nameWithType>  
- <xref:System.IO.BinaryReader.PeekChar%2A?displayProperty=nameWithType>
