---
title: Vue d'ensemble du contrôle TableLayoutPanel
ms.date: 03/30/2017
f1_keywords:
- TableLayoutPanel
helpviewer_keywords:
- controls [Windows Forms], resizing
- resizable controls [Windows Forms]
- Windows Forms controls, proportional resizing
- Windows Forms, proportional resizing of controls
- layout [Windows Forms], TableLayoutPanel control
- TableLayoutPanel control [Windows Forms], about TableLayoutPanel control
ms.assetid: 337661c8-61cb-44ee-93e0-3662bddec327
ms.openlocfilehash: 57a57b9f888f2fc46eddba5b97b9e833a7e9f028
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59134015"
---
# <a name="tablelayoutpanel-control-overview"></a>Vue d'ensemble du contrôle TableLayoutPanel
Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> réorganise son contenu dans une grille. La disposition étant effectuée au moment du design et au moment de l'exécution, elle peut changer dynamiquement quand l'environnement d'application change. Cela permet de redimensionner proportionnellement les contrôles du panneau, pour pouvoir répondre à des modifications telles que le redimensionnement du contrôle parent ou le changement de longueur de texte en raison de la localisation.  
  
 Tout contrôle Windows Forms peut être un enfant du contrôle <xref:System.Windows.Forms.TableLayoutPanel>, y compris d'autres instances de <xref:System.Windows.Forms.TableLayoutPanel>. Cela vous permet de construire des dispositions sophistiquées qui s'adaptent aux modifications au moment de l'exécution.  
  
 Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> peut s'étendre pour accepter de nouveaux contrôles quand ils sont ajoutés, en fonction de la valeur des propriétés <xref:System.Windows.Forms.TableLayoutPanel.RowCount%2A>, <xref:System.Windows.Forms.TableLayoutPanel.ColumnCount%2A>, et <xref:System.Windows.Forms.TableLayoutPanel.GrowStyle%2A>. L'affectation de la valeur 0 à la propriété <xref:System.Windows.Forms.TableLayoutPanel.RowCount%2A> ou <xref:System.Windows.Forms.TableLayoutPanel.ColumnCount%2A> indique que le <xref:System.Windows.Forms.TableLayoutPanel> sera indépendant dans la direction correspondante.  
  
 Vous pouvez également contrôler la direction d'expansion (horizontale ou verticale) une fois que le contrôle <xref:System.Windows.Forms.TableLayoutPanel> est rempli de contrôles enfants. Par défaut, le contrôle <xref:System.Windows.Forms.TableLayoutPanel> s'étend vers le bas en ajoutant des lignes.  
  
 Si vous souhaitez que les lignes et les colonnes se comportent différemment du comportement par défaut, vous pouvez contrôler leurs propriétés à l'aide des propriétés <xref:System.Windows.Forms.TableLayoutPanel.RowStyles%2A> et <xref:System.Windows.Forms.TableLayoutPanel.ColumnStyles%2A>. Vous pouvez définir les propriétés des lignes ou des colonnes individuellement.  
  
 Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> ajoute les propriétés suivantes à ses contrôles enfants : `Cell`, `Column`, `Row`, `ColumnSpan`, et `RowSpan`.  
  
 Vous pouvez fusionner des cellules dans le contrôle <xref:System.Windows.Forms.TableLayoutPanel> en définissant les propriétés `ColumnSpan` ou `RowSpan` sur un contrôle enfant.  
  
1.  [Procédure : aligner et étirer un contrôle dans un contrôle TableLayoutPanel](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2.  [Procédure : étendre des lignes et des colonnes dans un contrôle TableLayoutPanel](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
3.  [Procédure : modifier des colonnes et des lignes dans un contrôle TableLayoutPanel](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
4.  [Procédure pas à pas : organisation des contrôles dans Windows Forms à l’aide d’un TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.FlowLayoutPanel>
- <xref:System.Windows.Forms.TableLayoutSettings>
- [Procédure : créer une disposition Windows Forms qui répond bien à la localisation](how-to-design-a-windows-forms-layout-that-responds-well-to-localization.md)
- [Procédure : créer un formulaire Windows redimensionnable pour l’entrée de données](how-to-create-a-resizable-windows-form-for-data-entry.md)
- [Meilleures pratiques pour le contrôle TableLayoutPanel](best-practices-for-the-tablelayoutpanel-control.md)
