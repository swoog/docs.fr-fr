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
# <a name="how-to-retrieve-the-contents-of-the-my-documents-directory-in-visual-basic"></a><span data-ttu-id="21015-102">Procédure : récupérer le contenu du répertoire Mes documents en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="21015-102">How to: Retrieve the Contents of the My Documents Directory in Visual Basic</span></span>
<span data-ttu-id="21015-103">Vous pouvez utiliser l’objet <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories> pour lire la plupart des répertoires de **Tous les utilisateurs**, tels que **Mes documents** ou **Bureau**.</span><span class="sxs-lookup"><span data-stu-id="21015-103">The <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories> object can be used to read from many of the **All Users** directories, such as **My Documents** or **Desktop**.</span></span>  
  
### <a name="to-read-from-the-my-documents-folder"></a><span data-ttu-id="21015-104">Pour lire à partir du dossier Mes documents</span><span class="sxs-lookup"><span data-stu-id="21015-104">To read from the My Documents folder</span></span>  
  
- <span data-ttu-id="21015-105">Utilisez la méthode `ReadAllText` pour lire le texte de chaque fichier dans un répertoire spécifique.</span><span class="sxs-lookup"><span data-stu-id="21015-105">Use the `ReadAllText` method to read the text from each file in a specific directory.</span></span> <span data-ttu-id="21015-106">Le code suivant spécifie un répertoire et un fichier, puis il utilise `ReadAllText` pour les lire dans la chaîne nommée `patients`.</span><span class="sxs-lookup"><span data-stu-id="21015-106">The following code specifies a directory and file and then uses `ReadAllText` to read them into the string named `patients`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#15)]  
  
## <a name="see-also"></a><span data-ttu-id="21015-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21015-107">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A>
