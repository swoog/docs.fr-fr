---
title: 'Procédure : récupérer le contenu du répertoire Mes documents en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- My Documents directory
ms.assetid: 26560d01-7dda-4457-8e95-21db23d71aea
ms.openlocfilehash: f03dbe1811dd5367dab2d32d94ba35ff05fad198
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64623146"
---
# <a name="how-to-retrieve-the-contents-of-the-my-documents-directory-in-visual-basic"></a>Procédure : récupérer le contenu du répertoire Mes documents en Visual Basic
Vous pouvez utiliser l’objet <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories> pour lire la plupart des répertoires de **Tous les utilisateurs**, tels que **Mes documents** ou **Bureau**.  
  
### <a name="to-read-from-the-my-documents-folder"></a>Pour lire à partir du dossier Mes documents  
  
- Utilisez la méthode `ReadAllText` pour lire le texte de chaque fichier dans un répertoire spécifique. Le code suivant spécifie un répertoire et un fichier, puis il utilise `ReadAllText` pour les lire dans la chaîne nommée `patients`.  
  
     [!code-vb[VbVbcnMyFileSystem#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#15)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A>
