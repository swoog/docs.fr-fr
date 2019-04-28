---
title: 'Procédure : déplacer un ToolStrip hors d’un ToolStripContainer dans un formulaire'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStrip control [Windows Forms], parenting to forms
- Windows Forms, parenting ToolStrip controls
ms.assetid: a1c94a7f-6fc5-4e4c-84cf-ff11dc573d33
ms.openlocfilehash: 9106a69ea9f28442da6e3270f7cf5abb9374b62d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913653"
---
# <a name="how-to-move-a-toolstrip-out-of-a-toolstripcontainer-onto-a-form"></a>Procédure : déplacer un ToolStrip hors d’un ToolStripContainer dans un formulaire
Utilisez la procédure suivante pour déplacer un <xref:System.Windows.Forms.ToolStrip> d’un <xref:System.Windows.Forms.ToolStripContainer> sur un formulaire.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-move-a-toolstrip-out-of-a-toolstripcontainer-onto-a-form"></a>Pour déplacer un ToolStrip hors d’un ToolStripContainer dans un formulaire  
  
1. Sélectionnez le contrôle <xref:System.Windows.Forms.ToolStrip>.  
  
2. Couper la <xref:System.Windows.Forms.ToolStrip> en appuyant sur CTRL + X, ou cliquez sur le <xref:System.Windows.Forms.ToolStrip> et choisissez **couper** dans le menu contextuel.  
  
3. Sélectionnez le formulaire.  
  
4. Coller le <xref:System.Windows.Forms.ToolStrip> en appuyant sur CTRL + V, ou choisissez **coller** à partir de la **modifier** menu.  
  
5. Définir le <xref:System.Windows.Forms.ToolStrip.Dock%2A> propriété de la <xref:System.Windows.Forms.ToolStrip> à **haut**.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripContainer>
- [Vue d’ensemble du contrôle ToolStrip](toolstrip-control-overview-windows-forms.md)
