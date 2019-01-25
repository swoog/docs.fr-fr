---
title: Configuration des comportements clients
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: df5b32fa-e73b-4e8e-b66f-357c748e0173
ms.openlocfilehash: bf65844cda195847989d1eb8ef752fe87c9de22c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54532194"
---
# <a name="configuring-client-behaviors"></a>Configuration des comportements clients
Windows Communication Foundation (WCF) configure les comportements de deux manières : soit en vous reportant aux configurations de comportement, qui sont définies dans la `<behavior>` section d’un fichier de configuration client application – ou par programmation dans l’appel application. Cette rubrique décrit ces deux approches.  
  
 Lors de l'utilisation d'un fichier de configuration, la configuration du comportement est une collection nommée de paramètres de configuration. Le nom de chaque configuration de comportement doit être unique. Cette chaîne est utilisée dans l'attribut `behaviorConfiguration` d'une configuration de point de terminaison pour lier le point de terminaison au comportement.  
  
## <a name="example"></a>Exemple  
 Le code de configuration suivant définit un comportement appelé `myBehavior`. Le point de terminaison de client référence ce comportement dans l'attribut `behaviorConfiguration`.  
  
```xml  
<configuration>  
    <system.serviceModel>  
        <behaviors>  
            <endpointBehaviors>  
                <behavior name="myBehavior">  
                    <clientVia />  
                </behavior>  
            </endpointBehaviors>  
        </behaviors>  
        <bindings>  
            <basicHttpBinding>  
                <binding name="myBinding" maxReceivedMessageSize="10000" />  
            </basicHttpBinding>  
        </bindings>  
        <client>  
            <endpoint address="myAddress" binding="basicHttpBinding" bindingConfiguration="myBinding" behaviorConfiguration="myBehavior" contract="myContract" />  
        </client>  
    </system.serviceModel>  
</configuration>  
```  
  
## <a name="using-behaviors-programmatically"></a>Utilisation de comportements par programme  
 Vous pouvez également configurer ou insérer par programme des comportements en localisant approprié `Behaviors` propriété sur l’objet de client Windows Communication Foundation (WCF) ou sur l’objet de fabrique de canal client avant d’ouvrir le client.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant indique comment insérer par programme un comportement en accédant à la propriété <xref:System.ServiceModel.Description.ServiceEndpoint.Behaviors%2A> sur <xref:System.ServiceModel.Description.ServiceEndpoint> retournée à partir de la propriété <xref:System.ServiceModel.ChannelFactory.Endpoint%2A> avant la création de l'objet de canal.  
  
 [!code-csharp[ChannelFactoryBehaviors#10](../../../samples/snippets/csharp/VS_Snippets_CFX/channelfactorybehaviors/cs/client.cs#10)]
 [!code-vb[ChannelFactoryBehaviors#10](../../../samples/snippets/visualbasic/VS_Snippets_CFX/channelfactorybehaviors/vb/client.vb#10)]  
  
## <a name="see-also"></a>Voir aussi
- [\<behaviors>](../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md)
