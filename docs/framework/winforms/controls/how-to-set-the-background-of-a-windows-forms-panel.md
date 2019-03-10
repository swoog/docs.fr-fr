---
title: 'Procédure : Définir l’arrière-plan d’un contrôle Panel Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- background colors [Windows Forms], Windows Forms Panel controls
- background images [Windows Forms], Windows Forms Panel controls
- Panel control [Windows Forms], background
- colors [Windows Forms], Windows Forms Panel controls
ms.assetid: 096cbd8d-45cc-47b8-b1ef-a27f60ea8be0
ms.openlocfilehash: b0cf7666e6d969b3d02d13e86eb45904307d3ce3
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57722683"
---
# <a name="how-to-set-the-background-of-a-windows-forms-panel"></a>Procédure : Définir l’arrière-plan d’un contrôle Panel Windows Forms
Un formulaire Windows <xref:System.Windows.Forms.Panel> contrôle peut afficher une couleur d’arrière-plan et une image d’arrière-plan. Le <xref:System.Windows.Forms.Control.BackColor%2A> propriété définit la couleur d’arrière-plan pour les contrôles de relation contenant-contenus, tels que des étiquettes et des cases d’option. Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété n’est pas définie, la <xref:System.Windows.Forms.Control.BackColor%2A> sélection remplira du panneau tout entier. Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété est définie, l’image est affichée derrière les contrôles contenus.  
  
### <a name="to-set-the-background-programmatically"></a>Pour définir l’arrière-plan par programmation  
  
1.  Définir le panneau <xref:System.Windows.Forms.Control.BackColor%2A> propriété une valeur de type <xref:System.Drawing.Color?displayProperty=nameWithType>.  
  
    ```vb  
    Panel1.BackColor = Color.AliceBlue  
    ```  
  
    ```csharp  
    panel1.BackColor = Color.AliceBlue;  
    ```  
  
    ```cpp  
    panel1->BackColor = Color::AliceBlue;  
    ```  
  
2.  Définir le panneau <xref:System.Windows.Forms.Control.BackgroundImage%2A> à l’aide de la propriété le <xref:System.Drawing.Image.FromFile%2A> méthode de la <xref:System.Drawing.Image?displayProperty=nameWithType> classe.  
  
    ```vb  
    ' You should replace the bolded image   
    ' in the sample below with an image of your own choosing.  
    Panel1.BackgroundImage = Image.FromFile _  
        (System.Environment.GetFolderPath _  
        (System.Environment.SpecialFolder.Personal) _  
        & "\Image.gif")  
    ```  
  
    ```csharp  
    // You should replace the bolded image   
    // in the sample below with an image of your own choosing.  
    // Note the escape character used (@) when specifying the path.  
    panel1.BackgroundImage = Image.FromFile  
       (System.Environment.GetFolderPath  
       (System.Environment.SpecialFolder.Personal)  
       + @"\Image.gif");  
    ```  
  
    ```cpp  
    // You should replace the bolded image   
    // in the sample below with an image of your own choosing.  
    panel1->BackgroundImage = Image::FromFile(String::Concat(  
       System::Environment::GetFolderPath  
       (System::Environment::SpecialFolder::Personal),  
       "\\Image.gif"));  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Control.BackColor%2A>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
- [Panel, contrôle](panel-control-windows-forms.md)
- [Vue d’ensemble du contrôle Panel](panel-control-overview-windows-forms.md)
