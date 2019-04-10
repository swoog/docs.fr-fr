---
title: 'Procédure : regrouper des contrôles avec le contrôle Panel Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- Panel control [Windows Forms], grouping controls
- controls [Windows Forms], grouping
- Windows Forms controls, grouping
ms.assetid: 7e1cd708-fdb1-49d8-9ca2-5640b276bf2e
ms.openlocfilehash: 662343af42f72816a5a673d2cd6d839a5dca9190
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59341398"
---
# <a name="how-to-group-controls-with-the-windows-forms-panel-control-using-the-designer"></a>Procédure : regrouper des contrôles avec le contrôle Panel Windows Forms à l’aide du concepteur
Windows Forms <xref:System.Windows.Forms.Panel> contrôles sont utilisés pour regrouper d’autres contrôles. Il existe trois raisons pour regrouper des contrôles. Regroupement d’éléments connexes pour une interface utilisateur claire ; visuel regroupement de programmation, des cases d’option, par exemple ; la dernière est pour déplacer les contrôles en tant qu’unité au moment du design.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-a-group-of-controls"></a>Pour créer un groupe de contrôles  
  
1. Faites glisser un <xref:System.Windows.Forms.Panel> contrôle depuis la **Windows Forms** onglet de la boîte à outils sur un formulaire.  
  
2. Ajoutez des contrôles pour le dessin du panneau, chacun à l’intérieur du panneau.  
  
     Si vous avez des contrôles existants que vous souhaitez placer dans un panneau, vous pouvez sélectionner tous les contrôles, les couper dans le Presse-papiers, sélectionnez le <xref:System.Windows.Forms.Panel> contrôler et collez-les dans le panneau de configuration. Vous pouvez également faites-les glisser dans le panneau de configuration.  
  
3. (Facultatif) Si vous souhaitez ajouter une bordure à un panneau, définissez son <xref:System.Windows.Forms.BorderStyle> propriété. Il existe trois possibilités : <xref:System.Windows.Forms.BorderStyle.Fixed3D>, <xref:System.Windows.Forms.BorderStyle.FixedSingle>, et <xref:System.Windows.Forms.BorderStyle.None>.  
  
## <a name="see-also"></a>Voir aussi

- [Panel, contrôle](panel-control-windows-forms.md)
- [Vue d’ensemble du contrôle Panel](panel-control-overview-windows-forms.md)
- [Procédure : définir l’arrière-plan d’un panneau](how-to-set-the-background-of-a-windows-forms-panel.md)
