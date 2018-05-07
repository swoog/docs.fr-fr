---
title: Vue d'ensemble du composant OpenFileDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- OpenFileDialog
helpviewer_keywords:
- OpenFileDialog component [Windows Forms], about OpenFileDialog
- Open File dialog box [Windows Forms], displaying in Windows Forms
ms.assetid: cd717300-46b6-4f82-8207-b218fa7fa407
ms.openlocfilehash: a49298b2e2cc620ad95e2e0b601a2f49f6ff79d4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="openfiledialog-component-overview-windows-forms"></a>Vue d'ensemble du composant OpenFileDialog (Windows Forms)
Le composant Windows Forms <xref:System.Windows.Forms.OpenFileDialog>  est une boîte de dialogue préconfigurée. Il s’agit du même **ouvrir le fichier** boîte de dialogue exposée par le système d’exploitation Windows. Il hérite de la classe <xref:System.Windows.Forms.CommonDialog>.  
  
## <a name="using-this-component"></a>À l’aide de ce composant  
 Utilisez ce composant dans votre application Windows comme une solution simple pour la sélection de fichier au lieu de configurer votre propre boîte de dialogue. En vous appuyant sur des boîtes de dialogue Windows standard, vous pouvez créer des applications dont la fonction de base est immédiatement familière aux utilisateurs. Cependant, sachez que quand à l’aide de la <xref:System.Windows.Forms.OpenFileDialog> composant, vous devez écrire votre propre logique d’ouverture de fichier.  
  
 Utilisez la <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution. Vous pouvez activer les utilisateurs de sélectionner plusieurs fichiers à ouvrir avec le <xref:System.Windows.Forms.OpenFileDialog.Multiselect%2A> propriété. En outre, vous pouvez utiliser le <xref:System.Windows.Forms.OpenFileDialog.ShowReadOnly%2A> propriété pour déterminer si une case à cocher en lecture seule s’affiche dans la boîte de dialogue. Le <xref:System.Windows.Forms.OpenFileDialog.ReadOnlyChecked%2A> propriété indique si la case à cocher en lecture seule est sélectionnée. Enfin, le <xref:System.Windows.Forms.FileDialog.Filter%2A> propriété définit la chaîne de filtre du nom de fichier actuel, qui détermine les options qui apparaissent dans la zone « Types de fichiers » dans la boîte de dialogue.  
  
 Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.OpenFileDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.OpenFileDialog>  
 [OpenFileDialog, composant](../../../../docs/framework/winforms/controls/openfiledialog-component-windows-forms.md)
