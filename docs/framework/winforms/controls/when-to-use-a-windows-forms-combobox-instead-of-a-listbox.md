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
ms.openlocfilehash: 5dc7778f43c01fd28a14489a7b4179dd851568b2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57702995"
---
# <a name="when-to-use-a-windows-forms-combobox-instead-of-a-listbox"></a>Utilisation d'un contrôle ComboBox Windows Forms à la place d'un contrôle ListBox
Le <xref:System.Windows.Forms.ComboBox> et <xref:System.Windows.Forms.ListBox> contrôles ont des comportements semblables et dans certains cas interchangeables. Il existe, toutefois, un ou l’autre est parfois plus approprié d’une tâche.  
  
 En règle générale, une zone de liste déroulante est appropriée quand il existe une liste de choix proposés, et une zone de liste est appropriée lorsque vous souhaitez limiter l’entrée à ce qui est dans la liste. Une zone de liste déroulante contient un champ de zone de texte, choix pas dans la liste peut être tapés dans. L’exception est levée quand le <xref:System.Windows.Forms.ComboBox.DropDownStyle%2A> propriété est définie sur <xref:System.Windows.Forms.ComboBoxStyle.DropDownList>. Dans ce cas, le contrôle sélectionne un élément si vous tapez sa première lettre.  
  
 En outre, zones de liste déroulante économiser de l’espace sur un formulaire. Étant donné que la liste complète n’est pas affichée jusqu'à ce que l’utilisateur clique sur la flèche vers le bas, une zone de liste déroulante permettre facilement tenir dans un petit espace dans lequel une zone de liste n’est pas compatible. Une exception est levée quand le <xref:System.Windows.Forms.ComboBox.DropDownStyle%2A> propriété est définie sur <xref:System.Windows.Forms.ComboBoxStyle.Simple>: la liste complète est affichée et la zone de liste déroulante occupe plus de place que serait une zone de liste.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- [Guide pratique pour Ajouter et supprimer des éléments d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle](add-and-remove-items-from-a-wf-combobox.md)
- [Guide pratique pour Trier le contenu d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle](sort-the-contents-of-a-wf-combobox-listbox-or-checkedlistbox-control.md)
- [Contrôles Windows Forms utilisés pour l’affichage de listes d’options](windows-forms-controls-used-to-list-options.md)
