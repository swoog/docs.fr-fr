---
title: '&lt;transactedBatching&gt;'
ms.date: 03/30/2017
ms.assetid: 2f790a0d-8f03-4b86-81b5-ce1bc1a6c575
ms.openlocfilehash: f0cf0b78ddcbd3214e30a36ce7641d115275a265
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="lttransactedbatchinggt"></a><span data-ttu-id="63c65-102">&lt;transactedBatching&gt;</span><span class="sxs-lookup"><span data-stu-id="63c65-102">&lt;transactedBatching&gt;</span></span>
<span data-ttu-id="63c65-103">Spécifie si le traitement par lots de la transaction est pris en charge pour les opérations de réception.</span><span class="sxs-lookup"><span data-stu-id="63c65-103">Specifies whether transaction batching is supported for receive operations.</span></span>  
  
 <span data-ttu-id="63c65-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="63c65-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="63c65-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="63c65-105">\<behaviors></span></span>  
<span data-ttu-id="63c65-106">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="63c65-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="63c65-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="63c65-107">\<behavior></span></span>  
<span data-ttu-id="63c65-108">\<transactedBatching ></span><span class="sxs-lookup"><span data-stu-id="63c65-108">\<transactedBatching></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63c65-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63c65-109">Syntax</span></span>  
  
```xml  
<transactedBatching maxBatchSize="Integer" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="63c65-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="63c65-110">Attributes and Elements</span></span>  
 <span data-ttu-id="63c65-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="63c65-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="63c65-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="63c65-112">Attributes</span></span>  
  
|<span data-ttu-id="63c65-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="63c65-113">Attribute</span></span>|<span data-ttu-id="63c65-114">Description</span><span class="sxs-lookup"><span data-stu-id="63c65-114">Description</span></span>|  
|---------------|-----------------|  
|`maxBatchSize`|<span data-ttu-id="63c65-115">Entier qui spécifie le nombre maximal d'opérations de réception qui peuvent être regroupées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="63c65-115">An integer that specifies the maximum number of receive operations that can be batched together in one transaction.</span></span> <span data-ttu-id="63c65-116">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="63c65-116">The default is 0.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="63c65-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="63c65-117">Child Elements</span></span>  
 <span data-ttu-id="63c65-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="63c65-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="63c65-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="63c65-119">Parent Elements</span></span>  
  
|<span data-ttu-id="63c65-120">Élément</span><span class="sxs-lookup"><span data-stu-id="63c65-120">Element</span></span>|<span data-ttu-id="63c65-121">Description</span><span class="sxs-lookup"><span data-stu-id="63c65-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="63c65-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="63c65-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="63c65-123">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="63c65-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="63c65-124">Notes</span><span class="sxs-lookup"><span data-stu-id="63c65-124">Remarks</span></span>  
 <span data-ttu-id="63c65-125">Un transport configuré avec le traitement par lots de la transaction fait des tentatives de traitement par lot de plusieurs opérations de réception en une transaction.</span><span class="sxs-lookup"><span data-stu-id="63c65-125">A transport that is configured with transaction batching attempts to batch several receive operations into one transaction.</span></span> <span data-ttu-id="63c65-126">Ainsi, le coût relativement élevé de la création d’une transaction et de sa validation dans chaque opération de réception est évité.</span><span class="sxs-lookup"><span data-stu-id="63c65-126">By doing so, the relatively high cost of creating a transaction and committing it in every receive operation is avoided.</span></span>  
  
## <a name="example"></a><span data-ttu-id="63c65-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="63c65-127">Example</span></span>  
 <span data-ttu-id="63c65-128">L'exemple suivant explique comment ajouter le comportement de traitement par lot avec transaction à un service dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="63c65-128">The following example shows how to add the transacted batching behavior to a service in a configuration file.</span></span>  
  
```xml  
<system.serviceModel>  
  <services>  
    <service name="Microsoft.ServiceModel.Samples.CalculatorService"  
             behaviorConfiguration="CalculatorServiceBehavior">  
      <host>  
        <baseAddresses>  
          <add baseAddress="http://localhost:8000/ServiceModelSamples/service"/>  
        </baseAddresses>  
      </host>  
  
      <!-- Define NetMsmqEndpoint -->  
      <endpoint address="net.msmq://localhost/private/ServiceModelSamples"  
                binding="netMsmqBinding"  
                contract="Microsoft.ServiceModel.Samples.IQueueCalculator" />  
  
      <!-- the mex endpoint is explosed at http://localhost:8000/ServiceModelSamples/service/mex -->  
      <endpoint address="mex"  
                binding="mexHttpBinding"  
                contract="IMetadataExchange" />  
    </service>  
  </services>  
  
  <behaviors>  
    <endpointBehaviors>  
      <behavior name="endpointBehavior">  
        <transactedBatching maxBatchSize="10" />  
      </behavior>  
    </endpointBehaviors>  
    <serviceBehaviors>  
      <behavior name="CalculatorServiceBehavior">  
        <serviceMetadata httpGetEnabled="true" />  
      </behavior>  
    </serviceBehaviors>  
  </behaviors>  
</system.serviceModel>  
```  
  
## <a name="see-also"></a><span data-ttu-id="63c65-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63c65-129">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.TransactedBatchingElement>  
 <xref:System.ServiceModel.Description.TransactedBatchingBehavior>
