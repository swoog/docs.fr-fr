---
title: '&lt;transactionFlow&gt;'
ms.date: 03/30/2017
ms.assetid: 8c7b4c5b-ace3-4fe3-89ff-7b13c9aacd13
ms.openlocfilehash: 6f0660ce94fdfbe1ab636aa4197ef31526c21348
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145794"
---
# <a name="lttransactionflowgt"></a><span data-ttu-id="5e1f6-102">&lt;transactionFlow&gt;</span><span class="sxs-lookup"><span data-stu-id="5e1f6-102">&lt;transactionFlow&gt;</span></span>
<span data-ttu-id="5e1f6-103">Spécifie le support du flux de la transaction pour la liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-103">Specifies transaction flow support for the custom binding.</span></span>  
  
 <span data-ttu-id="5e1f6-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5e1f6-104">\<system.serviceModel></span></span>  
<span data-ttu-id="5e1f6-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="5e1f6-105">\<bindings></span></span>  
<span data-ttu-id="5e1f6-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="5e1f6-106">\<customBinding></span></span>  
<span data-ttu-id="5e1f6-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5e1f6-107">\<binding></span></span>  
<span data-ttu-id="5e1f6-108">\<transactionFlow ></span><span class="sxs-lookup"><span data-stu-id="5e1f6-108">\<transactionFlow></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e1f6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e1f6-109">Syntax</span></span>  
  
```xml  
<transactionFlow transactionProtocol="OleTransactions/WSAtomicTransactionOctober2004" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5e1f6-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5e1f6-110">Attributes and Elements</span></span>  
 <span data-ttu-id="5e1f6-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5e1f6-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="5e1f6-112">Attributes</span></span>  
  
|<span data-ttu-id="5e1f6-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="5e1f6-113">Attribute</span></span>|<span data-ttu-id="5e1f6-114">Description</span><span class="sxs-lookup"><span data-stu-id="5e1f6-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5e1f6-115">transactionProtocol</span><span class="sxs-lookup"><span data-stu-id="5e1f6-115">transactionProtocol</span></span>|<span data-ttu-id="5e1f6-116">Spécifie le protocole de transaction à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-116">Specifies the transaction protocol to be used.</span></span> <span data-ttu-id="5e1f6-117">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e1f6-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="5e1f6-118">-OleTransactions</span><span class="sxs-lookup"><span data-stu-id="5e1f6-118">-   OleTransactions</span></span><br /><span data-ttu-id="5e1f6-119">-WSAtomicTransactionOctober2004</span><span class="sxs-lookup"><span data-stu-id="5e1f6-119">-   WSAtomicTransactionOctober2004</span></span><br /><br /> <span data-ttu-id="5e1f6-120">La valeur par défaut est OleTransactions.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-120">The default is OleTransactions.</span></span><br /><br /> <span data-ttu-id="5e1f6-121">Cet attribut est de type <xref:System.ServiceModel.TransactionProtocol>.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-121">This attribute is of type <xref:System.ServiceModel.TransactionProtocol>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5e1f6-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5e1f6-122">Child Elements</span></span>  
 <span data-ttu-id="5e1f6-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5e1f6-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5e1f6-124">Parent Elements</span></span>  
  
|<span data-ttu-id="5e1f6-125">Élément</span><span class="sxs-lookup"><span data-stu-id="5e1f6-125">Element</span></span>|<span data-ttu-id="5e1f6-126">Description</span><span class="sxs-lookup"><span data-stu-id="5e1f6-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5e1f6-127">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5e1f6-127">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="5e1f6-128">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-128">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5e1f6-129">Notes</span><span class="sxs-lookup"><span data-stu-id="5e1f6-129">Remarks</span></span>  
 <span data-ttu-id="5e1f6-130">Cet élément vous permet d’activer ou de désactiver le flux de transactions entrantes dans les paramètres de liaison d’un point de terminaison, ainsi que de spécifier le format de protocole souhaité pour les transactions entrantes.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-130">This element allows you to enable or disable incoming transaction flow in an endpoint’s binding settings, as well as to specify the desired protocol format for incoming transactions.</span></span> <span data-ttu-id="5e1f6-131">Pour plus d’informations sur l’utilisation de cet élément de configuration, consultez [Configuration des transactions ServiceModel](../../../../../docs/framework/wcf/feature-details/servicemodel-transaction-configuration.md) et [l’activation de flux de Transaction](../../../../../docs/framework/wcf/feature-details/enabling-transaction-flow.md).</span><span class="sxs-lookup"><span data-stu-id="5e1f6-131">For more information on using this configuration element, see [ServiceModel Transaction Configuration](../../../../../docs/framework/wcf/feature-details/servicemodel-transaction-configuration.md) and [Enabling Transaction Flow](../../../../../docs/framework/wcf/feature-details/enabling-transaction-flow.md).</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="5e1f6-132">Lors de l’utilisation du protocole `OleTransactions` pour faire passer les transactions d’un point de terminaison vers un autre, le délai d’attente de transaction peut se perdre si le point de terminaison de destination tente un nouveau flux à l’aide d’un autre protocole que `OleTransactions`.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-132">When using the `OleTransactions` protocol to flow transactions from endpoint to endpoint, the transaction timeout can be lost if the destination endpoint attempts to flow again using any protocol other than `OleTransactions`.</span></span> <span data-ttu-id="5e1f6-133">Cela peut provoquer l'expiration de tous les nœuds de niveau inférieur après le tronçon OleTransactions selon un délai plus long que prévu.</span><span class="sxs-lookup"><span data-stu-id="5e1f6-133">This can cause all down-level nodes after the OleTransactions hop to timeout later than expected.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e1f6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e1f6-134">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.TransactionFlowElement>  
 <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="5e1f6-135">Configuration des transactions ServiceModel</span><span class="sxs-lookup"><span data-stu-id="5e1f6-135">ServiceModel Transaction Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/servicemodel-transaction-configuration.md)  
 [<span data-ttu-id="5e1f6-136">Activation du flux de transaction</span><span class="sxs-lookup"><span data-stu-id="5e1f6-136">Enabling Transaction Flow</span></span>](../../../../../docs/framework/wcf/feature-details/enabling-transaction-flow.md)  
 [<span data-ttu-id="5e1f6-137">Liaisons</span><span class="sxs-lookup"><span data-stu-id="5e1f6-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="5e1f6-138">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="5e1f6-138">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="5e1f6-139">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="5e1f6-139">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="5e1f6-140">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="5e1f6-140">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
