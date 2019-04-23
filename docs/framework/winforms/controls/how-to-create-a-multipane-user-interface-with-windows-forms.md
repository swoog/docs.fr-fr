---
title: 'Procédure : créer une interface utilisateur à plusieurs volets avec Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SplitContainer control [Windows Forms], examples
- ListView control [Windows Forms], examples
- RichTextBox control [Windows Forms], examples
- Panel control [Windows Forms], examples
- TreeView control [Windows Forms], examples
- Splitter control [Windows Forms], examples
ms.assetid: e79f6bcc-3740-4d1e-b46a-c5594d9b7327
ms.openlocfilehash: 8650ba3b8011e50779080e31d94727609f2d08f1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59315152"
---
# <a name="how-to-create-a-multipane-user-interface-with-windows-forms"></a>Procédure : créer une interface utilisateur à plusieurs volets avec Windows Forms
Dans la procédure suivante, vous allez créer une interface utilisateur à plusieurs volets semblable à celle utilisée dans Microsoft Outlook, avec un **dossier** liste, un **Messages** volet et un **aperçu** volet. Cette disposition est obtenue principalement en ancrant les contrôles dans le formulaire.  
  
 Lorsque vous ancrez un contrôle, vous déterminez le bord du conteneur parent auquel un contrôle est attaché. Par conséquent, si vous définissez la <xref:System.Windows.Forms.SplitContainer.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Right>, le bord droit du contrôle sera ancré sur le bord droit de son contrôle parent. En outre, le bord du contrôle ancré est redimensionné pour correspondre à celle de son contrôle conteneur. Pour plus d’informations sur la façon dont <xref:System.Windows.Forms.SplitContainer.Dock%2A> fonctionne de la propriété, consultez [Comment : Ancrer des contrôles aux Windows Forms](how-to-dock-controls-on-windows-forms.md).  
  
 Cette procédure se concentre sur la disposition du <xref:System.Windows.Forms.SplitContainer> et d’autres contrôles sur le formulaire, et non sur l’ajout de fonctionnalités pour que l’application ressemble à Microsoft Outlook.  
  
 Pour créer cette interface utilisateur, vous placez tous les contrôles dans un <xref:System.Windows.Forms.SplitContainer> contrôle, qui contient un <xref:System.Windows.Forms.TreeView> contrôle dans le volet gauche. Le volet de droite de la <xref:System.Windows.Forms.SplitContainer> contrôle contient une seconde <xref:System.Windows.Forms.SplitContainer> contrôler avec un <xref:System.Windows.Forms.ListView> contrôle ci-dessus un <xref:System.Windows.Forms.RichTextBox> contrôle. Ces <xref:System.Windows.Forms.SplitContainer> les contrôles permettent un redimensionnement indépendant des autres contrôles sur le formulaire. Vous pouvez adapter les techniques de cette procédure pour les interfaces utilisateur personnalisées de métier de votre choix.  
  
### <a name="to-create-an-outlook-style-user-interface-programmatically"></a>Pour créer une interface utilisateur de type Outlook par programmation  
  
1. Dans un formulaire, déclarez chaque contrôle constituant votre interface utilisateur. Pour cet exemple, utilisez le <xref:System.Windows.Forms.TreeView>, <xref:System.Windows.Forms.ListView>, <xref:System.Windows.Forms.SplitContainer>, et <xref:System.Windows.Forms.RichTextBox> contrôles pour reproduire l’interface utilisateur de Microsoft Outlook.  
  
    ```vb  
    Private WithEvents treeView1 As System.Windows.Forms.TreeView  
    Private WithEvents listView1 As System.Windows.Forms.ListView  
    Private WithEvents richTextBox1 As System.Windows.Forms.RichTextBox  
    Private WithEvents splitContainer1 As _  
        System.Windows.Forms.SplitContainer  
    Private WithEvents splitContainer2 As _  
        System.Windows.Forms.SplitContainer  
    ```  
  
    ```csharp  
    private System.Windows.Forms.TreeView treeView1;  
    private System.Windows.Forms.ListView listView1;  
    private System.Windows.Forms.RichTextBox richTextBox1;  
    private System.Windows.Forms. SplitContainer splitContainer2;  
    private System.Windows.Forms. SplitContainer splitContainer1;  
    ```  
  
