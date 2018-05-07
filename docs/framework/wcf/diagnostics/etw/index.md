---
title: Traçage analytique avec ETW
ms.date: 03/30/2017
helpviewer_keywords:
- diagnostics [WCF], analytic tracing
- administration [WCF], analytic tracing
- analytic tracing [WCF]
ms.assetid: 1d518e47-a38d-41e8-93d7-8c3b361f6a56
ms.openlocfilehash: a0e3e3d27283e588b161e2209c5a682558d18f79
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="analytic-tracing-with-etw"></a>Traçage analytique avec ETW
Traçage analytique de Windows Communication Foundation (WCF) offre un moyen de capturer des informations de diagnostic pendant l’exécution d’un [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] service. Les événements de traçage analytique [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] sont émis à des points clés dans la pile [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] qui permettent de résoudre des problèmes liés aux services [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] dans un environnement de production. Traçage analytique pour [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] services a un impact minime sur les performances d’un serveur de produit qui héberge [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] des services que ces événements sont très efficacement émis à une session de suivi événements pour Windows (ETW).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d’ensemble du suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/analytic-tracing-overview.md)  
 Explique comment le traçage analytique [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] fonctionne avec [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)].  
  
 [Activation dynamique du suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/dynamically-enabling-analytic-tracing.md)  
 Explique comment activer ou désactiver le traçage de manière dynamique à l'aide d'ETW.  
  
 [Configuration du suivi de flux de messages](../../../../../docs/framework/wcf/diagnostics/etw/configuring-message-flow-tracing.md)  
 Décrit comment configurer le traçage du flux des messages.  
  
 [Informations de référence sur les événements de suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/analytic-trace-event-reference.md)  
 Affiche une table d'ID d'événements avec leurs niveaux d'événements, leurs messages d'événements et leurs mots clés.  
  
## <a name="see-also"></a>Voir aussi  
 [Services WCF et suivi des événements pour Windows](../../../../../docs/framework/wcf/samples/wcf-services-and-event-tracing-for-windows.md)  
 [Événements de suivi dans Event Tracing for Windows](../../../../../docs/framework/windows-workflow-foundation/samples/tracking-events-into-event-tracing-in-windows.md)
