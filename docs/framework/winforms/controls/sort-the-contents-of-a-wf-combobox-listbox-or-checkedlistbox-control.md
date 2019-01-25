---
title: 'Procédure : Trier le contenu d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle'
ms.date: 03/30/2017
helpviewer_keywords:
- CheckedListBox control [Windows Forms], sorting
- ComboBox control [Windows Forms], sorting contents
- combo boxes [Windows Forms], sorting contents
- list boxes [Windows Forms], sorting contents
- ListBox control [Windows Forms], sorting contents
ms.assetid: c268e387-3d1d-4d86-a940-19f6673c8d06
ms.openlocfilehash: 97965dcef1541aec51ba57a7cf314730f892f141
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54686320"
---
# <a name="how-to-sort-the-contents-of-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a>Procédure : Trier le contenu d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle
Contrôles Windows Forms ne pas trier lorsqu’ils sont liés aux données. Pour afficher les données triées, utilisez une source de données qui prend en charge le tri et puis ont la source de données à trier. Les sources de données qui prennent en charge le tri sont les vues de données, les gestionnaires de vues de données et les tableaux triés.  
  
 Si le contrôle n’est pas lié aux données, vous pouvez les trier.  
  
### <a name="to-sort-the-list"></a>Pour trier la liste  
  
1.  Affectez à la propriété `Sorted` la valeur `true`.  
  
     Ce paramètre repositionne tous les éléments de liste existants dans un ordre trié.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [Liaison de données Windows Forms](../../../../docs/framework/winforms/windows-forms-data-binding.md)
- [Guide pratique pour Ajouter et supprimer des éléments d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle](../../../../docs/framework/winforms/controls/add-and-remove-items-from-a-wf-combobox.md)
- [Utilisation d'un contrôle ComboBox Windows Forms à la place d'un contrôle ListBox](../../../../docs/framework/winforms/controls/when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)
- [Contrôles Windows Forms utilisés pour l’affichage de listes d’options](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
