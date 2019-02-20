---
title: Vue d'ensemble du contrôle FlowLayoutPanel
ms.date: 03/30/2017
f1_keywords:
- FlowLayoutPanel
helpviewer_keywords:
- forms [Windows Forms], dynamic layout
- layout [Windows Forms], dynamic
- Windows Forms, dynamic layout
- FlowLayoutPanel control [Windows Forms], about FlowLayoutPanel control
ms.assetid: 3883e024-f5a0-456d-9c27-b4dfa1cc9045
ms.openlocfilehash: 2b08566f4b13ed54bfc0bb83c39777410251dafa
ms.sourcegitcommit: acd8ed14fe94e9d4e3a7fb685fe83d05e941073c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56441768"
---
# <a name="flowlayoutpanel-control-overview"></a>Vue d'ensemble du contrôle FlowLayoutPanel
Le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> réorganise son contenu dans un sens de flux horizontal ou vertical. Vous pouvez encapsuler le contenu du contrôle d'une ligne à la suivante ou d'une colonne à la suivante. Vous pouvez également ajuster plutôt qu'encapsuler son contenu.  
  
 Vous pouvez spécifier le sens du flux en définissant la valeur de la propriété <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A>. Le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> inverse correctement son sens du flux dans les dispositions de droite à gauche (RTL, Right-to-Left). Vous pouvez également spécifier si le contenu du contrôle <xref:System.Windows.Forms.FlowLayoutPanel> est encapsulé ou coupé en définissant la valeur de la propriété <xref:System.Windows.Forms.FlowLayoutPanel.WrapContents%2A>.  
  
 Le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> prend automatiquement une dimension adaptée à son contenu quand vous affectez la valeur `true` à la propriété <xref:System.Windows.Forms.Control.AutoSize%2A>. Il fournit également un **FlowBreak** propriété à ses contrôles enfants. L'affectation de la valeur `true` à la propriété FlowBreak fait en sorte que le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> cesse de disposer les contrôles dans le sens du flux actuel et qu'il encapsule à la ligne ou la colonne suivante.  
  
 Tout contrôle Windows Forms peut être un enfant du contrôle <xref:System.Windows.Forms.FlowLayoutPanel>, y compris d'autres instances de <xref:System.Windows.Forms.FlowLayoutPanel>. Avec cette fonctionnalité, vous pouvez construire des dispositions sophistiquées qui s'adaptent aux dimensions de votre formulaire au moment de l'exécution.  
  
 Consultez également [procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A>
- <xref:System.Windows.Forms.TableLayoutPanel>
- [FlowLayoutPanel, contrôle](../../../../docs/framework/winforms/controls/flowlayoutpanel-control-windows-forms.md)
