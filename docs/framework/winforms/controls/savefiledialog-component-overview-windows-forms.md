---
title: Vue d'ensemble du composant SaveFileDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- SaveFileDialog
helpviewer_keywords:
- Save File dialog box [Windows Forms], displaying
- SaveFileDialog component [Windows Forms], about SaveFileDialog
ms.assetid: be7a625f-46fd-4d06-9985-b613dcbf9bd2
ms.openlocfilehash: 93bf0f63e18ee3a384aa062c80faa991b68a6abe
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57721500"
---
# <a name="savefiledialog-component-overview-windows-forms"></a>Vue d'ensemble du composant SaveFileDialog (Windows Forms)
Le composant Windows Forms <xref:System.Windows.Forms.SaveFileDialog>  est une boîte de dialogue préconfigurée. Il est identique à la norme **enregistrer le fichier** boîte de dialogue utilisée par Windows. Il hérite de la classe <xref:System.Windows.Forms.CommonDialog>.  
  
## <a name="working-with-the-savefiledialog-component"></a>Utilisation du composant SaveFileDialog  
 Utilisez-la comme une solution simple pour permettre aux utilisateurs d’enregistrer des fichiers au lieu de configurer votre propre boîte de dialogue. En vous appuyant sur les boîtes de dialogue Windows standards, les fonctionnalités de base des applications que vous créez sont immédiatement familière aux utilisateurs. Cependant, sachez qu’au moment où à l’aide de la <xref:System.Windows.Forms.SaveFileDialog> composant, vous devez écrire votre propre logique d’enregistrement du fichier.  
  
 Vous pouvez utiliser la <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution. Vous pouvez ouvrir un fichier en mode lecture/écriture à l’aide du <xref:System.Windows.Forms.SaveFileDialog.OpenFile%2A> (méthode).  
  
 Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.SaveFileDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.SaveFileDialog>
- [SaveFileDialog, composant](savefiledialog-component-windows-forms.md)
