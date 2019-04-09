---
title: Vue d'ensemble du contrôle RichTextBox (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- RichTextBox
helpviewer_keywords:
- RichTextBox control [Windows Forms], about RichTextBox control
- text boxes [Windows Forms], about text boxes
ms.assetid: 95081194-3dd4-4b84-9545-dd373e491eca
ms.openlocfilehash: 0827c1919597e9eb85bfa41721676008b76564d9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59201596"
---
# <a name="richtextbox-control-overview-windows-forms"></a>Vue d'ensemble du contrôle RichTextBox (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.RichTextBox> contrôle est utilisé pour l’affichage, la saisie et la manipulation de texte avec mise en forme. Le <xref:System.Windows.Forms.RichTextBox> contrôle fait tout le <xref:System.Windows.Forms.TextBox> effectue, mais il peut également afficher des polices, couleurs et des liens ; charger du texte et des images incorporées à partir d’un fichier ; et rechercher des caractères spécifiés. Le <xref:System.Windows.Forms.RichTextBox> contrôle est généralement utilisé pour fournir de manipulation de texte et d’affichage des fonctionnalités similaires aux applications de traitement de texte tel que Microsoft Word. Comme le <xref:System.Windows.Forms.TextBox> contrôle, le <xref:System.Windows.Forms.RichTextBox> contrôle peut afficher des barres de défilement ; mais contrairement à la <xref:System.Windows.Forms.TextBox> contrôle, sa valeur par défaut est d’afficher les barres de défilement horizontales et verticales en fonction des besoins, et il comporte des paramètres de barre de défilement supplémentaires.  
  
## <a name="working-with-the-richtextbox-control"></a>Utilisation du contrôle RichTextBox  
 Comme avec la <xref:System.Windows.Forms.TextBox> contrôle, le texte affiché est défini le <xref:System.Windows.Forms.RichTextBox.Text%2A> propriété. Le <xref:System.Windows.Forms.RichTextBox> contrôle possède de nombreuses propriétés en forme du texte. Pour plus d’informations sur ces propriétés, consultez [Comment : Définir les attributs de police pour les Windows Forms contrôle RichTextBox](how-to-set-font-attributes-for-the-windows-forms-richtextbox-control.md) et [Comment : Définir les retraits, les retraits négatifs et des paragraphes à puces avec le contrôle RichTextBox Windows Forms](set-indents-hanging-indents-bulleted-paragraphs-with-wf-richtextbox.md). Pour manipuler les fichiers, le <xref:System.Windows.Forms.RichTextBox.LoadFile%2A> et <xref:System.Windows.Forms.RichTextBox.SaveFile%2A> méthodes peuvent afficher et écrire plusieurs formats de fichiers, y compris le texte brut, texte brut Unicode et Format RTF (Rich Text Format). Formats de fichier sont répertoriés dans <xref:System.Windows.Forms.RichTextBoxStreamType>. Vous pouvez utiliser la <xref:System.Windows.Forms.RichTextBox.Find%2A> méthode pour rechercher des chaînes de texte ou des caractères spécifiques.  
  
 Vous pouvez également utiliser un <xref:System.Windows.Forms.RichTextBox> contrôle pour obtenir des liens de style Web en définissant le <xref:System.Windows.Forms.RichTextBox.DetectUrls%2A> propriété `true` et l’écriture de code pour gérer le <xref:System.Windows.Forms.RichTextBox.LinkClicked> événement. Pour plus d'informations, voir [Procédure : Afficher des liens de Style Web avec les Windows Forms contrôle RichTextBox](how-to-display-web-style-links-with-the-windows-forms-richtextbox-control.md). Vous pouvez empêcher l’utilisateur de manipuler tout ou partie du texte dans le contrôle en définissant le <xref:System.Windows.Forms.RichTextBox.SelectionProtected%2A> propriété `true`.  
  
 Vous pouvez annuler et rétablir la plupart des opérations d’édition dans un <xref:System.Windows.Forms.RichTextBox> contrôle en appelant le <xref:System.Windows.Forms.TextBoxBase.Undo%2A> et <xref:System.Windows.Forms.RichTextBox.Redo%2A> méthodes. Le <xref:System.Windows.Forms.RichTextBox.CanRedo%2A> méthode vous permet de déterminer si la dernière opération annulée par l’utilisateur peut être réappliquée au contrôle.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox, contrôle](richtextbox-control-windows-forms.md)
- [Vue d’ensemble du contrôle TextBox](textbox-control-overview-windows-forms.md)
