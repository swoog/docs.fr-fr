---
title: 'Procédure : Modifier la durée avant affichage du composant ToolTip Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolTip component [Windows Forms], delay values
- tooltips [Windows Forms], delay values
- examples [Windows Forms], tooltips
ms.assetid: 08979ba7-dd84-477b-ab17-8d06e759be99
ms.openlocfilehash: 5f3be7467aad8b14aa67dc57b8c23e585a62fa25
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57704473"
---
# <a name="how-to-change-the-delay-of-the-windows-forms-tooltip-component"></a><span data-ttu-id="6ef91-102">Procédure : Modifier la durée avant affichage du composant ToolTip Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6ef91-102">How to: Change the Delay of the Windows Forms ToolTip Component</span></span>
<span data-ttu-id="6ef91-103">Il existe plusieurs valeurs de délai que vous pouvez définir pour un formulaire Windows <xref:System.Windows.Forms.ToolTip> composant.</span><span class="sxs-lookup"><span data-stu-id="6ef91-103">There are multiple delay values that you can set for a Windows Forms <xref:System.Windows.Forms.ToolTip> component.</span></span> <span data-ttu-id="6ef91-104">L’unité de mesure pour toutes ces propriétés est millisecondes.</span><span class="sxs-lookup"><span data-stu-id="6ef91-104">The unit of measure for all these properties is milliseconds.</span></span> <span data-ttu-id="6ef91-105">Le <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> propriété détermine la durée pendant laquelle l’utilisateur doit pointer sur le contrôle associé pour la chaîne d’info-bulle apparaisse.</span><span class="sxs-lookup"><span data-stu-id="6ef91-105">The <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> property determines how long the user must point at the associated control for the ToolTip string to appear.</span></span> <span data-ttu-id="6ef91-106">Le <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> propriété définit le nombre de millisecondes nécessaire pour les chaînes d’info-bulle suivantes apparaissent lorsque la souris se déplace d’un contrôle associé à l’info-bulle à un autre.</span><span class="sxs-lookup"><span data-stu-id="6ef91-106">The <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> property sets the number of milliseconds it takes for subsequent ToolTip strings to appear as the mouse moves from one ToolTip-associated control to another.</span></span> <span data-ttu-id="6ef91-107">Le <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> propriété détermine la durée pendant laquelle la chaîne d’info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="6ef91-107">The <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> property determines the length of time the ToolTip string is shown.</span></span> <span data-ttu-id="6ef91-108">Vous pouvez définir ces valeurs individuellement ou en définissant la valeur de la <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> propriété ; le délai de propriétés sont définies en fonction de la valeur affectée à la <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="6ef91-108">You can set these values individually, or by setting the value of the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property; the other delay properties are set based on the value assigned to the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property.</span></span> <span data-ttu-id="6ef91-109">Par exemple, lorsque <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> est défini sur une valeur N, <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> a la valeur N, <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> est défini sur la valeur de <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> divisée par cinq (ou N/5), et <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> est défini sur une valeur qui est cinq fois la valeur de la <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> propriété (ou 5N).</span><span class="sxs-lookup"><span data-stu-id="6ef91-109">For example, when <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> is set to a value N, <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> is set to N, <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> is set to the value of <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> divided by five (or N/5), and <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> is set to a value that is five times the value of the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property (or 5N).</span></span>  
  
### <a name="to-set-the-delay"></a><span data-ttu-id="6ef91-110">Pour définir le délai</span><span class="sxs-lookup"><span data-stu-id="6ef91-110">To set the delay</span></span>  
  
1.  <span data-ttu-id="6ef91-111">Définissez les propriétés suivantes comme indiqué dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="6ef91-111">Set the following properties as shown in this example.</span></span>  
  
    ```vb  
    ToolTip1.InitialDelay = 500  
    ToolTip1.ReshowDelay = 100  
    ToolTip1.AutoPopDelay = 5000  
    ```  
  
    ```csharp  
    ToolTip1.InitialDelay = 500;  
    ToolTip1.ReshowDelay = 100;  
    ToolTip1.AutoPopDelay = 5000;  
    ```  
  
    ```cpp  
    toolTip1->InitialDelay = 500;  
    toolTip1->ReshowDelay = 100;  
    toolTip1->AutoPopDelay = 5000;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="6ef91-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ef91-112">See also</span></span>
- [<span data-ttu-id="6ef91-113">Vue d’ensemble du composant ToolTip</span><span class="sxs-lookup"><span data-stu-id="6ef91-113">ToolTip Component Overview</span></span>](tooltip-component-overview-windows-forms.md)
- [<span data-ttu-id="6ef91-114">Guide pratique pour Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du Design</span><span class="sxs-lookup"><span data-stu-id="6ef91-114">How to: Set ToolTips for Controls on a Windows Form at Design Time</span></span>](how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md)
- [<span data-ttu-id="6ef91-115">ToolTip, composant</span><span class="sxs-lookup"><span data-stu-id="6ef91-115">ToolTip Component</span></span>](tooltip-component-windows-forms.md)
