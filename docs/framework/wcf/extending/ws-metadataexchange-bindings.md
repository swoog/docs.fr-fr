---
title: Liaisons WS-MetadataExchange
ms.date: 03/30/2017
ms.assetid: 10f8de5d-b81d-4ea7-b37e-7f2c00c39714
ms.openlocfilehash: 384e5bb05ba4263f245f6901b84e2388ea19bd73
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="ws-metadataexchange-bindings"></a>Liaisons WS-MetadataExchange
Cette rubrique décrit comment les liaisons d’échange de métadonnées par défaut sont construites pour les divers transports.  
  
## <a name="the-default-bindings"></a>Liaisons par défaut  
  
|Nom de la liaison par défaut|Construction de la liaison|  
|--------------------------|------------------------------------|  
|MexHttpBinding|<xref:System.ServiceModel.WSHttpBinding> avec la sécurité au niveau du transport désactivée.|  
|MexHttpsBinding|<xref:System.ServiceModel.WSHttpBinding> qui prend en charge la sécurité au niveau du transport.|  
|MexNamedPipeBinding|<xref:System.ServiceModel.Channels.CustomBinding> avec <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement> en utilisant les valeurs par défaut.|  
|MexTcpBinding|<xref:System.ServiceModel.Channels.CustomBinding> avec <xref:System.ServiceModel.Channels.TcpTransportBindingElement> en utilisant les valeurs par défaut.|
