---
title: Attribution d'un nouveau nom à un service WCF
ms.date: 03/30/2017
ms.assetid: 14235a65-b1c5-409d-b6cc-a979acd54bbd
ms.openlocfilehash: 8cb86621972423f55bfa18c60c1d4eb60cacb205
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64651044"
---
# <a name="renaming-a-wcf-service"></a><span data-ttu-id="bc6f6-102">Attribution d'un nouveau nom à un service WCF</span><span class="sxs-lookup"><span data-stu-id="bc6f6-102">Renaming a WCF Service</span></span>
<span data-ttu-id="bc6f6-103">Cette rubrique décrit comment vous pouvez renommer un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="bc6f6-103">This topic describes how you can rename a Windows Communication Foundation (WCF) service.</span></span>  
  
## <a name="renaming-a-wcf-service"></a><span data-ttu-id="bc6f6-104">Attribution d'un nouveau nom à un service WCF</span><span class="sxs-lookup"><span data-stu-id="bc6f6-104">Renaming a WCF Service</span></span>  
 <span data-ttu-id="bc6f6-105">Procédez comme suit pour renommer un service dans un modèle de Windows Communication Foundation (WCF)</span><span class="sxs-lookup"><span data-stu-id="bc6f6-105">Perform the following steps to rename a service in a Windows Communication Foundation (WCF) template,</span></span>  
  
- <span data-ttu-id="bc6f6-106">Modifiez le nom de la classe qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-106">Change the name of the class that implements the service.</span></span>  
  
- <span data-ttu-id="bc6f6-107">Dans le fichier de configuration du service, remplacez le nom du service par celui que vous avez choisi, comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-107">In the configuration file of the service, change the name of the service to the new name you have chosen, as indicated in the following example.</span></span> <span data-ttu-id="bc6f6-108">Selon votre modèle d'hébergement, le fichier de configuration sera app.config ou web.config.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-108">The configuration file can be either app.config or web.config file depending on your hosting model.</span></span>  
  
```xml  
<system.servicemodel>  
   <services>  
      <service name="WcfService.NewName">  
      </service>  
   </services>  
</system.servicemodel>  
```  
  
- <span data-ttu-id="bc6f6-109">Si votre service est hébergé sur le Web, il utilise un fichier \*.svc.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-109">If your service is webhosted, it uses an \*.svc file.</span></span> <span data-ttu-id="bc6f6-110">Ouvrez le fichier svc et modifiez le nom de votre service comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-110">Open the svc file and modify the name of your service as indicated in the following example.</span></span> <span data-ttu-id="bc6f6-111">Cette étape n'est pas nécessaire pour les applications auto-hébergées, puisqu'il n'y a pas de fichier svc.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-111">This step is not necessary for self-hosted applications, as there is no svc file.</span></span>  
  
```  
<%@ ServiceHost Service="WcfService.NewName">  
```  
  
## <a name="renaming-a-wcf-service-contract"></a><span data-ttu-id="bc6f6-112">Attribution d'un nouveau nom à un contrat de service WCF</span><span class="sxs-lookup"><span data-stu-id="bc6f6-112">Renaming a WCF Service Contract</span></span>  
  
- <span data-ttu-id="bc6f6-113">Effectuez les étapes suivantes pour renommer le contrat de service</span><span class="sxs-lookup"><span data-stu-id="bc6f6-113">Perform the following steps to rename the service contract,</span></span>  
  
- <span data-ttu-id="bc6f6-114">Modifiez le nom du contrat de service.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-114">Change the name of the service contract.</span></span>  
  
- <span data-ttu-id="bc6f6-115">Dans le fichier de configuration du service, remplacez le nom du contrat de service par le celui que vous avez choisi, comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-115">In the configuration file of the service, change the name of the service contract to the new name you have chosen, as indicated in the following example.</span></span> <span data-ttu-id="bc6f6-116">Selon votre modèle d'hébergement, le fichier de configuration sera app.config ou web.config.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-116">The configuration file can be either app.config or web.config file depending on your hosting model.</span></span>  
  
```xml  
<system.servicemodel>  
   <services>  
      <service>  
         <endpoint contract="WcfService.NewContractName" />  
      </service>  
   </services>  
</system.servicemodel>  
```
