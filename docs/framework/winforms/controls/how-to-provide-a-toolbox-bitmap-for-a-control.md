---
title: 'Procédure : Fournir une Bitmap de boîte à outils pour un contrôle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Toolbox [Windows Forms], adding bitmaps for custom controls
- custom controls [Windows Forms], Toolbox bitmaps
- bitmaps [Windows Forms], custom controls
ms.assetid: 0ed0840a-616d-41ba-a27d-3573241932ad
ms.openlocfilehash: 9072f96bd6e3485e759ed72819229b3f0c33d641
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57715956"
---
# <a name="how-to-provide-a-toolbox-bitmap-for-a-control"></a><span data-ttu-id="de1b0-102">Procédure : Fournir une Bitmap de boîte à outils pour un contrôle</span><span class="sxs-lookup"><span data-stu-id="de1b0-102">How to: Provide a Toolbox Bitmap for a Control</span></span>
<span data-ttu-id="de1b0-103">Si vous souhaitez avoir une icône spéciale pour votre contrôle s’affichent dans le **boîte à outils**, vous pouvez spécifier une image particulière en utilisant le <xref:System.Drawing.ToolboxBitmapAttribute>.</span><span class="sxs-lookup"><span data-stu-id="de1b0-103">If you want to have a special icon for your control appear in the **Toolbox**, you can specify a particular image by using the <xref:System.Drawing.ToolboxBitmapAttribute>.</span></span> <span data-ttu-id="de1b0-104">Cette classe est un *attribut*, c’est-à-dire un type spécial de classe que vous pouvez joindre à d’autres classes.</span><span class="sxs-lookup"><span data-stu-id="de1b0-104">This class is an *attribute*, a special kind of class you can attach to other classes.</span></span> <span data-ttu-id="de1b0-105">Pour plus d’informations sur les attributs, consultez [vue d’ensemble des attributs (Visual Basic)](../../../visual-basic/programming-guide/concepts/attributes/index.md) pour Visual Basic ou [attributs (c#)](../../../csharp/programming-guide/concepts/attributes/index.md) pour c#.</span><span class="sxs-lookup"><span data-stu-id="de1b0-105">For more information about attributes, see [Attributes overview (Visual Basic)](../../../visual-basic/programming-guide/concepts/attributes/index.md) for Visual Basic or [Attributes (C#)](../../../csharp/programming-guide/concepts/attributes/index.md) for C#.</span></span>  
  
 <span data-ttu-id="de1b0-106">À l’aide de la <xref:System.Drawing.ToolboxBitmapAttribute>, vous pouvez spécifier une chaîne qui indique le chemin d’accès et le nom d’un bitmap de 16 par 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="de1b0-106">Using the <xref:System.Drawing.ToolboxBitmapAttribute>, you can specify a string that indicates the path and file name for a 16 by 16 pixel bitmap.</span></span> <span data-ttu-id="de1b0-107">Cette image bitmap apparaît alors en regard de votre contrôle lorsqu’elle est ajoutée à la **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="de1b0-107">This bitmap then appears next to your control when added to the **Toolbox**.</span></span> <span data-ttu-id="de1b0-108">Vous pouvez également spécifier un <xref:System.Type>, auquel cas l’image bitmap associée à ce type est chargé.</span><span class="sxs-lookup"><span data-stu-id="de1b0-108">You can also specify a <xref:System.Type>, in which case the bitmap associated with that type is loaded.</span></span> <span data-ttu-id="de1b0-109">Si vous spécifiez à la fois un <xref:System.Type> et une chaîne, le contrôle recherche une ressource d’image avec le nom spécifié par le paramètre de chaîne dans l’assembly contenant le type spécifié par le <xref:System.Type> paramètre.</span><span class="sxs-lookup"><span data-stu-id="de1b0-109">If you specify both a <xref:System.Type> and a string, the control searches for an image resource with the name specified by the string parameter in the assembly containing the type specified by the <xref:System.Type> parameter.</span></span>  
  
### <a name="to-specify-a-toolbox-bitmap-for-your-control"></a><span data-ttu-id="de1b0-110">Pour spécifier une image de bitmap dans la boîte à outils concernant votre contrôle</span><span class="sxs-lookup"><span data-stu-id="de1b0-110">To specify a Toolbox bitmap for your control</span></span>  
  
1.  <span data-ttu-id="de1b0-111">Ajouter le <xref:System.Drawing.ToolboxBitmapAttribute> à la déclaration de classe de votre contrôle avant le `Class` mot clé pour visual Basic et au-dessus de la déclaration de classe pour Visual c#.</span><span class="sxs-lookup"><span data-stu-id="de1b0-111">Add the <xref:System.Drawing.ToolboxBitmapAttribute> to the class declaration of your control before the `Class` keyword for visual Basic, and above the class declaration for Visual C#.</span></span>  
  
    ```vb  
    ' Specifies the bitmap associated with the Button type.  
    <ToolboxBitmap(GetType(Button))> Class MyControl1  
    ' Specifies a bitmap file.  
    End Class  
    <ToolboxBitmap("C:\Documents and Settings\Joe\MyPics\myImage.bmp")> _  
       Class MyControl2  
    End Class  
    ' Specifies a type that indicates the assembly to search, and the name   
    ' of an image resource to look for.  
    <ToolboxBitmap(GetType(MyControl), "MyControlBitmap")> Class MyControl  
    End Class  
    ```  
  
    ```csharp  
    // Specifies the bitmap associated with the Button type.  
    [ToolboxBitmap(typeof(Button))]  
    class MyControl1 : UserControl  
    {  
    }  
    // Specifies a bitmap file.  
    [ToolboxBitmap(@"C:\Documents and Settings\Joe\MyPics\myImage.bmp")]  
    class MyControl2 : UserControl  
    {  
    }  
    // Specifies a type that indicates the assembly to search, and the name   
    // of an image resource to look for.  
    [ToolboxBitmap(typeof(MyControl), "MyControlBitmap")]  
    class MyControl : UserControl  
    {  
    }  
    ```  
  
2.  <span data-ttu-id="de1b0-112">Regénérez le projet.</span><span class="sxs-lookup"><span data-stu-id="de1b0-112">Rebuild the project.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="de1b0-113">L’image bitmap n’apparaît pas dans la boîte à outils pour les composants et les contrôles générés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="de1b0-113">The bitmap does not appear in the Toolbox for autogenerated controls and components.</span></span> <span data-ttu-id="de1b0-114">Pour afficher l’image bitmap, rechargez le contrôle par le biais de la boîte de dialogue **Choisir des éléments de boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="de1b0-114">To see the bitmap, reload the control by using the **Choose Toolbox Items** dialog box.</span></span> <span data-ttu-id="de1b0-115">Pour plus d’informations, consultez [Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés](walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span><span class="sxs-lookup"><span data-stu-id="de1b0-115">For more information, see [Walkthrough: Automatically Populating the Toolbox with Custom Components](walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de1b0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de1b0-116">See also</span></span>

- <xref:System.Drawing.ToolboxBitmapAttribute>
- [<span data-ttu-id="de1b0-117">Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés</span><span class="sxs-lookup"><span data-stu-id="de1b0-117">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
- [<span data-ttu-id="de1b0-118">Développement de contrôles Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="de1b0-118">Developing Windows Forms Controls at Design Time</span></span>](developing-windows-forms-controls-at-design-time.md)
- [<span data-ttu-id="de1b0-119">Vue d’ensemble des attributs (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="de1b0-119">Attributes overview (Visual Basic)</span></span>](../../../visual-basic/programming-guide/concepts/attributes/index.md)
- [<span data-ttu-id="de1b0-120">Attributs (C#)</span><span class="sxs-lookup"><span data-stu-id="de1b0-120">Attributes (C#)</span></span>](../../../csharp/programming-guide/concepts/attributes/index.md)
