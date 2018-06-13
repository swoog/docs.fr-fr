---
title: Traçage analytique avec ETW
ms.date: 03/30/2017
helpviewer_keywords:
- diagnostics [WCF], analytic tracing
- administration [WCF], analytic tracing
- analytic tracing [WCF]
ms.assetid: 1d518e47-a38d-41e8-93d7-8c3b361f6a56
ms.openlocfilehash: 210418b8a8765a1fc59658e9df57c92ce087c95f
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
ms.locfileid: "33809262"
---
# <a name="analytic-tracing-with-etw"></a>Traçage analytique avec ETW
Traçage analytique de Windows Communication Foundation (WCF) offre un moyen de capturer des informations de diagnostic pendant l’exécution d’un service WCF. Événements de traçage analytique de WCF sont émis à des points clés dans la pile de WCF pour permettre la résolution des problèmes des services WCF dans un environnement de production. Traçage analytique pour les services WCF a un impact minime sur les performances d’un serveur de produit qui héberge [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] que ces événements sont très efficacement émis à une session de suivi événements pour Windows (ETW) des services WCF.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d’ensemble du suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/analytic-tracing-overview.md)  
 Décrit le fonctionne de traçage analytique de WCF dans [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)].  
  
 [Activation dynamique du suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/dynamically-enabling-analytic-tracing.md)  
 Explique comment activer ou désactiver le traçage de manière dynamique à l'aide d'ETW.  
  
 [Configuration du suivi de flux de messages](../../../../../docs/framework/wcf/diagnostics/etw/configuring-message-flow-tracing.md)  
 Décrit comment configurer le traçage du flux des messages.  
  
 [Informations de référence sur les événements de suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/analytic-trace-event-reference.md)  
 Affiche une table d'ID d'événements avec leurs niveaux d'événements, leurs messages d'événements et leurs mots clés.  
  
## <a name="see-also"></a>Voir aussi  
 [Services WCF et suivi des événements pour Windows](../../../../../docs/framework/wcf/samples/wcf-services-and-event-tracing-for-windows.md)  
 [Événements de suivi dans Event Tracing for Windows](../../../../../docs/framework/windows-workflow-foundation/samples/tracking-events-into-event-tracing-in-windows.md)
