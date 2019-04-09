---
title: 'Procédure : regrouper des contrôles avec le contrôle GroupBox Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], grouping
- GroupBox control [Windows Forms], grouping controls
- Windows Forms controls, grouping
ms.assetid: 0bda316d-bd2a-43aa-ac73-342453303169
ms.openlocfilehash: 706655c8cb2c2548b393b6ad731c13e47fd9381a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59179624"
---
# <a name="how-to-group-controls-with-the-windows-forms-groupbox-control"></a><span data-ttu-id="db411-102">Procédure : regrouper des contrôles avec le contrôle GroupBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="db411-102">How to: Group Controls with the Windows Forms GroupBox Control</span></span>
<span data-ttu-id="db411-103">Windows Forms <xref:System.Windows.Forms.GroupBox> contrôles sont utilisés pour regrouper d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="db411-103">Windows Forms <xref:System.Windows.Forms.GroupBox> controls are used to group other controls.</span></span> <span data-ttu-id="db411-104">Il existe trois raisons pour regrouper des contrôles :</span><span class="sxs-lookup"><span data-stu-id="db411-104">There are three reasons to group controls:</span></span>  
  
-   <span data-ttu-id="db411-105">Pour créer un regroupement visuel des éléments connexes pour une interface utilisateur clair.</span><span class="sxs-lookup"><span data-stu-id="db411-105">To create a visual grouping of related form elements for a clear user interface.</span></span>  
  
-   <span data-ttu-id="db411-106">Pour créer un regroupement par programmation (des cases d’option, par exemple).</span><span class="sxs-lookup"><span data-stu-id="db411-106">To create programmatic grouping (of radio buttons, for example).</span></span>  
  
-   <span data-ttu-id="db411-107">Pour déplacer les contrôles en tant qu’unité au moment du design.</span><span class="sxs-lookup"><span data-stu-id="db411-107">For moving the controls as a unit at design time.</span></span>  
  
### <a name="to-create-a-group-of-controls"></a><span data-ttu-id="db411-108">Pour créer un groupe de contrôles</span><span class="sxs-lookup"><span data-stu-id="db411-108">To create a group of controls</span></span>  
  
1.  <span data-ttu-id="db411-109">Dessiner un <xref:System.Windows.Forms.GroupBox> contrôle sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="db411-109">Draw a <xref:System.Windows.Forms.GroupBox> control on a form.</span></span>  
  
2.  <span data-ttu-id="db411-110">Ajoutez des contrôles à la zone de groupe, en dessinant à l’intérieur de la zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="db411-110">Add other controls to the group box, drawing each inside the group box.</span></span>  
  
     <span data-ttu-id="db411-111">Si vous avez des contrôles existants que vous souhaitez placer dans une zone de groupe, vous pouvez sélectionner tous les contrôles, les couper dans le Presse-papiers, sélectionnez le <xref:System.Windows.Forms.GroupBox> contrôler et collez-les dans la zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="db411-111">If you have existing controls that you want to enclose in a group box, you can select all the controls, cut them to the Clipboard, select the <xref:System.Windows.Forms.GroupBox> control, and then paste them into the group box.</span></span> <span data-ttu-id="db411-112">Vous pouvez également faire glisser les dans la zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="db411-112">You can also drag them into the group box.</span></span>  
  
3.  <span data-ttu-id="db411-113">Définir le <xref:System.Windows.Forms.GroupBox.Text%2A> propriété de la zone de groupe pour une légende appropriée.</span><span class="sxs-lookup"><span data-stu-id="db411-113">Set the <xref:System.Windows.Forms.GroupBox.Text%2A> property of the group box to an appropriate caption.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db411-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db411-114">See also</span></span>

- <xref:System.Windows.Forms.GroupBox>
- [<span data-ttu-id="db411-115">GroupBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="db411-115">GroupBox Control</span></span>](groupbox-control-windows-forms.md)
