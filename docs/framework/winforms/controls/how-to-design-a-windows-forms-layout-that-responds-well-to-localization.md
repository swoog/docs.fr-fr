---
title: 'Procédure : créer une disposition Windows Forms qui répond bien à la localisation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- application design [Windows Forms], localization
- Windows Forms, localization
- localization [Windows Forms], Windows Forms layout
ms.assetid: d13eff2d-701c-4b6e-8838-3885cbfb7223
ms.openlocfilehash: 095427ce633ee6db5a448c8f3f69304ed25ab82a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59142595"
---
# <a name="how-to-design-a-windows-forms-layout-that-responds-well-to-localization"></a>Procédure : créer une disposition Windows Forms qui répond bien à la localisation
La création de formulaires qui sont prêts à être localisés accélère considérablement le développement pour les marchés internationaux. Vous pouvez utiliser le contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour implémenter des dispositions qui répondent correctement au redimensionnement des contrôles suite aux modifications de leurs valeurs de propriétés <xref:System.Windows.Forms.Control.Text%2A>.  
  
## <a name="example"></a>Exemple  
 Ce formulaire montre comment créer une disposition qui s'ajuste proportionnellement quand vous traduisez les valeurs de chaînes affichées dans d'autres langues. Ce processus de traduction est appelé *localisation*. Pour plus d’informations, consultez [Localisation](../../../standard/globalization-localization/localization.md).  
  
 Cette tâche est très bien prise en charge dans Visual Studio.  Voir aussi [procédure pas à pas : Création d’une présentation qui ajuste la Proportion pour la localisation](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/7k9fa71y(v=vs.100)).  
  
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/CS/localizableform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/VB/localizableform.vb#1)]  
  
## <a name="additional-resources"></a>Ressources supplémentaires
1.  [Procédure : aligner et étirer un contrôle dans un contrôle TableLayoutPanel](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2.  [Procédure pas à pas : organisation des contrôles dans des Windows Forms à l’aide d’un FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)  

3.  [Procédure : étendre des lignes et des colonnes dans un contrôle TableLayoutPanel](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
4.  [Procédure : modifier des colonnes et des lignes dans un contrôle TableLayoutPanel](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
5.  [Procédure pas à pas : exécution de tâches courantes à l’aide de balises actives dans les contrôles Windows Forms](performing-common-tasks-using-smart-tags-on-wf-controls.md)  
  
6.  [Procédure pas à pas : organisation des contrôles dans Windows Forms à l’aide d’un TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)  

7.  [Procédure pas à pas : disposition des contrôles Windows Forms avec le remplissage, les marges et la propriété AutoSize](windows-forms-controls-padding-autosize.md)  
  
8.  [Procédure : Prend en charge de la localisation sur les formulaires Windows à l’aide du redimensionnement automatique et le contrôle TableLayoutPanel](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/1zkt8b33(v=vs.100))  
  
9. [Procédure pas à pas : Création d’un formulaire Windows redimensionnable pour l’entrée de données](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100))  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
- [Localisation](../../../standard/globalization-localization/localization.md)
