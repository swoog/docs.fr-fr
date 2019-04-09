---
title: 'Procédure : afficher des barres de défilement dans le contrôle RichTextBox Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- text boxes [Windows Forms], displaying scroll bars
- scroll bars [Windows Forms], displaying in controls
- RichTextBox control [Windows Forms], displaying scroll bars
ms.assetid: cdeb42e1-86e8-410c-ba46-18aec264ef5f
ms.openlocfilehash: 52c33239524e76bc26b9b2375578aa46bff51bf6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59142556"
---
# <a name="how-to-display-scroll-bars-in-the-windows-forms-richtextbox-control"></a>Procédure : afficher des barres de défilement dans le contrôle RichTextBox Windows Forms
Par défaut, les formulaires Windows <xref:System.Windows.Forms.RichTextBox> contrôle affiche des barres de défilement horizontales et verticales en fonction des besoins. Il existe sept valeurs possibles pour le <xref:System.Windows.Forms.RichTextBox.ScrollBars%2A> propriété de la <xref:System.Windows.Forms.RichTextBox> contrôle, qui sont décrites dans le tableau ci-dessous.  
  
### <a name="to-display-scroll-bars-in-a-richtextbox-control"></a>Pour afficher les barres de défilement dans un contrôle RichTextBox  
  
1.  Affectez à la propriété <xref:System.Windows.Forms.RichTextBox.Multiline%2A> la valeur `true`. Aucun type de barre de défilement, y compris horizontal, n’affiche si le <xref:System.Windows.Forms.RichTextBox.Multiline%2A> propriété est définie sur `false`.  
  
2.  Définir le <xref:System.Windows.Forms.RichTextBox.ScrollBars%2A> propriété une valeur appropriée de la <xref:System.Windows.Forms.RichTextBoxScrollBars> énumération.  
  
    |Value|Description|  
    |-----------|-----------------|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.Both> (valeur par défaut)|Affiche des barres de défilement horizontale ou verticale, ou les deux, uniquement lorsque le texte dépasse la largeur ou la longueur du contrôle.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.None>|N’affiche jamais de n’importe quel type de barre de défilement.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.Horizontal>|Affiche une barre uniquement lorsque le texte dépasse la largeur du contrôle de défilement horizontale. (Dans ce cas, le <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> propriété doit être définie sur `false`.)|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.Vertical>|Affiche une barre uniquement lorsque le texte dépasse la hauteur du contrôle de défilement verticale.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.ForcedHorizontal>|Affiche un défilement horizontal de la barre lorsque le <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> propriété est définie sur `false`. La barre de défilement apparaît grisée lorsque le texte ne dépasse pas la largeur du contrôle.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.ForcedVertical>|Affiche toujours une barre de défilement verticale. La barre de défilement apparaît grisée lorsque le texte ne dépasse pas la longueur du contrôle.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.ForcedBoth>|Affiche toujours une barre de défilement verticale. Affiche un défilement horizontal de la barre lorsque le <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> propriété est définie sur `false`. Les barres de défilement sont estompées lorsque le texte ne dépasse pas la largeur ou la longueur du contrôle.|  
  
3.  Affectez à la propriété <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> une valeur appropriée.  
  
    |Value|Description|  
    |-----------|-----------------|  
    |`false`|Texte dans le contrôle n’est pas ajustée automatiquement pour s’ajuster à la largeur du contrôle, donc il défilera vers la droite jusqu'à ce qu’un saut de ligne est atteinte. Utilisez cette valeur si vous avez choisi les barres de défilement horizontale ou les deux, ci-dessus.|  
    |`true` (valeur par défaut)|Texte dans le contrôle est automatiquement ajustée pour s’ajuster à la largeur du contrôle. La barre de défilement horizontale s’affiche pas. Utilisez cette valeur si vous avez choisi les barres de défilement vertical ou none, ci-dessus, pour afficher un ou plusieurs paragraphes.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.RichTextBoxScrollBars>
- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox, contrôle](richtextbox-control-windows-forms.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
