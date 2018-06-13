---
title: Modèles de transaction
ms.date: 03/30/2017
ms.assetid: 48a8bc1b-128b-4cf1-a421-8cc73223c340
ms.openlocfilehash: 9efe8c6994cc80957b707bbae0885a3c5896f70a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33499022"
---
# <a name="transaction-models"></a>Modèles de transaction
Cette rubrique décrit la relation entre les modèles de programmation de transactions et les composants d’infrastructure que Microsoft fournit.  
  
 Lors de l’utilisation de transactions dans Windows Communication Foundation (WCF), il est important de comprendre que vous ne choisissez ne pas entre des modèles transactionnels différents, mais évoluez dans des couches différentes d’un modèle intégré et cohérent.  
  
 Les sections suivantes décrivent les trois composants principaux d’une transaction.  
  
## <a name="windows-communication-foundation-transactions"></a>Transactions WCF (Windows Communication Foundation)  
 La prise en charge des transactions dans WCF vous permet de que écrire des services transactionnels. En outre, avec sa prise en charge du protocole WS-AtomicTransaction (WS-AT), les applications peuvent transférer des transactions aux services Web construits à l’aide de WCF ou une technologie tiers.  
  
 Dans une application ou un service WCF, fonctionnalités de la transaction WCF fournissent des attributs et configuration pour spécifier de façon déclarative comment et quand l’infrastructure doit créer, de flux et synchroniser des transactions.  
  
## <a name="systemtransactions-transactions"></a>Transactions System.Transactions  
 L'espace de noms <xref:System.Transactions> fournit un modèle de programmation explicite basé sur la classe <xref:System.Transactions.Transaction>, ainsi qu'un modèle de programmation implicite à utilisant la classe <xref:System.Transactions.TransactionScope>, dans lequel l'infrastructure gère automatiquement les transactions.  
  
 Pour plus d’informations sur la création d’une application transactionnelle à l’aide de ces deux modèles, consultez [l’écriture d’une Application transactionnelle](http://go.microsoft.com/fwlink/?LinkId=94947).  
  
 Dans une application, ou un service WCF <xref:System.Transactions> fournit le modèle de programmation pour créer des transactions dans une application cliente et pour interagir explicitement avec une transaction, à la demande, au sein d’un service.  
  
## <a name="msdtc-transactions"></a>Transactions MSDTC  
 MSDTC (Microsoft Distributed Transaction Coordinator) est un gestionnaire de transactions qui prend en charge les transactions distribuées.  
  
 Pour plus d’informations, consultez la [de référence du programmeur DTC](http://go.microsoft.com/fwlink/?LinkId=94948).  
  
 Dans une application ou un service WCF, MSDTC fournit l’infrastructure pour la coordination de transactions créées au sein d’un client ou un service.
