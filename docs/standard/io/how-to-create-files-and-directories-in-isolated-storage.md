---
title: "Comment : créer des fichiers et des répertoires dans un stockage isolé"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
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
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: cf6295e7d58d03e7b4bf4e0a00cfc509d289e071
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
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
 <xref:System.IO.IsolatedStorage.IsolatedStorageFile>  
 <xref:System.IO.IsolatedStorage.IsolatedStorageFileStream>  
 [Stockage isolé](../../../docs/standard/io/isolated-storage.md)
