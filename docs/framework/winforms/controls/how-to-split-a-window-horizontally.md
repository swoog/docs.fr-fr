---
title: 'Procédure : fractionner une fenêtre horizontalement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SplitContainer control [Windows Forms], horizontal splitter
- splitter windows [Windows Forms], changing splitter orientation
- splitter windows [Windows Forms], horizontal
- windows [Windows Forms], splitting horizontally
ms.assetid: a1f74f29-048c-4723-85fa-b9d375ab8f4b
ms.openlocfilehash: d10616e2f09eabec1209a26aabe501ea0af903cb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59189629"
---
# <a name="how-to-split-a-window-horizontally"></a>Procédure : fractionner une fenêtre horizontalement
L’exemple de code suivant effectue le séparateur qui divise le <xref:System.Windows.Forms.SplitContainer> horizontal du contrôle.  
  
> [!NOTE]
>  Le <xref:System.Windows.Forms.SplitContainer.Orientation%2A> propriété de la <xref:System.Windows.Forms.SplitContainer> contrôle détermine la direction du séparateur et non du contrôle lui-même.  
  
### <a name="to-split-a-window-horizontally"></a>Pour fractionner une fenêtre horizontalement  
  
1.  Dans une procédure, affectez la <xref:System.Windows.Forms.SplitContainer.Orientation%2A> propriété de la <xref:System.Windows.Forms.SplitContainer> le contrôle à <xref:System.Windows.Forms.Orientation.Horizontal>.  
  
    ```vb  
    Sub ShowSplitContainer()  
        Dim splitContainer1 as new SplitContainer()  
        splitContainer1.BorderStyle = BorderStyle.Fixed3D  
        splitContainer1.Location = New System.Drawing.Point(74, 20)  
        splitContainer1.Name = "DemoSplitContainer"  
        splitContainer1.Size = New System.Drawing.Size(212, 435)  
        splitContainer1.TabIndex = 0  
        splitContainer1.Orientation = Orientation.Horizontal  
        Controls.Add(splitContainer1)  
    End Sub  
    ```  
  
    ```csharp  
    public void showSplitContainer()  
    {  
        SplitContainer splitContainer1 = new SplitContainer ();  
        splitContainer1.BorderStyle = BorderStyle.Fixed3D;  
        splitContainer1.Location = new System.Drawing.Point (74, 20);  
        splitContainer1.Name = "DemoSplitContainer";  
        splitContainer1.Size = new System.Drawing.Size (212, 435);  
        splitContainer1.TabIndex = 0;  
        splitContainer1.Orientation = Orientation.Horizontal;  
        this.Controls.Add (splitContainer1);  
  
    }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.SplitContainer>
- [SplitContainer, contrôle](splitcontainer-control-windows-forms.md)
