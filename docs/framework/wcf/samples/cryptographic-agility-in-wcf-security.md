---
title: Agilité de chiffrement dans sécurité WCF
ms.date: 03/30/2017
ms.assetid: c2c549e5-ac19-40c5-b686-8f67f52b6dbf
ms.openlocfilehash: 64519e51b82780ce2b355251245d77bff0a9e73b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273317"
---
# <a name="cryptographic-agility-in-wcf-security"></a>Agilité de chiffrement dans sécurité WCF

Cet exemple montre comment spécifier dans un algorithme standard ou personnalisé pour fournir une implémentation de chiffrement agile dans un client Windows Communication Foundation (WCF) et le service. Cet exemple est composé des projets suivants :

**Service**

Il s’agit d’un service WCF auto-hébergé qui implémente le `ICalculator` interface et sécurise le point de terminaison en utilisant la <xref:System.ServiceModel.WSHttpBinding> avec la session sécurisée et la session fiable désactivée. Le service définit une classe `SecurityAlgorithmSuite` personnalisée pour spécifier les algorithmes de chiffrement à utiliser pour la sécurité du message.

**Client**

Il s’agit d’un client WCF qui accède au service après une authentification réussie. Il appelle les opérations exposées par l'interface `ICalculator` et implémentées par le service. Le client définit également la même classe `SecurityAlgorithmSuite` personnalisée pour spécifier les algorithmes de chiffrement à utiliser pour la sécurité du message.

## <a name="to-use-this-sample"></a>Pour utiliser cet exemple

1. Ouvrez la solution CryptoAgility.sln dans Visual Studio 2012.

2. Appuyez sur Ctrl+Maj+B pour générer la solution.

3. Ouvrez [!INCLUDE[fileExplorer](~/includes/fileexplorer-md.md)] , accédez au répertoire \WCF\Basic\Security\CryptoAgility\Service\bin et exécutez le fichier service.exe avec des privilèges d’administrateur en double-cliquant sur service.exe et en sélectionnant **exécuter en tant qu’administrateur**.

4. Accédez au répertoire \WCF\Basic\Security\CryptoAgility\Client\bin et exécutez le fichier client.exe normalement.

> [!IMPORTANT]
> Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Security\CryptoAgility`

## <a name="see-also"></a>Voir aussi

- [Sécurité dans Windows Communication Foundation](../feature-details/security.md)