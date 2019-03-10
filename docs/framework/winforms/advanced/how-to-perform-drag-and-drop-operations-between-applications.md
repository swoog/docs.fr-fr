---
title: 'Procédure : Effectuer des opérations de glisser-déplacer entre les Applications'
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms], between applications
ms.assetid: fa347436-2b12-4dd6-8507-59d7241f6a06
ms.openlocfilehash: 1e9556a69f3f5da4a47c5f5b1a6043a9a73dd8ff
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57713434"
---
# <a name="how-to-perform-drag-and-drop-operations-between-applications"></a>Procédure : Effectuer des opérations de glisser-déplacer entre les Applications
L’exécution d’opérations de glisser-déposer entre applications revient à activer cette action dans une application, du moment que les deux applications concernées respectent le "contrat" établi entre les propriétés <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A> et <xref:System.Windows.Forms.DragEventArgs.Effect%2A>.  
  
 Dans la procédure suivante, vous allez utiliser une application Windows que vous aurez créée, ainsi que le traitement de texte WordPad fourni avec le système d'exploitation Windows pour effectuer des opérations de glisser-déplacer entre applications. WordPad possède un ensemble d'effets autorisés pour le texte faisant l'objet du glisser-déplacer. L'application Windows pour laquelle vous allez écrire du code utilisera ces effets pour que les opérations de glisser-déplacer se déroulent correctement.  
  
### <a name="to-perform-a-drag-and-drop-procedure-between-applications"></a>Pour effectuer une opération de glisser-déplacer entre applications  
  
1.  Créez une application Windows Forms.  
  
2.  Ajoutez un contrôle <xref:System.Windows.Forms.TextBox> à votre formulaire.  
  
3.  Configurez le contrôle <xref:System.Windows.Forms.TextBox> pour recevoir les données déposées.  
  
     Pour plus d’informations, consultez [Procédure pas à pas : Exécution d’une opération de glisser-déplacer dans les Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).  
  
4.  Exécutez votre application Windows et pendant que celle-ci s'exécute, exécutez WordPad.  
  
     WordPad est un éditeur de texte installé par Windows qui permet les opérations de glisser-déplacer. Il est accessible en appuyant sur la **Démarrer** bouton, en sélectionnant **exécuter**, puis en tapant `WordPad` dans la zone de texte de la **exécuter** boîte de dialogue et en cliquant sur **OK**.  
  
5.  Une fois que WordPad est ouvert, tapez une chaîne de texte.  
  
6.  À l'aide de la souris, sélectionnez le texte, puis faites glisser le texte sélectionné vers le contrôle <xref:System.Windows.Forms.TextBox> dans votre application Windows.  
  
     Notez que quand vous placez la souris sur le contrôle <xref:System.Windows.Forms.TextBox> (et déclenchez donc l'événement <xref:System.Windows.Forms.Control.DragEnter>), le curseur se transforme et vous pouvez placer le texte sélectionné dans le contrôle <xref:System.Windows.Forms.TextBox>.  
  
     En outre, vous pouvez configurer le contrôle <xref:System.Windows.Forms.TextBox> pour permettre le glisser-déplacer des chaînes de texte dans WordPad. Pour plus d’informations, consultez [Procédure pas à pas : Exécution d’une opération de glisser-déplacer dans les Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Ajouter des données dans le Presse-papiers](how-to-add-data-to-the-clipboard.md)
- [Guide pratique pour Récupérer des données à partir du Presse-papiers](how-to-retrieve-data-from-the-clipboard.md)
- [Opérations glisser-déposer et prise en charge du Presse-papiers](drag-and-drop-operations-and-clipboard-support.md)
