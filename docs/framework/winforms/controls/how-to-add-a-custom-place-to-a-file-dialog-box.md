---
title: 'Procédure : Ajouter un emplacement personnalisé à une boîte de dialogue fichier'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Custom Place to dialog box
- adding Custom Place to dialog box
- CustomPlaces collection
ms.assetid: 63f6469b-59cd-40f6-9e61-8b5831856780
ms.openlocfilehash: d9c1373a16f7d62c2933e01e513478fc6c9866d2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57721877"
---
# <a name="how-to-add-a-custom-place-to-a-file-dialog-box"></a><span data-ttu-id="1b387-102">Procédure : Ajouter un emplacement personnalisé à une boîte de dialogue fichier</span><span class="sxs-lookup"><span data-stu-id="1b387-102">How To: Add a Custom Place to a File Dialog Box</span></span>
<span data-ttu-id="1b387-103">Les boîtes de dialogue d’ouverture et d’enregistrement par défaut sur [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] ont une zone sur le côté gauche intitulée **Liens favoris**.</span><span class="sxs-lookup"><span data-stu-id="1b387-103">The default open and save dialog boxes on [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] have an area on the left side of the dialog box titled **Favorite Links**.</span></span> <span data-ttu-id="1b387-104">Cette zone est appelée Emplacements personnalisés.</span><span class="sxs-lookup"><span data-stu-id="1b387-104">This area is called custom places.</span></span> <span data-ttu-id="1b387-105">Le <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> classes permettent d’ajouter des dossiers à la <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="1b387-105">The <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> classes allow you to add folders to the <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1b387-106">Dans l’ordre d’un emplacement personnalisé apparaisse dans le <xref:System.Windows.Forms.OpenFileDialog> ou <xref:System.Windows.Forms.SaveFileDialog>, le <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> propriété doit être définie sur `true` (la valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="1b387-106">In order for a custom place to appear in the <xref:System.Windows.Forms.OpenFileDialog> or <xref:System.Windows.Forms.SaveFileDialog>, the <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> property must be set to `true` (the default).</span></span>  
  
### <a name="to-add-a-custom-place-to-a-file-dialog-box"></a><span data-ttu-id="1b387-107">Pour ajouter un emplacement personnalisé à une boîte de dialogue Fichier</span><span class="sxs-lookup"><span data-stu-id="1b387-107">To add a custom place to a file dialog box</span></span>  
  
-   <span data-ttu-id="1b387-108">Ajouter un chemin d’accès, un GUID de dossier connu, ou un <xref:System.Windows.Forms.FileDialogCustomPlace> de l’objet à le <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1b387-108">Add a path, a Known Folder GUID, or a <xref:System.Windows.Forms.FileDialogCustomPlace> object to the <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection of the dialog box.</span></span>  
  
     <span data-ttu-id="1b387-109">L’exemple de code suivant montre comment ajouter un chemin :</span><span class="sxs-lookup"><span data-stu-id="1b387-109">The following code example shows how to add a path:</span></span>  
  
    ```vb  
    OpenFileDialog1.CustomPlaces.Add("C:\MyCustomPlace")  
    ```  
  
    ```csharp  
    openFileDialog1.CustomPlaces.Add("C:\\MyCustomPlace");  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="1b387-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b387-110">See also</span></span>
- <xref:System.Windows.Forms.FileDialog>
- <xref:System.Windows.Forms.FileDialogCustomPlacesCollection.Add%2A?displayProperty=nameWithType>
- [<span data-ttu-id="1b387-111">GUID de dossier connus pour des emplacements personnalisés de boîtes de dialogue Fichier</span><span class="sxs-lookup"><span data-stu-id="1b387-111">Known Folder GUIDs for File Dialog Custom Places</span></span>](known-folder-guids-for-file-dialog-custom-places.md)
