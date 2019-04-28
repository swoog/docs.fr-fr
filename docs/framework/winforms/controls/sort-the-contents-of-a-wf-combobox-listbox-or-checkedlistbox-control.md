---
title: 'Procédure : trier le contenu d’un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- CheckedListBox control [Windows Forms], sorting
- ComboBox control [Windows Forms], sorting contents
- combo boxes [Windows Forms], sorting contents
- list boxes [Windows Forms], sorting contents
- ListBox control [Windows Forms], sorting contents
ms.assetid: c268e387-3d1d-4d86-a940-19f6673c8d06
ms.openlocfilehash: bd26d396c238bfc53858320b8f4487df84b3436a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61902991"
---
# <a name="how-to-sort-the-contents-of-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="2b7ca-102">Procédure : trier le contenu d’un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2b7ca-102">How to: Sort the Contents of a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>
<span data-ttu-id="2b7ca-103">Contrôles Windows Forms ne pas trier lorsqu’ils sont liés aux données.</span><span class="sxs-lookup"><span data-stu-id="2b7ca-103">Windows Forms controls do not sort when they are data-bound.</span></span> <span data-ttu-id="2b7ca-104">Pour afficher les données triées, utilisez une source de données qui prend en charge le tri et puis ont la source de données à trier.</span><span class="sxs-lookup"><span data-stu-id="2b7ca-104">To display sorted data, use a data source that supports sorting and then have the data source sort it.</span></span> <span data-ttu-id="2b7ca-105">Les sources de données qui prennent en charge le tri sont les vues de données, les gestionnaires de vues de données et les tableaux triés.</span><span class="sxs-lookup"><span data-stu-id="2b7ca-105">Data sources that support sorting are data views, data view managers, and sorted arrays.</span></span>  
  
 <span data-ttu-id="2b7ca-106">Si le contrôle n’est pas lié aux données, vous pouvez les trier.</span><span class="sxs-lookup"><span data-stu-id="2b7ca-106">If the control is not data-bound, you can sort it.</span></span>  
  
### <a name="to-sort-the-list"></a><span data-ttu-id="2b7ca-107">Pour trier la liste</span><span class="sxs-lookup"><span data-stu-id="2b7ca-107">To sort the list</span></span>  
  
1. <span data-ttu-id="2b7ca-108">Affectez à la propriété `Sorted` la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="2b7ca-108">Set the `Sorted` property to `true`.</span></span>  
  
     <span data-ttu-id="2b7ca-109">Ce paramètre repositionne tous les éléments de liste existants dans un ordre trié.</span><span class="sxs-lookup"><span data-stu-id="2b7ca-109">This setting repositions all existing list items in sorted order.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b7ca-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b7ca-110">See also</span></span>

- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [<span data-ttu-id="2b7ca-111">Liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2b7ca-111">Windows Forms Data Binding</span></span>](../windows-forms-data-binding.md)
- [<span data-ttu-id="2b7ca-112">Guide pratique pour Ajouter et supprimer des éléments d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="2b7ca-112">How to: Add and Remove Items from a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>](add-and-remove-items-from-a-wf-combobox.md)
- [<span data-ttu-id="2b7ca-113">Utilisation d'un contrôle ComboBox Windows Forms à la place d'un contrôle ListBox</span><span class="sxs-lookup"><span data-stu-id="2b7ca-113">When to Use a Windows Forms ComboBox Instead of a ListBox</span></span>](when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)
- [<span data-ttu-id="2b7ca-114">Contrôles Windows Forms utilisés pour l’affichage de listes d’options</span><span class="sxs-lookup"><span data-stu-id="2b7ca-114">Windows Forms Controls Used to List Options</span></span>](windows-forms-controls-used-to-list-options.md)
