---
title: 'Procédure : Exposer les propriétés des contrôles constitutifs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- user controls [Windows Forms], exposing constituent controls
- controls [Windows Forms], constituent
- custom controls [Windows Forms], exposing properties
- constituent controls
ms.assetid: 5c1ec98b-aa48-4823-986e-4712551cfdf1
ms.openlocfilehash: 75ee93b7a601b4fc1480dca708d78740664c9a85
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57704516"
---
# <a name="how-to-expose-properties-of-constituent-controls"></a><span data-ttu-id="bb1d6-102">Procédure : Exposer les propriétés des contrôles constitutifs</span><span class="sxs-lookup"><span data-stu-id="bb1d6-102">How to: Expose Properties of Constituent Controls</span></span>
<span data-ttu-id="bb1d6-103">Les contrôles qui composent un contrôle composite sont appelés *contrôles constitutifs*.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-103">The controls that make up a composite control are called *constituent controls*.</span></span> <span data-ttu-id="bb1d6-104">Ces contrôles sont normalement déclarés privés et est donc pas accessible par le développeur.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-104">These controls are normally declared private, and thus cannot be accessed by the developer.</span></span> <span data-ttu-id="bb1d6-105">Si vous souhaitez rendre les propriétés de ces contrôles accessibles aux utilisateurs de futures, vous devez les exposer à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-105">If you want to make properties of these controls available to future users, you must expose them to the user.</span></span> <span data-ttu-id="bb1d6-106">Pour exposer une propriété d’un contrôle qui le composent en créant une propriété dans le contrôle utilisateur et à l’aide de la `get` et `set` accesseurs pour répercuter la modification dans la propriété privée du contrôle constitutif.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-106">A property of a constituent control is exposed by creating a property in the user control, and using the `get` and `set` accessors of that property to effect the change in the private property of the constituent control.</span></span>  
  
 <span data-ttu-id="bb1d6-107">Envisagez d’un contrôle utilisateur hypothétique avec un bouton qui le composent nommé `MyButton`.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-107">Consider a hypothetical user control with a constituent button named `MyButton`.</span></span> <span data-ttu-id="bb1d6-108">Dans cet exemple, lorsque l’utilisateur demande la `ConstituentButtonBackColor` propriété, la valeur stockée dans le <xref:System.Windows.Forms.Control.BackColor%2A> propriété du `MyButton` est remis.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-108">In this example, when the user requests the `ConstituentButtonBackColor` property, the value stored in the <xref:System.Windows.Forms.Control.BackColor%2A> property of `MyButton` is delivered.</span></span> <span data-ttu-id="bb1d6-109">Lorsque l’utilisateur assigne une valeur à cette propriété, cette valeur est automatiquement passée à la <xref:System.Windows.Forms.Control.BackColor%2A> propriété du `MyButton` et `set` code s’exécutera, changez la couleur du `MyButton`.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-109">When the user assigns a value to this property, that value is automatically passed to the <xref:System.Windows.Forms.Control.BackColor%2A> property of `MyButton` and the `set` code will execute, changing the color of `MyButton`.</span></span>  
  
 <span data-ttu-id="bb1d6-110">L’exemple suivant montre comment exposer les <xref:System.Windows.Forms.Control.BackColor%2A> propriété du bouton constitutif :</span><span class="sxs-lookup"><span data-stu-id="bb1d6-110">The following example shows how to expose the <xref:System.Windows.Forms.Control.BackColor%2A> property of the constituent button:</span></span>  
  
```vb  
Public Property ButtonColor() as System.Drawing.Color  
   Get  
      Return MyButton.BackColor  
   End Get  
   Set(Value as System.Drawing.Color)  
      MyButton.BackColor = Value  
   End Set  
End Property  
```  
  
```csharp  
public Color ButtonColor  
{  
   get  
   {  
      return(myButton.BackColor);  
   }  
   set  
   {  
      myButton.BackColor = value;  
   }  
}  
```  
  
### <a name="to-expose-a-property-of-a-constituent-control"></a><span data-ttu-id="bb1d6-111">Pour exposer une propriété de contrôle constitutif</span><span class="sxs-lookup"><span data-stu-id="bb1d6-111">To expose a property of a constituent control</span></span>  
  
1.  <span data-ttu-id="bb1d6-112">Créez une propriété publique pour votre contrôle utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-112">Create a public property for your user control.</span></span>  
  
2.  <span data-ttu-id="bb1d6-113">Dans la `get` section de la propriété, écrivez du code qui Récupère la valeur de la propriété que vous souhaitez exposer.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-113">In the `get` section of the property, write code that retrieves the value of the property you want to expose.</span></span>  
  
3.  <span data-ttu-id="bb1d6-114">Dans la `set` section de la propriété, écrivez du code qui transmet la valeur de la propriété à la propriété exposée du contrôle constitutif.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-114">In the `set` section of the property, write code that passes the value of the property to the exposed property of the constituent control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb1d6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb1d6-115">See also</span></span>
- <xref:System.Windows.Forms.UserControl>
- [<span data-ttu-id="bb1d6-116">Propriétés dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="bb1d6-116">Properties in Windows Forms Controls</span></span>](properties-in-windows-forms-controls.md)
- [<span data-ttu-id="bb1d6-117">Variétés de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="bb1d6-117">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)
