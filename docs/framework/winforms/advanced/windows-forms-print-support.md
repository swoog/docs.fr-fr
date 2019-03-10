---
title: Prise en charge de l'impression dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, printing
- printing [Windows Forms]
- forms [Windows Forms], printing (using designer)
- printing [Windows Forms], Windows Forms, support
- printing [Windows Forms], print support
ms.assetid: a4a2960c-eb70-48e2-b641-cfb222704e46
ms.openlocfilehash: 8e008f2cb4b2f32cdba676e68d9fd790530e2b06
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57708130"
---
# <a name="windows-forms-print-support"></a>Prise en charge de l'impression dans les Windows Forms
L’impression dans Windows Forms consiste principalement à l’aide de la [du composant PrintDocument](../controls/printdocument-component-windows-forms.md) composant pour permettre aux utilisateurs d’imprimer et le [du contrôle PrintPreviewDialog](../controls/printpreviewdialog-control-windows-forms.md) contrôle, [PrintDialog Composant](../controls/printdialog-component-windows-forms.md) et [du composant PageSetupDialog](../controls/pagesetupdialog-component-windows-forms.md) composants pour fournir une interface graphique familière aux utilisateurs habitués au système d’exploitation Windows.  
  
 En général, vous créez une nouvelle instance de la <xref:System.Drawing.Printing.PrintDocument> composant, définir les propriétés qui décrivent les éléments à imprimer à l’aide de la <xref:System.Drawing.Printing.PrinterSettings> et <xref:System.Drawing.Printing.PageSettings> classes, puis appelez le <xref:System.Drawing.Printing.PrintDocument.Print%2A> méthode réellement imprimer le document.  
  
 Au cours de l’impression à partir d’une application Windows, le <xref:System.Drawing.Printing.PrintDocument> composant affiche une boîte de dialogue d’impression d’annulation pour alerter les utilisateurs au fait que l’impression est en cours et pour permettre le travail d’impression doit être annulée.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour Créer des travaux d’impression Standard de Windows Forms](how-to-create-standard-windows-forms-print-jobs.md)  
 Explique comment utiliser le <xref:System.Drawing.Printing.PrintDocument> composant pour imprimer à partir d’un formulaire Windows.  
  
 [Guide pratique pour Capturer des entrées utilisateur à partir d’un composant PrintDialog au moment de l’exécution](how-to-capture-user-input-from-a-printdialog-at-run-time.md)  
 Explique comment modifier les options d’impression sélectionnées par programmation en utilisant le <xref:System.Windows.Forms.PrintDialog> composant.  
  
 [Guide pratique pour Choisir les imprimantes connectées à l’ordinateur d’un utilisateur dans les Windows Forms](how-to-choose-the-printers-attached-to-user-computer-in-windows-forms.md)  
 Décrit la modification de l’imprimante pour imprimer à l’utilisation de la <xref:System.Windows.Forms.PrintDialog> composant en cours d’exécution.  
  
 [Guide pratique pour Imprimer des graphiques dans les Windows Forms](how-to-print-graphics-in-windows-forms.md)  
 Décrit l’envoi de graphismes à l’imprimante.  
  
 [Guide pratique pour Imprimer un fichier texte de plusieurs pages dans les Windows Forms](how-to-print-a-multi-page-text-file-in-windows-forms.md)  
 Décrit l’envoi de texte à l’imprimante.  
  
 [Guide pratique pour Travaux d’impression de complète Windows Forms](how-to-complete-windows-forms-print-jobs.md)  
 Explique comment avertir les utilisateurs de l’achèvement d’un travail d’impression.  
  
 [Guide pratique pour Imprimer un formulaire Windows](how-to-print-a-windows-form.md)  
 Montre comment imprimer une copie de l’écran actuel.  
  
 [Guide pratique pour Imprimer dans les formulaires de Windows à l’aide de l’aperçu avant impression](how-to-print-in-windows-forms-using-print-preview.md)  
 Montre comment utiliser un <xref:System.Windows.Forms.PrintPreviewDialog> pour imprimer un document.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Composant PrintDocument](../controls/printdocument-component-windows-forms.md)  
 Explique comment utiliser le <xref:System.Drawing.Printing.PrintDocument> composant.  
  
 [PrintDialog, composant](../controls/printdialog-component-windows-forms.md)  
 Explique comment utiliser le <xref:System.Windows.Forms.PrintDialog> composant.  
  
 [PrintPreviewDialog, contrôle](../controls/printpreviewdialog-control-windows-forms.md)  
 Explique comment utiliser le <xref:System.Windows.Forms.PrintPreviewDialog> contrôle.  
  
 [PageSetupDialog, composant](../controls/pagesetupdialog-component-windows-forms.md)  
 Explique comment utiliser le <xref:System.Windows.Forms.PageSetupDialog> composant.  
  
 <xref:System.Drawing.Printing>  
 Décrit les classes dans le <xref:System.Drawing.Printing> espace de noms.
