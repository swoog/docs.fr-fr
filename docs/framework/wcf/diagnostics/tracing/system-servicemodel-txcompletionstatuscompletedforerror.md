---
title: System.ServiceModel.TxCompletionStatusCompletedForError
ms.date: 03/30/2017
ms.assetid: 8ade4722-a6d5-471c-b960-1cfea4ea2aa9
ms.openlocfilehash: 591e1a1dcb6746d79ff5eceba7e74e890f327354
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59112656"
---
# <a name="systemservicemodeltxcompletionstatuscompletedforerror"></a><span data-ttu-id="0c2da-102">System.ServiceModel.TxCompletionStatusCompletedForError</span><span class="sxs-lookup"><span data-stu-id="0c2da-102">System.ServiceModel.TxCompletionStatusCompletedForError</span></span>
<span data-ttu-id="0c2da-103">La transaction spécifiée pour l’opération spécifiée a été effectuée en raison d’une exception d’exécution non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0c2da-103">The specified transaction for the specified operation was completed due to an unhandled execution exception.</span></span>  
  
## <a name="description"></a><span data-ttu-id="0c2da-104">Description</span><span class="sxs-lookup"><span data-stu-id="0c2da-104">Description</span></span>  
 <span data-ttu-id="0c2da-105">Suivi lorsqu'une erreur se produit durant une tentative d'exécution de la transaction actuelle.</span><span class="sxs-lookup"><span data-stu-id="0c2da-105">Traced when an error occurs during an attempt to complete the current transaction.</span></span> <span data-ttu-id="0c2da-106">Cela se produit avant qu'une réponse ou une erreur ne soit envoyée à l'appelant.</span><span class="sxs-lookup"><span data-stu-id="0c2da-106">This happens before a reply or fault is sent to the caller.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="0c2da-107">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="0c2da-107">Troubleshooting</span></span>  
 <span data-ttu-id="0c2da-108">Inspectez le message tracé pour le message d'exception et tout élément sur lequel une action peut être effectuée.</span><span class="sxs-lookup"><span data-stu-id="0c2da-108">Inspect the traced message for the exception message and any actionable items.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c2da-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c2da-109">See also</span></span>

- [<span data-ttu-id="0c2da-110">Suivi</span><span class="sxs-lookup"><span data-stu-id="0c2da-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="0c2da-111">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="0c2da-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="0c2da-112">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="0c2da-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
