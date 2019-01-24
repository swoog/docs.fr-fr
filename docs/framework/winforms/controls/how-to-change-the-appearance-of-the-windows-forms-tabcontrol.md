---
title: 'Procédure : Modifier l’apparence du contrôle TabControl Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- icons [Windows Forms], displaying on tabs
- TabControl control [Windows Forms], changing page appearance
- tabs [Windows Forms], controlling appearance
- buttons [Windows Forms], displaying tabs as
ms.assetid: 7c6cc443-ed62-4d26-b94d-b8913b44f773
ms.openlocfilehash: 1ed062b3991d7738269d30a6ff13cda3c80927c2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54630318"
---
# <a name="how-to-change-the-appearance-of-the-windows-forms-tabcontrol"></a>Procédure : Modifier l’apparence du contrôle TabControl Windows Forms
Vous pouvez modifier l’apparence des onglets dans les Windows Forms à l’aide des propriétés de la <xref:System.Windows.Forms.TabControl> et <xref:System.Windows.Forms.TabPage> objets qui composent les différents onglets du contrôle. En définissant ces propriétés, vous pouvez afficher des images sur les onglets, afficher des onglets verticalement plutôt qu’horizontalement, afficher plusieurs lignes d’onglets et activer ou désactiver les onglets par programmation.  
  
### <a name="to-display-an-icon-on-the-label-part-of-a-tab"></a>Pour afficher une icône sur la partie de l’étiquette d’un onglet  
  
1.  Ajouter un <xref:System.Windows.Forms.ImageList> contrôle au formulaire.  
  
2.  Ajouter des images à la liste d’images.  
  
     Pour plus d’informations sur les listes d’images, consultez [composant ImageList](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md) et [Comment : Ajouter ou supprimer des Images avec les Windows Forms composant ImageList](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).  
  
3.  Définir le <xref:System.Windows.Forms.TabControl.ImageList%2A> propriété de la <xref:System.Windows.Forms.TabControl> à la <xref:System.Windows.Forms.ImageList> contrôle.  
  
4.  Définir le <xref:System.Windows.Forms.TabPage.ImageIndex%2A> propriété de la <xref:System.Windows.Forms.TabPage> à l’index d’une image appropriée dans la liste.  
  
### <a name="to-create-multiple-rows-of-tabs"></a>Pour créer plusieurs lignes d’onglets  
  
1.  Ajoutez le nombre de pages d’onglets.  
  
2.  Définir le <xref:System.Windows.Forms.TabControl.Multiline%2A> propriété de la <xref:System.Windows.Forms.TabControl> à `true`.  
  
3.  Si les onglets n’apparaissent pas déjà dans plusieurs lignes, définissez la <xref:System.Windows.Forms.Control.Width%2A> propriété de la <xref:System.Windows.Forms.TabControl> à être plus restrictif que tous les onglets.  
  
### <a name="to-arrange-tabs-on-the-side-of-the-control"></a>Pour réorganiser les onglets sur le côté du contrôle  
  
-   Définir le <xref:System.Windows.Forms.TabControl.Alignment%2A> propriété de la <xref:System.Windows.Forms.TabControl> à <xref:System.Windows.Forms.TabAlignment.Left> ou <xref:System.Windows.Forms.TabAlignment.Right>.  
  
### <a name="to-programmatically-enable-or-disable-all-controls-on-a-tab"></a>Pour activer ou désactiver tous les contrôles sur un onglet par programme  
  
1.  Définir le <xref:System.Windows.Forms.TabPage.Enabled%2A> propriété de la <xref:System.Windows.Forms.TabPage> à `true` ou `false`.  
  
    ```vb  
    TabPage1.Enabled = False  
    ```  
  
    ```csharp  
    tabPage1.Enabled = false;  
    ```  
  
    ```cpp  
    tabPage1->Enabled = false;  
    ```  
  
### <a name="to-display-tabs-as-buttons"></a>Pour afficher les onglets sous forme de boutons  
  
-   Définir le <xref:System.Windows.Forms.TabControl.Appearance%2A> propriété de la <xref:System.Windows.Forms.TabControl> à <xref:System.Windows.Forms.TabAppearance.Buttons> ou <xref:System.Windows.Forms.TabAppearance.FlatButtons>.  
  
## <a name="see-also"></a>Voir aussi
- [TabControl, contrôle](../../../../docs/framework/winforms/controls/tabcontrol-control-windows-forms.md)
- [Vue d’ensemble du contrôle TabControl](../../../../docs/framework/winforms/controls/tabcontrol-control-overview-windows-forms.md)
- [Guide pratique pour Ajouter un contrôle à une Page d’onglets](../../../../docs/framework/winforms/controls/how-to-add-a-control-to-a-tab-page.md)
- [Guide pratique pour Désactiver les Pages d’onglets](../../../../docs/framework/winforms/controls/how-to-disable-tab-pages.md)
- [Guide pratique pour Ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
