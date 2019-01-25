---
title: 'Procédure : Activer la touche TAB sortir d’un contrôle ToolStrip'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], moving between
- TAB key [Windows Forms], enabling
- ToolStrip control [Windows Forms], moving from
ms.assetid: 40f9e88b-09a3-428e-8da8-c00bb65079c6
ms.openlocfilehash: a98c8a54389daa898c877a08f8cc2cae46a11da9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663068"
---
# <a name="how-to-enable-the-tab-key-to-move-out-of-a-toolstrip-control"></a>Procédure : Activer la touche TAB sortir d’un contrôle ToolStrip
Utilisez la procédure suivante pour permettre aux utilisateurs d’appuyer sur la touche TAB pour sortir d’un <xref:System.Windows.Forms.ToolStrip> au contrôle suivant dans l’ordre de tabulation.  
  
 Le <xref:System.Windows.Forms.ToolStrip> accepte la première pression sur la touche TAB et les touches flèche sélectionner des éléments dans le <xref:System.Windows.Forms.ToolStrip>. Lorsque l’utilisateur appuie sur la touche TAB une deuxième fois, il dirige l’utilisateur vers le contrôle suivant dans l’ordre de tabulation.  
  
### <a name="to-enable-the-user-to-press-the-tab-key-to-move-out-of-a-toolstrip-to-the-next-control"></a>Pour permettre aux utilisateurs d’appuyer sur la touche TAB pour sortir d’un ToolStrip au contrôle suivant  
  
-   Définir le <xref:System.Windows.Forms.ToolStrip.TabStop%2A> propriété de la <xref:System.Windows.Forms.ToolStrip> à `true`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.TabStop%2A>
- [Vue d’ensemble du contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
