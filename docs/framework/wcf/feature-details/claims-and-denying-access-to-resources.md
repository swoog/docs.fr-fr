---
title: Revendications et refus de l'accès aux ressources
ms.date: 03/30/2017
helpviewer_keywords:
- claims [WCF], denying access to resources
ms.assetid: 145ebb41-680e-4256-b14c-1efb4af1e982
ms.openlocfilehash: df35ea2f01f96b044763c696434e5ede39d6b4bd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715749"
---
# <a name="claims-and-denying-access-to-resources"></a>Revendications et refus de l'accès aux ressources
Windows Communication Foundation (WCF) prend en charge un mécanisme d’autorisation basée sur les revendications. Tout en permettant l'accès aux ressources en fonction de la présence de certaines revendications, les systèmes refusent souvent cet accès en fonction de la présence d'autres revendications. Les systèmes de ce type doivent rechercher dans <xref:System.IdentityModel.Policy.AuthorizationContext> les revendications qui donnent lieu à un refus d'accès avant de rechercher celles donnant lieu à une autorisation d'accès.  
  
 Par exemple, un système peut refuser l'accès à une ressource à toute personne qui dispose d'une revendication de type `Age`, d'un droit <xref:System.IdentityModel.Claims.Rights.PossessProperty%2A> et d'une valeur de ressource `Under 21` uniquement si cette identité a également une revendication de type `Name`, un droit <xref:System.IdentityModel.Claims.Rights.Identity%2A> et une valeur de ressource `Mallory`. En d'autres termes, le système refuse l'accès à toute personne de moins de 21 ans et accorde l'accès si le nom est Mallory. Pour implémenter correctement cette sémantique, il est important de rechercher dans un premier temps la revendication `Age` et de déterminer si l'âge de la personne se situe au-dessous de 21 ans. Sinon, si Mallory à moins de 21 ans, alors l'accès à la ressource pourra être accordé uniquement sur la base de la revendication `Name`.  
  
## <a name="see-also"></a>Voir aussi
- [Gestion des revendications et autorisation avec le modèle d’identité](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)
- [Revendications et jetons](../../../../docs/framework/wcf/feature-details/claims-and-tokens.md)
