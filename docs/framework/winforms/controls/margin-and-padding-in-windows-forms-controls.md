---
title: Marge et marge intérieure dans les contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Padding property [Windows Forms]
- layout [Windows Forms], margins and padding
- Windows Forms, layout
- Margin property [Windows Forms]
ms.assetid: 3781b5a1-3085-4072-bed0-44670c23ffdc
ms.openlocfilehash: a3218ad029735f4a5d70b3166951dcd93e061c26
ms.sourcegitcommit: 2b986afe4ce9e13bbeec929c9737757eb61de60e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56665223"
---
# <a name="margin-and-padding-in-windows-forms-controls"></a><span data-ttu-id="075af-102">Marge et marge intérieure dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="075af-102">Margin and Padding in Windows Forms Controls</span></span>
<span data-ttu-id="075af-103">Le positionnement précis des contrôles sur votre formulaire constitue une haute priorité pour de nombreuses applications.</span><span class="sxs-lookup"><span data-stu-id="075af-103">Precise placement of controls on your form is a high priority for many applications.</span></span> <span data-ttu-id="075af-104">L'espace de noms <xref:System.Windows.Forms?displayProperty=nameWithType> propose pour cela de nombreuses fonctionnalités de disposition.</span><span class="sxs-lookup"><span data-stu-id="075af-104">The <xref:System.Windows.Forms?displayProperty=nameWithType> namespace gives you many layout features to accomplish this.</span></span> <span data-ttu-id="075af-105">Deux des plus importantes sont les propriétés <xref:System.Windows.Forms.Control.Margin%2A> et <xref:System.Windows.Forms.Control.Padding%2A>.</span><span class="sxs-lookup"><span data-stu-id="075af-105">Two of the most important are the <xref:System.Windows.Forms.Control.Margin%2A> and <xref:System.Windows.Forms.Control.Padding%2A> properties.</span></span>  
  
 <span data-ttu-id="075af-106">La propriété <xref:System.Windows.Forms.Control.Margin%2A> définit l'espace autour du contrôle qui maintient les autres contrôles à une distance spécifiée des bordures du contrôle.</span><span class="sxs-lookup"><span data-stu-id="075af-106">The <xref:System.Windows.Forms.Control.Margin%2A> property defines the space around the control that keeps other controls a specified distance from the control's borders.</span></span>  
  
 <span data-ttu-id="075af-107">La propriété <xref:System.Windows.Forms.Control.Padding%2A> définit l'espace à l'intérieur d'un contrôle qui maintient le contenu du contrôle (par exemple la valeur de sa propriété <xref:System.Windows.Forms.Control.Text%2A>) à une distance spécifiée des bordures du contrôle.</span><span class="sxs-lookup"><span data-stu-id="075af-107">The <xref:System.Windows.Forms.Control.Padding%2A> property defines the space in the interior of a control that keeps the control's content (for example, the value of its <xref:System.Windows.Forms.Control.Text%2A> property) a specified distance from the control's borders.</span></span>  
  
 <span data-ttu-id="075af-108">L'illustration suivante montre les propriétés <xref:System.Windows.Forms.Control.Padding%2A> et <xref:System.Windows.Forms.Control.Margin%2A> d'un contrôle.</span><span class="sxs-lookup"><span data-stu-id="075af-108">The following illustration shows the <xref:System.Windows.Forms.Control.Padding%2A> and <xref:System.Windows.Forms.Control.Margin%2A> properties on a control.</span></span>  
  
 <span data-ttu-id="075af-109">![Remplissage et marge pour les Windows Forms contrôles](../../../../docs/framework/winforms/controls/media/vs-winformpadmargin.gif "VS_WinFormPadMargin")</span><span class="sxs-lookup"><span data-stu-id="075af-109">![Padding And Margin for Windows Forms Controls](../../../../docs/framework/winforms/controls/media/vs-winformpadmargin.gif "VS_WinFormPadMargin")</span></span>  
  
 <span data-ttu-id="075af-110">Cette fonctionnalité est prise en charge au moment du design dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="075af-110">There is design-time support for this feature in Visual Studio.</span></span> <span data-ttu-id="075af-111">Consultez également [procédure pas à pas : Disposition des Windows Forms contrôles avec les propriétés Padding, marges et la propriété AutoSize](windows-forms-controls-padding-autosize.md).</span><span class="sxs-lookup"><span data-stu-id="075af-111">Also see [Walkthrough: Laying Out Windows Forms Controls with Padding, Margins, and the AutoSize Property](windows-forms-controls-padding-autosize.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="075af-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="075af-112">See also</span></span>
- <xref:System.Windows.Forms.Control.AutoSize%2A>
- <xref:System.Windows.Forms.Control.Margin%2A>
- <xref:System.Windows.Forms.Control.Padding%2A>
- <xref:System.Windows.Forms.Control.LayoutEngine%2A>
- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
