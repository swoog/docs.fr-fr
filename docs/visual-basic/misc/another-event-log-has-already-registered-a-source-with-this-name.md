---
title: Une source de ce nom a déjà été inscrite dans un autre journal des événements.
ms.date: 07/20/2015
ms.assetid: e6f5cd95-bb3f-4845-84fb-ae623a9bd44e
ms.openlocfilehash: b32169b79521ec7d0c429e1dce641aca9d747bb1
ms.sourcegitcommit: 5c1abeec15fbddcc7dbaa729fabc1f1f29f12045
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58032152"
---
# <a name="another-event-log-has-already-registered-a-source-with-this-name"></a><span data-ttu-id="75b64-102">Une source de ce nom a déjà été inscrite dans un autre journal des événements.</span><span class="sxs-lookup"><span data-stu-id="75b64-102">Another event log has already registered a source with this name</span></span>
<span data-ttu-id="75b64-103">Il a été tenté d’écrire une entrée dans un journal d’événements dans lequel la source spécifiée est inscrite dans un autre journal d’événements.</span><span class="sxs-lookup"><span data-stu-id="75b64-103">An attempt was made to write an entry to an event log where the specified source is registered with another event log.</span></span>  
  
 <span data-ttu-id="75b64-104">Vous devez définir la propriété <xref:System.Diagnostics.EventLog.Source%2A> de l’instance de votre composant <xref:System.Diagnostics.EventLog> avant que celui-ci écrive une entrée dans un journal.</span><span class="sxs-lookup"><span data-stu-id="75b64-104">You must set the <xref:System.Diagnostics.EventLog.Source%2A> property of your <xref:System.Diagnostics.EventLog> component instance before your component writes an entry to a log.</span></span> <span data-ttu-id="75b64-105">Dans ce cas, le système vérifie que la source que vous avez spécifiée est inscrite dans le journal d’événements dans lequel le composant écrit et appelle <xref:System.Diagnostics.EventLog.CreateEventSource%2A> , si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="75b64-105">When this happens, the system checks that the source you specified is registered with the event log to which the component is writing, and calls <xref:System.Diagnostics.EventLog.CreateEventSource%2A> if needed.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="75b64-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="75b64-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="75b64-107">Supprimez l’association entre la source et le premier journal à l’aide de la méthode <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> ou <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> .</span><span class="sxs-lookup"><span data-stu-id="75b64-107">Remove the association of the source with the first log using the <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> or the <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> method.</span></span>  
  
2.  <span data-ttu-id="75b64-108">Inscrivez la source dans le nouveau journal.</span><span class="sxs-lookup"><span data-stu-id="75b64-108">Register the source with the new log.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75b64-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75b64-109">See also</span></span>

- [<span data-ttu-id="75b64-110">My.Application.Log</span><span class="sxs-lookup"><span data-stu-id="75b64-110">My.Application.Log</span></span>](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)
