---
title: "Comment : charger une image à l'aide du concepteur (Windows Forms)"
ms.date: 03/30/2017
helpviewer_keywords:
- picture formats
- images [Windows Forms], displaying on Windows Forms
- pictures [Windows Forms], displaying
- forms [Windows Forms], displaying images
- PictureBox control [Windows Forms], adding pictures
ms.assetid: 4dc7b973-afb1-4276-8322-20825af96655
ms.openlocfilehash: e01e5d1dc0fad8171e705e85debc2b15d6a506eb
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43466532"
---
# <a name="how-to-load-a-picture-using-the-designer-windows-forms"></a>Comment : charger une image à l'aide du concepteur (Windows Forms)
Avec les formulaires Windows <xref:System.Windows.Forms.PictureBox> contrôle, vous pouvez charger et afficher une image sur un formulaire au moment du design en définissant le <xref:System.Windows.Forms.PictureBox.Image%2A> propriété à une image valide. Le tableau suivant présente les types de fichier acceptables.  
  
|Type|Extension de nom de fichier|  
|----------|-------------------------|  
|Bitmap|.bmp|  
|Icône|.ico|  
|GIF|.gif|  
|Métafichier|.wmf|  
|JPEG|.jpg|  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-display-a-picture-at-design-time"></a>Pour afficher une image au moment du design  
  
1.  Dessiner un <xref:System.Windows.Forms.PictureBox> contrôle sur un formulaire.  
  
2.  Dans la fenêtre Propriétés, sélectionnez le <xref:System.Windows.Forms.PictureBox.Image%2A> propriété, puis cliquez sur le bouton de sélection pour afficher la **Open** boîte de dialogue.  
  
3.  Si vous recherchez un type de fichier spécifique (par exemple, des fichiers .gif), sélectionnez-le dans la **fichiers de type** boîte.  
  
4.  Sélectionnez le fichier que vous souhaitez afficher.  
  
### <a name="to-clear-the-picture-at-design-time"></a>Pour effacer l’image au moment du design  
  
1.  Sur le **propriétés** fenêtre, sélectionnez le <xref:System.Windows.Forms.PictureBox.Image%2A> propriété et clic droit de l’image miniature qui s’affiche à gauche du nom de l’objet image. Choisissez **réinitialiser**.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.PictureBox>  
 [Vue d’ensemble du contrôle PictureBox](../../../../docs/framework/winforms/controls/picturebox-control-overview-windows-forms.md)  
 [Guide pratique pour modifier la taille ou l'emplacement d'une image au moment de l'exécution](../../../../docs/framework/winforms/controls/how-to-modify-the-size-or-placement-of-a-picture-at-run-time-windows-forms.md)  
 [Guide pratique pour définir des images au moment de l'exécution](../../../../docs/framework/winforms/controls/how-to-set-pictures-at-run-time-windows-forms.md)  
 [PictureBox, contrôle](../../../../docs/framework/winforms/controls/picturebox-control-windows-forms.md)
