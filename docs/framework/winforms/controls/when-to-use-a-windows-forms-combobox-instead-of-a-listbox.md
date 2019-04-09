---
title: Utilisation d'un contrôle ComboBox Windows Forms à la place d'un contrôle ListBox
ms.date: 03/30/2017
helpviewer_keywords:
- ListBox control [Windows Forms], adding and removing items
- ListBox control [Windows Forms], vs. ComboBox
- bound controls [Windows Forms], combo boxes
- Windows Forms controls, data binding
- ComboBox control [Windows Forms], compared to ListBox
- combo boxes [Windows Forms], compared to list boxes
- ListBox control [Windows Forms], accessing items
- ListCount property
ms.assetid: 7bcaea58-1cfa-46db-9baf-b75a69d8f9ec
ms.openlocfilehash: 8a2429049acf1a22edde8d132ece17da4e91f1db
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59111421"
---
# <a name="when-to-use-a-windows-forms-combobox-instead-of-a-listbox"></a><span data-ttu-id="c3d6c-102">Utilisation d'un contrôle ComboBox Windows Forms à la place d'un contrôle ListBox</span><span class="sxs-lookup"><span data-stu-id="c3d6c-102">When to Use a Windows Forms ComboBox Instead of a ListBox</span></span>
<span data-ttu-id="c3d6c-103">Le <xref:System.Windows.Forms.ComboBox> et <xref:System.Windows.Forms.ListBox> contrôles ont des comportements semblables et dans certains cas interchangeables.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-103">The <xref:System.Windows.Forms.ComboBox> and the <xref:System.Windows.Forms.ListBox> controls have similar behaviors, and in some cases may be interchangeable.</span></span> <span data-ttu-id="c3d6c-104">Il existe, toutefois, un ou l’autre est parfois plus approprié d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-104">There are times, however, when one or the other is more appropriate to a task.</span></span>  
  
 <span data-ttu-id="c3d6c-105">En règle générale, une zone de liste déroulante est appropriée quand il existe une liste de choix proposés, et une zone de liste est appropriée lorsque vous souhaitez limiter l’entrée à ce qui est dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-105">Generally, a combo box is appropriate when there is a list of suggested choices, and a list box is appropriate when you want to limit input to what is on the list.</span></span> <span data-ttu-id="c3d6c-106">Une zone de liste déroulante contient un champ de zone de texte, choix pas dans la liste peut être tapés dans.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-106">A combo box contains a text box field, so choices not on the list can be typed in.</span></span> <span data-ttu-id="c3d6c-107">L’exception est levée quand le <xref:System.Windows.Forms.ComboBox.DropDownStyle%2A> propriété est définie sur <xref:System.Windows.Forms.ComboBoxStyle.DropDownList>.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-107">The exception is when the <xref:System.Windows.Forms.ComboBox.DropDownStyle%2A> property is set to <xref:System.Windows.Forms.ComboBoxStyle.DropDownList>.</span></span> <span data-ttu-id="c3d6c-108">Dans ce cas, le contrôle sélectionne un élément si vous tapez sa première lettre.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-108">In that case, the control will select an item if you type its first letter.</span></span>  
  
 <span data-ttu-id="c3d6c-109">En outre, zones de liste déroulante économiser de l’espace sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-109">In addition, combo boxes save space on a form.</span></span> <span data-ttu-id="c3d6c-110">Étant donné que la liste complète n’est pas affichée jusqu'à ce que l’utilisateur clique sur la flèche vers le bas, une zone de liste déroulante permettre facilement tenir dans un petit espace dans lequel une zone de liste n’est pas compatible.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-110">Because the full list is not displayed until the user clicks the down arrow, a combo box can easily fit in a small space where a list box would not fit.</span></span> <span data-ttu-id="c3d6c-111">Une exception est levée quand le <xref:System.Windows.Forms.ComboBox.DropDownStyle%2A> propriété est définie sur <xref:System.Windows.Forms.ComboBoxStyle.Simple>: la liste complète est affichée et la zone de liste déroulante occupe plus de place que serait une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="c3d6c-111">An exception is when the <xref:System.Windows.Forms.ComboBox.DropDownStyle%2A> property is set to <xref:System.Windows.Forms.ComboBoxStyle.Simple>: the full list is displayed, and the combo box takes up more room than a list box would.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3d6c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3d6c-112">See also</span></span>

- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- [<span data-ttu-id="c3d6c-113">Procédure : ajouter et supprimer des éléments dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c3d6c-113">How to: Add and Remove Items from a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>](add-and-remove-items-from-a-wf-combobox.md)
- [<span data-ttu-id="c3d6c-114">Procédure : trier le contenu d’un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c3d6c-114">How to: Sort the Contents of a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>](sort-the-contents-of-a-wf-combobox-listbox-or-checkedlistbox-control.md)
- [<span data-ttu-id="c3d6c-115">Contrôles Windows Forms utilisés pour l'affichage de listes d'options</span><span class="sxs-lookup"><span data-stu-id="c3d6c-115">Windows Forms Controls Used to List Options</span></span>](windows-forms-controls-used-to-list-options.md)