2. Créer une procédure qui définit votre interface utilisateur. Le code suivant définit les propriétés afin que le formulaire ressemble à l’interface utilisateur dans Microsoft Outlook. Toutefois, à l’aide d’autres contrôles ou les ancrant différemment, il est tout aussi facile de créer d’autres interfaces utilisateur qui sont tout aussi souples.  
  
    ```vb  
    Public Sub CreateOutlookUI()  
        ' Create an instance of each control being used.  
        Me.components = New System.ComponentModel.Container()  
        Me.treeView1 = New System.Windows.Forms.TreeView()  
        Me.listView1 = New System.Windows.Forms.ListView()  
        Me.richTextBox1 = New System.Windows.Forms.RichTextBox()  
        Me.splitContainer1 = New System.Windows.Forms.SplitContainer()  
        Me.splitContainer2= New System.Windows.Forms. SplitContainer()  
  
        ' Should you develop this into a working application,  
        ' use the AddHandler method to hook up event procedures here.  
  
        ' Set properties of TreeView control.  
        ' Use the With statement to avoid repetitive code.  
        With Me.treeView1  
            .Dock = System.Windows.Forms.DockStyle.Fill  
            .TabIndex = 0  
            .Nodes.Add("treeView")  
        End With  
  
    ' Set properties of ListView control.  
       With Me.listView1  
          .Dock = System.Windows.Forms.DockStyle.Top  
          .TabIndex = 2  
          .Items.Add("listView")  
       End With  
  
    ' Set properties of RichTextBox control.  
       With Me.richTextBox1  
          .Dock = System.Windows.Forms.DockStyle.Fill  
          .TabIndex = 3  
          .Text = "richTextBox1"  
       End With  
  
        ' Set properties of the first SplitContainer control.  
        With Me.splitContainer1  
            .Dock = System.Windows.Forms.DockStyle.Fill  
            .TabIndex = 1  
            .SplitterWidth = 4  
            .SplitterDistance = 150  
            .Orientation = Orientation.Horizontal  
            .Panel1.Controls.Add(Me.listView1)  
            .Panel2.Controls.Add(Me.richTextBox1)  
    End With  
  
        ' Set properties of the second SplitContainer control.  
        With Me.splitContainer2  
            .Dock = System.Windows.Forms.DockStyle.Fill  
            .TabIndex = 4  
            .SplitterWidth = 4  
            .SplitterDistance = 100  
            .Panel1.Controls.Add(Me.treeView1)  
            .Panel2.Controls.Add(Me.SplitContainer1)  
    End With  
  
    ' Add the main SplitContainer control to the form.  
        Me.Controls.Add(Me.splitContainer2)  
        Me.Text = "Intricate UI Example"  
    End Sub  
    ```  
  
    ```csharp  
    public void createOutlookUI()  
    {  
        // Create an instance of each control being used.  
        treeView1 = new System.Windows.Forms.TreeView();  
        listView1 = new System.Windows.Forms.ListView();  
        richTextBox1 = new System.Windows.Forms.RichTextBox();  
        splitContainer2 = new System.Windows.Forms.SplitContainer();  
        splitContainer1 = new System.Windows.Forms.SplitContainer();  
  
        // Insert code here to hook up event methods.  
  
        // Set properties of TreeView control.  
        treeView1.Dock = System.Windows.Forms.DockStyle.Fill;  
        treeView1.TabIndex = 0;  
        treeView1.Nodes.Add("treeView");  
  
        // Set properties of ListView control.  
        listView1.Dock = System.Windows.Forms.DockStyle.Top;  
        listView1.TabIndex = 2;  
        listView1.Items.Add("listView");  
  
        // Set properties of RichTextBox control.  
        richTextBox1.Dock = System.Windows.Forms.DockStyle.Fill;  
        richTextBox1.TabIndex = 3;  
        richTextBox1.Text = "richTextBox1";  
  
        // Set properties of first SplitContainer control.  
        splitContainer1.Dock = System.Windows.Forms.DockStyle.Fill;  
        splitContainer2.TabIndex = 1;  
        splitContainer2.SplitterWidth = 4;  
        splitContainer2.SplitterDistance = 150;  
        splitContainer2.Orientation = Orientation.Horizontal;  
        splitContainer2.Panel1.Controls.Add(this.listView1);  
        splitContainer2.Panel1.Controls.Add(this.richTextBox1);  
  
        // Set properties of second SplitContainer control.  
        splitContainer2.Dock = System.Windows.Forms.DockStyle.Fill;  
        splitContainer2.TabIndex = 4;  
        splitContainer2.SplitterWidth = 4;  
        splitContainer2.SplitterDistance = 100;  
        splitContainer2.Panel1.Controls.Add(this.treeView1);  
        splitContainer2.Panel1.Controls.Add(this.splitContainer1);  
  
        // Add the main SplitContainer control to the form.  
        this.Controls.Add(this.splitContainer2);  
        this.Text = "Intricate UI Example";  
    }  
    ```  
  
3. Dans Visual Basic, ajoutez un appel à la procédure que vous venez de créer dans le `New()` procédure. Dans Visual C#, ajoutez cette ligne de code au constructeur pour la classe de formulaire.  
  
    ```vb  
    ' Add this to the New procedure.  
    CreateOutlookUI()  
    ```  
  
    ```csharp  
    // Add this to the form class's constructor.  
    createOutlookUI();  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.SplitContainer>
- [SplitContainer, contrôle](splitcontainer-control-windows-forms.md)
- [Guide pratique pour Créer une Interface utilisateur à plusieurs volets avec des formulaires Windows à l’aide du Concepteur](create-a-multipane-user-interface-with-wf-using-the-designer.md)
