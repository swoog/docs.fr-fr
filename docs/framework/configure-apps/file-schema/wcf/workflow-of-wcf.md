---
title: <workflow> de WCF
ms.date: 03/30/2017
ms.assetid: c0443eba-d3b4-4fae-886e-9878daf77691
ms.openlocfilehash: 190e66096cf2dfa2028c95b22526fc3c84712ab8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59122068"
---
# <a name="workflow-of-wcf"></a><span data-ttu-id="dba18-102">\<flux de travail > de WCF</span><span class="sxs-lookup"><span data-stu-id="dba18-102">\<workflow> of WCF</span></span>
<span data-ttu-id="dba18-103">Configurez un participant au suivi qui écoute les enregistrements de suivi émis directement du runtime et les traite en fonction de sa configuration.</span><span class="sxs-lookup"><span data-stu-id="dba18-103">Configure a tracking participant that listens to the tracking records being emitted from the runtime directly and process them in whatever way it was configured.</span></span> <span data-ttu-id="dba18-104">Cela inclut l'écriture dans une sortie spécifique (par exemple, un fichier, une console ou le suivi d'événements pour Windows [ETW]), le traitement/regroupement des enregistrements ou toute autre combinaison requise.</span><span class="sxs-lookup"><span data-stu-id="dba18-104">This includes writing to a specific output (e.g., file, Console, ETW), processing/aggregating the records, or any other combination that might be required.</span></span>  
  
 <span data-ttu-id="dba18-105">Pour plus d’informations de suivi de flux de travail et les participants de suivi, consultez [suivi et traçage de Workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) et [les participants au suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md).</span><span class="sxs-lookup"><span data-stu-id="dba18-105">For more information in workflow tracking and tracking participants, see [Workflow Tracking and Tracing](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Tracking Participants](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md).</span></span>  
  
 <span data-ttu-id="dba18-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="dba18-106">\<system.serviceModel></span></span>  
<span data-ttu-id="dba18-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="dba18-107">\<tracking></span></span>  
<span data-ttu-id="dba18-108">\<participants></span><span class="sxs-lookup"><span data-stu-id="dba18-108">\<participants></span></span>  
<span data-ttu-id="dba18-109">\<add></span><span class="sxs-lookup"><span data-stu-id="dba18-109">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dba18-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dba18-110">Syntax</span></span>  
  
