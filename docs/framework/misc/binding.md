---
title: <binding>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 666183d6-4d1f-45c7-ac64-bdf93ee8f36f
ms.openlocfilehash: fb51eb1962603439b89a203eb668dfb543049170
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271471"
---
# <a name="binding"></a><span data-ttu-id="4fff1-101">\<binding></span><span class="sxs-lookup"><span data-stu-id="4fff1-101">\<binding></span></span>
<span data-ttu-id="4fff1-102">Vous pouvez utiliser l’élément de `binding` pour configurer différents types de liaisons prédéfinies fournis par Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="4fff1-102">You can use the `binding` element to configure different types of predefined bindings provided by Windows Communication Foundation (WCF).</span></span>  
  
## <a name="system-provided-binding"></a><span data-ttu-id="4fff1-103">Liaison fournie par le système</span><span class="sxs-lookup"><span data-stu-id="4fff1-103">System-Provided Binding</span></span>  
 <span data-ttu-id="4fff1-104">Les liaisons fournies par le système masquent la complexité de la pile de la messagerie du WCF.</span><span class="sxs-lookup"><span data-stu-id="4fff1-104">System-provided bindings hide the complexity of the WCF messaging stack.</span></span> <span data-ttu-id="4fff1-105">Les applications qui utilisent des liaisons fournies par le système ne requièrent pas de contrôle total sur la pile.</span><span class="sxs-lookup"><span data-stu-id="4fff1-105">Applications using system-provided bindings do not require full control over the stack.</span></span> <span data-ttu-id="4fff1-106">Les attributs exposés sur chaque liaison fournie par le système sont les plus appropriés pour le scénario d'utilisation des adresses de liaison.</span><span class="sxs-lookup"><span data-stu-id="4fff1-106">The attributes exposed on each system-provided binding are the ones most appropriate for the usage scenario the binding addresses.</span></span>  
  
 <span data-ttu-id="4fff1-107">La section de configuration de chaque liaison fournie par le système peut définir plusieurs configurations utilisées en vue de configurer la liaison.</span><span class="sxs-lookup"><span data-stu-id="4fff1-107">The configuration section for each system-provided binding can define several configurations used to configure the binding.</span></span> <span data-ttu-id="4fff1-108">Chaque configuration est identifiée par un nom unique.</span><span class="sxs-lookup"><span data-stu-id="4fff1-108">Each configuration is identified by a unique name.</span></span>  
  
 <span data-ttu-id="4fff1-109">Il n'est pas possible d'ajouter des éléments ou des attributs à une liaison fournie par le système.</span><span class="sxs-lookup"><span data-stu-id="4fff1-109">It is not possible to add elements or attributes to a system-provided binding.</span></span> <span data-ttu-id="4fff1-110">Pour cela, vous devez implémenter une liaison personnalisée, telle que décrite dans la section « Liaison personnalisée » de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4fff1-110">To do so, you should implement a custom binding as described in the "Custom Binding" section of this topic.</span></span> <span data-ttu-id="4fff1-111">Il est possible de définir une liaison personnalisée qui imite parfaitement une liaison fournie par le système et ajoute quelques paramètres sur lesquels l'utilisateur de l'application souhaite avoir le contrôle.</span><span class="sxs-lookup"><span data-stu-id="4fff1-111">It is possible to define a custom binding that mimics a system-provided binding perfectly and adds a few settings the user application wants to have control over.</span></span>  
  
## <a name="custom-binding"></a><span data-ttu-id="4fff1-112">Liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="4fff1-112">Custom Binding</span></span>  
 <span data-ttu-id="4fff1-113">Les liaisons personnalisées permettent d'exercer un contrôle total sur la pile de messagerie WCF.</span><span class="sxs-lookup"><span data-stu-id="4fff1-113">Custom bindings provide full control over the WCF messaging stack.</span></span> <span data-ttu-id="4fff1-114">Une liaison individuelle définit la pile de messages en spécifiant les éléments de configuration des éléments de la pile suivant leur l'ordre d'apparition dans cette pile.</span><span class="sxs-lookup"><span data-stu-id="4fff1-114">An individual binding defines the message stack by specifying the configuration elements for the stack elements in the order they appear on the stack.</span></span> <span data-ttu-id="4fff1-115">Chaque élément définit et configure l'élément de la pile.</span><span class="sxs-lookup"><span data-stu-id="4fff1-115">Each element defines and configures the one element of the stack.</span></span> <span data-ttu-id="4fff1-116">Il doit y avoir un seul élément de `transport` dans chaque liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4fff1-116">There must be one and only one `transport` element in each custom binding.</span></span> <span data-ttu-id="4fff1-117">Sans cet élément, la pile de messagerie est incomplète.</span><span class="sxs-lookup"><span data-stu-id="4fff1-117">Without this element, the messaging stack is incomplete.</span></span>  
  
 <span data-ttu-id="4fff1-118">L'ordre dans lequel les éléments apparaissent dans la pile est important car il s'agit de l'ordre dans lequel les opérations sont appliquées au message.</span><span class="sxs-lookup"><span data-stu-id="4fff1-118">The order in which elements appear in the stack matters, because it is the order in which operations are applied to the message.</span></span> <span data-ttu-id="4fff1-119">Voici l'ordre recommandé des éléments de la pile :</span><span class="sxs-lookup"><span data-stu-id="4fff1-119">The recommended order of stack elements is the following:</span></span>  
  
1.  <span data-ttu-id="4fff1-120">Transactions (facultatif)</span><span class="sxs-lookup"><span data-stu-id="4fff1-120">Transactions (optional)</span></span>  
  
2.  <span data-ttu-id="4fff1-121">Messagerie fiable (facultatif)</span><span class="sxs-lookup"><span data-stu-id="4fff1-121">Reliable Messaging (optional)</span></span>  
  
3.  <span data-ttu-id="4fff1-122">Sécurité (facultatif)</span><span class="sxs-lookup"><span data-stu-id="4fff1-122">Security (optional)</span></span>  
  
4.  <span data-ttu-id="4fff1-123">Encodeur</span><span class="sxs-lookup"><span data-stu-id="4fff1-123">Encoder</span></span>  
  
5.  <span data-ttu-id="4fff1-124">Transport</span><span class="sxs-lookup"><span data-stu-id="4fff1-124">Transport</span></span>  
  
 <span data-ttu-id="4fff1-125">Les liaisons personnalisées sont identifiées par leur attribut `name`.</span><span class="sxs-lookup"><span data-stu-id="4fff1-125">Custom bindings are identified by their `name` attribute.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4fff1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fff1-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.BindingsSection>
- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- [<span data-ttu-id="4fff1-127">Liaisons</span><span class="sxs-lookup"><span data-stu-id="4fff1-127">Bindings</span></span>](../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="4fff1-128">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="4fff1-128">Custom Bindings</span></span>](../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="4fff1-129">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4fff1-129">\<customBinding></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
