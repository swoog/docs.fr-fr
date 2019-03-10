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
# <a name="how-to-add-a-custom-place-to-a-file-dialog-box"></a>Procédure : Ajouter un emplacement personnalisé à une boîte de dialogue fichier
Les boîtes de dialogue d’ouverture et d’enregistrement par défaut sur [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] ont une zone sur le côté gauche intitulée **Liens favoris**. Cette zone est appelée Emplacements personnalisés. Le <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> classes permettent d’ajouter des dossiers à la <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection.  
  
> [!NOTE]
>  Dans l’ordre d’un emplacement personnalisé apparaisse dans le <xref:System.Windows.Forms.OpenFileDialog> ou <xref:System.Windows.Forms.SaveFileDialog>, le <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> propriété doit être définie sur `true` (la valeur par défaut).  
  
### <a name="to-add-a-custom-place-to-a-file-dialog-box"></a>Pour ajouter un emplacement personnalisé à une boîte de dialogue Fichier  
  
-   Ajouter un chemin d’accès, un GUID de dossier connu, ou un <xref:System.Windows.Forms.FileDialogCustomPlace> de l’objet à le <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection de la boîte de dialogue.  
  
     L’exemple de code suivant montre comment ajouter un chemin :  
  
    ```vb  
    OpenFileDialog1.CustomPlaces.Add("C:\MyCustomPlace")  
    ```  
  
    ```csharp  
    openFileDialog1.CustomPlaces.Add("C:\\MyCustomPlace");  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.FileDialog>
- <xref:System.Windows.Forms.FileDialogCustomPlacesCollection.Add%2A?displayProperty=nameWithType>
- [GUID de dossier connus pour des emplacements personnalisés de boîtes de dialogue Fichier](known-folder-guids-for-file-dialog-custom-places.md)
