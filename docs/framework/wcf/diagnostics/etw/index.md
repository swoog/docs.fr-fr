---
title: Traçage analytique avec ETW
ms.date: 03/30/2017
helpviewer_keywords:
- diagnostics [WCF], analytic tracing
- administration [WCF], analytic tracing
- analytic tracing [WCF]
ms.assetid: 1d518e47-a38d-41e8-93d7-8c3b361f6a56
ms.openlocfilehash: cff13439995d8a90da15b7afa15723f21574e35e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61962043"
---
# <a name="analytic-tracing-with-etw"></a>Traçage analytique avec ETW
Traçage analytique de Windows Communication Foundation (WCF) offre un moyen pour capturer les informations de diagnostic pendant l’exécution d’un service WCF. Événements de traçage analytique de WCF sont émis à des points clés dans la pile WCF pour permettre le dépannage des services WCF dans un environnement de production. Traçage analytique pour les services WCF a un impact minimal sur les performances d’un serveur de produit qui héberge [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] comme ces événements sont très efficacement émis vers une session de suivi d’événements Windows (ETW) des services WCF.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d’ensemble du suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/analytic-tracing-overview.md)  
 Décrit le fonctionne de traçage analytique de WCF [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)].  
  
 [Activation dynamique du suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/dynamically-enabling-analytic-tracing.md)  
 Explique comment activer ou désactiver le traçage de manière dynamique à l'aide d'ETW.  
  
 [Configuration du suivi de flux de messages](../../../../../docs/framework/wcf/diagnostics/etw/configuring-message-flow-tracing.md)  
 Décrit comment configurer le traçage du flux des messages.  
  
 [Informations de référence sur les événements de suivi analytique](../../../../../docs/framework/wcf/diagnostics/etw/analytic-trace-event-reference.md)  
 Affiche une table d'ID d'événements avec leurs niveaux d'événements, leurs messages d'événements et leurs mots clés.  
  
## <a name="see-also"></a>Voir aussi

- [Services WCF et suivi des événements pour Windows](../../../../../docs/framework/wcf/samples/wcf-services-and-event-tracing-for-windows.md)
- [Événements de suivi dans Event Tracing for Windows](../../../../../docs/framework/windows-workflow-foundation/samples/tracking-events-into-event-tracing-in-windows.md)
