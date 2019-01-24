---
title: "Procédure : Créer qu'un Windows Forms de disposition qui répond bien à la localisation"
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
ms.openlocfilehash: 15f290f7d076eede7a8092d7295df810e4e51bf3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563520"
---
# <a name="how-to-design-a-windows-forms-layout-that-responds-well-to-localization"></a>Procédure : Créer qu'un Windows Forms de disposition qui répond bien à la localisation
La création de formulaires qui sont prêts à être localisés accélère considérablement le développement pour les marchés internationaux. Vous pouvez utiliser le contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour implémenter des dispositions qui répondent correctement au redimensionnement des contrôles suite aux modifications de leurs valeurs de propriétés <xref:System.Windows.Forms.Control.Text%2A>.  
  
## <a name="example"></a>Exemple  
 Ce formulaire montre comment créer une disposition qui s'ajuste proportionnellement quand vous traduisez les valeurs de chaînes affichées dans d'autres langues. Ce processus de traduction est appelé *localisation*. Pour plus d’informations, consultez [Localisation](../../../../docs/standard/globalization-localization/localization.md).  
  
 Cette tâche est très bien prise en charge dans Visual Studio.  Voir aussi [procédure pas à pas : Création d’une présentation qui ajuste la Proportion pour la localisation](https://msdn.microsoft.com/library/7k9fa71y\(v=vs.110\)).  
  
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/CS/localizableform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/VB/localizableform.vb#1)]  
  
1.  [Guide pratique pour Aligner et étirer un contrôle dans un contrôle TableLayoutPanel](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2.  [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un FlowLayoutPanel](https://msdn.microsoft.com/library/z9w7ek2f\(v=vs.110\))  
  
3.  [Guide pratique pour Étendre des lignes et colonnes dans un contrôle TableLayoutPanel](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
4.  [Guide pratique pour Modifier des colonnes et lignes dans un contrôle TableLayoutPanel](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
5.  [Procédure pas à pas : Effectuer des tâches courantes à l’aide d’intelligent des balises sur Windows Forms contrôles](https://msdn.microsoft.com/library/xhz359sc\(v=vs.110\))  
  
6.  [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel](https://msdn.microsoft.com/library/w4yc3e8c\(v=vs.110\))  
  
7.  [Procédure pas à pas : Disposition des Windows Forms contrôles avec la propriété AutoSize, des marges et remplissage](https://msdn.microsoft.com/library/3z3f9e8b\(v=vs.110\))  
  
8.  [Guide pratique pour Prend en charge de la localisation sur les formulaires Windows à l’aide du redimensionnement automatique et le contrôle TableLayoutPanel](https://msdn.microsoft.com/library/1zkt8b33\(v=vs.110\))  
  
9. [Procédure pas à pas : Création d’un formulaire Windows redimensionnable pour l’entrée de données](https://msdn.microsoft.com/library/991eahec\(v=vs.110\))  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
- [Localisation](../../../../docs/standard/globalization-localization/localization.md)
