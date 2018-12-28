---
title: Liaisons WS-MetadataExchange
ms.date: 03/30/2017
ms.assetid: 10f8de5d-b81d-4ea7-b37e-7f2c00c39714
ms.openlocfilehash: 03e6e6d5ee7e69b397acd0f51b8037f02c1804ec
ms.sourcegitcommit: 0888d7b24f475c346a3f444de8d83ec1ca7cd234
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/22/2018
ms.locfileid: "53767346"
---
# <a name="ws-metadataexchange-bindings"></a>Liaisons WS-MetadataExchange
Cette rubrique décrit comment les liaisons d’échange de métadonnées par défaut sont construites pour les divers transports.  
  
## <a name="the-default-bindings"></a>Liaisons par défaut  
  
|Nom de la liaison par défaut|Construction de la liaison|  
|--------------------------|------------------------------------|  
|mexHttpBinding|<xref:System.ServiceModel.WSHttpBinding> avec la sécurité au niveau du transport désactivée.|  
|mexHttpsBinding|<xref:System.ServiceModel.WSHttpBinding> qui prend en charge la sécurité au niveau du transport.|  
|mexNamedPipeBinding|<xref:System.ServiceModel.Channels.CustomBinding> avec <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement> en utilisant les valeurs par défaut.|  
|mexTcpBinding|<xref:System.ServiceModel.Channels.CustomBinding> avec <xref:System.ServiceModel.Channels.TcpTransportBindingElement> en utilisant les valeurs par défaut.|
