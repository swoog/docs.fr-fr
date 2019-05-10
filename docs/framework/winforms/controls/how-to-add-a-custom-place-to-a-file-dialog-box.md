---
title: 'Procédure : ajouter un emplacement personnalisé à une boîte de dialogue fichier'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Custom Place to dialog box
- adding Custom Place to dialog box
- CustomPlaces collection
ms.assetid: 63f6469b-59cd-40f6-9e61-8b5831856780
ms.openlocfilehash: 129ebed6d0a2b075020e635c8463536f97629d2f
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64624107"
---
# <a name="how-to-add-a-custom-place-to-a-file-dialog-box"></a><span data-ttu-id="81aa9-102">Procédure : ajouter un emplacement personnalisé à une boîte de dialogue fichier</span><span class="sxs-lookup"><span data-stu-id="81aa9-102">How To: Add a Custom Place to a File Dialog Box</span></span>
<span data-ttu-id="81aa9-103">Les boîtes de dialogue d’ouverture et d’enregistrement par défaut sur [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] ont une zone sur le côté gauche intitulée **Liens favoris**.</span><span class="sxs-lookup"><span data-stu-id="81aa9-103">The default open and save dialog boxes on [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] have an area on the left side of the dialog box titled **Favorite Links**.</span></span> <span data-ttu-id="81aa9-104">Cette zone est appelée Emplacements personnalisés.</span><span class="sxs-lookup"><span data-stu-id="81aa9-104">This area is called custom places.</span></span> <span data-ttu-id="81aa9-105">Le <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> classes permettent d’ajouter des dossiers à la <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="81aa9-105">The <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> classes allow you to add folders to the <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="81aa9-106">Dans l’ordre d’un emplacement personnalisé apparaisse dans le <xref:System.Windows.Forms.OpenFileDialog> ou <xref:System.Windows.Forms.SaveFileDialog>, le <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> propriété doit être définie sur `true` (la valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="81aa9-106">In order for a custom place to appear in the <xref:System.Windows.Forms.OpenFileDialog> or <xref:System.Windows.Forms.SaveFileDialog>, the <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> property must be set to `true` (the default).</span></span>  
  
### <a name="to-add-a-custom-place-to-a-file-dialog-box"></a><span data-ttu-id="81aa9-107">Pour ajouter un emplacement personnalisé à une boîte de dialogue Fichier</span><span class="sxs-lookup"><span data-stu-id="81aa9-107">To add a custom place to a file dialog box</span></span>  
  
- <span data-ttu-id="81aa9-108">Ajouter un chemin d’accès, un GUID de dossier connu, ou un <xref:System.Windows.Forms.FileDialogCustomPlace> de l’objet à le <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="81aa9-108">Add a path, a Known Folder GUID, or a <xref:System.Windows.Forms.FileDialogCustomPlace> object to the <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection of the dialog box.</span></span>  
  
     <span data-ttu-id="81aa9-109">L’exemple de code suivant montre comment ajouter un chemin :</span><span class="sxs-lookup"><span data-stu-id="81aa9-109">The following code example shows how to add a path:</span></span>  
  
    ```vb  
    OpenFileDialog1.CustomPlaces.Add("C:\MyCustomPlace")  
    ```  
  
    ```csharp  
    openFileDialog1.CustomPlaces.Add("C:\\MyCustomPlace");  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="81aa9-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81aa9-110">See also</span></span>

- <xref:System.Windows.Forms.FileDialog>
- <xref:System.Windows.Forms.FileDialogCustomPlacesCollection.Add%2A?displayProperty=nameWithType>
- [<span data-ttu-id="81aa9-111">GUID de dossier connus pour des emplacements personnalisés de boîtes de dialogue Fichier</span><span class="sxs-lookup"><span data-stu-id="81aa9-111">Known Folder GUIDs for File Dialog Custom Places</span></span>](known-folder-guids-for-file-dialog-custom-places.md)
