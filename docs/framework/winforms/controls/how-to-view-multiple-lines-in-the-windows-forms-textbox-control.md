---
title: 'Procédure : Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- newline
- end of line
- ScrollBars property [Windows Forms], in TextBox control
- CRLF
- MultiLine property in TextBox control
- line-feed
- TextBox control [Windows Forms], viewing multiple lines
- carriage return
ms.assetid: 43173201-0b74-4067-a472-605029ca5f35
ms.openlocfilehash: d80a0262455b9b5e0e8535d88eb6292ab60e3ea8
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716008"
---
# <a name="how-to-view-multiple-lines-in-the-windows-forms-textbox-control"></a>Procédure : Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms
Par défaut, les formulaires Windows <xref:System.Windows.Forms.TextBox> contrôle affiche une seule ligne de texte et n’affiche pas de barres de défilement. Si le texte est supérieure à l’espace disponible, seule une partie du texte est visible. Vous pouvez modifier ce comportement par défaut en définissant le <xref:System.Windows.Forms.TextBox.Multiline%2A>, <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A>, et <xref:System.Windows.Forms.TextBox.ScrollBars%2A> valeurs appropriées aux propriétés.  
  
### <a name="to-display-a-carriage-return-in-the-textbox-control"></a>Pour afficher un retour chariot dans le contrôle de zone de texte  
  
-   Pour afficher un retour chariot dans une ligne multi <xref:System.Windows.Forms.TextBox>, utilisez le <xref:System.Environment.NewLine%2A> propriété.  
  
     N’oubliez pas que l’interprétation des caractères d’échappement (\\) est spécifique au langage. Visual Basic utilise `Chr$(13) & Chr$(10)` pour la combinaison de caractères de saut de ligne et de retour chariot.  
  
### <a name="to-view-multiple-lines-in-the-textbox-control"></a>Pour afficher plusieurs lignes dans le contrôle de zone de texte  
  
1.  Affectez à la propriété <xref:System.Windows.Forms.TextBox.Multiline%2A> la valeur `true`. Si <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> est `true` (la valeur par défaut), puis le texte dans le contrôle apparaîtra comme un ou plusieurs paragraphes ; sinon, il s’affiche sous forme de liste dans laquelle certaines lignes peuvent être tronquées à la périphérie du contrôle.  
  
2.  Affectez à la propriété <xref:System.Windows.Forms.TextBox.ScrollBars%2A> une valeur appropriée.  
  
    |Value|Description|  
    |-----------|-----------------|  
    |<xref:System.Windows.Forms.ScrollBars.None>|Utilisez cette valeur si le texte sera un paragraphe qui correspond presque toujours le contrôle. L’utilisateur peut utiliser le pointeur de la souris pour vous déplacer le contrôle si le texte est trop long à afficher à la fois.|  
    |<xref:System.Windows.Forms.ScrollBars.Horizontal>|Utilisez cette valeur si vous souhaitez afficher une liste de lignes, dont certaines peuvent être plus longue que la largeur de la <xref:System.Windows.Forms.TextBox> contrôle.|  
    |<xref:System.Windows.Forms.ScrollBars.Both>|Utilisez cette valeur si la liste peut être supérieure à la hauteur du contrôle.|  
  
3.  Affectez à la propriété <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> une valeur appropriée.  
  
    |Value|Description|  
    |-----------|-----------------|  
    |`false`|Texte dans le contrôle n’est pas automatiquement encapsulée, donc il défilera vers la droite jusqu'à ce qu’un saut de ligne est atteinte. Utilisez cette valeur si vous avez choisi <xref:System.Windows.Forms.ScrollBars.Horizontal> les barres de défilement ou <xref:System.Windows.Forms.ScrollBars.Both>, ci-dessus.|  
    |`true` (valeur par défaut)|La barre de défilement horizontale s’affiche pas. Utilisez cette valeur si vous avez choisi <xref:System.Windows.Forms.ScrollBars.Vertical> les barres de défilement ou <xref:System.Windows.Forms.ScrollBars.None>, ci-dessus, pour afficher un ou plusieurs paragraphes.|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.TextBox>
- [Vue d’ensemble du contrôle TextBox](textbox-control-overview-windows-forms.md)
- [Guide pratique pour Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [Guide pratique pour Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [Guide pratique pour Créer une zone de texte en lecture seule](how-to-create-a-read-only-text-box-windows-forms.md)
- [Guide pratique pour Placez des guillemets doubles dans une chaîne](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [Guide pratique pour Sélectionner du texte dans le contrôle de zone de texte Windows Forms](how-to-select-text-in-the-windows-forms-textbox-control.md)
- [TextBox, contrôle](textbox-control-windows-forms.md)
