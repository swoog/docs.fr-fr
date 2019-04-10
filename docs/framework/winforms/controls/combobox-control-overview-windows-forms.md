---
title: Vue d'ensemble du contrôle ComboBox (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ComboBox
helpviewer_keywords:
- drop-down lists [Windows Forms], Windows Forms
- ComboBox control [Windows Forms], about ComboBox control
- drop-down lists [Windows Forms], ComboBox control
- combo boxes [Windows Forms], about combo boxes
ms.assetid: a58b393f-a614-45d1-8961-857a024b5acd
ms.openlocfilehash: 80056771744c9b97828a024adf32638e545a839e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59211571"
---
# <a name="combobox-control-overview-windows-forms"></a>Vue d'ensemble du contrôle ComboBox (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.ComboBox> contrôle est utilisé pour afficher des données dans une zone de liste déroulante modifiable. Par défaut, le <xref:System.Windows.Forms.ComboBox> contrôle s’affiche en deux parties : la partie supérieure est une zone de texte qui permet à l’utilisateur à entrer un élément de liste. La deuxième partie est une zone de liste qui affiche une liste d’éléments à partir de laquelle l’utilisateur peut sélectionner une. Pour plus d’informations sur d’autres styles de zone de liste déroulante, consultez [quand utiliser un contrôle ComboBox Instead of un contrôle ListBox Windows Forms](when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md).  
  
 Le <xref:System.Windows.Forms.ComboBox.SelectedIndex%2A> propriété retourne une valeur entière qui correspond à l’élément de liste sélectionné. Vous pouvez modifier par programmation de l’élément sélectionné en modifiant la <xref:System.Windows.Forms.ComboBox.SelectedIndex%2A> valeur dans le code ; l’élément correspondant dans la liste s’affiche dans la zone de texte de la zone de liste déroulante. Si aucun élément n’est sélectionné, le <xref:System.Windows.Forms.ComboBox.SelectedIndex%2A> valeur est -1. Si le premier élément dans la liste est sélectionné, puis le <xref:System.Windows.Forms.ComboBox.SelectedIndex%2A> valeur est 0. Le <xref:System.Windows.Forms.ComboBox.SelectedItem%2A> propriété est similaire à <xref:System.Windows.Forms.ComboBox.SelectedIndex%2A> , mais retourne l’élément lui-même, en général une valeur de chaîne. Le <xref:System.Windows.Forms.ComboBox.ObjectCollection.Count%2A> propriété reflète le nombre d’éléments dans la liste et la valeur de la <xref:System.Windows.Forms.ComboBox.ObjectCollection.Count%2A> propriété est toujours un plus que la plus grande possible <xref:System.Windows.Forms.ComboBox.SelectedIndex%2A> valeur car <xref:System.Windows.Forms.ComboBox.SelectedIndex%2A> est de base zéro.  
  
 Pour ajouter ou supprimer des éléments dans un <xref:System.Windows.Forms.ComboBox> contrôler, utilisez le <xref:System.Windows.Forms.ComboBox.ObjectCollection.Add%2A>, <xref:System.Windows.Forms.ComboBox.ObjectCollection.Insert%2A>, <xref:System.Windows.Forms.ComboBox.ObjectCollection.Clear%2A> ou <xref:System.Windows.Forms.ComboBox.ObjectCollection.Remove%2A> (méthode). Vous pouvez également ajouter des éléments à la liste à l’aide de la <xref:System.Windows.Forms.ComboBox.Items%2A> propriété dans le concepteur.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ComboBox>
- [Vue d’ensemble du contrôle ListBox](listbox-control-overview-windows-forms.md)
- [Utilisation d'un contrôle ComboBox Windows Forms à la place d'un contrôle ListBox](when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)
- [Procédure : ajouter et supprimer des éléments dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms](add-and-remove-items-from-a-wf-combobox.md)
- [Procédure : trier le contenu d’un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms](sort-the-contents-of-a-wf-combobox-listbox-or-checkedlistbox-control.md)
- [Procédure : accéder à des éléments spécifiques dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms](access-specific-items-in-a-wf-combobox-listbox-or-checkedlistbox.md)
- [Procédure : lier un contrôle ComboBox ou ListBox Windows Forms à des données](how-to-bind-a-windows-forms-combobox-or-listbox-control-to-data.md)
- [Contrôles Windows Forms utilisés pour l'affichage de listes d'options](windows-forms-controls-used-to-list-options.md)
- [Procédure : créer une table de choix pour un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms](create-a-lookup-table-for-a-wf-combobox-listbox.md)
