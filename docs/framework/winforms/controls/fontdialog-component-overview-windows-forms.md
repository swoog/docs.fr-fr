---
title: Vue d'ensemble du composant FontDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- FontDialog
helpviewer_keywords:
- Font dialog box [Windows Forms], Windows Forms
- Font dialog box
- FontDialog component [Windows Forms], about FontDialog component
ms.assetid: daf46e57-1b4b-4b7a-bad0-b50ca7ba75dc
ms.openlocfilehash: 854f54454c0c88f965d9ac8240c11f6821f0c64b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594562"
---
# <a name="fontdialog-component-overview-windows-forms"></a>Vue d'ensemble du composant FontDialog (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.FontDialog> composant est une boîte de dialogue préconfigurée qui est le standard Windows **police** boîte de dialogue permet d’exposer les polices qui sont actuellement installés sur le système. Utilisez-la dans votre application Windows comme une solution simple pour la sélection de police que de configurer votre propre boîte de dialogue.  
  
 Par défaut, la boîte de dialogue affiche les zones de liste pour la police, style de police et la taille ; cases à cocher pour les effets comme barré et souligné ; une liste déroulante pour le Script ; et un exemple montrant comment la police s’affiche. (Script fait référence à différents jeux de caractères qui est disponibles pour une police, par exemple, hébreu ou le japonais.) Pour afficher la boîte de dialogue Police, appelez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).  
  
## <a name="key-properties"></a>Propriétés de clé  
 Le composant a un nombre de propriétés qui définissent son apparence. Les propriétés qui définissent les sélections de la boîte de dialogue sont <xref:System.Windows.Forms.FontDialog.Font%2A> et <xref:System.Windows.Forms.FontDialog.Color%2A>. Le <xref:System.Windows.Forms.FontDialog.Font%2A> propriété définit la police, le style, taille, script et effets ; par exemple, `Arial, 10pt, style=Italic, Strikeout`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.FontDialog>
- [FontDialog, composant](../../../../docs/framework/winforms/controls/fontdialog-component-windows-forms.md)
