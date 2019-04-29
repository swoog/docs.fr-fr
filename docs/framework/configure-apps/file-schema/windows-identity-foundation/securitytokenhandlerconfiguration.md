---
title: <securityTokenHandlerConfiguration>
ms.date: 03/30/2017
ms.assetid: 28724cc6-020c-4a06-9a1f-d7594f315019
author: BrucePerlerMS
ms.openlocfilehash: 29e18cdda9e18addef4f0f32fd30e9abf6af78fc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793846"
---
# <a name="securitytokenhandlerconfiguration"></a><span data-ttu-id="51c9e-101">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="51c9e-101">\<securityTokenHandlerConfiguration></span></span>
<span data-ttu-id="51c9e-102">Fournit la configuration de la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="51c9e-102">Provides configuration for the collection of token handlers.</span></span>  
  
 <span data-ttu-id="51c9e-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="51c9e-103">\<system.identityModel></span></span>  
<span data-ttu-id="51c9e-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="51c9e-104">\<identityConfiguration></span></span>  
<span data-ttu-id="51c9e-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="51c9e-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="51c9e-106">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="51c9e-106">\<securityTokenHandlerConfiguration></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51c9e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51c9e-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration saveBootstrapContext=xs:boolean  
          maximumClockSkew=TimeSpan>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="51c9e-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="51c9e-108">Attributes and Elements</span></span>  
 <span data-ttu-id="51c9e-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="51c9e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="51c9e-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="51c9e-110">Attributes</span></span>  
  
