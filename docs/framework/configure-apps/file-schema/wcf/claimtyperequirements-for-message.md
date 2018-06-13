---
title: '&lt;claimTypeRequirements&gt; de &lt;message&gt;'
ms.date: 03/30/2017
ms.assetid: f95c5ecd-abb6-4b77-a6d7-a38727f4a142
ms.openlocfilehash: f4460311f5478f441b819bc8a48540d6feea69b1
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32754543"
---
# <a name="ltclaimtyperequirementsgt-for-ltmessagegt"></a>&lt;claimTypeRequirements&gt; de &lt;message&gt;
Spécifie une collection de types de revendications requis.  
  
 La collection est utilisée par le service pour spécifier toutes les revendications obligatoires et facultatives qui doivent se trouver dans le jeton émis que le client utilise pour accéder au service. Le service expose les types de revendication obligatoires dans les métadonnées si la publication WSDL est activée mais WCF ne requiert pas que le jeton émis contienne les types de revendication spécifiés. Les services qui souhaitent appliquer l'obligation de présence des types de revendication obligatoires doivent le faire à l'aide de la stratégie d'autorisation.  
  
 Sur les clients fédérés, cette collection contient la liste des revendications obligatoires et facultatives envoyée au service d’émission de jeton de sécurité dans la demande de jeton émis du client.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.ClaimTypeRequirements%2A>  
 <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>  
 <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.ClaimTypeRequirements%2A>  
 <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ClaimTypeElement>
