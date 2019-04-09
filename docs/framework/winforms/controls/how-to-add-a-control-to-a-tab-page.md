---
title: 'Procédure : ajouter un contrôle à un onglet'
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
ms.openlocfilehash: b42845ab996c0985fe6a48ac588e6d706905faac
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195850"
---
# <a name="how-to-add-a-control-to-a-tab-page"></a><span data-ttu-id="29f27-102">Procédure : ajouter un contrôle à un onglet</span><span class="sxs-lookup"><span data-stu-id="29f27-102">How to: Add a Control to a Tab Page</span></span>
<span data-ttu-id="29f27-103">Vous pouvez utiliser les formulaires Windows <xref:System.Windows.Forms.TabControl> pour afficher d’autres contrôles dans une structure organisée.</span><span class="sxs-lookup"><span data-stu-id="29f27-103">You can use the Windows Forms <xref:System.Windows.Forms.TabControl> to display other controls in an organized fashion.</span></span> <span data-ttu-id="29f27-104">La procédure suivante montre comment ajouter un bouton pour le premier onglet. Pour plus d’informations sur l’ajout d’une icône dans la partie de l’étiquette d’une page d’onglet, consultez [Comment : Modifier l’apparence du contrôle TabControl Windows Forms](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="29f27-104">The following procedure shows how to add a button to the first tab. For information about adding an icon to the label part of a tab page, see [How to: Change the Appearance of the Windows Forms TabControl](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).</span></span>  
  
### <a name="to-add-a-control-programmatically"></a><span data-ttu-id="29f27-105">Pour ajouter un contrôle par programmation</span><span class="sxs-lookup"><span data-stu-id="29f27-105">To add a control programmatically</span></span>  
  
1.  <span data-ttu-id="29f27-106">Utilisez le <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> méthode de la collection retournée par la <xref:System.Windows.Forms.Control.Controls%2A> propriété du <xref:System.Windows.Forms.TabPage>:</span><span class="sxs-lookup"><span data-stu-id="29f27-106">Use the <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> method of the collection returned by the <xref:System.Windows.Forms.Control.Controls%2A> property of <xref:System.Windows.Forms.TabPage>:</span></span>  
  
     [!code-cpp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/cpp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cpp/add.cpp#1)]
     [!code-csharp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/csharp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cs/add.cs#1)]
     [!code-vb[TabPageControlCollectionHowToAdd#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/vb/add.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="29f27-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29f27-107">See also</span></span>

- [<span data-ttu-id="29f27-108">TabControl, contrôle</span><span class="sxs-lookup"><span data-stu-id="29f27-108">TabControl Control</span></span>](tabcontrol-control-windows-forms.md)
- [<span data-ttu-id="29f27-109">Vue d’ensemble du contrôle TabControl</span><span class="sxs-lookup"><span data-stu-id="29f27-109">TabControl Control Overview</span></span>](tabcontrol-control-overview-windows-forms.md)
- [<span data-ttu-id="29f27-110">Procédure : modifier l’aspect du contrôle TabControl Windows Forms</span><span class="sxs-lookup"><span data-stu-id="29f27-110">How to: Change the Appearance of the Windows Forms TabControl</span></span>](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
- [<span data-ttu-id="29f27-111">Procédure : désactiver des onglets</span><span class="sxs-lookup"><span data-stu-id="29f27-111">How to: Disable Tab Pages</span></span>](how-to-disable-tab-pages.md)
- [<span data-ttu-id="29f27-112">Procédure : ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="29f27-112">How to: Add and Remove Tabs with the Windows Forms TabControl</span></span>](how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
