---
title: Vue d’ensemble des transactions Windows Communication Foundation
ms.date: 03/30/2017
helpviewer_keywords:
- transactions [WCF]
- WCF, transactions
- Windows Communication Foundation, transactions
ms.assetid: c7757854-1207-4019-8b31-552578b7d570
ms.openlocfilehash: 42276a9b450b6f0664901747239195ab13f7c44d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59223106"
---
# <a name="windows-communication-foundation-transactions-overview"></a>Vue d’ensemble des transactions Windows Communication Foundation
Les transactions permettent de regrouper un ensemble d’actions ou d’opérations dans une unité d’exécution unique et indivisible. Une transaction est une collection d'opérations avec les propriétés suivantes :  
  
-   Atomicité. Cela garantit que toutes les mises à jour effectuées sous une transaction spécifique sont validées et rendues durable ou qu'elles sont toutes interrompues et rétablies à leur état précédent.  
  
-   Cohérence. Cela garantit que les modifications effectuées sous une transaction représentent une transformation d'un état cohérent à un autre. Par exemple, une transaction qui transfère de l’argent d’un compte chèques à un compte épargne ne modifie pas la somme d’argent dans le compte bancaire global.  
  
-   Isolement. Cela empêche une transaction d’observer des modifications non validées appartenant à d’autres transactions simultanées. L’isolation fournit une abstraction de l’accès concurrentiel tout en garantissant qu’une transaction ne peut pas avoir d’impact inattendu sur l’exécution d’une autre transaction.  
  
-   Durabilité. Cela signifie qu’une fois validées, les mises à jour des ressources managées (telles qu’un enregistrement de base de données) seront persistantes en cas de défaillance.  
  
 Windows Communication Foundation (WCF) fournit un ensemble rich de fonctionnalités qui vous permettent de créer des transactions distribuées dans votre application de service Web.  
  
 WCF implémente la prise en charge le protocole WS-AtomicTransaction (WS-AT) qui permet aux applications WCF pour transférer des transactions aux applications interopérables, telles que les services Web interopérables créés à l’aide d’une technologie tierce. WCF implémente également la prise en charge pour le protocole OLE Transactions, qui peut être utilisé dans les scénarios où vous n’avez pas besoin des fonctionnalités d’interopérabilité pour activer le flux de transaction.  
  
 Vous pouvez utiliser un fichier de configuration d’application pour configurer des liaisons afin d’activer ou de désactiver le flux de transaction, ainsi que pour définir le protocole de transaction souhaité sur une liaison. De plus, vous pouvez définir des délais d’expiration de transaction au niveau du service à l’aide du fichier de configuration. Pour plus d’informations, consultez [l’activation de flux de Transaction](../../../../docs/framework/wcf/feature-details/enabling-transaction-flow.md).  
  
 Les attributs de transaction dans l’espace de noms <xref:System.ServiceModel> vous permettent d’effectuer les opérations suivantes :  
  
-   configurer des délais d’expiration de transaction et un filtrage de niveau isolation à l’aide de l’attribut <xref:System.ServiceModel.ServiceBehaviorAttribute> ;  
  
-   activer la fonctionnalité de transactions et configurer le comportement de fin de transaction à l'aide de l'attribut <xref:System.ServiceModel.OperationBehaviorAttribute> ;  
  
-   utiliser les attributs <xref:System.ServiceModel.ServiceContractAttribute> et <xref:System.ServiceModel.OperationContractAttribute> sur une méthode de contrat pour exiger, autoriser ou refuser le flux de transaction.  
  
 Pour plus d’informations, consultez [attributs de Transaction ServiceModel](../../../../docs/framework/wcf/feature-details/servicemodel-transaction-attributes.md).  
  
## <a name="see-also"></a>Voir aussi

- [Attributs de transaction ServiceModel](../../../../docs/framework/wcf/feature-details/servicemodel-transaction-attributes.md)
- [Activation du flux de transaction](../../../../docs/framework/wcf/feature-details/enabling-transaction-flow.md)
