---
title: "Comment : grouper les contrôles avec le contrôle Panel Windows Forms à l'aide du concepteur"
ms.date: 03/30/2017
helpviewer_keywords:
- Panel control [Windows Forms], grouping controls
- controls [Windows Forms], grouping
- Windows Forms controls, grouping
ms.assetid: 7e1cd708-fdb1-49d8-9ca2-5640b276bf2e
ms.openlocfilehash: 1cf4519a9aaaa1c4f0df321ab38c3f543c87b2a2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33525621"
---
# <a name="how-to-group-controls-with-the-windows-forms-panel-control-using-the-designer"></a>Comment : grouper les contrôles avec le contrôle Panel Windows Forms à l'aide du concepteur
Windows Forms <xref:System.Windows.Forms.Panel> contrôles sont utilisés pour regrouper d’autres contrôles. Il existe trois raisons pour regrouper des contrôles. Regroupement d’éléments connexes pour une interface utilisateur claire ; visuel regroupement de programmation, des cases d’option, par exemple ; le dernier est pour déplacer les contrôles en tant qu’unité au moment du design.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnalisation des paramètres de développement dans Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-create-a-group-of-controls"></a>Pour créer un groupe de contrôles  
  
1.  Faites glisser un <xref:System.Windows.Forms.Panel> contrôle depuis la **Windows Forms** onglet de la boîte à outils sur un formulaire.  
  
2.  Ajouter d’autres contrôles pour le panneau de configuration, en dessinant à l’intérieur du Panneau de configuration.  
  
     Si vous avez des contrôles existants que vous souhaitez placer dans un panneau de configuration, vous pouvez sélectionner tous les contrôles, les couper dans le Presse-papiers, sélectionnez le <xref:System.Windows.Forms.Panel> contrôler, puis collez-les dans le panneau de configuration. Vous pouvez également les glisser dans le panneau de configuration.  
  
3.  (Facultatif) Si vous souhaitez ajouter une bordure à un panneau de configuration, définissez son <xref:System.Windows.Forms.BorderStyle> propriété. Il existe trois possibilités : <xref:System.Windows.Forms.BorderStyle.Fixed3D>, <xref:System.Windows.Forms.BorderStyle.FixedSingle>, et <xref:System.Windows.Forms.BorderStyle.None>.  
  
## <a name="see-also"></a>Voir aussi  
 [Panel, contrôle](../../../../docs/framework/winforms/controls/panel-control-windows-forms.md)  
 [Vue d’ensemble du contrôle Panel](../../../../docs/framework/winforms/controls/panel-control-overview-windows-forms.md)  
 [Guide pratique pour définir l'arrière-plan d'un contrôle Panel](../../../../docs/framework/winforms/controls/how-to-set-the-background-of-a-windows-forms-panel.md)
