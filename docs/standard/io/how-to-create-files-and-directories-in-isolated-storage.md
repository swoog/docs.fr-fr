---
title: 'Comment : créer des fichiers et des répertoires dans un stockage isolé'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- directories [.NET Framework], isolated storage
- files [.NET Framework], isolated storage
- isolated storage, creating files and directories
- data stores, creating files and directories
- data storage using isolated storage, creating files and directories
- stores, creating files and directories
- storing data using isolated storage, creating files and directories
ms.assetid: 2ca4d2a4-809b-4f00-bc08-bf4a64d3a5c3
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 08beb44fdb58ab1c1d53f70ac0653348b96fcb18
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44227046"
---
# <a name="how-to-create-files-and-directories-in-isolated-storage"></a>Comment : créer des fichiers et des répertoires dans un stockage isolé
Après avoir obtenu un magasin isolé, vous pouvez créer des répertoires et des fichiers pour le stockage des données. Dans un magasin, les noms de répertoires et de fichiers sont spécifiées par rapport à la racine du système de fichiers virtuel.  
  
 Pour créer un répertoire, utilisez la méthode d’instance <xref:System.IO.IsolatedStorage.IsolatedStorageFile.CreateDirectory%2A?displayProperty=nameWithType>. Si vous spécifiez un sous-répertoire d’un répertoire qui n’existe pas, les deux répertoires sont créés. Si vous spécifiez un répertoire qui existe déjà, la méthode retourne sans créer de répertoire et aucune exception n’est levée. Toutefois, si vous spécifiez un nom de répertoire qui contient des caractères non valides, une exception <xref:System.IO.IsolatedStorage.IsolatedStorageException> est levée.  
  
 Utilisez la méthode <xref:System.IO.IsolatedStorage.IsolatedStorageFile.CreateFile%2A?displayProperty=nameWithType> pour créer un fichier.  
  
 Dans le système d’exploitation Windows, les noms de fichiers et de répertoires du stockage isolé ne sont pas sensibles à la casse. Autrement dit, si vous créez un fichier nommé `ThisFile.txt`, puis créez un autre fichier nommé `THISFILE.TXT`, un seul fichier est créé. Le nom de fichier conserve sa casse d’origine pour l’affichage.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant illustre comment créer des fichiers et des répertoires dans un magasin isolé.  
  
 [!code-csharp[Conceptual.IsolatedStorage#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.isolatedstorage/cs/source.cs#1)]
 [!code-vb[Conceptual.IsolatedStorage#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.isolatedstorage/vb/source.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO.IsolatedStorage.IsolatedStorageFile>  
- <xref:System.IO.IsolatedStorage.IsolatedStorageFileStream>  
- [Stockage isolé](../../../docs/standard/io/isolated-storage.md)
