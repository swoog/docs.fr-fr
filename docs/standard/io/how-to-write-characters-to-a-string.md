---
title: 'Procédure : écrire des caractères dans une chaîne'
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
ms.openlocfilehash: 125c8ba03c4d1006535dd1e10cbd162b32fede4f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54740981"
---
# <a name="how-to-write-characters-to-a-string"></a>Procédure : écrire des caractères dans une chaîne
Les exemples de code suivants écrivent des caractères de façon synchrone et asynchrone à partir d’un tableau de caractères dans une chaîne.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant écrit 5 caractères de façon synchrone à partir d’un tableau dans une chaîne.  
  
 [!code-csharp[Conceptual.StringBuilder#9](../../../samples/snippets/csharp/VS_Snippets_CLR/Conceptual.StringBuilder/cs/example2.cs#9)]
 [!code-vb[Conceptual.StringBuilder#9](../../../samples/snippets/visualbasic/VS_Snippets_CLR/Conceptual.StringBuilder/vb/example2.vb#9)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant lit tous les caractères de façon asynchrone à partir d’un contrôle <xref:System.Windows.Controls.TextBox> et les stocke dans un tableau. Ensuite, il écrit de façon asynchrone chaque lettre ou espace blanc sur une ligne distincte, suivie d’un saut de ligne dans un contrôle <xref:System.Windows.Controls.TextBlock>.  
  
 [!code-csharp[Conceptual.StringReader#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source2.cs#2)]
 [!code-vb[Conceptual.StringReader#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source2.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO.StringWriter>
- <xref:System.IO.StringWriter.Write%2A?displayProperty=nameWithType>
- <xref:System.Text.StringBuilder>
- [Fichier et flux de données E/S](../../../docs/standard/io/index.md)
- [Asynchronous File I/O](../../../docs/standard/io/asynchronous-file-i-o.md)
- [Guide pratique pour énumérer des répertoires et des fichiers](../../../docs/standard/io/how-to-enumerate-directories-and-files.md)
- [Guide pratique pour lire et écrire dans un fichier de données créé récemment](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)
- [Guide pratique pour ouvrir un fichier journal et y ajouter des éléments](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)
- [Guide pratique pour lire du texte dans un fichier](../../../docs/standard/io/how-to-read-text-from-a-file.md)
- [Guide pratique pour écrire du texte dans un fichier](../../../docs/standard/io/how-to-write-text-to-a-file.md)
- [Guide pratique pour lire les caractères d’une chaîne](../../../docs/standard/io/how-to-read-characters-from-a-string.md)
