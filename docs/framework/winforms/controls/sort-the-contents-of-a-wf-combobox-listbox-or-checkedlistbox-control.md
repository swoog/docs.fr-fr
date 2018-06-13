---
title: "Comment : trier le contenu d'un contrôle ComboBox, CheckedListBox ou ListBox Windows Forms"
ms.date: 03/30/2017
helpviewer_keywords:
- CheckedListBox control [Windows Forms], sorting
- ComboBox control [Windows Forms], sorting contents
- combo boxes [Windows Forms], sorting contents
- list boxes [Windows Forms], sorting contents
- ListBox control [Windows Forms], sorting contents
ms.assetid: c268e387-3d1d-4d86-a940-19f6673c8d06
ms.openlocfilehash: 8b8f9c7ad0ad7d3bbb7f3eeffd44e555207b82c4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33535644"
---
# <a name="how-to-sort-the-contents-of-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="fbf3d-102">Comment : trier le contenu d'un contrôle ComboBox, CheckedListBox ou ListBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fbf3d-102">How to: Sort the Contents of a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>
<span data-ttu-id="fbf3d-103">Contrôles Windows Forms ne triez pas lorsqu’ils sont liés aux données.</span><span class="sxs-lookup"><span data-stu-id="fbf3d-103">Windows Forms controls do not sort when they are data-bound.</span></span> <span data-ttu-id="fbf3d-104">Pour afficher les données triées, utilisez une source de données qui prend en charge le tri et devez ensuite trier la source de données.</span><span class="sxs-lookup"><span data-stu-id="fbf3d-104">To display sorted data, use a data source that supports sorting and then have the data source sort it.</span></span> <span data-ttu-id="fbf3d-105">Les sources de données qui prennent en charge le tri sont les vues de données, les gestionnaires de vues de données et les tableaux triés.</span><span class="sxs-lookup"><span data-stu-id="fbf3d-105">Data sources that support sorting are data views, data view managers, and sorted arrays.</span></span>  
  
 <span data-ttu-id="fbf3d-106">Si le contrôle n’est pas lié aux données, vous pouvez les trier.</span><span class="sxs-lookup"><span data-stu-id="fbf3d-106">If the control is not data-bound, you can sort it.</span></span>  
  
### <a name="to-sort-the-list"></a><span data-ttu-id="fbf3d-107">Pour trier la liste</span><span class="sxs-lookup"><span data-stu-id="fbf3d-107">To sort the list</span></span>  
  
1.  <span data-ttu-id="fbf3d-108">Affectez à la propriété `Sorted` la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="fbf3d-108">Set the `Sorted` property to `true`.</span></span>  
  
     <span data-ttu-id="fbf3d-109">Ce paramètre repositionne tous les éléments de liste existants dans un ordre trié.</span><span class="sxs-lookup"><span data-stu-id="fbf3d-109">This setting repositions all existing list items in sorted order.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fbf3d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf3d-110">See Also</span></span>  
 <xref:System.Windows.Forms.ComboBox>  
 <xref:System.Windows.Forms.ListBox>  
 <xref:System.Windows.Forms.CheckedListBox>  
 [<span data-ttu-id="fbf3d-111">Liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fbf3d-111">Windows Forms Data Binding</span></span>](../../../../docs/framework/winforms/windows-forms-data-binding.md)  
 [<span data-ttu-id="fbf3d-112">Guide pratique pour ajouter et supprimer des éléments d'un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fbf3d-112">How to: Add and Remove Items from a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>](../../../../docs/framework/winforms/controls/add-and-remove-items-from-a-wf-combobox.md)  
 [<span data-ttu-id="fbf3d-113">Utilisation d'un contrôle ComboBox Windows Forms à la place d'un contrôle ListBox</span><span class="sxs-lookup"><span data-stu-id="fbf3d-113">When to Use a Windows Forms ComboBox Instead of a ListBox</span></span>](../../../../docs/framework/winforms/controls/when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)  
 [<span data-ttu-id="fbf3d-114">Contrôles Windows Forms utilisés pour l’affichage de listes d’options</span><span class="sxs-lookup"><span data-stu-id="fbf3d-114">Windows Forms Controls Used to List Options</span></span>](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
