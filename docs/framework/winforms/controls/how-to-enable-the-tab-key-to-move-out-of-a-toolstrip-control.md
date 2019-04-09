---
title: 'Procédure : activer l’utilisation de la touche Tab pour sortir d’un contrôle ToolStrip'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], moving between
- TAB key [Windows Forms], enabling
- ToolStrip control [Windows Forms], moving from
ms.assetid: 40f9e88b-09a3-428e-8da8-c00bb65079c6
ms.openlocfilehash: d4de7345a4e3ce122c4e1fc0a92f09b447204eb6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59113163"
---
# <a name="how-to-enable-the-tab-key-to-move-out-of-a-toolstrip-control"></a><span data-ttu-id="1de9c-102">Procédure : activer l’utilisation de la touche Tab pour sortir d’un contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="1de9c-102">How to: Enable the TAB Key to Move Out of a ToolStrip Control</span></span>
<span data-ttu-id="1de9c-103">Utilisez la procédure suivante pour permettre aux utilisateurs d’appuyer sur la touche TAB pour sortir d’un <xref:System.Windows.Forms.ToolStrip> au contrôle suivant dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="1de9c-103">Use the following procedure to enable the user to press the TAB key to move out of a <xref:System.Windows.Forms.ToolStrip> to the next control in the tab order.</span></span>  
  
 <span data-ttu-id="1de9c-104">Le <xref:System.Windows.Forms.ToolStrip> accepte la première pression sur la touche TAB et les touches flèche sélectionner des éléments dans le <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="1de9c-104">The <xref:System.Windows.Forms.ToolStrip> accepts the first press of the TAB key, and the arrow keys select items within the <xref:System.Windows.Forms.ToolStrip>.</span></span> <span data-ttu-id="1de9c-105">Lorsque l’utilisateur appuie sur la touche TAB une deuxième fois, il dirige l’utilisateur vers le contrôle suivant dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="1de9c-105">When the user presses the TAB key a second time, it takes the user to the next control in the tab order.</span></span>  
  
### <a name="to-enable-the-user-to-press-the-tab-key-to-move-out-of-a-toolstrip-to-the-next-control"></a><span data-ttu-id="1de9c-106">Pour permettre aux utilisateurs d’appuyer sur la touche TAB pour sortir d’un ToolStrip au contrôle suivant</span><span class="sxs-lookup"><span data-stu-id="1de9c-106">To enable the user to press the TAB key to move out of a ToolStrip to the next control</span></span>  
  
-   <span data-ttu-id="1de9c-107">Définir le <xref:System.Windows.Forms.ToolStrip.TabStop%2A> propriété de la <xref:System.Windows.Forms.ToolStrip> à `true`.</span><span class="sxs-lookup"><span data-stu-id="1de9c-107">Set the <xref:System.Windows.Forms.ToolStrip.TabStop%2A> property of the <xref:System.Windows.Forms.ToolStrip> to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1de9c-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1de9c-108">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.TabStop%2A>
- [<span data-ttu-id="1de9c-109">Vue d’ensemble du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="1de9c-109">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
