---
title: Conversations sécurisées et sessions sécurisées
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 48cb104a-532d-40ae-aa57-769dae103fda
caps.latest.revision: 13
author: BrucePerlerMS
ms.author: bruceper
manager: mbaldwin
ms.workload:
- dotnet
ms.openlocfilehash: 502064ce30f6e117168834643a116d3983811fb8
ms.sourcegitcommit: 94d33cadc5ff81d2ac389bf5f26422c227832052
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2018
---
# <a name="secure-conversations-and-secure-sessions"></a><span data-ttu-id="fdb83-102">Conversations sécurisées et sessions sécurisées</span><span class="sxs-lookup"><span data-stu-id="fdb83-102">Secure Conversations and Secure Sessions</span></span>
<span data-ttu-id="fdb83-103">[!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] a la capacité d'établir des sessions sécurisées entre deux points de terminaison qui s'authentifient l'un l'autre et conviennent d'un chiffrement et d'un processus de signature numérique.</span><span class="sxs-lookup"><span data-stu-id="fdb83-103">A feature of [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] is the ability to establish secure sessions between two endpoints that authenticate each other and agree upon an encryption and digital signature process.</span></span> <span data-ttu-id="fdb83-104">Par exemple, le point de terminaison de service peut demander qu'un point de terminaison de client envoie un jeton de sécurité basé sur un certificat X.509 pour l'authentification.</span><span class="sxs-lookup"><span data-stu-id="fdb83-104">For example, the service endpoint might require a client endpoint to send a security token based upon an X.509 certificate for authentication.</span></span> <span data-ttu-id="fdb83-105">Une fois que le client est authentifié, le point de terminaison de service renvoie un jeton de contexte de sécurité (SCT) au client, utilisé ensuite pour sécuriser tous les messages suivants dans la session.</span><span class="sxs-lookup"><span data-stu-id="fdb83-105">Once the client is authenticated, the service endpoint returns a security context token (SCT) back to the client that is then used to secure all subsequent messages within the session.</span></span> <span data-ttu-id="fdb83-106">L'établissement de cette session sécurisée permet d'améliorer l'ensemble des messages échangés entre les deux points de terminaison, parce que le SCT a une clé symétrique.</span><span class="sxs-lookup"><span data-stu-id="fdb83-106">Establishing this secure session enables the set of messages that are exchanged between the two endpoints to be more efficient, because the SCT has a symmetric key.</span></span> <span data-ttu-id="fdb83-107">Les clés asymétriques, sur lesquelles les certificats X.509 sont basés, requièrent beaucoup plus de puissance de calcul que les clés symétriques pour générer une signature numérique ou chiffrer un jeu de données.</span><span class="sxs-lookup"><span data-stu-id="fdb83-107">Asymmetric keys, which X.509 certificates are based upon, require significantly more computational power than symmetric keys when generating a digital signature or encrypting a set of data.</span></span>  
  
 <span data-ttu-id="fdb83-108">La stratégie de démarrage (défini dans la section 6.2.7 de la [WS-SecurityPolicy](http://go.microsoft.com/fwlink/?LinkId=99817) standard) contient les assertions de sécurité de message utilisées pour sécuriser le canal et d’authentifier le client avant l’échange RST/SCT et RSTR/SCT.</span><span class="sxs-lookup"><span data-stu-id="fdb83-108">The bootstrap policy (defined in section 6.2.7 of the [WS-SecurityPolicy](http://go.microsoft.com/fwlink/?LinkId=99817) standard) contains the message security assertions used to secure the channel and authenticate the client prior to the RST/SCT and RSTR/SCT exchange.</span></span> <span data-ttu-id="fdb83-109">Certaines liaisons standard [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] ont une propriété `Security.Message.EstablishSecurityContext` qui contrôle si la conversation sécurisée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fdb83-109">Certain [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] standard bindings have a `Security.Message.EstablishSecurityContext` property which controls whether secure conversation is used.</span></span> <span data-ttu-id="fdb83-110">Lorsque vous utilisez des liaisons personnalisées le programme d’amorçage est indiqué par imbrication éléments de liaison de sécurité, que ce soit via [ \<secureConversationBootstrap >](../../../../docs/framework/configure-apps/file-schema/wcf/secureconversationbootstrap.md) dans le fichier de configuration, ou en appelant <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateSecureConversationBindingElement%2A> dans le code.</span><span class="sxs-lookup"><span data-stu-id="fdb83-110">When using custom bindings the bootstrap is indicated by nesting security binding elements, either through [\<secureConversationBootstrap>](../../../../docs/framework/configure-apps/file-schema/wcf/secureconversationbootstrap.md) in the configuration file, or by calling <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateSecureConversationBindingElement%2A> in code.</span></span>  
  
 <span data-ttu-id="fdb83-111">Pour plus d’informations sur les sessions, consultez [à l’aide de Sessions](../../../../docs/framework/wcf/using-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="fdb83-111">For more information about sessions, see [Using Sessions](../../../../docs/framework/wcf/using-sessions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fdb83-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdb83-112">See Also</span></span>  
 [<span data-ttu-id="fdb83-113">Sessions, instanciation et accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="fdb83-113">Sessions, Instancing, and Concurrency</span></span>](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)  
 [<span data-ttu-id="fdb83-114">Guide pratique pour créer un service qui requiert des sessions</span><span class="sxs-lookup"><span data-stu-id="fdb83-114">How to: Create a Service That Requires Sessions</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-that-requires-sessions.md)
