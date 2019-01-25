---
title: 'Procédure : Groupe Windows Forms contrôles RadioButton en tant qu’ensemble'
ms.date: 03/30/2017
helpviewer_keywords:
- radio buttons [Windows Forms], grouping
- controls [Windows Forms], grouping
- Windows Forms controls, grouping
- RadioButton control [Windows Forms], grouping
ms.assetid: 58f8fe34-50b7-49d8-a2be-c271be3c6b32
ms.openlocfilehash: 2758ff2380431668b2c908dbddd5dbe2094ccd0c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569334"
---
# <a name="how-to-group-windows-forms-radiobutton-controls-to-function-as-a-set"></a><span data-ttu-id="9a6db-102">Procédure : Groupe Windows Forms contrôles RadioButton en tant qu’ensemble</span><span class="sxs-lookup"><span data-stu-id="9a6db-102">How to: Group Windows Forms RadioButton Controls to Function as a Set</span></span>
<span data-ttu-id="9a6db-103">Windows Forms <xref:System.Windows.Forms.RadioButton> contrôles sont conçus pour donner aux utilisateurs un choix parmi deux ou plusieurs paramètres, dont une seule peut être assignée à une procédure ou un objet.</span><span class="sxs-lookup"><span data-stu-id="9a6db-103">Windows Forms <xref:System.Windows.Forms.RadioButton> controls are designed to give users a choice among two or more settings, of which only one can be assigned to a procedure or object.</span></span> <span data-ttu-id="9a6db-104">Par exemple, un groupe de <xref:System.Windows.Forms.RadioButton> contrôles peuvent afficher une liste d’opérateurs de package pour une commande, mais uniquement des transporteurs sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="9a6db-104">For example, a group of <xref:System.Windows.Forms.RadioButton> controls may display a choice of package carriers for an order, but only one of the carriers will be used.</span></span> <span data-ttu-id="9a6db-105">Par conséquent seul <xref:System.Windows.Forms.RadioButton> à la fois peut être sélectionné, même s’il fait partie d’un groupe fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="9a6db-105">Therefore only one <xref:System.Windows.Forms.RadioButton> at a time can be selected, even if it is a part of a functional group.</span></span>  
  
 <span data-ttu-id="9a6db-106">Groupe de cases d’option en dessinant comme à l’intérieur d’un conteneur un <xref:System.Windows.Forms.Panel> contrôle, un <xref:System.Windows.Forms.GroupBox> contrôle ou un formulaire.</span><span class="sxs-lookup"><span data-stu-id="9a6db-106">You group radio buttons by drawing them inside a container such as a <xref:System.Windows.Forms.Panel> control, a <xref:System.Windows.Forms.GroupBox> control, or a form.</span></span> <span data-ttu-id="9a6db-107">Toutes les cases d’option qui sont ajoutés directement à un formulaire devient un groupe.</span><span class="sxs-lookup"><span data-stu-id="9a6db-107">All radio buttons that are added directly to a form become one group.</span></span> <span data-ttu-id="9a6db-108">Pour ajouter des groupes distincts, vous devez les placer à l’intérieur de panneaux ou zones de groupe.</span><span class="sxs-lookup"><span data-stu-id="9a6db-108">To add separate groups, you must place them inside panels or group boxes.</span></span> <span data-ttu-id="9a6db-109">Pour plus d’informations sur les panneaux ou zones de groupe, consultez [vue d’ensemble du contrôle de panneau](../../../../docs/framework/winforms/controls/panel-control-overview-windows-forms.md) ou [vue d’ensemble du contrôle GroupBox](../../../../docs/framework/winforms/controls/groupbox-control-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="9a6db-109">For more information about panels or group boxes, see [Panel Control Overview](../../../../docs/framework/winforms/controls/panel-control-overview-windows-forms.md) or [GroupBox Control Overview](../../../../docs/framework/winforms/controls/groupbox-control-overview-windows-forms.md).</span></span>  
  
### <a name="to-group-radiobutton-controls-as-a-set-to-function-independently-of-other-sets"></a><span data-ttu-id="9a6db-110">Pour regrouper des contrôles RadioButton en tant qu’ensemble de la fonction indépendamment des autres jeux</span><span class="sxs-lookup"><span data-stu-id="9a6db-110">To group RadioButton controls as a set to function independently of other sets</span></span>  
  
1.  <span data-ttu-id="9a6db-111">Faites glisser un <xref:System.Windows.Forms.GroupBox> ou <xref:System.Windows.Forms.Panel> contrôler à partir de la **Windows Forms** onglet sur le **boîte à outils** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9a6db-111">Drag a <xref:System.Windows.Forms.GroupBox> or <xref:System.Windows.Forms.Panel> control from the **Windows Forms** tab on the **Toolbox** onto the form.</span></span>  
  
2.  <span data-ttu-id="9a6db-112">Dessiner <xref:System.Windows.Forms.RadioButton> contrôle sur le <xref:System.Windows.Forms.GroupBox> ou <xref:System.Windows.Forms.Panel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="9a6db-112">Draw <xref:System.Windows.Forms.RadioButton> controls on the <xref:System.Windows.Forms.GroupBox> or <xref:System.Windows.Forms.Panel> control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a6db-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a6db-113">See also</span></span>
- <xref:System.Windows.Forms.RadioButton>
- [<span data-ttu-id="9a6db-114">Vue d’ensemble du contrôle RadioButton</span><span class="sxs-lookup"><span data-stu-id="9a6db-114">RadioButton Control Overview</span></span>](../../../../docs/framework/winforms/controls/radiobutton-control-overview-windows-forms.md)
- [<span data-ttu-id="9a6db-115">Vue d’ensemble du contrôle Panel</span><span class="sxs-lookup"><span data-stu-id="9a6db-115">Panel Control Overview</span></span>](../../../../docs/framework/winforms/controls/panel-control-overview-windows-forms.md)
- [<span data-ttu-id="9a6db-116">Vue d’ensemble du contrôle GroupBox</span><span class="sxs-lookup"><span data-stu-id="9a6db-116">GroupBox Control Overview</span></span>](../../../../docs/framework/winforms/controls/groupbox-control-overview-windows-forms.md)
- [<span data-ttu-id="9a6db-117">Vue d'ensemble du contrôle CheckBox</span><span class="sxs-lookup"><span data-stu-id="9a6db-117">CheckBox Control Overview</span></span>](../../../../docs/framework/winforms/controls/checkbox-control-overview-windows-forms.md)
- [<span data-ttu-id="9a6db-118">RadioButton, contrôle</span><span class="sxs-lookup"><span data-stu-id="9a6db-118">RadioButton Control</span></span>](../../../../docs/framework/winforms/controls/radiobutton-control-windows-forms.md)
