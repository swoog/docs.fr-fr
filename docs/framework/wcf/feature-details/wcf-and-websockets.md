---
title: WCF et WebSockets
ms.date: 03/30/2017
ms.assetid: 1e53b49e-022c-49c7-8984-4b21b53c05b3
ms.openlocfilehash: ac888db14ebd21c4aed2f717c1f71bed310b8388
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768730"
---
# <a name="wcf-and-websockets"></a>WCF et WebSockets
.NET Framework 4.5 introduit la prise en charge de WebSockets dans Windows Communication Foundation.  WebSockets est une technologie efficace basée sur des normes qui permet la communication bidirectionnelle sur les ports HTTP standard 80 et 443. L'utilisation des ports HTTP standard permet à WebSockets de communiquer sur le Web via des intermédiaires.  Deux nouvelles liaisons standard ont été ajoutées pour prendre en charge les communications via un transport WebSocket. Voir <xref:System.ServiceModel.NetHttpBinding> et <xref:System.ServiceModel.NetHttpsBinding>. Paramètres spécifiques à WebSockets peuvent être configurés sur le <xref:System.ServiceModel.Channels.HttpTransportBindingElement> en accédant à la <xref:System.ServiceModel.Channels.HttpTransportBindingElement.WebSocketSettings%2A> propriété.
  
## <a name="in-this-section"></a>Dans cette section  
 [Utilisation de NetHttpBinding](../../../../docs/framework/wcf/feature-details/using-the-nethttpbinding.md)  
 Décrit <xref:System.ServiceModel.NetHttpBinding> et la façon de le configurer.  
  
 [Guide pratique pour Créer un Service WCF qui communique sur WebSockets](../../../../docs/framework/wcf/feature-details/how-to-create-a-wcf-service-that-communicates-over-websockets.md)  
 Décrit comment créer un service WCF qui communique sur WebSockets  
  
## <a name="reference"></a>Référence  
  
## <a name="related-sections"></a>Rubriques connexes
