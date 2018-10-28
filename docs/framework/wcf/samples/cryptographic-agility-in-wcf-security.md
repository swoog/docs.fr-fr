---
title: Agilité de chiffrement dans sécurité WCF
ms.date: 03/30/2017
ms.assetid: c2c549e5-ac19-40c5-b686-8f67f52b6dbf
ms.openlocfilehash: 9f7c1157c9bf4f2e0baf7dcbafbcc9fca4aee89d
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50187333"
---
# <a name="cryptographic-agility-in-wcf-security"></a><span data-ttu-id="0021c-102">Agilité de chiffrement dans sécurité WCF</span><span class="sxs-lookup"><span data-stu-id="0021c-102">Cryptographic Agility in WCF Security</span></span>
<span data-ttu-id="0021c-103">Cet exemple montre comment spécifier dans un algorithme standard ou personnalisé pour fournir une implémentation de chiffrement agile dans un client Windows Communication Foundation (WCF) et le service.</span><span class="sxs-lookup"><span data-stu-id="0021c-103">This sample shows how to specify in a standard/custom algorithm to provide a cryptographic agile implementation in a Windows Communication Foundation (WCF) client and service.</span></span> <span data-ttu-id="0021c-104">Cet exemple est composé des projets suivants :</span><span class="sxs-lookup"><span data-stu-id="0021c-104">The sample is composed of the following projects:</span></span>

 <span data-ttu-id="0021c-105">Service, il s’agit d’un service WCF auto-hébergé qui implémente le `ICalculator` interface et sécurise le point de terminaison à l’aide de la <<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`> avec la session sécurisée et la session fiable désactivée.</span><span class="sxs-lookup"><span data-stu-id="0021c-105">Service This is a self-hosted WCF service that implements the `ICalculator` interface and secures the endpoint using the <<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`> with secure session and reliable session disabled.</span></span> <span data-ttu-id="0021c-106">Le service définit une classe `SecurityAlgorithmSuite` personnalisée pour spécifier les algorithmes de chiffrement à utiliser pour la sécurité du message.</span><span class="sxs-lookup"><span data-stu-id="0021c-106">The service defines a custom `SecurityAlgorithmSuite` class to specify the cryptographic algorithms to be used for message security.</span></span>

 <span data-ttu-id="0021c-107">Client il s’agit d’un WCFclient qui accède au service après une authentification réussie.</span><span class="sxs-lookup"><span data-stu-id="0021c-107">Client This is a WCFclient that accesses the service after successful authentication.</span></span> <span data-ttu-id="0021c-108">Il appelle les opérations exposées par l'interface `ICalculator` et implémentées par le service.</span><span class="sxs-lookup"><span data-stu-id="0021c-108">It invokes the operations exposed by the `ICalculator` interface and implemented by the service.</span></span> <span data-ttu-id="0021c-109">Le client définit également la même classe `SecurityAlgorithmSuite` personnalisée pour spécifier les algorithmes de chiffrement à utiliser pour la sécurité du message.</span><span class="sxs-lookup"><span data-stu-id="0021c-109">The client also defines the same custom `SecurityAlgorithmSuite` class to specify the cryptographic algorithms to be used for message security.</span></span>

### <a name="to-use-this-sample"></a><span data-ttu-id="0021c-110">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="0021c-110">To use this sample</span></span>

1.  <span data-ttu-id="0021c-111">Ouvrez la solution CryptoAgility.sln dans Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="0021c-111">Open the CryptoAgility.sln solution in Visual Studio 2012.</span></span>

2.  <span data-ttu-id="0021c-112">Appuyez sur Ctrl+Maj+B pour générer la solution.</span><span class="sxs-lookup"><span data-stu-id="0021c-112">Press CTRL+SHIFT+B to build the solution.</span></span>

3.  <span data-ttu-id="0021c-113">Ouvrez [!INCLUDE[fileExplorer](../../../../includes/fileexplorer-md.md)] , accédez au répertoire \WCF\Basic\Security\CryptoAgility\Service\bin et exécutez le fichier service.exe avec des privilèges d’administrateur en double-cliquant sur service.exe et en sélectionnant **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="0021c-113">Open [!INCLUDE[fileExplorer](../../../../includes/fileexplorer-md.md)] and navigate to the \WCF\Basic\Security\CryptoAgility\Service\bin directory and run the service.exe file with administrator privileges by right-clicking service.exe and selecting **Run as administrator**.</span></span>

4.  <span data-ttu-id="0021c-114">Accédez au répertoire \WCF\Basic\Security\CryptoAgility\Client\bin et exécutez le fichier client.exe normalement.</span><span class="sxs-lookup"><span data-stu-id="0021c-114">Navigate to \WCF\Basic\Security\CryptoAgility\Client\bin directory and run the client.exe file normally.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="0021c-115">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0021c-115">The samples may already be installed on your machine.</span></span> <span data-ttu-id="0021c-116">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="0021c-116">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="0021c-117">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="0021c-117">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="0021c-118">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="0021c-118">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Security\CryptoAgility`  
  
## <a name="see-also"></a><span data-ttu-id="0021c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0021c-119">See Also</span></span>  
 [<span data-ttu-id="0021c-120">Sécurité</span><span class="sxs-lookup"><span data-stu-id="0021c-120">Security</span></span>](../../../../docs/framework/wcf/feature-details/security.md)
