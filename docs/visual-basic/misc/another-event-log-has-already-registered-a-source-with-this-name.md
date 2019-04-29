---
title: Une source de ce nom a déjà été inscrite dans un autre journal des événements.
ms.date: 07/20/2015
ms.assetid: e6f5cd95-bb3f-4845-84fb-ae623a9bd44e
ms.openlocfilehash: d932869504b2d8a5f3a948b190e5528bfcfa664f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940607"
---
# <a name="another-event-log-has-already-registered-a-source-with-this-name"></a>Une source de ce nom a déjà été inscrite dans un autre journal des événements.
Il a été tenté d’écrire une entrée dans un journal d’événements dans lequel la source spécifiée est inscrite dans un autre journal d’événements.  
  
 Vous devez définir la propriété <xref:System.Diagnostics.EventLog.Source%2A> de l’instance de votre composant <xref:System.Diagnostics.EventLog> avant que celui-ci écrive une entrée dans un journal. Dans ce cas, le système vérifie que la source que vous avez spécifiée est inscrite dans le journal d’événements dans lequel le composant écrit et appelle <xref:System.Diagnostics.EventLog.CreateEventSource%2A> , si nécessaire.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Supprimez l’association entre la source et le premier journal à l’aide de la méthode <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> ou <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> .  
  
2. Inscrivez la source dans le nouveau journal.  
  
## <a name="see-also"></a>Voir aussi

- [My.Application.Log](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)
