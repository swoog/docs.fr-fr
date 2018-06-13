---
title: Vue d'ensemble du composant PrintDocument (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- PrintDocument
helpviewer_keywords:
- PrintDocument component [Windows Forms], about PrintDocument component
- printing [Windows Forms], PrintDocument component
ms.assetid: b59b4b60-dce5-42ca-8421-3a54a2f7bab0
ms.openlocfilehash: b02133321624d27b9c1e8faae9cac1b4fe8f76c3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33538263"
---
# <a name="printdocument-component-overview-windows-forms"></a>Vue d'ensemble du composant PrintDocument (Windows Forms)
Le composant [PrintDocument](../../../../docs/framework/winforms/controls/printdocument-component-windows-forms.md) Windows Forms permet de définir les propriétés qui décrivent les éléments à imprimer, puis d’imprimer le document dans des applications Windows. Il peut être utilisé conjointement avec le composant [PrintDialog](../../../../docs/framework/winforms/controls/printdialog-component-windows-forms.md) pour contrôler tous les aspects de l’impression du document.  
  
## <a name="working-with-the-printdocument-component"></a>Utilisation du composant PrintDocument  
 Parmi les principaux scénarios qui impliquent le <xref:System.Drawing.Printing.PrintDocument> composant sont :  
  
-   Travaux d’impression simples, tels que l’impression d’un fichier texte. Dans ce cas, vous devez ajouter le <xref:System.Drawing.Printing.PrintDocument> composant à un Windows Form, puis ajoutez la logique de programmation qui imprime un fichier dans le <xref:System.Drawing.Printing.PrintDocument.PrintPage> Gestionnaire d’événements. La logique de programmation doit déboucher sur la <xref:System.Drawing.Printing.PrintDocument.Print%2A> méthode pour imprimer le document. Cette méthode envoie un <xref:System.Drawing.Graphics> objet contenu dans le <xref:System.Drawing.Printing.PrintPageEventArgs.Graphics%2A> propriété de la <xref:System.Drawing.Printing.PrintPageEventArgs> (classe), à l’imprimante. Pour obtenir un exemple qui montre comment imprimer un document de texte à l’aide de la <xref:System.Drawing.Printing.PrintDocument> composant, consultez [Comment : imprimer un fichier de texte comportant plusieurs pages dans les Windows Forms](../../../../docs/framework/winforms/advanced/how-to-print-a-multi-page-text-file-in-windows-forms.md).  
  
-   Travaux d’impression plus complexes, comme lorsque vous souhaitez réutiliser la logique d’impression que vous avez écrite. Dans ce cas, vous devez dériver un nouveau composant à partir de la <xref:System.Drawing.Printing.PrintDocument> composant et substituer (voir [substitue](~/docs/visual-basic/language-reference/modifiers/overrides.md) pour Visual Basic ou [remplacer](~/docs/csharp/language-reference/keywords/override.md) pour c#) le <xref:System.Drawing.Printing.PrintDocument.PrintPage> événement.  
  
 Lorsqu’il est ajouté à un formulaire, le <xref:System.Drawing.Printing.PrintDocument> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Drawing.Graphics>  
 <xref:System.Drawing.Printing.PrintDocument>  
 [Prise en charge de l’impression dans les Windows Forms](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md)  
 [Composant PrintDocument](../../../../docs/framework/winforms/controls/printdocument-component-windows-forms.md)
