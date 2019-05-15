---
title: 'Procédure : Lire un fichier texte - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- StreamReader.ReadToEnd
helpviewer_keywords:
- text files, writing to
- reading text files
- reading data, text files
- text files, reading
ms.assetid: 92246c5b-e819-4eea-9370-1a9460e12de3
ms.openlocfilehash: 236e730eaae0bc73c715e9b1c2c71d6c870d78e3
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64608533"
---
# <a name="how-to-read-from-a-text-file-c-programming-guide"></a>Procédure : Lire un fichier texte (Guide de programmation C#)
Cet exemple lit le contenu d’un fichier texte à l’aide des méthodes statiques <xref:System.IO.File.ReadAllText%2A> et <xref:System.IO.File.ReadAllLines%2A> de la classe <xref:System.IO.File?displayProperty=nameWithType>.  
  
 Pour obtenir un exemple utilisant <xref:System.IO.StreamReader>, consultez [Guide pratique pour lire un fichier texte ligne par ligne](../../../csharp/programming-guide/file-system/how-to-read-a-text-file-one-line-at-a-time.md).  
  
> [!NOTE]
>  Les fichiers qui sont utilisés dans cet exemple sont créés dans la rubrique [Guide pratique pour écrire dans un fichier texte](../../../csharp/programming-guide/file-system/how-to-write-to-a-text-file.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csFilesandFolders#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csFilesAndFolders/CS/FileIteration.cs#4)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Copiez le code et collez-le dans une application console C#.  
  
 Si vous n’utilisez pas les fichiers texte à partir de [Guide pratique pour écrire dans un fichier texte](../../../csharp/programming-guide/file-system/how-to-write-to-a-text-file.md), remplacez l’argument par `ReadAllText` et `ReadAllLines`, en fournissant le chemin et le nom correspondants sur votre ordinateur.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
- Le fichier n’existe pas ou ne se trouve pas à l’emplacement spécifié. Vérifiez le chemin et l’orthographe du nom de fichier.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Ne comptez pas sur le nom d’un fichier pour en déduire le contenu. Par exemple, le fichier `myFile.cs` peut ne pas être un fichier source C#.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO?displayProperty=nameWithType>
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Système de fichiers et Registre (Guide de programmation C#)](../../../csharp/programming-guide/file-system/index.md)
