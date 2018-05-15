---
title: '&lt;add&gt; de &lt;filters&gt;'
ms.date: 03/30/2017
ms.assetid: e3bf437c-dd99-49f3-9792-9a8721e6eaad
ms.openlocfilehash: 2a26a94c01fdb04b8a9e2d381a28cc909bbdac8f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltaddgt-of-ltfiltersgt"></a><span data-ttu-id="9d7dd-102">&lt;add&gt; de &lt;filters&gt;</span><span class="sxs-lookup"><span data-stu-id="9d7dd-102">&lt;add&gt; of &lt;filters&gt;</span></span>
<span data-ttu-id="9d7dd-103">Filtre XPath qui spécifie le type de message à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-103">A XPath filter that specifies the kind of message to be logged.</span></span>  
  
 <span data-ttu-id="9d7dd-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="9d7dd-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="9d7dd-105">\<diagnostic ></span><span class="sxs-lookup"><span data-stu-id="9d7dd-105">\<diagnostic></span></span>  
<span data-ttu-id="9d7dd-106">\<enregistrement des messages ></span><span class="sxs-lookup"><span data-stu-id="9d7dd-106">\<messageLogging></span></span>  
<span data-ttu-id="9d7dd-107">\<filtres ></span><span class="sxs-lookup"><span data-stu-id="9d7dd-107">\<filters></span></span>  
<span data-ttu-id="9d7dd-108">\<add></span><span class="sxs-lookup"><span data-stu-id="9d7dd-108">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d7dd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d7dd-109">Syntax</span></span>  
  
```xml  
<filters>  
   <add filter="String"/>  
</filters>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9d7dd-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9d7dd-110">Attributes and Elements</span></span>  
 <span data-ttu-id="9d7dd-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9d7dd-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="9d7dd-112">Attributes</span></span>  
  
|<span data-ttu-id="9d7dd-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d7dd-113">Attribute</span></span>|<span data-ttu-id="9d7dd-114">Description</span><span class="sxs-lookup"><span data-stu-id="9d7dd-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9d7dd-115">filtre</span><span class="sxs-lookup"><span data-stu-id="9d7dd-115">filter</span></span>|<span data-ttu-id="9d7dd-116">Chaîne qui spécifie une requête sur un document XML défini par une expression XPath 1.0.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-116">A string that specifies a query on an XML document defined by an XPath 1.0 expression.</span></span> <span data-ttu-id="9d7dd-117">Pour plus d'informations, consultez <xref:System.ServiceModel.Dispatcher.XPathMessageFilter>.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-117">For more information, see <xref:System.ServiceModel.Dispatcher.XPathMessageFilter>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9d7dd-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9d7dd-118">Child Elements</span></span>  
 <span data-ttu-id="9d7dd-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9d7dd-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9d7dd-120">Parent Elements</span></span>  
  
|<span data-ttu-id="9d7dd-121">Élément</span><span class="sxs-lookup"><span data-stu-id="9d7dd-121">Element</span></span>|<span data-ttu-id="9d7dd-122">Description</span><span class="sxs-lookup"><span data-stu-id="9d7dd-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9d7dd-123">\<filtres ></span><span class="sxs-lookup"><span data-stu-id="9d7dd-123">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters.md)|<span data-ttu-id="9d7dd-124">Contient une collection de filtres XPath utilisés pour contrôler le type de message enregistré.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-124">Contains a collection of XPath filters used to control what kind of message is logged.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9d7dd-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9d7dd-125">Remarks</span></span>  
 <span data-ttu-id="9d7dd-126">Les filtres sont appliqués uniquement à la couche de transport, spécifiée par `logMessagesAtTransportLevel` (valeur `true`).</span><span class="sxs-lookup"><span data-stu-id="9d7dd-126">Filters are applied only at the transport layer, specified by `logMessagesAtTransportLevel` is `true`.</span></span> <span data-ttu-id="9d7dd-127">Le niveau de service et l'enregistrement du message incorrect ne sont pas affectés par les filtres.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-127">Service level and malformed message logging are not affected by filters.</span></span>  
  
 <span data-ttu-id="9d7dd-128">Pour ajouter un filtre à la collection, utilisez le mot clé `add`.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-128">To add a filter to the collection, use the `add` keyword.</span></span> <span data-ttu-id="9d7dd-129">Lorsqu'un ou plusieurs filtres sont définis, seuls les messages qui correspondent au moins à l'un des filtres sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-129">When one or more filters are defined, only messages that match at least one of the filters are logged.</span></span> <span data-ttu-id="9d7dd-130">Si aucun filtre n'est défini, tous les messages passent.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-130">If no filter is defined, all messages pass through.</span></span>  
  
 <span data-ttu-id="9d7dd-131">Les filtres prennent en charge la syntaxe XPath complète et s'appliquent dans l'ordre dans lequel ils apparaissent dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-131">Filters support the full XPath syntax, and are applied in the order they appear in the configuration file.</span></span> <span data-ttu-id="9d7dd-132">Un filtre syntaxiquement incorrect provoque la levée d'une exception de configuration.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-132">A syntactically incorrect filter results in a configuration exception.</span></span>  
  
 <span data-ttu-id="9d7dd-133">L'exemple de code suivant illustre comment configurer un filtre afin que seuls les messages contenant une section d'en-tête SOAP soient enregistrés.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-133">The following is an example of how to configure a filter that records only messages that have a SOAP Header section.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9d7dd-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d7dd-134">Example</span></span>  
 <span data-ttu-id="9d7dd-135">L'exemple de code suivant illustre comment configurer un filtre afin que seuls les messages contenant une section d'en-tête SOAP soient enregistrés.</span><span class="sxs-lookup"><span data-stu-id="9d7dd-135">The following is an example of how to configure a filter that records only messages that have a SOAP Header section.</span></span>  
  
```xml  
<messageLogging logEntireMessage="true"  
     logMalformedMessages="true" logMessagesAtServiceLevel="true"  
     logMessagesAtTransportLevel="true" maxMessagesToLog="420">  
     <filters>  
        <add xmlns:soap="http://www.w3.org/2003/05/soap-envelope">  
                        /soap:Envelope/soap:Headers  
        </add>  
     </filters>  
</messageLogging>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9d7dd-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d7dd-136">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DiagnosticSection>  
 <xref:System.ServiceModel.Diagnostics>  
 <xref:System.ServiceModel.Configuration.DiagnosticSection.MessageLogging%2A>  
 <xref:System.ServiceModel.Configuration.MessageLoggingElement>  
 <xref:System.ServiceModel.Configuration.MessageLoggingElement.Filters%2A>  
 <xref:System.ServiceModel.Configuration.XPathMessageFilterElement>  
 <xref:System.ServiceModel.Dispatcher.XPathMessageFilter>  
 [<span data-ttu-id="9d7dd-137">Configuration de la journalisation des messages</span><span class="sxs-lookup"><span data-stu-id="9d7dd-137">Configuring Message Logging</span></span>](../../../../../docs/framework/wcf/diagnostics/configuring-message-logging.md)  
 [<span data-ttu-id="9d7dd-138">Configuration de la journalisation des messages</span><span class="sxs-lookup"><span data-stu-id="9d7dd-138">Configuring Message Logging</span></span>](../../../../../docs/framework/wcf/diagnostics/configuring-message-logging.md)  
 [<span data-ttu-id="9d7dd-139">\<enregistrement des messages ></span><span class="sxs-lookup"><span data-stu-id="9d7dd-139">\<messageLogging></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagelogging.md)
