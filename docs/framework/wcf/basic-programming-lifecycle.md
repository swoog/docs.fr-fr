---
title: Cycle de vie de la programmation de base
ms.date: 03/30/2017
helpviewer_keywords:
- service creation [WCF]
ms.assetid: 7cf21bfe-23bd-46aa-8033-609f851dbf76
ms.openlocfilehash: d5322dfca1aa006ba2fc85b5dedebd09941f9c0e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499221"
---
# <a name="basic-programming-lifecycle"></a>Cycle de vie de la programmation de base
Windows Communication Foundation (WCF) permet aux applications de communiquer s’ils sont sur le même ordinateur, via Internet ou sur différentes plateformes d’application. Cette rubrique présente les tâches qui sont nécessaires pour générer une application WCF. Pour un exemple d’application fonctionnel, consultez [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md).  
  
## <a name="the-basic-tasks"></a>Tâches de base  
 Les tâches de base à accomplir sont les suivantes, dans l'ordre :  
  
1.  Définition du contrat de service. Un contrat de service spécifie la signature d'un service, les données qu'il échange et les autres données requises contractuellement. Pour plus d’informations, consultez [Designing Service Contracts](../../../docs/framework/wcf/designing-service-contracts.md).  
  
2.  Implémentation du contrat. Pour implémenter un contrat de service, créez une classe qui implémente le contrat et spécifiez les comportements personnalisés requis pour le runtime. Pour plus d’informations, consultez [Implementing Service Contracts](../../../docs/framework/wcf/implementing-service-contracts.md).  
  
3.  Configuration du service en spécifiant les informations de points de terminaison et d'autres informations de comportement. Pour plus d’informations, consultez [configuration des Services](../../../docs/framework/wcf/configuring-services.md).  
  
4.  Hébergement du service. Pour plus d’informations, consultez [Services d’hébergement](../../../docs/framework/wcf/hosting-services.md).  
  
5.  Création d'une application cliente. Pour plus d’informations, consultez [génération de Clients](../../../docs/framework/wcf/building-clients.md).  
  
 Bien que les rubriques de cette section suivent cet ordre, certains scénarios ne commencent pas au début. Par exemple, si vous souhaitez générer un client pour un service préexistant, démarrez à l'étape 5. Autrement, si vous générez un service que d'autres utiliseront, vous pouvez ignorer l'étape 5.  
  
 Une fois que vous êtes familiarisé avec le développement des contrats de service, vous pouvez également lire [Introduction à l’extensibilité](../../../docs/framework/wcf/introduction-to-extensibility.md). Si vous rencontrez des problèmes avec votre service, vérifiez [WCF résolution des problèmes de démarrage rapide](../../../docs/framework/wcf/wcf-troubleshooting-quickstart.md) pour voir si d’autres utilisateurs sur lesquels les problèmes similaires ou identiques.  
  
## <a name="see-also"></a>Voir aussi
- [Implémentation de contrats de service](../../../docs/framework/wcf/implementing-service-contracts.md)
