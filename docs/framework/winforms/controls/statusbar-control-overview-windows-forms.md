---
title: Vue d'ensemble du contrôle StatusBar (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- StatusBar
helpviewer_keywords:
- StatusBar control [Windows Forms], about StatusBar control
- status bars
ms.assetid: b7b9852c-633d-4416-bb2e-94852b989c6c
ms.openlocfilehash: 5fdefa7d7e7c7ef543f677be7beb61dfee54e077
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009699"
---
# <a name="statusbar-control-overview-windows-forms"></a>Vue d'ensemble du contrôle StatusBar (Windows Forms)
> [!IMPORTANT]
>  Le <xref:System.Windows.Forms.StatusStrip> et <xref:System.Windows.Forms.ToolStripStatusLabel> contrôles remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.StatusBar> et <xref:System.Windows.Forms.StatusBarPanel> contrôle ; Toutefois, le <xref:System.Windows.Forms.StatusBar> et <xref:System.Windows.Forms.StatusBarPanel> contrôles ont été conservés pour la compatibilité descendante et une utilisation ultérieure, si vous Choisissez.  
  
 Les formulaires Windows [du contrôle StatusBar](statusbar-control-windows-forms.md) est utilisé sur les formulaires comme une zone, généralement affichée en bas d’une fenêtre dans laquelle une application peut afficher différents types d’informations d’état. <xref:System.Windows.Forms.StatusBar> contrôles peuvent avoir des panneaux de barre d’état affiche du texte ou des icônes pour indiquer l’état, ou une série d’icônes dans une animation qui indiquent le qu'utilisation d’un processus ; par exemple, [!INCLUDE[ofprword](../../../../includes/ofprword-md.md)] indiquant que le document est enregistré.  
  
## <a name="using-the-statusbar-control"></a>Utilisation du contrôle StatusBar  
 Internet Explorer utilise une barre d’état pour indiquer l’URL d’une page lorsque la souris passe sur le lien hypertexte ; [!INCLUDE[ofprword](../../../../includes/ofprword-md.md)] vous donne des informations sur l’emplacement de la page, l’emplacement de la section et modes d’édition comme refrappe et de suivi des modifications ; et de Visual Studio utilise la barre d’état pour donner des informations contextuelles, telles que de vous indiquer comment manipuler les fenêtres ancrables ancrés ou flottants.  
  
 Vous pouvez afficher un message sur la barre d’état en définissant le <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> propriété `false` (la valeur par défaut) et en définissant le <xref:System.Windows.Forms.StatusBar.Text%2A> propriété de la barre d’état pour le texte que vous souhaitez voir apparaître dans la barre d’état. Vous pouvez diviser la barre d’état en panneaux pour afficher plusieurs types d’informations en définissant le <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> propriété `true` et à l’aide de la <xref:System.Windows.Forms.StatusBar.StatusBarPanelCollection.Add%2A> méthode de <xref:System.Windows.Forms.StatusBar.StatusBarPanelCollection>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [Guide pratique pour Déterminer l’utilisateur a cliqué sur le panneau du contrôle StatusBar Windows Forms](determine-which-panel-wf-statusbar-control-was-clicked.md)
