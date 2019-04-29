---
title: Transports dans Windows Communication Foundation
ms.date: 03/30/2017
helpviewer_keywords:
- transports [WCF]
- WCF, transports
- Windows Communication Foundation, transports
ms.assetid: 005c894b-af70-48aa-a1c1-c99338083c27
ms.openlocfilehash: 6bb8e8b90c26533661684bd403b9ec439f1bb37e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61933729"
---
# <a name="transports-in-windows-communication-foundation"></a><span data-ttu-id="22942-102">Transports dans Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="22942-102">Transports in Windows Communication Foundation</span></span>
<span data-ttu-id="22942-103">La couche de transport se situe au niveau le plus bas de la pile des canaux.</span><span class="sxs-lookup"><span data-stu-id="22942-103">The transport layer is at the lowest level of the channel stack.</span></span> <span data-ttu-id="22942-104">Les principaux transports utilisés dans Windows Communication Foundation (WCF) sont HTTP, HTTPS, TCP et canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="22942-104">The main transports used in Windows Communication Foundation (WCF) are HTTP, HTTPS, TCP, and named pipes.</span></span> <span data-ttu-id="22942-105">Les rubriques de cette section contiennent des conseils et des instructions permettant de savoir quel protocole choisir, de le configurer et de définir les propriétés de réglage afférentes.</span><span class="sxs-lookup"><span data-stu-id="22942-105">The topics in this section discuss choosing among these transports, configuring the transport, and setting tuning properties.</span></span>  
  
 <span data-ttu-id="22942-106">WCF inclut des transports supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="22942-106">WCF includes additional transports.</span></span> <span data-ttu-id="22942-107">Pour plus d’informations sur le transport Message Queuing (également appelé MSMQ), consultez [files d’attente et Sessions fiables](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="22942-107">For information about Message Queuing (also known as MSMQ) transport, see [Queues and Reliable Sessions](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md).</span></span> <span data-ttu-id="22942-108">Pour plus d’informations sur le transport de peer-to-peer, consultez [mise en réseau Peer-to-Peer](../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span><span class="sxs-lookup"><span data-stu-id="22942-108">For information about peer-to-peer transport, see [Peer-to-Peer Networking](../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="22942-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="22942-109">In This Section</span></span>  
 [<span data-ttu-id="22942-110">Choix d’un transport</span><span class="sxs-lookup"><span data-stu-id="22942-110">Choosing a Transport</span></span>](../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 <span data-ttu-id="22942-111">Présente les trois transports principaux et aborde les différents points à prendre en considération lors de leur sélection.</span><span class="sxs-lookup"><span data-stu-id="22942-111">Describes the three main transports and considerations in selecting one.</span></span>  
  
 [<span data-ttu-id="22942-112">Sélection d’un encodeur de message</span><span class="sxs-lookup"><span data-stu-id="22942-112">Choosing a Message Encoder</span></span>](../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)  
 <span data-ttu-id="22942-113">Aborde les facteurs à prendre en considération lors de la sélection d’un élément de liaison d’encodage de message.</span><span class="sxs-lookup"><span data-stu-id="22942-113">Describes factors to consider when choosing a message-encoding binding element.</span></span>  
  
 [<span data-ttu-id="22942-114">Transfert des messages par streaming</span><span class="sxs-lookup"><span data-stu-id="22942-114">Streaming Message Transfer</span></span>](../../../../docs/framework/wcf/feature-details/streaming-message-transfer.md)  
 <span data-ttu-id="22942-115">Contient des instructions permettant de configurer la couche de transport pour une diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="22942-115">Describes how to configure the transport layer to do streaming.</span></span>  
  
 [<span data-ttu-id="22942-116">Configuration de HTTP et HTTPS</span><span class="sxs-lookup"><span data-stu-id="22942-116">Configuring HTTP and HTTPS</span></span>](../../../../docs/framework/wcf/feature-details/configuring-http-and-https.md)  
 <span data-ttu-id="22942-117">Contient des instructions permettant de configurer les éléments de liaison de transport HTTP et HTTPS.</span><span class="sxs-lookup"><span data-stu-id="22942-117">Describes how to configure the HTTP and HTTPS transport binding elements.</span></span>  
  
 [<span data-ttu-id="22942-118">Guide pratique pour Remplacer la réservation d’URL WCF par une réservation restreinte</span><span class="sxs-lookup"><span data-stu-id="22942-118">How to: Replace the WCF URL Reservation with a Restricted Reservation</span></span>](../../../../docs/framework/wcf/feature-details/how-to-replace-the-wcf-url-reservation-with-a-restricted-reservation.md)  
 <span data-ttu-id="22942-119">Décrit comment utiliser les réservations WCFURL restreint.</span><span class="sxs-lookup"><span data-stu-id="22942-119">Describes how to use WCFURL restricted reservations.</span></span>  
  
 [<span data-ttu-id="22942-120">Quotas de transport</span><span class="sxs-lookup"><span data-stu-id="22942-120">Transport Quotas</span></span>](../../../../docs/framework/wcf/feature-details/transport-quotas.md)  
 <span data-ttu-id="22942-121">Aborde les points à prendre en considération lors de la définition de quotas pour la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="22942-121">Describes considerations in setting the quotas available in the transport layer.</span></span>  
  
 [<span data-ttu-id="22942-122">Utilisation des NAT et des pare-feu</span><span class="sxs-lookup"><span data-stu-id="22942-122">Working with NATs and Firewalls</span></span>](../../../../docs/framework/wcf/feature-details/working-with-nats-and-firewalls.md)  
 <span data-ttu-id="22942-123">Contient des instructions permettant de configurer la couche de transport lorsque les messages envoyés ou reçus rencontrent un pare-feu ou lorsqu'un traducteur d'adresses réseau (NAT) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="22942-123">Describes how to configure the transport layer when messages are sent or received behind a firewall or when network address translation (NAT) is present.</span></span>  
  
 [<span data-ttu-id="22942-124">Partage de ports Net.TCP</span><span class="sxs-lookup"><span data-stu-id="22942-124">Net.TCP Port Sharing</span></span>](../../../../docs/framework/wcf/feature-details/net-tcp-port-sharing.md)  
 <span data-ttu-id="22942-125">Décrit comment utiliser le composant Partage de Port Net.TCP de WCF.</span><span class="sxs-lookup"><span data-stu-id="22942-125">Describes how to use the Net.TCP Port Sharing component of WCF.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="22942-126">Référence</span><span class="sxs-lookup"><span data-stu-id="22942-126">Reference</span></span>  
 <xref:System.ServiceModel.Channels.HttpTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.HttpsTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.TcpTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>  
  
## <a name="related-sections"></a><span data-ttu-id="22942-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22942-127">Related Sections</span></span>  
 [<span data-ttu-id="22942-128">Liaisons</span><span class="sxs-lookup"><span data-stu-id="22942-128">Bindings</span></span>](../../../../docs/framework/wcf/feature-details/bindings.md)  
  
 [<span data-ttu-id="22942-129">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="22942-129">Extending Bindings</span></span>](../../../../docs/framework/wcf/extending/extending-bindings.md)
