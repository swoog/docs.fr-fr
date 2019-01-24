---
title: '&lt;binding&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 666183d6-4d1f-45c7-ac64-bdf93ee8f36f
ms.openlocfilehash: fb4fafda31205e2ce5efd01ab265fcacfa70bdf6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539192"
---
# <a name="ltbindinggt"></a><span data-ttu-id="1dcd9-102">&lt;binding&gt;</span><span class="sxs-lookup"><span data-stu-id="1dcd9-102">&lt;binding&gt;</span></span>
<span data-ttu-id="1dcd9-103">Vous pouvez utiliser l’élément de `binding` pour configurer différents types de liaisons prédéfinies fournis par Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="1dcd9-103">You can use the `binding` element to configure different types of predefined bindings provided by Windows Communication Foundation (WCF).</span></span>  
  
## <a name="system-provided-binding"></a><span data-ttu-id="1dcd9-104">Liaison fournie par le système</span><span class="sxs-lookup"><span data-stu-id="1dcd9-104">System-Provided Binding</span></span>  
 <span data-ttu-id="1dcd9-105">Les liaisons fournies par le système masquent la complexité de la pile de la messagerie du WCF.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-105">System-provided bindings hide the complexity of the WCF messaging stack.</span></span> <span data-ttu-id="1dcd9-106">Les applications qui utilisent des liaisons fournies par le système ne requièrent pas de contrôle total sur la pile.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-106">Applications using system-provided bindings do not require full control over the stack.</span></span> <span data-ttu-id="1dcd9-107">Les attributs exposés sur chaque liaison fournie par le système sont les plus appropriés pour le scénario d'utilisation des adresses de liaison.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-107">The attributes exposed on each system-provided binding are the ones most appropriate for the usage scenario the binding addresses.</span></span>  
  
 <span data-ttu-id="1dcd9-108">La section de configuration de chaque liaison fournie par le système peut définir plusieurs configurations utilisées en vue de configurer la liaison.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-108">The configuration section for each system-provided binding can define several configurations used to configure the binding.</span></span> <span data-ttu-id="1dcd9-109">Chaque configuration est identifiée par un nom unique.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-109">Each configuration is identified by a unique name.</span></span>  
  
 <span data-ttu-id="1dcd9-110">Il n'est pas possible d'ajouter des éléments ou des attributs à une liaison fournie par le système.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-110">It is not possible to add elements or attributes to a system-provided binding.</span></span> <span data-ttu-id="1dcd9-111">Pour cela, vous devez implémenter une liaison personnalisée, telle que décrite dans la section « Liaison personnalisée » de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-111">To do so, you should implement a custom binding as described in the "Custom Binding" section of this topic.</span></span> <span data-ttu-id="1dcd9-112">Il est possible de définir une liaison personnalisée qui imite parfaitement une liaison fournie par le système et ajoute quelques paramètres sur lesquels l'utilisateur de l'application souhaite avoir le contrôle.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-112">It is possible to define a custom binding that mimics a system-provided binding perfectly and adds a few settings the user application wants to have control over.</span></span>  
  
## <a name="custom-binding"></a><span data-ttu-id="1dcd9-113">Liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="1dcd9-113">Custom Binding</span></span>  
 <span data-ttu-id="1dcd9-114">Les liaisons personnalisées permettent d'exercer un contrôle total sur la pile de messagerie WCF.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-114">Custom bindings provide full control over the WCF messaging stack.</span></span> <span data-ttu-id="1dcd9-115">Une liaison individuelle définit la pile de messages en spécifiant les éléments de configuration des éléments de la pile suivant leur l'ordre d'apparition dans cette pile.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-115">An individual binding defines the message stack by specifying the configuration elements for the stack elements in the order they appear on the stack.</span></span> <span data-ttu-id="1dcd9-116">Chaque élément définit et configure l'élément de la pile.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-116">Each element defines and configures the one element of the stack.</span></span> <span data-ttu-id="1dcd9-117">Il doit y avoir un seul élément de `transport` dans chaque liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-117">There must be one and only one `transport` element in each custom binding.</span></span> <span data-ttu-id="1dcd9-118">Sans cet élément, la pile de messagerie est incomplète.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-118">Without this element, the messaging stack is incomplete.</span></span>  
  
 <span data-ttu-id="1dcd9-119">L'ordre dans lequel les éléments apparaissent dans la pile est important car il s'agit de l'ordre dans lequel les opérations sont appliquées au message.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-119">The order in which elements appear in the stack matters, because it is the order in which operations are applied to the message.</span></span> <span data-ttu-id="1dcd9-120">Voici l'ordre recommandé des éléments de la pile :</span><span class="sxs-lookup"><span data-stu-id="1dcd9-120">The recommended order of stack elements is the following:</span></span>  
  
1.  <span data-ttu-id="1dcd9-121">Transactions (facultatif)</span><span class="sxs-lookup"><span data-stu-id="1dcd9-121">Transactions (optional)</span></span>  
  
2.  <span data-ttu-id="1dcd9-122">Messagerie fiable (facultatif)</span><span class="sxs-lookup"><span data-stu-id="1dcd9-122">Reliable Messaging (optional)</span></span>  
  
3.  <span data-ttu-id="1dcd9-123">Sécurité (facultatif)</span><span class="sxs-lookup"><span data-stu-id="1dcd9-123">Security (optional)</span></span>  
  
4.  <span data-ttu-id="1dcd9-124">Encodeur</span><span class="sxs-lookup"><span data-stu-id="1dcd9-124">Encoder</span></span>  
  
5.  <span data-ttu-id="1dcd9-125">Transport</span><span class="sxs-lookup"><span data-stu-id="1dcd9-125">Transport</span></span>  
  
 <span data-ttu-id="1dcd9-126">Les liaisons personnalisées sont identifiées par leur attribut `name`.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-126">Custom bindings are identified by their `name` attribute.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1dcd9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1dcd9-127">See also</span></span>
- <xref:System.ServiceModel.Configuration.BindingsSection>
- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- [<span data-ttu-id="1dcd9-128">Liaisons</span><span class="sxs-lookup"><span data-stu-id="1dcd9-128">Bindings</span></span>](../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="1dcd9-129">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="1dcd9-129">Custom Bindings</span></span>](../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="1dcd9-130">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="1dcd9-130">\<customBinding></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