|<span data-ttu-id="51c9e-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="51c9e-111">Attribute</span></span>|<span data-ttu-id="51c9e-112">Description</span><span class="sxs-lookup"><span data-stu-id="51c9e-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="51c9e-113">saveBootstrapContext</span><span class="sxs-lookup"><span data-stu-id="51c9e-113">saveBootstrapContext</span></span>|<span data-ttu-id="51c9e-114">Spécifie si les jetons de démarrage doivent être inclus dans le jeton de session.</span><span class="sxs-lookup"><span data-stu-id="51c9e-114">Specifies whether bootstrap tokens should be included in the session token.</span></span> <span data-ttu-id="51c9e-115">La valeur peut également être définie sur une collection de gestionnaires de jetons en définissant le `saveBootstrapContext` d’attribut sur le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément.</span><span class="sxs-lookup"><span data-stu-id="51c9e-115">The value may also be set on a token handler collection by setting the `saveBootstrapContext` attribute on the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element.</span></span> <span data-ttu-id="51c9e-116">Une valeur définie sur la collection de gestionnaires de jetons substitue à la valeur définie sur le service.</span><span class="sxs-lookup"><span data-stu-id="51c9e-116">A value set on the token handler collection overrides the value set on the service.</span></span>|  
|<span data-ttu-id="51c9e-117">maximumClockSkew</span><span class="sxs-lookup"><span data-stu-id="51c9e-117">maximumClockSkew</span></span>|<span data-ttu-id="51c9e-118">Un <xref:System.TimeSpan> qui spécifie le décalage d’horloge maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="51c9e-118">A <xref:System.TimeSpan> that specifies the maximum allowed clock skew.</span></span> <span data-ttu-id="51c9e-119">Contrôle le décalage d’horloge maximale autorisée lorsque vous effectuez des opérations de contrainte de temps, telles que la validation de l’heure d’expiration d’une session de connexion.</span><span class="sxs-lookup"><span data-stu-id="51c9e-119">Controls the maximum allowed clock skew when performing time-sensitive operations, such as validating the expiration time of a sign-in session.</span></span> <span data-ttu-id="51c9e-120">La valeur par défaut est 5 minutes, « 00 : 05:00 ».</span><span class="sxs-lookup"><span data-stu-id="51c9e-120">The default is 5 minutes, "00:05:00".</span></span> <span data-ttu-id="51c9e-121">Pour plus d’informations sur la spécification <xref:System.TimeSpan> valeurs, consultez [valeurs Timespan](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="51c9e-121">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="51c9e-122">Le décalage d’horloge maximale peut également être défini au niveau du service en définissant le `maximumClockSkew` d’attribut sur le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément.</span><span class="sxs-lookup"><span data-stu-id="51c9e-122">The maximum clock skew may also be set at the service level by setting the `maximumClockSkew` attribute on the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element.</span></span> <span data-ttu-id="51c9e-123">Une valeur définie sur la collection de gestionnaires de jetons substitue à la valeur définie sur le service.</span><span class="sxs-lookup"><span data-stu-id="51c9e-123">A value set on the token handler collection overrides the value set on the service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="51c9e-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="51c9e-124">Child Elements</span></span>  
  
|<span data-ttu-id="51c9e-125">Élément</span><span class="sxs-lookup"><span data-stu-id="51c9e-125">Element</span></span>|<span data-ttu-id="51c9e-126">Description</span><span class="sxs-lookup"><span data-stu-id="51c9e-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51c9e-127">\<audienceUris></span><span class="sxs-lookup"><span data-stu-id="51c9e-127">\<audienceUris></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/audienceuris.md)|<span data-ttu-id="51c9e-128">Spécifie le jeu d’URI qui sont des identificateurs acceptables de cette partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="51c9e-128">Specifies the set of URIs that are acceptable identifiers of this relying party.</span></span> <span data-ttu-id="51c9e-129">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="51c9e-129">Optional.</span></span>|  
|[<span data-ttu-id="51c9e-130">\<caches></span><span class="sxs-lookup"><span data-stu-id="51c9e-130">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="51c9e-131">Inscrit les caches utilisés pour la détection de relecture de jetons et de jetons de session.</span><span class="sxs-lookup"><span data-stu-id="51c9e-131">Registers the caches used for session tokens and token replay detection.</span></span> <span data-ttu-id="51c9e-132">Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="51c9e-132">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="51c9e-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="51c9e-133">Optional.</span></span>|  
|[<span data-ttu-id="51c9e-134">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="51c9e-134">\<certificateValidation></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|<span data-ttu-id="51c9e-135">Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats.</span><span class="sxs-lookup"><span data-stu-id="51c9e-135">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="51c9e-136">Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="51c9e-136">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="51c9e-137">Ces paramètres sont remplacés si un gestionnaire spécifique est configuré avec son propre validateur.</span><span class="sxs-lookup"><span data-stu-id="51c9e-137">These settings are overridden if a specific handler is configured with its own validator.</span></span> <span data-ttu-id="51c9e-138">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="51c9e-138">Optional.</span></span>|  
|[<span data-ttu-id="51c9e-139">\<issuerNameRegistry></span><span class="sxs-lookup"><span data-stu-id="51c9e-139">\<issuerNameRegistry></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuernameregistry.md)|<span data-ttu-id="51c9e-140">Configure le Registre de nom de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="51c9e-140">Configures the issuer name registry that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="51c9e-141">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="51c9e-141">Optional.</span></span>|  
|[<span data-ttu-id="51c9e-142">\<issuerTokenResolver></span><span class="sxs-lookup"><span data-stu-id="51c9e-142">\<issuerTokenResolver></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuertokenresolver.md)|<span data-ttu-id="51c9e-143">Inscrit le résolveur de jeton de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="51c9e-143">Registers the issuer token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="51c9e-144">Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="51c9e-144">The issuer token resolver is used to resolve the signing token on incoming tokens and messages.</span></span> <span data-ttu-id="51c9e-145">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="51c9e-145">Optional.</span></span>|  
|[<span data-ttu-id="51c9e-146">\<serviceTokenResolver></span><span class="sxs-lookup"><span data-stu-id="51c9e-146">\<serviceTokenResolver></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/servicetokenresolver.md)|<span data-ttu-id="51c9e-147">Inscrit le résolveur de jeton de service qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="51c9e-147">Registers the service token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="51c9e-148">Le programme de résolution de jeton de service est utilisé pour résoudre le jeton de chiffrement sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="51c9e-148">The service token resolver is used to resolve the encryption token on incoming tokens and messages.</span></span> <span data-ttu-id="51c9e-149">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="51c9e-149">Optional.</span></span>|  
|[<span data-ttu-id="51c9e-150">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="51c9e-150">\<tokenReplayDetection></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)|<span data-ttu-id="51c9e-151">Active la détection de relecture de jetons et spécifie le délai d’expiration pour les jetons.</span><span class="sxs-lookup"><span data-stu-id="51c9e-151">Enables token replay detection and specifies the expiration time for tokens.</span></span> <span data-ttu-id="51c9e-152">Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="51c9e-152">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="51c9e-153">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="51c9e-153">Optional.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="51c9e-154">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="51c9e-154">Parent Elements</span></span>  
  
|<span data-ttu-id="51c9e-155">Élément</span><span class="sxs-lookup"><span data-stu-id="51c9e-155">Element</span></span>|<span data-ttu-id="51c9e-156">Description</span><span class="sxs-lookup"><span data-stu-id="51c9e-156">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51c9e-157">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="51c9e-157">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="51c9e-158">Spécifie une collection de gestionnaires de jetons de sécurité qui sont inscrits avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="51c9e-158">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="51c9e-159">Notes</span><span class="sxs-lookup"><span data-stu-id="51c9e-159">Remarks</span></span>  
 <span data-ttu-id="51c9e-160">Cette section fournit des valeurs de propriété pour un <xref:System.IdentityModel.Tokens.SecurityTokenHandlerConfiguration> objet.</span><span class="sxs-lookup"><span data-stu-id="51c9e-160">This section provides property values for a <xref:System.IdentityModel.Tokens.SecurityTokenHandlerConfiguration> object.</span></span> <span data-ttu-id="51c9e-161">Paramètres configurés dans cette section remplacent ceux configurés sur le service.</span><span class="sxs-lookup"><span data-stu-id="51c9e-161">Settings configured in this section override those configured on the service.</span></span> <span data-ttu-id="51c9e-162">Certains de ces paramètres peuvent, à son tour, être substituée par les paramètres qui sont spécifiés lors de l’ajout d’un gestionnaire à la collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="51c9e-162">Some of these settings can, in turn, be overridden by settings that are specified when a handler is added to the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="51c9e-163">Exemple</span><span class="sxs-lookup"><span data-stu-id="51c9e-163">Example</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>   
      <securityTokenHandlerConfiguration>  
  
        <audienceUris>  
          <clear/>  
          <add value="http://www.example.com/myapp/" />  
        </audienceUris>  
  
        <issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel">  
          <trustedIssuers>  
            <add thumbprint="97249e1a … 4c9158de" name="contoso.com" />  
          </trustedIssuers>  
        </issuerNameRegistry>  
  
        <issuerTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
  
        <serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```
