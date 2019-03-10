---
title: 'Procédure : Configurer la fusion de menus automatique pour les Applications MDI'
ms.date: 03/30/2017
helpviewer_keywords:
- MenuStrip [Windows Forms], merging
- Merging [Windows Forms], automatic menu
ms.assetid: 55e32cad-1141-4a56-aa33-d9543ca3d393
ms.openlocfilehash: 152db39e7c947d5a49eaed81b00d13c02aa8014c
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57719726"
---
# <a name="how-to-set-up-automatic-menu-merging-for-mdi-applications"></a>Procédure : Configurer la fusion de menus automatique pour les Applications MDI
La procédure suivante indique les étapes de base pour configurer la fusion automatique dans une application d’interface multidocument (MDI) avec <xref:System.Windows.Forms.MenuStrip>.  
  
### <a name="to-set-up-automatic-menu-merging"></a>Pour configurer la fusion de menus automatique  
  
1.  Créer un formulaire MDI parent en définissant son <xref:System.Windows.Forms.Form.IsMdiContainer%2A> propriété `true`.  
  
2.  Ajouter un <xref:System.Windows.Forms.MenuStrip> le parent MDI, en définissant son <xref:System.Windows.Forms.Form.MainMenuStrip%2A> propriété qui <xref:System.Windows.Forms.MenuStrip>.  
  
3.  Créer un formulaire enfant MDI et définir son <xref:System.Windows.Forms.Form.MdiParent%2A> propriété le nom du formulaire parent.  
  
4.  Ajouter un <xref:System.Windows.Forms.MenuStrip> au formulaire enfant MDI.  
  
5.  Sur le formulaire enfant, définissez le <xref:System.Windows.Forms.ToolStripItem.Visible%2A> propriété de la <xref:System.Windows.Forms.MenuStrip> à `false`.  
  
6.  Ajouter des éléments de menu à la forme enfant <xref:System.Windows.Forms.MenuStrip> que vous souhaitez fusionner dans le formulaire parent <xref:System.Windows.Forms.MenuStrip> lorsque le formulaire enfant est activé.  
  
7.  Utilisez le <xref:System.Windows.Forms.ToolStripItem.MergeAction%2A> les éléments de propriété dans le menu sous la forme enfant <xref:System.Windows.Forms.MenuStrip> pour contrôler leur fusion dans le formulaire parent.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [Vue d'ensemble du contrôle MenuStrip](menustrip-control-overview-windows-forms.md)
