---
title: Réglage des performances dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], performance tuning
- performance [Windows Forms], DataGridView control
- performance tuning [Windows Forms], data grids
ms.assetid: 6ccbff28-a0ff-41e4-b601-61b31b61851d
ms.openlocfilehash: 97bf6f36ce029f879c3524fa92df08a483c2cb77
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33536980"
---
# <a name="performance-tuning-in-the-windows-forms-datagridview-control"></a>Réglage des performances dans le contrôle DataGridView Windows Forms
Lorsque vous travaillez avec grandes quantités de données, le `DataGridView` contrôle peut consommer une grande quantité de mémoire, sauf si vous l’utilisez avec précaution. Sur les clients avec une mémoire limitée, vous pouvez éviter certains cette surcharge en évitant les fonctionnalités qui ont un coût de mémoire élevée. Vous pouvez également gérer tout ou partie de la maintenance des données et les tâches de récupération à l’aide du mode virtuel afin de personnaliser l’utilisation de la mémoire pour votre scénario.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Meilleures pratiques pour la mise à l'échelle du contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md)  
 Décrit comment utiliser le `DataGridView` contrôle de façon à éviter de trop handicaper les performances et l’utilisation inutile de mémoire lorsque vous travaillez avec grandes quantités de données.  
  
 [Mode virtuel dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/virtual-mode-in-the-windows-forms-datagridview-control.md)  
 Décrit comment utiliser le mode virtuel pour compléter ou remplacer le mécanisme de liaison de données standard.  
  
 [Procédure pas à pas : implémentation du mode virtuel dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/implementing-virtual-mode-wf-datagridview-control.md)  
 Décrit comment implémenter des gestionnaires pour plusieurs événements de mode virtuel. Montre également comment implémenter la restauration au niveau des lignes et validation pour les modifications de l’utilisateur.  
  
 [Implémentation du mode virtuel avec le chargement immédiat des données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)  
 Décrit comment charger des données à la demande, ce qui est utile lorsque vous avez plus de données à afficher que la mémoire du client peut stocker.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.DataGridView>  
 Fournit la documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.  
  
 <xref:System.Windows.Forms.DataGridView.VirtualMode%2A>  
 Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété.  
  
## <a name="see-also"></a>Voir aussi  
 [DataGridView, contrôle](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)  
 [Modes d’affichage des données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/data-display-modes-in-the-windows-forms-datagridview-control.md)
