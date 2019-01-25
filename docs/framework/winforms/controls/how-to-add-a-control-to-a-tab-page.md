---
title: 'Procédure : Ajouter un contrôle à une Page d’onglets'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TabPage control
- tab controls [Windows Forms], tab order
- tab pages [Windows Forms], adding controls
ms.assetid: b092532e-7346-469f-b9a1-897f9bea4fb7
ms.openlocfilehash: 42f0be64a6ac050fe8873588263b1faf7e2491a6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710181"
---
# <a name="how-to-add-a-control-to-a-tab-page"></a><span data-ttu-id="6c249-102">Procédure : Ajouter un contrôle à une Page d’onglets</span><span class="sxs-lookup"><span data-stu-id="6c249-102">How to: Add a Control to a Tab Page</span></span>
<span data-ttu-id="6c249-103">Vous pouvez utiliser les formulaires Windows <xref:System.Windows.Forms.TabControl> pour afficher d’autres contrôles dans une structure organisée.</span><span class="sxs-lookup"><span data-stu-id="6c249-103">You can use the Windows Forms <xref:System.Windows.Forms.TabControl> to display other controls in an organized fashion.</span></span> <span data-ttu-id="6c249-104">La procédure suivante montre comment ajouter un bouton pour le premier onglet. Pour plus d’informations sur l’ajout d’une icône dans la partie de l’étiquette d’une page d’onglet, consultez [Comment : Modifier l’apparence du contrôle TabControl Windows Forms](../../../../docs/framework/winforms/controls/how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="6c249-104">The following procedure shows how to add a button to the first tab. For information about adding an icon to the label part of a tab page, see [How to: Change the Appearance of the Windows Forms TabControl](../../../../docs/framework/winforms/controls/how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).</span></span>  
  
### <a name="to-add-a-control-programmatically"></a><span data-ttu-id="6c249-105">Pour ajouter un contrôle par programmation</span><span class="sxs-lookup"><span data-stu-id="6c249-105">To add a control programmatically</span></span>  
  
1.  <span data-ttu-id="6c249-106">Utilisez le <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> méthode de la collection retournée par la <xref:System.Windows.Forms.Control.Controls%2A> propriété du <xref:System.Windows.Forms.TabPage>:</span><span class="sxs-lookup"><span data-stu-id="6c249-106">Use the <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> method of the collection returned by the <xref:System.Windows.Forms.Control.Controls%2A> property of <xref:System.Windows.Forms.TabPage>:</span></span>  
  
     [!code-cpp[TabPageControlCollectionHowToAdd#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cpp/add.cpp#1)]
     [!code-csharp[TabPageControlCollectionHowToAdd#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cs/add.cs#1)]
     [!code-vb[TabPageControlCollectionHowToAdd#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/vb/add.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="6c249-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c249-107">See also</span></span>
- [<span data-ttu-id="6c249-108">TabControl, contrôle</span><span class="sxs-lookup"><span data-stu-id="6c249-108">TabControl Control</span></span>](../../../../docs/framework/winforms/controls/tabcontrol-control-windows-forms.md)
- [<span data-ttu-id="6c249-109">Vue d’ensemble du contrôle TabControl</span><span class="sxs-lookup"><span data-stu-id="6c249-109">TabControl Control Overview</span></span>](../../../../docs/framework/winforms/controls/tabcontrol-control-overview-windows-forms.md)
- [<span data-ttu-id="6c249-110">Guide pratique pour Modifier l’apparence du contrôle TabControl Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6c249-110">How to: Change the Appearance of the Windows Forms TabControl</span></span>](../../../../docs/framework/winforms/controls/how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
- [<span data-ttu-id="6c249-111">Guide pratique pour Désactiver les Pages d’onglets</span><span class="sxs-lookup"><span data-stu-id="6c249-111">How to: Disable Tab Pages</span></span>](../../../../docs/framework/winforms/controls/how-to-disable-tab-pages.md)
- [<span data-ttu-id="6c249-112">Guide pratique pour Ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6c249-112">How to: Add and Remove Tabs with the Windows Forms TabControl</span></span>](../../../../docs/framework/winforms/controls/how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
