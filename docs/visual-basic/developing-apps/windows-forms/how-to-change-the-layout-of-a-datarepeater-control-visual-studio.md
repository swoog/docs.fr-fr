---
title: 'Procédure : Modifier la disposition d’un contrôle DataRepeater (Visual Studio)'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, changing layout style
- DataRepeater, changing orientation
ms.assetid: 33aa8fd5-ac63-4bd0-ba13-8c2ab17e7824
ms.openlocfilehash: 3389daa6383444b48faab4c5383b281e44349bce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625599"
---
# <a name="how-to-change-the-layout-of-a-datarepeater-control-visual-studio"></a>Procédure : Modifier la disposition d’un contrôle DataRepeater (Visual Studio)
Le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle peut être affiché dans un (éléments défilement) à la verticale ou horizontale (éléments défilement) orientation. Vous pouvez modifier l’orientation au moment du design ou au moment de l’exécution en modifiant le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> propriété. Si vous modifiez le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> propriété au moment de l’exécution, peut également voulue pour redimensionner le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> et repositionner les contrôles enfants.  
  
> [!NOTE]
>  Si vous repositionnez des contrôles sur le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> en cours d’exécution, vous devez appeler la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A> et <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A> méthodes au début et à la fin du bloc de code qui repositionne les contrôles.  
  
### <a name="to-change-the-layout-at-design-time"></a>Pour modifier la disposition au moment du design  
  
1.  Dans le Concepteur Windows Forms, sélectionnez le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle.  
  
    > [!NOTE]
    >  Vous devez sélectionner la bordure externe de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle en cliquant dans la région inférieure du contrôle, pas dans le coin supérieur <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> région.  
  
2.  Dans la fenêtre Propriétés, définissez la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> propriété <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Vertical> ou <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal>.  
  
### <a name="to-change-the-layout-at-run-time"></a>Pour modifier la disposition au moment de l’exécution  
  
1.  Ajoutez le code suivant à un bouton ou menu `Click` Gestionnaire d’événements :  
  
     [!code-csharp[VbPowerPacksDataRepeaterLayout#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterLayout#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_1.vb)]  
  
2.  Dans la plupart des cas, vous devez ajouter du code similaire à celle illustrée dans la section exemple pour redimensionner le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> et réorganiser les contrôles pour s’ajuster à la nouvelle orientation.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment répondre à la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyleChanged> événement dans un gestionnaire d’événements. Cet exemple nécessite que vous avez un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle nommé `DataRepeater1` sur un formulaire et que son <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> contiennent deux <xref:System.Windows.Forms.TextBox> contrôles nommés `TextBox1` et `TextBox2`.  
  
 [!code-csharp[VbPowerPacksDataRepeaterLayout#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_2.cs)]
 [!code-vb[VbPowerPacksDataRepeaterLayout#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_2.vb)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A>
- [Introduction au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [Dépannage des problèmes liés au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [Guide pratique pour Modifier l’apparence d’un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
