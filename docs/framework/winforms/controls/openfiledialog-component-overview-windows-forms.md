---
title: Vue d'ensemble du composant OpenFileDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- OpenFileDialog
helpviewer_keywords:
- OpenFileDialog component [Windows Forms], about OpenFileDialog
- Open File dialog box [Windows Forms], displaying in Windows Forms
ms.assetid: cd717300-46b6-4f82-8207-b218fa7fa407
ms.openlocfilehash: 1aea4466fd66d84e5c6ede74ecb46d6d659db8d5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564264"
---
# <a name="openfiledialog-component-overview-windows-forms"></a>Vue d'ensemble du composant OpenFileDialog (Windows Forms)
Le composant Windows Forms <xref:System.Windows.Forms.OpenFileDialog>  est une boîte de dialogue préconfigurée. Il est identique à **ouvrir un fichier** boîte de dialogue exposée par le système d’exploitation Windows. Il hérite de la classe <xref:System.Windows.Forms.CommonDialog>.  
  
## <a name="using-this-component"></a>À l’aide de ce composant  
 Utiliser ce composant dans votre application Windows comme une solution simple pour la sélection de fichier au lieu de configurer votre propre boîte de dialogue. En vous appuyant sur des boîtes de dialogue Windows standard, vous pouvez créer des applications dont la fonction de base est immédiatement familière aux utilisateurs. Cependant, sachez qu’au moment où à l’aide de la <xref:System.Windows.Forms.OpenFileDialog> composant, vous devez écrire votre propre logique d’ouverture de fichier.  
  
 Utilisez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution. Vous pouvez autoriser les utilisateurs à sélectionner plusieurs fichiers à ouvrir avec le <xref:System.Windows.Forms.OpenFileDialog.Multiselect%2A> propriété. En outre, vous pouvez utiliser le <xref:System.Windows.Forms.OpenFileDialog.ShowReadOnly%2A> propriété afin de déterminer si une case à cocher en lecture seule s’affiche dans la boîte de dialogue. Le <xref:System.Windows.Forms.OpenFileDialog.ReadOnlyChecked%2A> propriété indique si la case à cocher en lecture seule est sélectionnée. Enfin, le <xref:System.Windows.Forms.FileDialog.Filter%2A> propriété définit la chaîne de filtre du nom de fichier actuel, qui détermine les choix qui s’affichent dans la zone « Fichiers de type » dans la boîte de dialogue.  
  
 Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.OpenFileDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.OpenFileDialog>
- [OpenFileDialog, composant](../../../../docs/framework/winforms/controls/openfiledialog-component-windows-forms.md)
