---
title: Opérations glisser-déposer et prise en charge du Presse-papiers
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms]
- drag and drop [Windows Forms], Windows Forms
- Clipboard [Windows Forms], Windows Forms
ms.assetid: 7cce79b6-5835-46fd-b690-73f12ad368b2
ms.openlocfilehash: 5e7bb75b648163dab7e410a159d55ebbb75f1b0a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756427"
---
# <a name="drag-and-drop-operations-and-clipboard-support"></a>Opérations glisser-déposer et prise en charge du Presse-papiers
Vous pouvez activer les opérations de glisser-déplacer dans une application Windows en gérant une série d'événements, notamment <xref:System.Windows.Forms.Control.DragEnter>, <xref:System.Windows.Forms.Control.DragLeave>, et <xref:System.Windows.Forms.Control.DragDrop> .  
  
 Vous pouvez aussi implémenter la prise en charge des opérations couper/copier/coller par l'utilisateur et le transfert de données par l'utilisateur dans le Presse-papiers dans vos applications Windows à l'aide de simples appels de méthode.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Procédure pas à pas : Exécution d’une opération de glisser-déplacer dans les Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md)  
 Explique comment démarrer une opération de glisser-déplacer.  
  
 [Guide pratique pour Effectuer des opérations de glisser-déplacer entre les Applications](how-to-perform-drag-and-drop-operations-between-applications.md)  
 Montre comment effectuer des opérations de glisser-déplacer entre des applications.  
  
 [Guide pratique pour Ajouter des données dans le Presse-papiers](how-to-add-data-to-the-clipboard.md)  
 Décrit un moyen d'insérer des informations dans le Presse-papiers par programmation.  
  
 [Guide pratique pour Récupérer des données à partir du Presse-papiers](how-to-retrieve-data-from-the-clipboard.md)  
 Décrit comment accéder aux données stockées dans le Presse-papiers.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Fonctionnalité de glisser-déposer dans les Windows Forms](../drag-and-drop-functionality-in-windows-forms.md)  
 Décrit les méthodes, les événements et les classes utilisés pour implémenter le comportement de glisser-déplacer.  
  
 <xref:System.Windows.Forms.Control.QueryContinueDrag>  
 Décrit les complexités de l'événement qui demande l'autorisation de continuer l'opération glisser.  
  
 <xref:System.Windows.Forms.Control.DoDragDrop%2A>  
 Décrit les complexités de la méthode qui est centrale au démarrage d'une opération glisser.  
  
 <xref:System.Windows.Forms.Clipboard>  
 Voir également [Guide pratique pour Envoyer des données à l’enfant MDI actif](how-to-send-data-to-the-active-mdi-child.md).
