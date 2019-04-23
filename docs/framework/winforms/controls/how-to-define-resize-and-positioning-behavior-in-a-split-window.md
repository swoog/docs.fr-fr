---
title: 'Procédure : définir le comportement de redimensionnement et de positionnement dans une fenêtre fractionnée'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- split windows [Windows Forms], resizing
- splitter windows [Windows Forms], resizing
- SplitContainer control [Windows Forms], resizing
ms.assetid: 9bf73f36-ed2d-4a02-b15a-0770eff4fdfa
ms.openlocfilehash: 8cdcfdfaa135a92ed6a6e96d4a72de2c97f2493d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59328671"
---
# <a name="how-to-define-resize-and-positioning-behavior-in-a-split-window"></a>Procédure : définir le comportement de redimensionnement et de positionnement dans une fenêtre fractionnée
Les panneaux de la <xref:System.Windows.Forms.SplitContainer> contrôle se prêtent bien au redimensionnement et manipulées par les utilisateurs. Toutefois, il peut arriver lorsque vous souhaitez contrôler par programme le séparateur, où il est positionné, et dans quelle mesure il peut être déplacé.  
  
 Le <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> propriété et les autres propriétés sur le <xref:System.Windows.Forms.SplitContainer> contrôle vous donnent un contrôle précis sur le comportement de votre interface utilisateur selon vos besoins. Ces propriétés sont répertoriées dans le tableau suivant.  
  
|Nom|Description|  
|----------|-----------------|  
|Propriété <xref:System.Windows.Forms.SplitContainer.IsSplitterFixed%2A>|Détermine si le séparateur est mobile au moyen du clavier ou la souris.|  
|Propriété <xref:System.Windows.Forms.SplitContainer.SplitterDistance%2A>|Détermine la distance en pixels en partant du bord gauche ou supérieur à la barre de fractionnement mobile.|  
|Propriété <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A>|Détermine la distance minimale, en pixels, que le séparateur peut être déplacé par l’utilisateur.|  
  
 L’exemple suivant modifie le <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> propriété pour créer un effet « séparateur d’alignement » ; lorsque l’utilisateur fait glisser le séparateur, il incrémente en unités de 10 pixels plutôt que la valeur par défaut 1.  
  
### <a name="to-define-splitcontainer-resize-behavior"></a>Pour définir le comportement de redimensionnement SplitContainer  
  
1. Dans une procédure, définissez le <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> propriété à la taille souhaitée, afin que le comportement « alignement » du séparateur s’exécute.  
  
     Dans l’exemple de code suivant, dans le formulaire <xref:System.Windows.Forms.Form.Load> événement, le séparateur dans le <xref:System.Windows.Forms.SplitContainer> contrôle est défini sur le saut de 10 pixels lorsque vous faites glisser.  
  
    ```vb  
    Private Sub Form1_Load(ByVal sender As System.Object, _  
        ByVal e As System.EventArgs) Handles MyBase.Load  
        Dim splitSnapper as new SplitContainer()  
        splitSnapper.SplitterIncrement = 10  
        splitSnapper.Dock = DockStyle.Fill  
        splitSnapper.Parent = me  
    End Sub  
    ```  
  
    ```csharp  
    private void Form1_Load(System.Object sender, System.EventArgs e)  
    {  
        SplitContainer splitSnapper = new SplitContainer();  
        splitSnapper.SplitterIncrement = 10;  
        splitSnapper.Dock = DockStyle.Fill;  
        splitSnapper.Parent = this;  
    }  
    ```  
  
     (Visual C#) Placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.  
  
    ```csharp  
    this.Load += new System.EventHandler(this.Form1_Load);  
    ```  
  
     Déplacer le séparateur légèrement vers la gauche ou droite n’a aucun effet apparent ; Toutefois, lorsque le pointeur de la souris va 10 pixels dans les deux sens, le séparateur s’aligne à la nouvelle position.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.SplitContainer>
- <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A>
