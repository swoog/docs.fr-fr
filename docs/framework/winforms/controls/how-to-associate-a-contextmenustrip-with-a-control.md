---
title: 'Procédure : associer un ContextMenuStrip à un contrôle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- context menus [Windows Forms], relating
- ContextMenuStrips [Windows Forms], associating with controls
- context menus [Windows Forms], associating with controls
- ContextMenuStrips [Windows Forms], relating
ms.assetid: 6fc40a42-5d69-427f-aa30-0a146193226b
ms.openlocfilehash: e1b2a49196d6da66d478a3d44eab64298cebe969
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65586606"
---
# <a name="how-to-associate-a-contextmenustrip-with-a-control"></a><span data-ttu-id="1a67b-102">Procédure : associer un ContextMenuStrip à un contrôle</span><span class="sxs-lookup"><span data-stu-id="1a67b-102">How to: Associate a ContextMenuStrip with a Control</span></span>
<span data-ttu-id="1a67b-103">Après avoir créé vos contrôles et menus contextuels, appliquez les procédures suivantes pour afficher un menu contextuel donné quand l'utilisateur clique avec le bouton droit sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="1a67b-103">After creating your controls and shortcut menus, use the following procedures to display a given shortcut menu when the user right-clicks the control.</span></span> <span data-ttu-id="1a67b-104">Ces procédures associent un <xref:System.Windows.Forms.ContextMenuStrip> à un Windows Form et à un contrôle <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="1a67b-104">These procedures associate a <xref:System.Windows.Forms.ContextMenuStrip> with a Windows Form and with a <xref:System.Windows.Forms.ToolStrip> control.</span></span>  
  
### <a name="to-associate-a-contextmenustrip-with-a-windows-form"></a><span data-ttu-id="1a67b-105">Pour associer un ContextMenuStrip à un Windows Form</span><span class="sxs-lookup"><span data-stu-id="1a67b-105">To associate a ContextMenuStrip with a Windows Form</span></span>  
  
1. <span data-ttu-id="1a67b-106">Affectez le nom du <xref:System.Windows.Forms.ContextMenuStrip> associé comme valeur de la propriété <xref:System.Windows.Forms.Control.ContextMenuStrip%2A>.</span><span class="sxs-lookup"><span data-stu-id="1a67b-106">Set the <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> property to the name of the associated <xref:System.Windows.Forms.ContextMenuStrip>.</span></span>  
  
### <a name="to-associate-a-contextmenustrip-with-a-toolstrip-control"></a><span data-ttu-id="1a67b-107">Pour associer un ContextMenuStrip à un contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="1a67b-107">To associate a ContextMenuStrip with a ToolStrip control</span></span>  
  
1. <span data-ttu-id="1a67b-108">Affectez le nom du <xref:System.Windows.Forms.ContextMenuStrip> associé comme valeur de la propriété <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1a67b-108">Set the control's <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> property to the name of the associated <xref:System.Windows.Forms.ContextMenuStrip>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1a67b-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="1a67b-109">Example</span></span>  
 <span data-ttu-id="1a67b-110">L'exemple de code suivant crée un Windows Form et un <xref:System.Windows.Forms.ToolStrip>, et associe un contrôle <xref:System.Windows.Forms.ContextMenuStrip> différent à chacun d'eux.</span><span class="sxs-lookup"><span data-stu-id="1a67b-110">The following code example creates a Windows Form and a <xref:System.Windows.Forms.ToolStrip>, and associates a different <xref:System.Windows.Forms.ContextMenuStrip> control with each of them.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ContextMenuStrip#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ContextMenuStrip/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ContextMenuStrip#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ContextMenuStrip/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="1a67b-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="1a67b-111">Compiling the Code</span></span>  
 <span data-ttu-id="1a67b-112">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="1a67b-112">This example requires:</span></span>  
  
- <span data-ttu-id="1a67b-113">Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="1a67b-113">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a67b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a67b-114">See also</span></span>

- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.Control.ContextMenuStrip%2A>
- <xref:System.Windows.Forms.ToolStrip>
- [<span data-ttu-id="1a67b-115">Guide pratique pour Ajouter des éléments de Menu à un ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="1a67b-115">How to: Add Menu Items to a ContextMenuStrip</span></span>](how-to-add-menu-items-to-a-contextmenustrip.md)
- [<span data-ttu-id="1a67b-116">ContextMenuStrip, contrôle</span><span class="sxs-lookup"><span data-stu-id="1a67b-116">ContextMenuStrip Control</span></span>](contextmenustrip-control.md)
