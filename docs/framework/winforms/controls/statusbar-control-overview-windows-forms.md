---
title: Vue d'ensemble du contrôle StatusBar (Windows Forms)
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-winforms
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- StatusBar
helpviewer_keywords:
- StatusBar control [Windows Forms], about StatusBar control
- status bars
ms.assetid: b7b9852c-633d-4416-bb2e-94852b989c6c
caps.latest.revision: 11
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 8e84ae7d62649c0c547417e954560ac0faccafdd
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2018
---
# <a name="statusbar-control-overview-windows-forms"></a>Vue d'ensemble du contrôle StatusBar (Windows Forms)
> [!IMPORTANT]
>  Le <xref:System.Windows.Forms.StatusStrip> et <xref:System.Windows.Forms.ToolStripStatusLabel> contrôles remplacer et ajouter des fonctionnalités à la <xref:System.Windows.Forms.StatusBar> et <xref:System.Windows.Forms.StatusBarPanel> contrôle ; Toutefois, le <xref:System.Windows.Forms.StatusBar> et <xref:System.Windows.Forms.StatusBarPanel> contrôles sont conservés pour la compatibilité descendante et l’utilisation future si vous Choisissez.  
  
 Windows Forms [contrôle StatusBar](../../../../docs/framework/winforms/controls/statusbar-control-windows-forms.md) est utilisé sur les formulaires comme une zone, s’affichée habituellement au bas d’une fenêtre dans laquelle une application peut afficher différents types d’informations d’état. <xref:System.Windows.Forms.StatusBar> les contrôles peuvent avoir des panneaux de barre d’état affichent du texte ou des icônes pour indiquer l’état, ou une série d’icônes dans une animation indiquant qu’un processus fonctionne ; par exemple, [!INCLUDE[ofprword](../../../../includes/ofprword-md.md)] indiquant que le document est enregistré.  
  
## <a name="using-the-statusbar-control"></a>L’utilisation du contrôle StatusBar  
 Internet Explorer utilise une barre d’état pour indiquer l’URL d’une page lorsque la souris passe sur le lien hypertexte. [!INCLUDE[ofprword](../../../../includes/ofprword-md.md)] fournit des informations sur l’emplacement de la page, l’emplacement de la section et modes d’édition comme refrappe et de suivi des modifications et de Visual Studio utilise la barre d’état afin de donner des informations contextuelles, par exemple pour la manipulation des fenêtres ancrables ancré ou flottant.  
  
 Vous pouvez afficher un message sur la barre d’état en définissant le <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> propriété `false` (la valeur par défaut) et en définissant le <xref:System.Windows.Forms.StatusBar.Text%2A> propriété de la barre d’état pour le texte que vous souhaitez voir apparaître dans la barre d’état. Vous pouvez diviser la barre d’état en panneaux pour afficher plusieurs types d’informations en définissant le <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> propriété `true` et à l’aide de la <xref:System.Windows.Forms.StatusBar.StatusBarPanelCollection.Add%2A> méthode <xref:System.Windows.Forms.StatusBar.StatusBarPanelCollection>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.StatusBar>  
 <xref:System.Windows.Forms.ToolStripStatusLabel>  
 [Guide pratique pour déterminer le panneau du contrôle StatusBar Windows Forms sur lequel l’utilisateur a cliqué](../../../../docs/framework/winforms/controls/determine-which-panel-wf-statusbar-control-was-clicked.md)
