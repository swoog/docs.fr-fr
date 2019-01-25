---
title: 'Procédure : Redimensionner des Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- resizing Windows Forms
- Windows Forms, resizing
ms.assetid: 5d9dd47e-e68c-48c9-a0a3-a9ff34ba009d
ms.openlocfilehash: f9a1aae4e9a787b798d6c27f9daa597955b208a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614572"
---
# <a name="how-to-resize-windows-forms"></a><span data-ttu-id="83496-102">Procédure : Redimensionner des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="83496-102">How to: Resize Windows Forms</span></span>
<span data-ttu-id="83496-103">Vous pouvez spécifier la taille de votre Windows Form de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="83496-103">You can specify the size of your Windows Form in several ways.</span></span> <span data-ttu-id="83496-104">Vous pouvez modifier à la fois la hauteur et la largeur du formulaire par programmation en affectant une nouvelle valeur à la propriété <xref:System.Windows.Forms.Form.Size%2A>, ou ajuster les propriétés <xref:System.Windows.Forms.Control.Height%2A> et <xref:System.Windows.Forms.Control.Width%2A> individuellement.</span><span class="sxs-lookup"><span data-stu-id="83496-104">You can change both the height and the width of the form programmatically by setting a new value for the <xref:System.Windows.Forms.Form.Size%2A> property, or adjust the <xref:System.Windows.Forms.Control.Height%2A> or <xref:System.Windows.Forms.Control.Width%2A> properties individually.</span></span> <span data-ttu-id="83496-105">Si vous utilisez Visual Studio, vous pouvez modifier la taille à l’aide du Concepteur de formulaires Windows.</span><span class="sxs-lookup"><span data-stu-id="83496-105">If you are using Visual Studio, you can change the size using the Windows Forms Designer.</span></span> <span data-ttu-id="83496-106">Voir également [Guide pratique pour Redimensionner les formulaires Windows à l’aide du concepteur](https://msdn.microsoft.com/library/37k2zkwx\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="83496-106">Also see [How to: Resize Windows Forms Using the Designer](https://msdn.microsoft.com/library/37k2zkwx\(v=vs.110\)).</span></span>  
  
### <a name="to-resize-a-form-programmatically"></a><span data-ttu-id="83496-107">Pour redimensionner un formulaire par programmation</span><span class="sxs-lookup"><span data-stu-id="83496-107">To resize a form programmatically</span></span>  
  
-   <span data-ttu-id="83496-108">Définissez la taille d'un formulaire au moment de l'exécution en définissant la propriété <xref:System.Windows.Forms.Form.Size%2A> du formulaire.</span><span class="sxs-lookup"><span data-stu-id="83496-108">Define the size of a form at run time by setting the <xref:System.Windows.Forms.Form.Size%2A> property of the form.</span></span>  
  
     <span data-ttu-id="83496-109">L'exemple de code suivant montre la taille de formulaire définie sur 100 × 100 pixels.</span><span class="sxs-lookup"><span data-stu-id="83496-109">The following code example shows the form size set to 100 × 100 pixels.</span></span>  
  
    ```vb  
    Form1.Size = New System.Drawing.Size(100, 100)  
    ```  
  
    ```csharp  
    Form1.Size = new System.Drawing.Size(100, 100);  
    ```  
  
    ```cpp  
    Form1->Size = System::Drawing::Size(100, 100);  
    ```  
  
### <a name="to-change-form-width-and-height-programmatically"></a><span data-ttu-id="83496-110">Pour modifier la hauteur et la largeur du formulaire par programmation</span><span class="sxs-lookup"><span data-stu-id="83496-110">To change form width and height programmatically</span></span>  
  
-   <span data-ttu-id="83496-111">Une fois le <xref:System.Windows.Forms.Form.Size%2A> défini, modifiez la hauteur ou la largeur du formulaire à l'aide de la propriété <xref:System.Windows.Forms.Control.Width%2A> ou <xref:System.Windows.Forms.Control.Height%2A>.</span><span class="sxs-lookup"><span data-stu-id="83496-111">After the <xref:System.Windows.Forms.Form.Size%2A> is defined, change either the form height or width by using the <xref:System.Windows.Forms.Control.Width%2A> or <xref:System.Windows.Forms.Control.Height%2A> properties.</span></span>  
  
     <span data-ttu-id="83496-112">L'exemple de code suivant montre la largeur du formulaire définie sur 300 pixels à partir du bord gauche du formulaire, alors que la hauteur reste constante.</span><span class="sxs-lookup"><span data-stu-id="83496-112">The following code example shows the width of the form set to 300 pixels from the left edge of the form, whereas the height stays constant.</span></span>  
  
    ```vb  
    Form1.Width = 300  
    ```  
  
    ```csharp  
    Form1.Width = 300;  
    ```  
  
    ```cpp  
    Form1->Width = 300;  
    ```  
  
     <span data-ttu-id="83496-113">ou</span><span class="sxs-lookup"><span data-stu-id="83496-113">-or-</span></span>  
  
     <span data-ttu-id="83496-114">Modifiez <xref:System.Drawing.Size.Width%2A> ou <xref:System.Drawing.Size.Height%2A> en définissant la propriété <xref:System.Windows.Forms.Form.Size%2A>.</span><span class="sxs-lookup"><span data-stu-id="83496-114">Change <xref:System.Drawing.Size.Width%2A> or <xref:System.Drawing.Size.Height%2A> by setting the <xref:System.Windows.Forms.Form.Size%2A> property.</span></span>  
  
     <span data-ttu-id="83496-115">Toutefois, comme le montre l'exemple de code suivant, cette approche est plus laborieuse que la simple définition de la propriété <xref:System.Windows.Forms.Control.Width%2A> ou <xref:System.Windows.Forms.Control.Height%2A>.</span><span class="sxs-lookup"><span data-stu-id="83496-115">However, as the following code example shows, this approach is more cumbersome than just setting <xref:System.Windows.Forms.Control.Width%2A> or <xref:System.Windows.Forms.Control.Height%2A> properties.</span></span>  
  
    ```vb  
    Form1.Size = New Size(300, Form1.Size.Height)  
    ```  
  
    ```csharp  
    Form1.Size = new Size(300, Form1.Size.Height);  
    ```  
  
    ```cpp  
    Form1->Size = System::Drawing::Size(300, Form1->Size.Height);  
    ```  
  
### <a name="to-change-form-size-by-increments-programmatically"></a><span data-ttu-id="83496-116">Pour modifier la taille de formulaire par incréments par programmation</span><span class="sxs-lookup"><span data-stu-id="83496-116">To change form size by increments programmatically</span></span>  
  
-   <span data-ttu-id="83496-117">Pour incrémenter la taille du formulaire, définissez les propriétés <xref:System.Drawing.Size.Width%2A> et <xref:System.Drawing.Size.Height%2A>.</span><span class="sxs-lookup"><span data-stu-id="83496-117">To increment the size of the form, set the <xref:System.Drawing.Size.Width%2A> and <xref:System.Drawing.Size.Height%2A> properties.</span></span>  
  
     <span data-ttu-id="83496-118">L'exemple de code suivant montre la largeur du formulaire définie sur 200 pixels de plus que la valeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="83496-118">The following code example shows the width of the form set to 200 pixels wider than the current setting.</span></span>  
  
    ```vb  
    Form1.Width += 200  
    ```  
  
    ```csharp  
    Form1.Width += 200;  
    ```  
  
    ```cpp  
    Form1->Width += 200;  
    ```  
  
    > [!CAUTION]
    >  <span data-ttu-id="83496-119">Utilisez toujours la propriété <xref:System.Drawing.Size.Height%2A> ou <xref:System.Drawing.Size.Width%2A> pour modifier une dimension d'un formulaire, sauf si vous définissez les dimensions de hauteur et de largeur en même temps en affectant une nouvelle structure <xref:System.Drawing.Size> à la propriété <xref:System.Windows.Forms.Form.Size%2A>.</span><span class="sxs-lookup"><span data-stu-id="83496-119">Always use the <xref:System.Drawing.Size.Height%2A> or <xref:System.Drawing.Size.Width%2A> property to change a dimension of a form, unless you are setting both height and width dimensions at the same time by setting the <xref:System.Windows.Forms.Form.Size%2A> property to a new <xref:System.Drawing.Size> structure.</span></span> <span data-ttu-id="83496-120">La propriété <xref:System.Windows.Forms.Form.Size%2A> retourne une structure <xref:System.Drawing.Size>, qui est un type valeur.</span><span class="sxs-lookup"><span data-stu-id="83496-120">The <xref:System.Windows.Forms.Form.Size%2A> property returns a <xref:System.Drawing.Size> structure, which is a value type.</span></span> <span data-ttu-id="83496-121">Vous ne pouvez pas attribuer une nouvelle valeur à la propriété d'un type valeur.</span><span class="sxs-lookup"><span data-stu-id="83496-121">You cannot assign a new value to the property of a value type.</span></span> <span data-ttu-id="83496-122">Le code suivant, par exemple, ne sera pas compilé :</span><span class="sxs-lookup"><span data-stu-id="83496-122">Therefore, the following code example will not compile.</span></span>  
  
    ```vb  
    ' NOTE: CODE WILL NOT COMPILE  
    Dim f As New Form()  
    f.Size.Width += 100  
    ```  
  
    ```csharp  
    // NOTE: CODE WILL NOT COMPILE  
    Form f = new Form();  
    f.Size.Width += 100;  
    ```  
  
    ```cpp  
    // NOTE: CODE WILL NOT COMPILE  
    Form^ f = gcnew Form();  
    f->Size->X += 100;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="83496-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83496-123">See also</span></span>
- [<span data-ttu-id="83496-124">Bien démarrer avec Windows Forms</span><span class="sxs-lookup"><span data-stu-id="83496-124">Getting Started with Windows Forms</span></span>](../../../docs/framework/winforms/getting-started-with-windows-forms.md)
- [<span data-ttu-id="83496-125">Amélioration des applications Windows Forms</span><span class="sxs-lookup"><span data-stu-id="83496-125">Enhancing Windows Forms Applications</span></span>](../../../docs/framework/winforms/advanced/index.md)
