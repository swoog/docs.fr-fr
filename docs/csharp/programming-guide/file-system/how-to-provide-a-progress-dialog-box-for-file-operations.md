---
title: 'Comment : fournir une boîte de dialogue de progression pour les opérations sur les fichiers (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- progress dialog [C#]
ms.assetid: 01b71fe7-8178-4dc8-aeb1-12053be7b51c
ms.openlocfilehash: e93ce06a01046dfaf4465470ba7fdc687effa58d
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46710801"
---
# <a name="how-to-provide-a-progress-dialog-box-for-file-operations-c-programming-guide"></a>Comment : fournir une boîte de dialogue de progression pour les opérations sur les fichiers (Guide de programmation C#)
Vous pouvez fournir une boîte de dialogue standard qui montre la progression des opérations sur les fichiers dans Windows si vous utilisez la méthode <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile%28System.String%2CSystem.String%2CMicrosoft.VisualBasic.FileIO.UIOption%29> de l’espace de noms <xref:Microsoft.VisualBasic?displayProperty=nameWithType>.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-add-a-reference-in-visual-studio"></a>Pour ajouter une référence dans Visual Studio  
  
1.  Dans la barre de menus, choisissez **Projet**, **Ajouter une référence**.  
  
     La boîte de dialogue **Gestionnaire de références** s’affiche.  
  
2.  Dans la zone **Assemblys**, choisissez **Framework** s’il n’est pas déjà sélectionné.  
  
3.  Dans la liste des noms, cochez la case **Microsoft.VisualBasic**, puis choisissez le bouton **OK** pour fermer la boîte de dialogue.  
  
## <a name="example"></a>Exemple  
 Le code suivant copie le répertoire spécifié par `sourcePath` dans le répertoire spécifié par `destinationPath`. Ce code fournit également une boîte de dialogue standard qui affiche une estimation du temps restant avant la fin de l’opération.  
  
 [!code-csharp[csFilesandFolders#11](../../../csharp/programming-guide/file-system/codesnippet/CSharp/how-to-provide-a-progress-dialog-box-for-file-operations_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Système de fichiers et Registre (Guide de programmation C#)](../../../csharp/programming-guide/file-system/index.md)
