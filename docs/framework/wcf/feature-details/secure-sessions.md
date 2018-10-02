---
title: Sessions sécurisées
ms.date: 03/30/2017
ms.assetid: 7b50602f-d7b5-42e9-8e92-1f0413df0d8b
author: BrucePerlerMS
ms.openlocfilehash: 09c261afb2c64a46fc1f4619c4ec6b2e87b3fbbf
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48027323"
---
# <a name="secure-sessions"></a>Sessions sécurisées
Une fonctionnalité de Windows Communication Foundation (WCF) est les sessions fiables qui garantissent des messages sont reçus dans l’ordre qu’ils ont été envoyés. Les rubriques de cette section traitent des implications de sécurité à considérer lors de la création d'une session fiable. Pour plus d’informations sur les sessions fiables, consultez [à l’aide de Sessions](../../../../docs/framework/wcf/using-sessions.md).  
  
> [!NOTE]
>  Lorsque l’emprunt d’identité est requis sur Windows XP, utilisez une session sécurisée sans jeton de contexte de sécurité avec état (SCT). Lorsque des SCT avec état sont utilisés avec l'emprunt d'identité, une <xref:System.InvalidOperationException> est levée. Pour plus d’informations, consultez [scénarios non pris en charge](../../../../docs/framework/wcf/feature-details/unsupported-scenarios.md).  
  
## <a name="in-this-section"></a>Dans cette section  
  
|||  
|-|-|  
|[Conversations sécurisées et sessions sécurisées](../../../../docs/framework/wcf/feature-details/secure-conversations-and-secure-sessions.md)|Les termes « conversations sécurisées » et « sessions sécurisées » sont synonymes. Cette rubrique explique le fonctionnement d’une conversation sécurisée et quand et pourquoi utiliser le modèle.|  
|[Guide pratique pour créer une session sécurisée](../../../../docs/framework/wcf/feature-details/how-to-create-a-secure-session.md)|Présente les étapes essentielles de la création d'une session sécurisée.|  
|[Guide pratique pour créer un jeton de contexte de sécurité pour une session sécurisée](../../../../docs/framework/wcf/feature-details/how-to-create-a-security-context-token-for-a-secure-session.md)|Présente les étapes nécessaires à la création d'une batterie de serveurs Web qui maintiendra l'état et les sessions avec les clients.|  
|[Considérations sur la sécurité pour les sessions sécurisées](../../../../docs/framework/wcf/feature-details/security-considerations-for-secure-sessions.md)|Décrit des considérations spéciales relatives aux sessions sécurisées.|  
  
## <a name="reference"></a>Référence  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Sessions, instanciation et accès concurrentiel](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)  
  
 [Conception et implémentation de services](../../../../docs/framework/wcf/designing-and-implementing-services.md)  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour activer la détection de relecture des messages](../../../../docs/framework/wcf/feature-details/how-to-enable-message-replay-detection.md)  
 [Attaques par relecture](../../../../docs/framework/wcf/feature-details/replay-attacks.md)  
 [Guide pratique pour créer un service qui requiert des sessions](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-that-requires-sessions.md)
