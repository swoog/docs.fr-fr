---
title: <transactedBatching>
ms.date: 03/30/2017
ms.assetid: 2f790a0d-8f03-4b86-81b5-ce1bc1a6c575
ms.openlocfilehash: 43415d9eac5e61f42006aecb3248dec9811eb3e6
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57366451"
---
# <a name="transactedbatching"></a><span data-ttu-id="ef157-101">\<transactedBatching></span><span class="sxs-lookup"><span data-stu-id="ef157-101">\<transactedBatching></span></span>

<span data-ttu-id="ef157-102">Spécifie si le traitement par lots de la transaction est pris en charge pour les opérations de réception.</span><span class="sxs-lookup"><span data-stu-id="ef157-102">Specifies whether transaction batching is supported for receive operations.</span></span>

<span data-ttu-id="ef157-103">\<system.ServiceModel>\\</span><span class="sxs-lookup"><span data-stu-id="ef157-103">\<system.ServiceModel>\\</span></span>
<span data-ttu-id="ef157-104">\<behaviors>\\</span><span class="sxs-lookup"><span data-stu-id="ef157-104">\<behaviors>\\</span></span>
<span data-ttu-id="ef157-105">\<endpointBehaviors>\\</span><span class="sxs-lookup"><span data-stu-id="ef157-105">\<endpointBehaviors>\\</span></span>
<span data-ttu-id="ef157-106">\<behavior>\\</span><span class="sxs-lookup"><span data-stu-id="ef157-106">\<behavior>\\</span></span>
<span data-ttu-id="ef157-107">\<transactedBatching></span><span class="sxs-lookup"><span data-stu-id="ef157-107">\<transactedBatching></span></span>

## <a name="syntax"></a><span data-ttu-id="ef157-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef157-108">Syntax</span></span>

```xml
<transactedBatching maxBatchSize="Integer" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="ef157-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ef157-109">Attributes and Elements</span></span>

<span data-ttu-id="ef157-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ef157-110">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="ef157-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ef157-111">Attributes</span></span>

|<span data-ttu-id="ef157-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="ef157-112">Attribute</span></span>|<span data-ttu-id="ef157-113">Description</span><span class="sxs-lookup"><span data-stu-id="ef157-113">Description</span></span>|
|---------------|-----------------|
|`maxBatchSize`|<span data-ttu-id="ef157-114">Entier qui spécifie le nombre maximal d'opérations de réception qui peuvent être regroupées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="ef157-114">An integer that specifies the maximum number of receive operations that can be batched together in one transaction.</span></span> <span data-ttu-id="ef157-115">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="ef157-115">The default is 0.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="ef157-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ef157-116">Child Elements</span></span>

<span data-ttu-id="ef157-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ef157-117">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="ef157-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ef157-118">Parent Elements</span></span>

|<span data-ttu-id="ef157-119">Élément</span><span class="sxs-lookup"><span data-stu-id="ef157-119">Element</span></span>|<span data-ttu-id="ef157-120">Description</span><span class="sxs-lookup"><span data-stu-id="ef157-120">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="ef157-121">\<behavior></span><span class="sxs-lookup"><span data-stu-id="ef157-121">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="ef157-122">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ef157-122">Specifies an endpoint behavior.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ef157-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ef157-123">Remarks</span></span>

<span data-ttu-id="ef157-124">Un transport configuré avec le traitement par lots de la transaction fait des tentatives de traitement par lot de plusieurs opérations de réception en une transaction.</span><span class="sxs-lookup"><span data-stu-id="ef157-124">A transport that is configured with transaction batching attempts to batch several receive operations into one transaction.</span></span> <span data-ttu-id="ef157-125">Ainsi, le coût relativement élevé de la création d’une transaction et de sa validation dans chaque opération de réception est évité.</span><span class="sxs-lookup"><span data-stu-id="ef157-125">By doing so, the relatively high cost of creating a transaction and committing it in every receive operation is avoided.</span></span>

## <a name="example"></a><span data-ttu-id="ef157-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="ef157-126">Example</span></span>

<span data-ttu-id="ef157-127">L'exemple suivant explique comment ajouter le comportement de traitement par lot avec transaction à un service dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="ef157-127">The following example shows how to add the transacted batching behavior to a service in a configuration file.</span></span>

```xml
<system.serviceModel>
  <services>
    <service name="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <host>
        <baseAddresses>
          <add baseAddress="http://localhost:8000/ServiceModelSamples/service" />
        </baseAddresses>
      </host>
      <!-- Define NetMsmqEndpoint -->
      <endpoint address="net.msmq://localhost/private/ServiceModelSamples"
                binding="netMsmqBinding"
                contract="Microsoft.ServiceModel.Samples.IQueueCalculator" />
      <!-- the mex endpoint is exposed at http://localhost:8000/ServiceModelSamples/service/mex -->
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

## <a name="see-also"></a><span data-ttu-id="ef157-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef157-128">See also</span></span>

- <xref:System.ServiceModel.Configuration.TransactedBatchingElement>
- <xref:System.ServiceModel.Description.TransactedBatchingBehavior>
