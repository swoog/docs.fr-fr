---
title: System.ServiceModel.MessageClosedAgain
ms.date: 03/30/2017
ms.assetid: 24c274d4-65cd-4c91-9869-bc6eb34ef979
ms.openlocfilehash: 3a73834888ae4a8945bd71492d787e23868fa5e8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33480741"
---
# <a name="systemservicemodelmessageclosedagain"></a><span data-ttu-id="4cad5-102">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="4cad5-102">System.ServiceModel.MessageClosedAgain</span></span>
<span data-ttu-id="4cad5-103">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="4cad5-103">System.ServiceModel.MessageClosedAgain</span></span>  
  
## <a name="description"></a><span data-ttu-id="4cad5-104">Description</span><span class="sxs-lookup"><span data-stu-id="4cad5-104">Description</span></span>  
 <span data-ttu-id="4cad5-105">Un message a de nouveau été fermé.</span><span class="sxs-lookup"><span data-stu-id="4cad5-105">A message was closed again.</span></span>  
  
 <span data-ttu-id="4cad5-106">Un message ne doit être fermé qu'une seule fois.</span><span class="sxs-lookup"><span data-stu-id="4cad5-106">A message should be closed only once.</span></span> <span data-ttu-id="4cad5-107">Si ce suivi est émis dans le code d'extension utilisateur, il indique que ce code ferme un message qui a déjà été fermé.</span><span class="sxs-lookup"><span data-stu-id="4cad5-107">If this trace is being emitted in user extension code, it indicates that the user extension code is closing a message that has already been closed.</span></span> <span data-ttu-id="4cad5-108">Si ce suivi est émis via le code produit, il indique que le code d’extension utilisateur peut éventuellement fermer un message trop tôt.</span><span class="sxs-lookup"><span data-stu-id="4cad5-108">If this trace is being emitted through product code, it indicates that the user extension code could potentially be closing a message too early.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4cad5-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cad5-109">See Also</span></span>  
 [<span data-ttu-id="4cad5-110">Suivi</span><span class="sxs-lookup"><span data-stu-id="4cad5-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="4cad5-111">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="4cad5-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="4cad5-112">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="4cad5-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
