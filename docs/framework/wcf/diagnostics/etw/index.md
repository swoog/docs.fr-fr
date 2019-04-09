---
title: Traçage analytique avec ETW
ms.date: 03/30/2017
helpviewer_keywords:
- diagnostics [WCF], analytic tracing
- administration [WCF], analytic tracing
- analytic tracing [WCF]
ms.assetid: 1d518e47-a38d-41e8-93d7-8c3b361f6a56
ms.openlocfilehash: cff13439995d8a90da15b7afa15723f21574e35e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59193712"
---
# <a name="analytic-tracing-with-etw"></a><span data-ttu-id="18b76-102">Traçage analytique avec ETW</span><span class="sxs-lookup"><span data-stu-id="18b76-102">Analytic Tracing with ETW</span></span>
<span data-ttu-id="18b76-103">Traçage analytique de Windows Communication Foundation (WCF) offre un moyen pour capturer les informations de diagnostic pendant l’exécution d’un service WCF.</span><span class="sxs-lookup"><span data-stu-id="18b76-103">Windows Communication Foundation (WCF) analytic tracing offers a way to capture diagnostic information during the execution of a WCF service.</span></span> <span data-ttu-id="18b76-104">Événements de traçage analytique de WCF sont émis à des points clés dans la pile WCF pour permettre le dépannage des services WCF dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="18b76-104">WCF analytic tracing events are emitted at key points in the WCF stack to allow troubleshooting of WCF services in a production environment.</span></span> <span data-ttu-id="18b76-105">Traçage analytique pour les services WCF a un impact minimal sur les performances d’un serveur de produit qui héberge [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] comme ces événements sont très efficacement émis vers une session de suivi d’événements Windows (ETW) des services WCF.</span><span class="sxs-lookup"><span data-stu-id="18b76-105">Analytic tracing for WCF services has minimal impact on the performance of a product server that hosts [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] WCF services as these events are very efficiently emitted to an Event Tracing for Windows (ETW) session.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="18b76-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="18b76-106">In This Section</span></span>  
 [<span data-ttu-id="18b76-107">Vue d'ensemble du traçage analytique</span><span class="sxs-lookup"><span data-stu-id="18b76-107">Analytic Tracing Overview</span></span>](../../../../../docs/framework/wcf/diagnostics/etw/analytic-tracing-overview.md)  
 <span data-ttu-id="18b76-108">Décrit le fonctionne de traçage analytique de WCF [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="18b76-108">Discusses how WCF analytic tracing works in [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)].</span></span>  
  
 [<span data-ttu-id="18b76-109">Activation dynamique du traçage analytique</span><span class="sxs-lookup"><span data-stu-id="18b76-109">Dynamically Enabling Analytic Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/etw/dynamically-enabling-analytic-tracing.md)  
 <span data-ttu-id="18b76-110">Explique comment activer ou désactiver le traçage de manière dynamique à l'aide d'ETW.</span><span class="sxs-lookup"><span data-stu-id="18b76-110">Discusses how to enable or disable tracing dynamically using ETW.</span></span>  
  
 [<span data-ttu-id="18b76-111">Configuration du suivi de flux de messages</span><span class="sxs-lookup"><span data-stu-id="18b76-111">Configuring Message Flow Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/etw/configuring-message-flow-tracing.md)  
 <span data-ttu-id="18b76-112">Décrit comment configurer le traçage du flux des messages.</span><span class="sxs-lookup"><span data-stu-id="18b76-112">Describes how to configure message flow tracing.</span></span>  
  
 [<span data-ttu-id="18b76-113">Référence d'événement de trace analytique</span><span class="sxs-lookup"><span data-stu-id="18b76-113">Analytic Trace Event Reference</span></span>](../../../../../docs/framework/wcf/diagnostics/etw/analytic-trace-event-reference.md)  
 <span data-ttu-id="18b76-114">Affiche une table d'ID d'événements avec leurs niveaux d'événements, leurs messages d'événements et leurs mots clés.</span><span class="sxs-lookup"><span data-stu-id="18b76-114">Shows a table of event IDs with their event levels, event messages and keywords.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18b76-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18b76-115">See also</span></span>

- [<span data-ttu-id="18b76-116">WCF Services et suivi d'événements Windows</span><span class="sxs-lookup"><span data-stu-id="18b76-116">WCF Services and Event Tracing for Windows</span></span>](../../../../../docs/framework/wcf/samples/wcf-services-and-event-tracing-for-windows.md)
- [<span data-ttu-id="18b76-117">Événements de suivi dans Event Tracing for Windows</span><span class="sxs-lookup"><span data-stu-id="18b76-117">Tracking Events into Event Tracing in Windows</span></span>](../../../../../docs/framework/windows-workflow-foundation/samples/tracking-events-into-event-tracing-in-windows.md)
