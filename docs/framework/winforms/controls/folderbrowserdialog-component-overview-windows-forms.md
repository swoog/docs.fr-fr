---
title: Vue d’ensemble du composant FolderBrowserDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- FolderBrowserDialog
helpviewer_keywords:
- FolderBrowserDialog component [Windows Forms], about FolderBrowserDialog
- directories [Windows Forms], enabling browsing in applications
- folders [Windows Forms], enabling browsing in applications
ms.assetid: 796b622c-3ba9-4356-93bb-e217fc52f2c7
ms.openlocfilehash: a735749698266ac20e2ea9ee5569fd210ee9977b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="folderbrowserdialog-component-overview-windows-forms"></a>Vue d’ensemble du composant FolderBrowserDialog (Windows Forms)
Windows Forms <xref:System.Windows.Forms.FolderBrowserDialog> composant est une boîte de dialogue modale qui est utilisée pour parcourir et sélectionner des dossiers. Nouveaux dossiers peuvent également être créés dans le <xref:System.Windows.Forms.FolderBrowserDialog> composant.  
  
> [!NOTE]
>  Pour sélectionner des fichiers, dossiers, au lieu d’utiliser le [OpenFileDialog](../../../../docs/framework/winforms/controls/openfiledialog-component-windows-forms.md) composant.  
  
 Le <xref:System.Windows.Forms.FolderBrowserDialog> composant s’affiche au moment de l’exécution à l’aide du <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode). Définir le <xref:System.Windows.Forms.FolderBrowserDialog.RootFolder%2A> propriété pour déterminer le dossier supérieur et tous les sous-dossiers qui seront affichent dans l’arborescence de la boîte de dialogue. Une fois la boîte de dialogue a été affichée, vous pouvez utiliser le <xref:System.Windows.Forms.FolderBrowserDialog.SelectedPath%2A> propriété à obtenir le chemin d’accès du dossier qui a été sélectionné.  
  
 Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.FolderBrowserDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.FolderBrowserDialog>  
 [Guide pratique pour sélectionner des dossiers avec le composant FolderBrowserDialog Windows Forms](../../../../docs/framework/winforms/controls/how-to-choose-folders-with-the-windows-forms-folderbrowserdialog-component.md)  
 [FolderBrowserDialog, composant](../../../../docs/framework/winforms/controls/folderbrowserdialog-component-windows-forms.md)
