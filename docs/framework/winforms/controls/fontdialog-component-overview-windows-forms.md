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
ms.openlocfilehash: 3a4707ffe471161988d0526ce0908b37299f3e07
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="fontdialog-component-overview-windows-forms"></a>Vue d'ensemble du composant FontDialog (Windows Forms)
Windows Forms <xref:System.Windows.Forms.FontDialog> composant est une boîte de dialogue préconfigurée de manière standard de Windows **police** boîte de dialogue permet d’exposer les polices installées actuellement sur le système. L’utiliser dans votre application Windows comme une solution simple pour la sélection de police que de configurer votre propre boîte de dialogue.  
  
 Par défaut, la boîte de dialogue affiche les zones de liste Police, style de police et la taille ; cases à cocher pour les effets comme barré et souligné ; une liste déroulante pour le Script ; et un exemple de l’apparence de la police. (Script fait référence à différents jeux de caractères qui sont disponibles pour une police donnée, par exemple, hébreu ou le japonais). Pour afficher la boîte de dialogue Police, appelez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).  
  
## <a name="key-properties"></a>Propriétés de clé  
 Le composant possède un nombre de propriétés qui définissent son apparence. Les propriétés qui définissent les sélections de la boîte de dialogue sont <xref:System.Windows.Forms.FontDialog.Font%2A> et <xref:System.Windows.Forms.FontDialog.Color%2A>. Le <xref:System.Windows.Forms.FontDialog.Font%2A> propriété définit la police, le style, taille, script et effets ; par exemple, `Arial, 10pt, style=Italic, Strikeout`.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.FontDialog>  
 [FontDialog, composant](../../../../docs/framework/winforms/controls/fontdialog-component-windows-forms.md)
