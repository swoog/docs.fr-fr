---
title: Guide pratique pour ajouter un emplacement personnalisé à une boîte de dialogue Fichier
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Custom Place to dialog box
- adding Custom Place to dialog box
- CustomPlaces collection
ms.assetid: 63f6469b-59cd-40f6-9e61-8b5831856780
ms.openlocfilehash: 7a6ace385f7594a467785fbc677517c8a6e1ab53
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-add-a-custom-place-to-a-file-dialog-box"></a>Guide pratique pour ajouter un emplacement personnalisé à une boîte de dialogue Fichier
Les boîtes de dialogue d’ouverture et d’enregistrement par défaut sur [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] ont une zone sur le côté gauche intitulée **Liens favoris**. Cette zone est appelée Emplacements personnalisés. Le <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> classes permettent d’ajouter des dossiers à la <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection.  
  
> [!NOTE]
>  Dans l’ordre d’un emplacement personnalisé s’affichent dans le <xref:System.Windows.Forms.OpenFileDialog> ou <xref:System.Windows.Forms.SaveFileDialog>, le <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> propriété doit être définie sur `true` (la valeur par défaut).  
  
### <a name="to-add-a-custom-place-to-a-file-dialog-box"></a>Pour ajouter un emplacement personnalisé à une boîte de dialogue Fichier  
  
-   Ajouter un chemin d’accès, un GUID de dossier connus, ou un <xref:System.Windows.Forms.FileDialogCustomPlace> de l’objet à le <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection de la boîte de dialogue.  
  
     L’exemple de code suivant montre comment ajouter un chemin :  
  
    ```vb  
    OpenFileDialog1.CustomPlaces.Add("C:\MyCustomPlace")  
    ```  
  
    ```csharp  
    openFileDialog1.CustomPlaces.Add("C:\\MyCustomPlace");  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.FileDialog>  
 <xref:System.Windows.Forms.FileDialogCustomPlacesCollection.Add%2A?displayProperty=nameWithType>  
 [GUID de dossier connus pour des emplacements personnalisés de boîtes de dialogue Fichier](../../../../docs/framework/winforms/controls/known-folder-guids-for-file-dialog-custom-places.md)
