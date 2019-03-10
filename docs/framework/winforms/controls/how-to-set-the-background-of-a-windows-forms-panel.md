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
# <a name="how-to-set-the-background-of-a-windows-forms-panel"></a><span data-ttu-id="a0bd2-102">Procédure : Définir l’arrière-plan d’un contrôle Panel Windows Forms</span><span class="sxs-lookup"><span data-stu-id="a0bd2-102">How to: Set the Background of a Windows Forms Panel</span></span>
<span data-ttu-id="a0bd2-103">Un formulaire Windows <xref:System.Windows.Forms.Panel> contrôle peut afficher une couleur d’arrière-plan et une image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-103">A Windows Forms <xref:System.Windows.Forms.Panel> control can display both a background color and a background image.</span></span> <span data-ttu-id="a0bd2-104">Le <xref:System.Windows.Forms.Control.BackColor%2A> propriété définit la couleur d’arrière-plan pour les contrôles de relation contenant-contenus, tels que des étiquettes et des cases d’option.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-104">The <xref:System.Windows.Forms.Control.BackColor%2A> property sets the background color for the contained controls, such as labels and radio buttons.</span></span> <span data-ttu-id="a0bd2-105">Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété n’est pas définie, la <xref:System.Windows.Forms.Control.BackColor%2A> sélection remplira du panneau tout entier.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-105">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is not set, the <xref:System.Windows.Forms.Control.BackColor%2A> selection will fill the entire panel.</span></span> <span data-ttu-id="a0bd2-106">Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété est définie, l’image est affichée derrière les contrôles contenus.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-106">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is set, the image will be displayed behind the contained controls.</span></span>  
  
### <a name="to-set-the-background-programmatically"></a><span data-ttu-id="a0bd2-107">Pour définir l’arrière-plan par programmation</span><span class="sxs-lookup"><span data-stu-id="a0bd2-107">To set the background programmatically</span></span>  
  
1.  <span data-ttu-id="a0bd2-108">Définir le panneau <xref:System.Windows.Forms.Control.BackColor%2A> propriété une valeur de type <xref:System.Drawing.Color?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-108">Set the panel's <xref:System.Windows.Forms.Control.BackColor%2A> property to a value of type <xref:System.Drawing.Color?displayProperty=nameWithType>.</span></span>  
  
    ```vb  
    Panel1.BackColor = Color.AliceBlue  
    ```  
  
    ```csharp  
    panel1.BackColor = Color.AliceBlue;  
    ```  
  
    ```cpp  
    panel1->BackColor = Color::AliceBlue;  
    ```  
  
2.  <span data-ttu-id="a0bd2-109">Définir le panneau <xref:System.Windows.Forms.Control.BackgroundImage%2A> à l’aide de la propriété le <xref:System.Drawing.Image.FromFile%2A> méthode de la <xref:System.Drawing.Image?displayProperty=nameWithType> classe.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-109">Set the panel's <xref:System.Windows.Forms.Control.BackgroundImage%2A> property using the <xref:System.Drawing.Image.FromFile%2A> method of the <xref:System.Drawing.Image?displayProperty=nameWithType> class.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="a0bd2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0bd2-110">See also</span></span>
- <xref:System.Windows.Forms.Control.BackColor%2A>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
- [<span data-ttu-id="a0bd2-111">Panel, contrôle</span><span class="sxs-lookup"><span data-stu-id="a0bd2-111">Panel Control</span></span>](panel-control-windows-forms.md)
- [<span data-ttu-id="a0bd2-112">Vue d’ensemble du contrôle Panel</span><span class="sxs-lookup"><span data-stu-id="a0bd2-112">Panel Control Overview</span></span>](panel-control-overview-windows-forms.md)
