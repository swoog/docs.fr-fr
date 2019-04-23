---
title: System.ServiceModel.MessageClosedAgain
ms.date: 03/30/2017
ms.assetid: 24c274d4-65cd-4c91-9869-bc6eb34ef979
ms.openlocfilehash: a18355d55359df665d0e936ce95da34bf07aec6a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181334"
---
# <a name="systemservicemodelmessageclosedagain"></a><span data-ttu-id="bbe04-102">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="bbe04-102">System.ServiceModel.MessageClosedAgain</span></span>
<span data-ttu-id="bbe04-103">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="bbe04-103">System.ServiceModel.MessageClosedAgain</span></span>  
  
## <a name="description"></a><span data-ttu-id="bbe04-104">Description</span><span class="sxs-lookup"><span data-stu-id="bbe04-104">Description</span></span>  
 <span data-ttu-id="bbe04-105">Un message a de nouveau été fermé.</span><span class="sxs-lookup"><span data-stu-id="bbe04-105">A message was closed again.</span></span>  
  
 <span data-ttu-id="bbe04-106">Un message ne doit être fermé qu'une seule fois.</span><span class="sxs-lookup"><span data-stu-id="bbe04-106">A message should be closed only once.</span></span> <span data-ttu-id="bbe04-107">Si ce suivi est émis dans le code d’extension utilisateur, il indique que ce code ferme un message qui a déjà été fermé.</span><span class="sxs-lookup"><span data-stu-id="bbe04-107">If this trace is being emitted in user extension code, it indicates that the user extension code is closing a message that has already been closed.</span></span> <span data-ttu-id="bbe04-108">Si ce suivi est émis via le code produit, il indique que le code d’extension utilisateur peut éventuellement fermer un message trop tôt.</span><span class="sxs-lookup"><span data-stu-id="bbe04-108">If this trace is being emitted through product code, it indicates that the user extension code could potentially be closing a message too early.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bbe04-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbe04-109">See also</span></span>

- [<span data-ttu-id="bbe04-110">Suivi</span><span class="sxs-lookup"><span data-stu-id="bbe04-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="bbe04-111">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="bbe04-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="bbe04-112">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="bbe04-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
