---
title: 'Procédure : Définir les retraits, les retraits négatifs et des paragraphes à puces avec le contrôle RichTextBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- text boxes [Windows Forms], setting indents
- .rtf files [Windows Forms], formatting in RichTextBox control
- examples [Windows Forms], text boxes
- RTF files [Windows Forms], formatting in RichTextBox control
- RichTextBox control [Windows Forms], setting indents and bullets
- text boxes [Windows Forms], bullets
ms.assetid: abfb40e6-5642-4691-8ec1-9d9ae91688dc
ms.openlocfilehash: b2173769634ddc4b7b42c822c3f60212eb8d8886
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57713027"
---
# <a name="how-to-set-indents-hanging-indents-and-bulleted-paragraphs-with-the-windows-forms-richtextbox-control"></a>Procédure : Définir les retraits, les retraits négatifs et des paragraphes à puces avec le contrôle RichTextBox Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.RichTextBox> contrôle a de nombreuses options pour mettre en forme le texte affiché. Vous pouvez mettre en forme des paragraphes sélectionnés sous forme de listes à puces en définissant le <xref:System.Windows.Forms.RichTextBox.SelectionBullet%2A> propriété. Vous pouvez également utiliser le <xref:System.Windows.Forms.RichTextBox.SelectionIndent%2A>, <xref:System.Windows.Forms.RichTextBox.SelectionRightIndent%2A>, et <xref:System.Windows.Forms.RichTextBox.SelectionHangingIndent%2A> propriétés à définir la mise en retrait des paragraphes par rapport à gauche et les bords droit du contrôle et le bord gauche des autres lignes de texte.  
  
### <a name="to-format-a-paragraph-as-a-bulleted-list"></a>Pour mettre en forme un paragraphe sous forme de liste à puces  
  
1.  Affectez à la propriété <xref:System.Windows.Forms.RichTextBox.SelectionBullet%2A> la valeur `true`.  
  
    ```vb  
    RichTextBox1.SelectionBullet = True  
    ```  
  
    ```csharp  
    richTextBox1.SelectionBullet = true;  
    ```  
  
    ```cpp  
    richTextBox1->SelectionBullet = true;  
    ```  
  
### <a name="to-indent-a-paragraph"></a>Pour mettre en retrait un paragraphe  
  
1.  Définir le <xref:System.Windows.Forms.RichTextBox.SelectionIndent%2A> propriété vers un entier représentant la distance en pixels entre le bord gauche du contrôle et le bord gauche du texte.  
  
2.  Définir le <xref:System.Windows.Forms.RichTextBox.SelectionHangingIndent%2A> propriété vers un entier représentant la distance en pixels entre le bord gauche de la première ligne de texte dans le paragraphe et le bord gauche des lignes suivantes du même paragraphe. La valeur de la <xref:System.Windows.Forms.RichTextBox.SelectionHangingIndent%2A> propriété s’applique uniquement aux lignes d’un paragraphe qui ont été renvoyées sous la première ligne.  
  
3.  Définir le <xref:System.Windows.Forms.RichTextBox.SelectionRightIndent%2A> propriété vers un entier représentant la distance en pixels entre le bord droit du contrôle et le bord droit du texte.  
  
    ```vb  
    RichTextBox1.SelectionIndent = 8  
    RichTextBox1.SelectionHangingIndent = 3  
    RichTextBox1.SelectionRightIndent = 12  
    ```  
  
    ```csharp  
    richTextBox1.SelectionIndent = 8;  
    richTextBox1.SelectionHangingIndent = 3;  
    richTextBox1.SelectionRightIndent = 12;  
    ```  
  
    ```cpp  
    richTextBox1->SelectionIndent = 8;  
    richTextBox1->SelectionHangingIndent = 3;  
    richTextBox1->SelectionRightIndent = 12;  
    ```  
  
    > [!NOTE]
    >  Toutes ces propriétés affectent tous les paragraphes contenant du texte sélectionné et également le texte tapé après le point d’insertion actif. Par exemple, quand un utilisateur sélectionne un mot dans un paragraphe puis ajuste le retrait, les nouveaux paramètres s’appliquent à l’ensemble du paragraphe contenant ce mot et également à tous les paragraphes entrés ultérieurement après le paragraphe sélectionné. Pour plus d’informations sur la sélection de texte par programmation, consultez <xref:System.Windows.Forms.TextBoxBase.Select%2A>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox, contrôle](richtextbox-control-windows-forms.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
