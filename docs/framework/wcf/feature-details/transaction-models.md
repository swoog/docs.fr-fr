---
title: Modèles de transaction
ms.date: 03/30/2017
ms.assetid: 48a8bc1b-128b-4cf1-a421-8cc73223c340
ms.openlocfilehash: 8731b72d0657aa420dbb020e216c3af059916ce9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62050777"
---
# <a name="transaction-models"></a>Modèles de transaction
Cette rubrique décrit la relation entre les modèles de programmation de transactions et les composants d'infrastructure que Microsoft fournit.  
  
 Lorsque vous utilisez des transactions dans Windows Communication Foundation (WCF), il est important de comprendre que vous en sélectionnant ne pas entre différents modèles transactionnelles, mais plutôt d’exploitation sur les différentes couches d’un modèle intégré et cohérent.  
  
 Les sections suivantes décrivent les trois composants principaux d'une transaction.  
  
## <a name="windows-communication-foundation-transactions"></a>Transactions WCF (Windows Communication Foundation)  
 La prise en charge de transactions dans WCF vous permet de que écrire des services transactionnels. En outre, avec sa prise en charge pour le protocole WS-AtomicTransaction (WS-AT), les applications peuvent transférer des transactions aux services Web construits à l’aide de WCF ou une technologie tierce.  
  
 Dans une application ou un service WCF, fonctionnalités de transaction WCF fournissent des attributs et configuration pour spécifier de façon déclarative comment et quand l’infrastructure doit créer, flux et synchroniser des transactions.  
  
## <a name="systemtransactions-transactions"></a>Transactions System.Transactions  
 L’espace de noms <xref:System.Transactions> fournit un modèle de programmation explicite basé sur la classe <xref:System.Transactions.Transaction>, ainsi qu’un modèle de programmation implicite à utilisant la classe <xref:System.Transactions.TransactionScope>, dans lequel l’infrastructure gère automatiquement les transactions.  
  
 Pour plus d’informations sur la création d’une application transactionnelle à l’aide de ces deux modèles, consultez [écriture d’une Application transactionnelle](https://go.microsoft.com/fwlink/?LinkId=94947).  
  
 Dans une application, ou un service WCF <xref:System.Transactions> fournit le modèle de programmation pour la création de transactions au sein d’une application cliente et pour interagir explicitement avec une transaction, lorsque nécessaire, au sein d’un service.  
  
## <a name="msdtc-transactions"></a>Transactions MSDTC  
 MSDTC (Microsoft Distributed Transaction Coordinator) est un gestionnaire de transactions qui prend en charge les transactions distribuées.  
  
 Pour plus d’informations, consultez le [de référence du programmeur DTC](https://go.microsoft.com/fwlink/?LinkId=94948).  
  
 Dans une application ou un service WCF, MSDTC fournit l’infrastructure pour la coordination de transactions créées au sein d’un client ou un service.
