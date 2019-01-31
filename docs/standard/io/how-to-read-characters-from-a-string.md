---
title: 'Procédure : lire les caractères d’une chaîne'
ms.date: 03/30/2017
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
ms.openlocfilehash: cbf213c783d1688e9168265cedc27d2ac7a5a96d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504809"
---
# <a name="how-to-read-characters-from-a-string"></a>Procédure : lire les caractères d’une chaîne
Les exemples de code suivants montrent comment lire des caractères de façon synchrone et asynchrone à partir d’une chaîne.  
  
## <a name="example"></a>Exemple  
 Cet exemple lit 13 caractères de façon synchrone à partir d’une chaîne, les stocke dans un tableau et les affiche. Ensuite, il lit les caractères restants de la chaîne, les stocke dans le tableau à partir du sixième élément et affiche le contenu du tableau.  
  
 [!code-cpp[Conceptual.StringReader#1](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.stringreader/cpp/source.cpp#1)]
 [!code-csharp[Conceptual.StringReader#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source.cs#1)]
 [!code-vb[Conceptual.StringReader#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source.vb#1)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant lit tous les caractères de façon asynchrone à partir d’un contrôle <xref:System.Windows.Controls.TextBox> et les stocke dans un tableau. Ensuite, il écrit de façon asynchrone chaque lettre ou espace blanc sur une ligne distincte, suivie d’un saut de ligne dans un contrôle <xref:System.Windows.Controls.TextBlock>.  
  
 [!code-csharp[Conceptual.StringReader#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source2.cs#2)]
 [!code-vb[Conceptual.StringReader#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source2.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO.StringReader>
- <xref:System.IO.StringReader.Read%2A?displayProperty=nameWithType>
- [Asynchronous File I/O](../../../docs/standard/io/asynchronous-file-i-o.md)
- [NIB : Procédure : créer un listing de répertoires](https://msdn.microsoft.com/library/4d2772b1-b991-4532-a8a6-6ef733277e69)
- [Guide pratique pour lire et écrire dans un fichier de données créé récemment](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)
- [Guide pratique pour ouvrir un fichier journal et y ajouter des éléments](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)
- [Guide pratique pour lire du texte dans un fichier](../../../docs/standard/io/how-to-read-text-from-a-file.md)
- [Guide pratique pour écrire du texte dans un fichier](../../../docs/standard/io/how-to-write-text-to-a-file.md)
- [Guide pratique pour écrire des caractères dans une chaîne](../../../docs/standard/io/how-to-write-characters-to-a-string.md)
- [Fichier et flux de données E/S](../../../docs/standard/io/index.md)
