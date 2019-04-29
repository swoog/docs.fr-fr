---
title: Liaisons WS-MetadataExchange
ms.date: 03/30/2017
ms.assetid: 10f8de5d-b81d-4ea7-b37e-7f2c00c39714
ms.openlocfilehash: 03e6e6d5ee7e69b397acd0f51b8037f02c1804ec
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61795471"
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