```xml  
<tracking>
  <participants>
    <add name="String"
         profileName="String"
         type="String" />
  </participants>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dba18-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dba18-111">Attributes and Elements</span></span>  
 <span data-ttu-id="dba18-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dba18-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dba18-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="dba18-113">Attributes</span></span>  
  
|<span data-ttu-id="dba18-114">Élément</span><span class="sxs-lookup"><span data-stu-id="dba18-114">Element</span></span>|<span data-ttu-id="dba18-115">Description</span><span class="sxs-lookup"><span data-stu-id="dba18-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="dba18-116">name</span><span class="sxs-lookup"><span data-stu-id="dba18-116">name</span></span>|<span data-ttu-id="dba18-117">Chaîne qui spécifie le nom d'un participant au suivi.</span><span class="sxs-lookup"><span data-stu-id="dba18-117">A string that specifies the name of a tracking participant.</span></span>|  
|<span data-ttu-id="dba18-118">profileName</span><span class="sxs-lookup"><span data-stu-id="dba18-118">profileName</span></span>|<span data-ttu-id="dba18-119">Chaîne qui spécifie le nom du modèle de suivi qui définit les enregistrements de suivi auxquels le participant au suivi s'est abonné.</span><span class="sxs-lookup"><span data-stu-id="dba18-119">A string that specifies the name of the tracking profile which defines the tracking records the tracking participant has subscribed to.</span></span>|  
|<span data-ttu-id="dba18-120">type</span><span class="sxs-lookup"><span data-stu-id="dba18-120">type</span></span>|<span data-ttu-id="dba18-121">Chaîne qui spécifie le type d'un participant au suivi.</span><span class="sxs-lookup"><span data-stu-id="dba18-121">A string that specifies the type of a tracking participant.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dba18-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dba18-122">Child Elements</span></span>  
 <span data-ttu-id="dba18-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dba18-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dba18-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dba18-124">Parent Elements</span></span>  
  
|<span data-ttu-id="dba18-125">Élément</span><span class="sxs-lookup"><span data-stu-id="dba18-125">Element</span></span>|<span data-ttu-id="dba18-126">Description</span><span class="sxs-lookup"><span data-stu-id="dba18-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dba18-127">\<participants></span><span class="sxs-lookup"><span data-stu-id="dba18-127">\<participants></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md)|<span data-ttu-id="dba18-128">Liste de participants au suivi</span><span class="sxs-lookup"><span data-stu-id="dba18-128">A list of tracking participants</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dba18-129">Notes</span><span class="sxs-lookup"><span data-stu-id="dba18-129">Remarks</span></span>  
 <span data-ttu-id="dba18-130">Les participants au suivi permettent d'obtenir les données de suivi émises du flux de travail et de les stocker dans différents médias.</span><span class="sxs-lookup"><span data-stu-id="dba18-130">Tracking participants are used to get the tracking data emitted from the workflow and store it into different mediums.</span></span> <span data-ttu-id="dba18-131">De la même manière, tout post-traitement effectué sur les enregistrements de suivi peut également être réalisé dans le participant au suivi.</span><span class="sxs-lookup"><span data-stu-id="dba18-131">Likewise, any post processing on the tracking Records can also be done within the tracking participant.</span></span>  
  
 <span data-ttu-id="dba18-132">Plusieurs participants au suivi peuvent consommer les événements de suivi simultanément.</span><span class="sxs-lookup"><span data-stu-id="dba18-132">Multiple tracking participants can consume the tracking events simultaneously.</span></span> <span data-ttu-id="dba18-133">Chaque participant au suivi peut être associé à un modèle de suivi différent.</span><span class="sxs-lookup"><span data-stu-id="dba18-133">Each tracking participant can be associated with a different tracking profile.</span></span>  
  
 <span data-ttu-id="dba18-134">Un participant au suivi standard est fourni, il écrit les enregistrements de suivi dans une session ETW.</span><span class="sxs-lookup"><span data-stu-id="dba18-134">A standard tracking participant is provided which writes the tracking records to an ETW session.</span></span> <span data-ttu-id="dba18-135">Le participant est configuré sur un service de flux de travail en ajoutant un comportement spécifique au suivi dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="dba18-135">The participant is configured on a workflow service by adding a tracking-specific behavior in a configuration file.</span></span> <span data-ttu-id="dba18-136">L'activation d'un participant au suivi ETW permet d'afficher les enregistrements de suivi dans l'Observateur d'événements.</span><span class="sxs-lookup"><span data-stu-id="dba18-136">Enabling an ETW tracking participant allows tracking records to be viewed in the event viewer.</span></span> <span data-ttu-id="dba18-137">Si cela ne répond pas à vos besoins, vous pouvez également écrire un participant de suivi personnalisé.</span><span class="sxs-lookup"><span data-stu-id="dba18-137">If that does not meet your requirements, you can also write a custom tracking participant.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dba18-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="dba18-138">Example</span></span>  
 <span data-ttu-id="dba18-139">L'exemple suivant présente la configuration du participant au suivi ETW standard dans le fichier Web.config.</span><span class="sxs-lookup"><span data-stu-id="dba18-139">The following configuration example shows the standard ETW tracking participant being configured in the Web.config file.</span></span>  
  
 <span data-ttu-id="dba18-140">L'ID de fournisseur dont se sert le participant au suivi ETW pour écrire les enregistrements de suivi dans une session ETW est défini dans la section `<diagnostics>`.</span><span class="sxs-lookup"><span data-stu-id="dba18-140">The Provider Id that the ETW Tracking Participant uses for writing the Tracking Records to ETW is defined in the `<diagnostics>` section.</span></span> <span data-ttu-id="dba18-141">Un profil est associé au participant au suivi pour spécifier les enregistrements de suivi auxquels il est abonné.</span><span class="sxs-lookup"><span data-stu-id="dba18-141">The tracking participant has a profile associated with it to specify the tracking records it has subscribed to.</span></span> <span data-ttu-id="dba18-142">Ce profil est défini par l'attribut `profileName` de l'élément `<add>`.</span><span class="sxs-lookup"><span data-stu-id="dba18-142">This is defined by the `profileName` attribute of the `<add>` element.</span></span> <span data-ttu-id="dba18-143">Une fois ces paramètres définis, le participant au suivi est ajouté au comportement de service `<etwTracking>`.</span><span class="sxs-lookup"><span data-stu-id="dba18-143">Once these are defined, the Tracking Participant is added to the `<etwTracking>` service behavior.</span></span> <span data-ttu-id="dba18-144">Les participants au suivi sélectionnés sont ajoutés aux extensions de l’instance de flux de travail, afin qu’ils commencent à recevoir les enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="dba18-144">This will add the selected Tracking Participants to the Workflow instance’s extensions, so that they begin to receive the Tracking Records.</span></span>  
  
```xml  
<configuration>
  <system.web>
    <compilation targetFrameworkMoniker=".NETFramework,Version=v4.0" />
  </system.web>
  <system.serviceModel>
    <diagnostics etwProviderId="52A3165D-4AD9-405C-B1E8-7D9A257EAC9F" />
    <tracking>
      <participants>
        <add name="EtwTrackingParticipant"
             type="System.Activities.Tracking.EtwTrackingParticipant, System.Activities, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
             profileName="HealthMonitoring_Tracking_Profile" />
      </participants>
    </tracking>
    <behaviors>
      <serviceBehaviors>
        <behavior>
          <etwTracking profileName="Sample Tracking Profile" />
        </behavior>
      </serviceBehaviors>
    </behaviors>
  </system.serviceModel>
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="dba18-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dba18-145">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection>
- <xref:System.ServiceModel.Activities.Description.EtwTrackingBehavior>
- <xref:System.ServiceModel.Activities.Configuration.EtwTrackingBehaviorElement>
- [<span data-ttu-id="dba18-146">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="dba18-146">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="dba18-147">Participants de suivi</span><span class="sxs-lookup"><span data-stu-id="dba18-147">Tracking Participants</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md)
