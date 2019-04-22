---
title: 'Procédure : créer un SecurityBindingElement pour un mode d’authentification spécifié'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a7c7747a-5b8c-463f-8493-7266dac75066
ms.openlocfilehash: e35df9a5dacc5f281af48cec292a09b291312119
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59124512"
---
# <a name="how-to-create-a-securitybindingelement-for-a-specified-authentication-mode"></a>Procédure : créer un SecurityBindingElement pour un mode d’authentification spécifié
Windows Communication Foundation (WCF) fournit plusieurs modes par lequel les clients et les services de s’authentifier entre eux. Vous pouvez créer des éléments de liaison de sécurité pour ces modes d'authentification en utilisant des méthodes statiques sur la classe <xref:System.ServiceModel.Channels.SecurityBindingElement> ou par la configuration, comme indiqué dans l'exemple suivant.  
  
 Pour plus d’informations sur les 18 modes d’authentification, consultez [Modes d’authentification SecurityBindingElement](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md).  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant présente des méthodes pour créer des liaisons pour les divers modes d’authentification.  
  
> [!NOTE]
>  Une fois qu'une instance de l'objet <xref:System.ServiceModel.Channels.SecurityBindingElement> est créée, plusieurs propriétés sont immuables, telles que <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.KeyType%2A> et <xref:System.ServiceModel.Channels.SecurityBindingElement.MessageSecurityVersion%2A>. L'appel de `set` sur de telles propriétés ne les modifie pas.  
  
 [!code-csharp[c_CustomBindingsAuthMode#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombindingsauthmode/cs/source.cs#2)]
 [!code-vb[c_CustomBindingsAuthMode#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_custombindingsauthmode/vb/source.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- [Modes d’authentification SecurityBindingElement](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md)
- [Guide pratique pour Créer une liaison personnalisée à l’aide de SecurityBindingElement](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
