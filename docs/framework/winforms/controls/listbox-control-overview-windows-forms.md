---
title: Vue d'ensemble du contrôle ListBox (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ListBox
helpviewer_keywords:
- list boxes [Windows Forms], about list boxes
- ListBox control [Windows Forms], about ListBox control
ms.assetid: 37ea226b-6fc8-4c70-936a-c6af4e0cad4c
ms.openlocfilehash: 2bba90f704458e1c724328feccaaf6f04b98ecb4
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723983"
---
# <a name="listbox-control-overview-windows-forms"></a>Vue d'ensemble du contrôle ListBox (Windows Forms)
Un formulaire Windows <xref:System.Windows.Forms.ListBox> contrôle affiche une liste à partir de laquelle l’utilisateur peut sélectionner un ou plusieurs éléments. Si le nombre total d’éléments dépasse le nombre qui peut être affiché, une barre de défilement est automatiquement ajoutée à la <xref:System.Windows.Forms.ListBox> contrôle. Lorsque le <xref:System.Windows.Forms.ListBox.MultiColumn%2A> propriété est définie sur `true`, la zone de liste affiche les éléments dans plusieurs colonnes et une barre de défilement horizontale s’affiche. Lorsque le <xref:System.Windows.Forms.ListBox.MultiColumn%2A> propriété est définie sur `false`, la zone de liste affiche les éléments dans une seule colonne et une barre de défilement verticale s’affiche. Lorsque <xref:System.Windows.Forms.ListBox.ScrollAlwaysVisible%2A> est défini sur `true`, la barre de défilement s’affiche, quel que soit le nombre d’éléments. Le <xref:System.Windows.Forms.ListBox.SelectionMode%2A> propriété détermine le nombre d’éléments peut être sélectionné simultanément.  
  
## <a name="ways-to-change-the-listbox-control"></a>Moyens de modifier le contrôle ListBox  
 Le <xref:System.Windows.Forms.ListBox.SelectedIndex%2A> propriété retourne une valeur entière qui correspond au premier élément sélectionné dans la zone de liste. Vous pouvez modifier par programmation de l’élément sélectionné en modifiant la <xref:System.Windows.Forms.ListBox.SelectedIndex%2A> valeur dans le code ; l’élément correspondant dans la liste s’affiche en surbrillance sur le formulaire Windows. Si aucun élément n’est sélectionné, le <xref:System.Windows.Forms.ListBox.SelectedIndex%2A> valeur est -1. Si le premier élément dans la liste est sélectionné, le <xref:System.Windows.Forms.ListBox.SelectedIndex%2A> valeur est 0. Lorsque plusieurs éléments sont sélectionnés, le <xref:System.Windows.Forms.ListBox.SelectedIndex%2A> valeur reflète l’élément sélectionné qui apparaît en premier dans la liste. Le <xref:System.Windows.Forms.ListBox.SelectedItem%2A> propriété est similaire à <xref:System.Windows.Forms.ListBox.SelectedIndex%2A>, mais retourne l’élément lui-même, en général une valeur de chaîne. Le <xref:System.Windows.Forms.ListBox.ObjectCollection.Count%2A> propriété reflète le nombre d’éléments dans la liste et la valeur de la <xref:System.Windows.Forms.ListBox.ObjectCollection.Count%2A> propriété est toujours un plus que la plus grande possible <xref:System.Windows.Forms.ListBox.SelectedIndex%2A> valeur car <xref:System.Windows.Forms.ListBox.SelectedIndex%2A> est de base zéro.  
  
 Pour ajouter ou supprimer des éléments dans un <xref:System.Windows.Forms.ListBox> contrôler, utilisez le <xref:System.Windows.Forms.ListBox.ObjectCollection.Add%2A>, <xref:System.Windows.Forms.ListBox.ObjectCollection.Insert%2A>, <xref:System.Windows.Forms.ListBox.ObjectCollection.Clear%2A> ou <xref:System.Windows.Forms.ListBox.ObjectCollection.Remove%2A> (méthode). Vous pouvez également ajouter des éléments à la liste à l’aide de la <xref:System.Windows.Forms.ListBox.Items%2A> propriété au moment du design.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ListBox>
- [Guide pratique pour Ajouter et supprimer des éléments d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle](add-and-remove-items-from-a-wf-combobox.md)
- [Guide pratique pour Trier le contenu d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle](sort-the-contents-of-a-wf-combobox-listbox-or-checkedlistbox-control.md)
- [Guide pratique pour Lier un contrôle ComboBox de Windows Forms ou d’un contrôle ListBox à des données](how-to-bind-a-windows-forms-combobox-or-listbox-control-to-data.md)
- [Vue d'ensemble du contrôle ComboBox](combobox-control-overview-windows-forms.md)
- [Vue d'ensemble du contrôle CheckedListBox](checkedlistbox-control-overview-windows-forms.md)
- [Contrôles Windows Forms utilisés pour l’affichage de listes d’options](windows-forms-controls-used-to-list-options.md)
- [Guide pratique pour Créer une Table de recherche pour un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle](create-a-lookup-table-for-a-wf-combobox-listbox.md)
