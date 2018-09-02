---
title: Opérations glisser-déposer et prise en charge du Presse-papiers
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms]
- drag and drop [Windows Forms], Windows Forms
- Clipboard [Windows Forms], Windows Forms
ms.assetid: 7cce79b6-5835-46fd-b690-73f12ad368b2
ms.openlocfilehash: c2bb3c24298ffe5308af03c5af5bae697a22c33b
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43398630"
---
# <a name="drag-and-drop-operations-and-clipboard-support"></a>Opérations glisser-déposer et prise en charge du Presse-papiers
Vous pouvez activer les opérations de glisser-déplacer dans une application Windows en gérant une série d'événements, notamment <xref:System.Windows.Forms.Control.DragEnter>, <xref:System.Windows.Forms.Control.DragLeave>, et <xref:System.Windows.Forms.Control.DragDrop> .  
  
 Vous pouvez aussi implémenter la prise en charge des opérations couper/copier/coller par l'utilisateur et le transfert de données par l'utilisateur dans le Presse-papiers dans vos applications Windows à l'aide de simples appels de méthode.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Procédure pas à pas : exécution d’opérations de glisser-déposer dans Windows Forms](../../../../docs/framework/winforms/advanced/walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md)  
 Explique comment démarrer une opération de glisser-déposer.  
  
 [Guide pratique pour exécuter des opérations de glisser-déposer entre des applications](../../../../docs/framework/winforms/advanced/how-to-perform-drag-and-drop-operations-between-applications.md)  
 Montre comment effectuer des opérations de glisser-déposer entre des applications.  
  
 [Guide pratique pour ajouter des données au Presse-papiers](../../../../docs/framework/winforms/advanced/how-to-add-data-to-the-clipboard.md)  
 Décrit un moyen d'insérer des informations dans le Presse-papiers par programmation.  
  
 [Guide pratique pour récupérer des données du Presse-papiers](../../../../docs/framework/winforms/advanced/how-to-retrieve-data-from-the-clipboard.md)  
 Décrit comment accéder aux données stockées dans le Presse-papiers.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Fonctionnalité de glisser-déposer dans les Windows Forms](../../../../docs/framework/winforms/drag-and-drop-functionality-in-windows-forms.md)  
 Décrit les méthodes, les événements et les classes utilisés pour implémenter le comportement de glisser-déposer.  
  
 <xref:System.Windows.Forms.Control.QueryContinueDrag>  
 Décrit les complexités de l'événement qui demande l'autorisation de continuer l'opération glisser.  
  
 <xref:System.Windows.Forms.Control.DoDragDrop%2A>  
 Décrit les complexités de la méthode qui est centrale au démarrage d'une opération glisser.  
  
 <xref:System.Windows.Forms.Clipboard>  
 Consultez également [Comment : envoyer des données à l’enfant MDI actif](https://msdn.microsoft.com/library/y0hkh2c8\(v=vs.110\)).
