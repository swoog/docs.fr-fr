---
title: Protocoles de sécurité version 1.0
ms.date: 03/30/2017
ms.assetid: ee3402d2-1076-410b-a3cb-fae0372bd7af
ms.openlocfilehash: 8114183109befcb77c3bf2b35fe246118da5afde
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64586884"
---
# <a name="security-protocols-version-10"></a><span data-ttu-id="e167d-102">Protocoles de sécurité version 1.0</span><span class="sxs-lookup"><span data-stu-id="e167d-102">Security Protocols version 1.0</span></span>
<span data-ttu-id="e167d-103">Les protocoles Web Services Security fournissent des mécanismes de sécurité des services Web qui couvrent l’ensemble des exigences de sécurité de la messagerie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e167d-103">The Web Services Security Protocols provide Web services security mechanisms that cover all existing enterprise messaging security requirements.</span></span> <span data-ttu-id="e167d-104">Cette section décrit les détails de la version 1.0 de Windows Communication Foundation (WCF) (implémenté dans le <xref:System.ServiceModel.Channels.SecurityBindingElement>) pour les services Web suivants protocoles de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e167d-104">This section describes the Windows Communication Foundation (WCF) version 1.0 details (implemented in the <xref:System.ServiceModel.Channels.SecurityBindingElement>) for the following Web services security protocols.</span></span>  
  
|<span data-ttu-id="e167d-105">Spécification/Document</span><span class="sxs-lookup"><span data-stu-id="e167d-105">Specification/Document</span></span>|<span data-ttu-id="e167d-106">Lien</span><span class="sxs-lookup"><span data-stu-id="e167d-106">Link</span></span>|  
|-|-|  
|<span data-ttu-id="e167d-107">WSS : SOAP Message Security 1.0</span><span class="sxs-lookup"><span data-stu-id="e167d-107">WSS: SOAP Message Security 1.0</span></span>|<https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0.pdf>|
|<span data-ttu-id="e167d-108">WSS : UserName Token Profile 1.0</span><span class="sxs-lookup"><span data-stu-id="e167d-108">WSS: Username Token Profile 1.0</span></span>|<https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-token-profile-1.0.pdf>|
|<span data-ttu-id="e167d-109">WSS : X509 token Profile 1.0</span><span class="sxs-lookup"><span data-stu-id="e167d-109">WSS: X509 Token Profile 1.0</span></span>|<https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0.pdf>|
|<span data-ttu-id="e167d-110">WSS : SAML 1.1 Token Profile 1.0</span><span class="sxs-lookup"><span data-stu-id="e167d-110">WSS: SAML 1.1 Token Profile 1.0</span></span>|<https://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.0.pdf>|
|<span data-ttu-id="e167d-111">WSS : Sécurité des messages SOAP 1.1</span><span class="sxs-lookup"><span data-stu-id="e167d-111">WSS: SOAP Message Security 1.1</span></span>|<https://www.oasis-open.org/committees/download.php/16790/wss-v1.1-spec-os-SOAPMessageSecurity.pdf>|
|<span data-ttu-id="e167d-112">WSS Username Token Profile 1.1</span><span class="sxs-lookup"><span data-stu-id="e167d-112">WSS Username Token Profile 1.1</span></span>|<https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-token-profile-1.0.pdf>|
|<span data-ttu-id="e167d-113">WSS : X.509 Token Profile 1.1</span><span class="sxs-lookup"><span data-stu-id="e167d-113">WSS: X.509 Token Profile 1.1</span></span>|<https://www.oasis-open.org/committees/download.php/16785/wss-v1.1-spec-os-x509TokenProfile.pdf>|
|<span data-ttu-id="e167d-114">WSS : Kerberos Token Profile 1.1</span><span class="sxs-lookup"><span data-stu-id="e167d-114">WSS: Kerberos Token Profile 1.1</span></span>|<https://www.oasis-open.org/committees/download.php/16788/wss-v1.1-spec-os-KerberosTokenProfile.pdf>|
|<span data-ttu-id="e167d-115">WSS : SAML 1.1 Token Profile 1.1</span><span class="sxs-lookup"><span data-stu-id="e167d-115">WSS: SAML 1.1 Token Profile 1.1</span></span>|<https://www.oasis-open.org/committees/download.php/16768/wss-v1.1-spec-os-SAMLTokenProfile.pdf>|
|<span data-ttu-id="e167d-116">WS-Secure Conversation</span><span class="sxs-lookup"><span data-stu-id="e167d-116">WS-Secure Conversation</span></span>|<http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf>|
|<span data-ttu-id="e167d-117">WS-Trust</span><span class="sxs-lookup"><span data-stu-id="e167d-117">WS-Trust</span></span>|<http://specs.xmlsoap.org/ws/2005/02/trust/ws-trust.pdf>|
|<span data-ttu-id="e167d-118">Note d'application :</span><span class="sxs-lookup"><span data-stu-id="e167d-118">Application Note:</span></span><br /><br /> <span data-ttu-id="e167d-119">Utilisation de WS-Trust pour la négociation TLS</span><span class="sxs-lookup"><span data-stu-id="e167d-119">Using WS-Trust for TLS Handshake</span></span>|<span data-ttu-id="e167d-120">À publier</span><span class="sxs-lookup"><span data-stu-id="e167d-120">To be published</span></span>|  
|<span data-ttu-id="e167d-121">Note d'application :</span><span class="sxs-lookup"><span data-stu-id="e167d-121">Application Note:</span></span><br /><br /> <span data-ttu-id="e167d-122">Utilisation de WS-Trust pour SPNEGO</span><span class="sxs-lookup"><span data-stu-id="e167d-122">Using WS-Trust for SPNEGO</span></span>|<span data-ttu-id="e167d-123">À publier</span><span class="sxs-lookup"><span data-stu-id="e167d-123">To be published</span></span>|  
|<span data-ttu-id="e167d-124">Note d'application :</span><span class="sxs-lookup"><span data-stu-id="e167d-124">Application Note:</span></span><br /><br /> <span data-ttu-id="e167d-125">Identité et références de point de terminaison Web Services Addressing</span><span class="sxs-lookup"><span data-stu-id="e167d-125">Web Services Addressing Endpoint References And Identity</span></span>|<span data-ttu-id="e167d-126">À publier</span><span class="sxs-lookup"><span data-stu-id="e167d-126">To be published</span></span>|  
|<span data-ttu-id="e167d-127">WS-SecurityPolicy 1.1</span><span class="sxs-lookup"><span data-stu-id="e167d-127">WS-SecurityPolicy 1.1</span></span><br /><br /> <span data-ttu-id="e167d-128">(2005/07)</span><span class="sxs-lookup"><span data-stu-id="e167d-128">(2005/07)</span></span>|<http://specs.xmlsoap.org/ws/2005/07/securitypolicy/ws-securitypolicy.pdf><br /><br /> <span data-ttu-id="e167d-129">tel qu’amendé par [errata](https://lists.oasis-open.org/archives/ws-sx/200512/msg00017.html) soumis au comité technique OASIS WS-SX</span><span class="sxs-lookup"><span data-stu-id="e167d-129">as amended by [errata](https://lists.oasis-open.org/archives/ws-sx/200512/msg00017.html) submitted to OASIS WS-SX Technical Committee</span></span> |  
  
 <span data-ttu-id="e167d-130">WCF, version 1, fournit 17 modes d’authentification qui peuvent servir comme base pour la configuration de sécurité des services Web.</span><span class="sxs-lookup"><span data-stu-id="e167d-130">WCF, version 1, provides 17 authentication modes that can be used as the basis for Web services security configuration.</span></span> <span data-ttu-id="e167d-131">Chaque mode est optimisé pour un jeu commun d’exigences de déploiement, tel que :</span><span class="sxs-lookup"><span data-stu-id="e167d-131">Each mode is optimized for a common set of deployment requirements, such as:</span></span>  
  
- <span data-ttu-id="e167d-132">Informations d'identification utilisées pour authentifier le client et le service.</span><span class="sxs-lookup"><span data-stu-id="e167d-132">Credentials used to authenticate client and service.</span></span>  
  
- <span data-ttu-id="e167d-133">Mécanismes de protection de la sécurité des messages et du transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-133">Message or transport security protection mechanisms.</span></span>  
  
- <span data-ttu-id="e167d-134">Modèles d'échange de messages.</span><span class="sxs-lookup"><span data-stu-id="e167d-134">Message exchange patterns.</span></span>  
  
|<span data-ttu-id="e167d-135">Mode d'authentification</span><span class="sxs-lookup"><span data-stu-id="e167d-135">Authentication Mode</span></span>|<span data-ttu-id="e167d-136">Authentification de client</span><span class="sxs-lookup"><span data-stu-id="e167d-136">Client Authentication</span></span>|<span data-ttu-id="e167d-137">Authentification de serveur</span><span class="sxs-lookup"><span data-stu-id="e167d-137">Server Authentication</span></span>|<span data-ttu-id="e167d-138">Mode</span><span class="sxs-lookup"><span data-stu-id="e167d-138">Mode</span></span>|  
|-------------------------|---------------------------|---------------------------|----------|  
|<span data-ttu-id="e167d-139">UserNameOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-139">UserNameOverTransport</span></span>|<span data-ttu-id="e167d-140">Nom d'utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="e167d-140">User name/password</span></span>|<span data-ttu-id="e167d-141">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-141">X509</span></span>|<span data-ttu-id="e167d-142">Transport</span><span class="sxs-lookup"><span data-stu-id="e167d-142">Transport</span></span>|  
|<span data-ttu-id="e167d-143">CertificateOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-143">CertificateOverTransport</span></span>|<span data-ttu-id="e167d-144">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-144">X509</span></span>|<span data-ttu-id="e167d-145">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-145">X509</span></span>|<span data-ttu-id="e167d-146">Transport</span><span class="sxs-lookup"><span data-stu-id="e167d-146">Transport</span></span>|  
|<span data-ttu-id="e167d-147">KerberosOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-147">KerberosOverTransport</span></span>|<span data-ttu-id="e167d-148">Windows</span><span class="sxs-lookup"><span data-stu-id="e167d-148">Windows</span></span>|<span data-ttu-id="e167d-149">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-149">X509</span></span>|<span data-ttu-id="e167d-150">Transport</span><span class="sxs-lookup"><span data-stu-id="e167d-150">Transport</span></span>|  
|<span data-ttu-id="e167d-151">IssuedTokenOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-151">IssuedTokenOverTransport</span></span>|<span data-ttu-id="e167d-152">Fédérée</span><span class="sxs-lookup"><span data-stu-id="e167d-152">Federated</span></span>|<span data-ttu-id="e167d-153">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-153">X509</span></span>|<span data-ttu-id="e167d-154">Transport</span><span class="sxs-lookup"><span data-stu-id="e167d-154">Transport</span></span>|  
|<span data-ttu-id="e167d-155">SspiNegotiatedOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-155">SspiNegotiatedOverTransport</span></span>|<span data-ttu-id="e167d-156">Windows Sspi Negotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-156">Windows Sspi Negotiated</span></span>|<span data-ttu-id="e167d-157">Windows Sspi Negotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-157">Windows Sspi Negotiated</span></span>|<span data-ttu-id="e167d-158">Transport</span><span class="sxs-lookup"><span data-stu-id="e167d-158">Transport</span></span>|  
|<span data-ttu-id="e167d-159">AnonymousForCertificate</span><span class="sxs-lookup"><span data-stu-id="e167d-159">AnonymousForCertificate</span></span>|<span data-ttu-id="e167d-160">None</span><span class="sxs-lookup"><span data-stu-id="e167d-160">None</span></span>|<span data-ttu-id="e167d-161">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-161">X509</span></span>|<span data-ttu-id="e167d-162">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-162">Message</span></span>|  
|<span data-ttu-id="e167d-163">UserNameForCertificate</span><span class="sxs-lookup"><span data-stu-id="e167d-163">UserNameForCertificate</span></span>|<span data-ttu-id="e167d-164">Nom d'utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="e167d-164">User name/password</span></span>|<span data-ttu-id="e167d-165">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-165">X509</span></span>|<span data-ttu-id="e167d-166">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-166">Message</span></span>|  
|<span data-ttu-id="e167d-167">MutualCertificate</span><span class="sxs-lookup"><span data-stu-id="e167d-167">MutualCertificate</span></span>|<span data-ttu-id="e167d-168">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-168">X509</span></span>|<span data-ttu-id="e167d-169">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-169">X509</span></span>|<span data-ttu-id="e167d-170">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-170">Message</span></span>|  
|<span data-ttu-id="e167d-171">MutualCertificateDuplex</span><span class="sxs-lookup"><span data-stu-id="e167d-171">MutualCertificateDuplex</span></span>|<span data-ttu-id="e167d-172">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-172">X509</span></span>|<span data-ttu-id="e167d-173">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-173">X509</span></span>|<span data-ttu-id="e167d-174">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-174">Message</span></span>|  
|<span data-ttu-id="e167d-175">IssuedTokenForCertificate</span><span class="sxs-lookup"><span data-stu-id="e167d-175">IssuedTokenForCertificate</span></span>|<span data-ttu-id="e167d-176">Fédérée</span><span class="sxs-lookup"><span data-stu-id="e167d-176">Federated</span></span>|<span data-ttu-id="e167d-177">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-177">X509</span></span>|<span data-ttu-id="e167d-178">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-178">Message</span></span>|  
|<span data-ttu-id="e167d-179">Kerberos</span><span class="sxs-lookup"><span data-stu-id="e167d-179">Kerberos</span></span>|<span data-ttu-id="e167d-180">Windows</span><span class="sxs-lookup"><span data-stu-id="e167d-180">Windows</span></span>|<span data-ttu-id="e167d-181">Windows</span><span class="sxs-lookup"><span data-stu-id="e167d-181">Windows</span></span>|<span data-ttu-id="e167d-182">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-182">Message</span></span>|  
|<span data-ttu-id="e167d-183">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="e167d-183">IssuedToken</span></span>|<span data-ttu-id="e167d-184">Fédérée</span><span class="sxs-lookup"><span data-stu-id="e167d-184">Federated</span></span>|<span data-ttu-id="e167d-185">Fédérée</span><span class="sxs-lookup"><span data-stu-id="e167d-185">Federated</span></span>|<span data-ttu-id="e167d-186">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-186">Message</span></span>|  
|<span data-ttu-id="e167d-187">SspiNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-187">SspiNegotiated</span></span>|<span data-ttu-id="e167d-188">Windows Sspi Negotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-188">Windows Sspi Negotiated</span></span>|<span data-ttu-id="e167d-189">Windows Sspi Negotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-189">Windows Sspi Negotiated</span></span>|<span data-ttu-id="e167d-190">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-190">Message</span></span>|  
|<span data-ttu-id="e167d-191">AnonymousForSslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-191">AnonymousForSslNegotiated</span></span>|<span data-ttu-id="e167d-192">None</span><span class="sxs-lookup"><span data-stu-id="e167d-192">None</span></span>|<span data-ttu-id="e167d-193">X509, TLS-Nego</span><span class="sxs-lookup"><span data-stu-id="e167d-193">X509, TLS-Nego</span></span>|<span data-ttu-id="e167d-194">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-194">Message</span></span>|  
|<span data-ttu-id="e167d-195">UserNameForSslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-195">UserNameForSslNegotiated</span></span>|<span data-ttu-id="e167d-196">Nom d'utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="e167d-196">User name/password</span></span>|<span data-ttu-id="e167d-197">X509, TLS-Nego</span><span class="sxs-lookup"><span data-stu-id="e167d-197">X509, TLS-Nego</span></span>|<span data-ttu-id="e167d-198">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-198">Message</span></span>|  
|<span data-ttu-id="e167d-199">MutualSslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-199">MutualSslNegotiated</span></span>|<span data-ttu-id="e167d-200">X509</span><span class="sxs-lookup"><span data-stu-id="e167d-200">X509</span></span>|<span data-ttu-id="e167d-201">X509, TLS-Nego</span><span class="sxs-lookup"><span data-stu-id="e167d-201">X509, TLS-Nego</span></span>|<span data-ttu-id="e167d-202">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-202">Message</span></span>|  
|<span data-ttu-id="e167d-203">IssuedTokenForSslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-203">IssuedTokenForSslNegotiated</span></span>|<span data-ttu-id="e167d-204">Fédérée</span><span class="sxs-lookup"><span data-stu-id="e167d-204">Federated</span></span>|<span data-ttu-id="e167d-205">X509, TLS-Nego</span><span class="sxs-lookup"><span data-stu-id="e167d-205">X509, TLS-Nego</span></span>|<span data-ttu-id="e167d-206">Message</span><span class="sxs-lookup"><span data-stu-id="e167d-206">Message</span></span>|  
  
 <span data-ttu-id="e167d-207">Les points de terminaison qui utilisent des modes d’authentification de ce type peuvent exprimer leurs exigences de sécurité à l’aide de WS-SP (WS-SecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="e167d-207">Endpoints using such authentication modes can express their security requirements using WS-SecurityPolicy (WS-SP).</span></span> <span data-ttu-id="e167d-208">Ce document décrit la structure des messages d'infrastructure et d'en-tête de sécurité pour chaque mode d'authentification et fournit des exemples de stratégies et de messages.</span><span class="sxs-lookup"><span data-stu-id="e167d-208">This document describes the structure of security header and infrastructure messages for each authentication mode and provides examples of policies and messages.</span></span>  
  
 <span data-ttu-id="e167d-209">WCF s’appuie sur WS-SecureConversation pour assurer la prise en charge des sessions sécurisées pour protéger les échanges de messages multiples entre les applications.</span><span class="sxs-lookup"><span data-stu-id="e167d-209">WCF leverages WS-SecureConversation to provide secure sessions support to protect multi-message exchanges between applications.</span></span>  <span data-ttu-id="e167d-210">Consultez la section « Sessions sécurisées » ci-après pour plus d'informations sur l'implémentation.</span><span class="sxs-lookup"><span data-stu-id="e167d-210">See "Secure Sessions" below for implementation details.</span></span>  
  
 <span data-ttu-id="e167d-211">Outre les modes d’authentification, WCF fournit des paramètres pour contrôler les mécanismes de protection courants qui s’appliquent à la plupart des modes de l’authentification basée sur la sécurité de message, par exemple : ordre de signature et opérations de chiffrement, suites algorithmiques, dérivation de clé et la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="e167d-211">In addition to authentication modes, WCF provides settings to control common protection mechanisms that apply to most message security-based authentication modes, for example: order of signature versus encryption operations, algorithm suites, key derivation, and signature confirmation.</span></span>  
  
 <span data-ttu-id="e167d-212">Les préfixes et espaces de noms suivants sont utilisés dans ce document.</span><span class="sxs-lookup"><span data-stu-id="e167d-212">The following prefixes and namespaces are used in this document.</span></span>  
  
|<span data-ttu-id="e167d-213">Préfixe</span><span class="sxs-lookup"><span data-stu-id="e167d-213">Prefix</span></span>|<span data-ttu-id="e167d-214">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e167d-214">Namespace</span></span>|  
|------------|---------------|  
|<span data-ttu-id="e167d-215">s</span><span class="sxs-lookup"><span data-stu-id="e167d-215">s</span></span>|<https://www.w3.org/2003/05/soap-envelope/>|
|<span data-ttu-id="e167d-216">sp</span><span class="sxs-lookup"><span data-stu-id="e167d-216">sp</span></span>|<http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/>|
|<span data-ttu-id="e167d-217">a</span><span class="sxs-lookup"><span data-stu-id="e167d-217">a</span></span>|<https://www.w3.org/2005/08/addressing>|  
|<span data-ttu-id="e167d-218">wsse</span><span class="sxs-lookup"><span data-stu-id="e167d-218">wsse</span></span>|<span data-ttu-id="e167d-219">TBD - URI OASIS WSS 1,0</span><span class="sxs-lookup"><span data-stu-id="e167d-219">TBD – OASIS WSS 1.0 URI</span></span>|  
|<span data-ttu-id="e167d-220">wsse11</span><span class="sxs-lookup"><span data-stu-id="e167d-220">wsse11</span></span>|<span data-ttu-id="e167d-221">TBD - URI OASIS WSS 1.1</span><span class="sxs-lookup"><span data-stu-id="e167d-221">TBD – OASIS WSS 1.1 URI</span></span>|  
|<span data-ttu-id="e167d-222">wsu</span><span class="sxs-lookup"><span data-stu-id="e167d-222">wsu</span></span>|<span data-ttu-id="e167d-223">TBD - URI OASIS WSS 1.0 Utility</span><span class="sxs-lookup"><span data-stu-id="e167d-223">TBD – OASIS WSS 1.0 Utility URI</span></span>|  
|<span data-ttu-id="e167d-224">ds</span><span class="sxs-lookup"><span data-stu-id="e167d-224">ds</span></span>|<span data-ttu-id="e167d-225">TBD - URI W3C XMLDSig</span><span class="sxs-lookup"><span data-stu-id="e167d-225">TBD – W3C XMLDSig URI</span></span>|  
|<span data-ttu-id="e167d-226">wst</span><span class="sxs-lookup"><span data-stu-id="e167d-226">wst</span></span>|<span data-ttu-id="e167d-227">TBD - URI WS-Trust 2005/02</span><span class="sxs-lookup"><span data-stu-id="e167d-227">TBD – WS-Trust 2005/02 URI</span></span>|  
|<span data-ttu-id="e167d-228">wssc</span><span class="sxs-lookup"><span data-stu-id="e167d-228">wssc</span></span>|<span data-ttu-id="e167d-229">TBD - URI WS-SecureConversation 2005/02</span><span class="sxs-lookup"><span data-stu-id="e167d-229">TBD – WS-SecureConversation 2005/02 URI</span></span>|  
|<span data-ttu-id="e167d-230">wsaw</span><span class="sxs-lookup"><span data-stu-id="e167d-230">wsaw</span></span>|<span data-ttu-id="e167d-231">TBD - espace de noms de stratégie WS-Addressing</span><span class="sxs-lookup"><span data-stu-id="e167d-231">TBD - WS-Addressing policy namespace</span></span>|  
|<span data-ttu-id="e167d-232">wsp</span><span class="sxs-lookup"><span data-stu-id="e167d-232">wsp</span></span>|<http://schemas.xmlsoap.org/ws/2004/09/policy>|  
|<span data-ttu-id="e167d-233">mssp</span><span class="sxs-lookup"><span data-stu-id="e167d-233">mssp</span></span>|<http://schemas.xmlsoap.org/ws/2005/07/securitypolicy>|
  
## <a name="1-token-profiles"></a><span data-ttu-id="e167d-234">1. Profils de jeton</span><span class="sxs-lookup"><span data-stu-id="e167d-234">1. Token Profiles</span></span>  
 <span data-ttu-id="e167d-235">Les spécifications Web Services Security représentent les informations d'identification sous forme de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e167d-235">Web Services Security specifications represent credential as security tokens.</span></span> <span data-ttu-id="e167d-236">WCF prend en charge les types de jetons suivants :</span><span class="sxs-lookup"><span data-stu-id="e167d-236">WCF supports the following token types:</span></span>  
  
### <a name="11-usernametoken"></a><span data-ttu-id="e167d-237">1.1 UsernameToken</span><span class="sxs-lookup"><span data-stu-id="e167d-237">1.1 UsernameToken</span></span>  
 <span data-ttu-id="e167d-238">WCF suit les profils UsernameToken10 et UsernameToken11 avec les contraintes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-238">WCF follows UsernameToken10 and UsernameToken11 profiles with the following constraints:</span></span>  
  
 <span data-ttu-id="e167d-239">R1101 - L'attribut PasswordType sur l'élément UsernameToken\Password DOIT être omis ou avoir la valeur #PasswordText (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="e167d-239">R1101 PasswordType attribute on UsernameToken\Password element MUST be either omitted or have value #PasswordText (default).</span></span>  
  
 <span data-ttu-id="e167d-240">Il est possible d'implémenter #PasswordDigest à l'aide de l'extensibilité.</span><span class="sxs-lookup"><span data-stu-id="e167d-240">One can implement the #PasswordDigest using extensibility.</span></span> <span data-ttu-id="e167d-241">Il a été observé que #PasswordDigest était souvent considéré à tort comme un mécanisme de protection par mot de passe suffisamment sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e167d-241">It has been observed that #PasswordDigest was often mistaken to be a secure enough password protection mechanism.</span></span> <span data-ttu-id="e167d-242">Mais #PasswordDigest ne peut pas servir de substitut pour le chiffrement de UsernameToken.</span><span class="sxs-lookup"><span data-stu-id="e167d-242">But #PasswordDigest cannot serve as a substitute for encryption of the UsernameToken.</span></span> <span data-ttu-id="e167d-243">L'objectif principal de #PasswordDigest est la protection contre des attaques par relecture.</span><span class="sxs-lookup"><span data-stu-id="e167d-243">The primary goal of #PasswordDigest is protection against replay attacks.</span></span> <span data-ttu-id="e167d-244">Dans les modes d’authentification WCF, les menaces d’attaques de relecture sont atténuées en utilisant des signatures de message.</span><span class="sxs-lookup"><span data-stu-id="e167d-244">In WCF authentication modes, replay attack threats are mitigated by using message signatures.</span></span>  
  
 <span data-ttu-id="e167d-245">B1102 WCF émet jamais les sous-éléments Nonce et Created de UsernameToken.</span><span class="sxs-lookup"><span data-stu-id="e167d-245">B1102 WCF never emits Nonce and Created sub-elements of the UsernameToken.</span></span>  
  
 <span data-ttu-id="e167d-246">Ces sous-éléments ont pour but de permettre la détection de relecture.</span><span class="sxs-lookup"><span data-stu-id="e167d-246">These sub-elements are intended to help replay detection.</span></span> <span data-ttu-id="e167d-247">WCF utilise les signatures de message à la place.</span><span class="sxs-lookup"><span data-stu-id="e167d-247">WCF uses message signatures instead.</span></span>  
  
 <span data-ttu-id="e167d-248">OASIS WSS SOAP Message Security UsernameToken Profile 1.1 (UsernameToken11) a introduit la fonctionnalité de dérivation de clé à partir du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e167d-248">OASIS WSS SOAP Message Security UsernameToken Profile 1.1 (UsernameToken11) introduced key derivation from password feature.</span></span>  
  
 <span data-ttu-id="e167d-249">B1103 - Le mot de passe UsernameToken NE DOIT PAS être utilisé pour la dérivation de clé et, par conséquent, pour les opérations de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="e167d-249">B1103 UsernameToken password MUST not be used for key derivation and therefore for cryptographic operations.</span></span>  
  
 <span data-ttu-id="e167d-250">Raisonnement : les mots de passe sont généralement considérés comme trop faibles pour être utilisés dans les opérations de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="e167d-250">Rationale: passwords are generally considered too weak to be used for cryptographic operations.</span></span>  
  
### <a name="12-x509-token"></a><span data-ttu-id="e167d-251">1.2 Jeton X509</span><span class="sxs-lookup"><span data-stu-id="e167d-251">1.2 X509 Token</span></span>  
 <span data-ttu-id="e167d-252">WCF prend en charge les certificats X509v3 comme un type d’informations d’identification et suit X509TokenProfile1.0 et X509TokenProfile1.1 avec les contraintes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-252">WCF supports X509v3 certificates as a credential type and follows X509TokenProfile1.0 and X509TokenProfile1.1 with the following constraints:</span></span>  
  
 <span data-ttu-id="e167d-253">R1201 - L'attribut ValueType sur l'élément BinarySecurityToken doit avoir la valeur #X509v3 lorsqu'il contient un certificat X509v3.</span><span class="sxs-lookup"><span data-stu-id="e167d-253">R1201 The ValueType attribute on the BinarySecurityToken element must have value #X509v3 when it contains an X509v3 certificate.</span></span>  
  
 <span data-ttu-id="e167d-254">WSS X509 Token Profile 1.0 et 1.1 définissent également #X509PKIPathv1 et #PKCS7 comme types de valeur.</span><span class="sxs-lookup"><span data-stu-id="e167d-254">WSS X509 Token Profile 1.0 and 1.1 define also #X509PKIPathv1 and #PKCS7 as value types.</span></span> <span data-ttu-id="e167d-255">WCF ne prend pas en charge ces types.</span><span class="sxs-lookup"><span data-stu-id="e167d-255">WCF does not support these types.</span></span>  
  
 <span data-ttu-id="e167d-256">R1202 - Si une extension SubjectKeyIdentifier (SKI) est présente dans un certificat X509, wsse:KeyIdentifier doit être utilisé pour les références externes au jeton, avec l’attribut ValueType comme #X509SubjectKeyIdentifier et son contenu comme valeur encodée en base 64 de l’extension SKI du certificat.</span><span class="sxs-lookup"><span data-stu-id="e167d-256">R1202 If a SubjectKeyIdentifier (SKI) extension is present in an X509 certificate, wsse:KeyIdentifier should be used for external references to the token, with the ValueType attribute as #X509SubjectKeyIdentifier and its content the base64-encoded value of certificate's SKI extension.</span></span>  
  
 <span data-ttu-id="e167d-257">Les références SKI sont largement implémentées et s'avèrent être un type de référence externe hautement interopérable.</span><span class="sxs-lookup"><span data-stu-id="e167d-257">SKI references are widely implemented and proven to be a highly interoperable external reference type.</span></span>  
  
 <span data-ttu-id="e167d-258">R1203 - Une Référence externe au jeton de sécurité X509 NE DOIT PAS utiliser ds:X509IssuerSerial.</span><span class="sxs-lookup"><span data-stu-id="e167d-258">R1203 An external Reference to X509 Security Token SHOULD NOT use ds:X509IssuerSerial.</span></span>  
  
 <span data-ttu-id="e167d-259">R1204 - Si X509TokenProfile1.1 est utilisé, une référence externe au jeton de sécurité X509 DOIT utiliser l'empreinte numérique introduite par WS-Security 1.1.</span><span class="sxs-lookup"><span data-stu-id="e167d-259">R1204 If X509TokenProfile1.1 is in use, an external reference to X509 Security Token SHOULD use the thumbprint introduced by WS-Security 1.1.</span></span>  
  
 <span data-ttu-id="e167d-260">WCF prend en charge X509IssuerSerial.</span><span class="sxs-lookup"><span data-stu-id="e167d-260">WCF supports X509IssuerSerial.</span></span> <span data-ttu-id="e167d-261">Toutefois il existe des problèmes d’interopérabilité avec X509IssuerSerial : WCF utilise une chaîne pour comparer deux valeurs de X509IssuerSerial.</span><span class="sxs-lookup"><span data-stu-id="e167d-261">However There are interoperability issues with X509IssuerSerial: WCF uses a string to compare two values of X509IssuerSerial.</span></span> <span data-ttu-id="e167d-262">Par conséquent, si une réorganise des composants du nom du sujet et envoie à un service WCF, une référence à un certificat, il peut être introuvable.</span><span class="sxs-lookup"><span data-stu-id="e167d-262">Therefore if one reorders components of the Subject Name and sends to an WCF service a reference to a certificate, it may not be found.</span></span>  
  
### <a name="13-kerberos-token"></a><span data-ttu-id="e167d-263">1.3 Jeton Kerberos</span><span class="sxs-lookup"><span data-stu-id="e167d-263">1.3 Kerberos Token</span></span>  
 <span data-ttu-id="e167d-264">WCF prend en charge kerberostokenprofile1.1 à pour les besoins de l’authentification Windows avec les contraintes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-264">WCF supports KerberosTokenProfile1.1 for the purpose of Windows authentication with the following constraints:</span></span>  
  
 <span data-ttu-id="e167d-265">R1301 - Un jeton Kerberos doit contenir la valeur d'un AP_REQ Kerberos v4 encapsulé GSS tel que défini dans GSS_API et la spécification Kerberos, et l'attribut ValueType doit avoir la valeur #GSS_Kerberosv5_AP_REQ.</span><span class="sxs-lookup"><span data-stu-id="e167d-265">R1301 A Kerberos Token must carry the value of a GSS wrapped Kerberos v4 AP_REQ as defined in GSS_API and the Kerberos specification, and must have the ValueType attribute with the value #GSS_Kerberosv5_AP_REQ.</span></span>  
  
 <span data-ttu-id="e167d-266">WCF utilise GSS encapsulé AP-REQ Kerberos, pas un AP-REQ nu</span><span class="sxs-lookup"><span data-stu-id="e167d-266">WCF uses GSS wrapped Kerberos AP-REQ, not a bare AP-REQ.</span></span> <span data-ttu-id="e167d-267">Il s'agit d'une méthode conseillée en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e167d-267">This is a security best practice.</span></span>  
  
### <a name="14-saml-v11-token"></a><span data-ttu-id="e167d-268">1.4 Jeton SAML v1.1</span><span class="sxs-lookup"><span data-stu-id="e167d-268">1.4 SAML v1.1 Token</span></span>  
 <span data-ttu-id="e167d-269">WCF prend en charge les profils de jeton WSS SAML 1.0 et 1.1 des jetons SAML v1.1.</span><span class="sxs-lookup"><span data-stu-id="e167d-269">WCF supports WSS SAML Token profiles 1.0 and 1.1 for SAML v1.1 tokens.</span></span> <span data-ttu-id="e167d-270">Il est possible d'implémenter d'autres versions de formats de jeton SAML.</span><span class="sxs-lookup"><span data-stu-id="e167d-270">It is possible to implement other versions of SAML token formats.</span></span>  
  
### <a name="15-security-context-token"></a><span data-ttu-id="e167d-271">1.5 Jeton de contexte de sécurité</span><span class="sxs-lookup"><span data-stu-id="e167d-271">1.5 Security Context Token</span></span>  
 <span data-ttu-id="e167d-272">WCF prend en charge le jeton SCT (Security Context) introduit dans WS-SecureCoversation.</span><span class="sxs-lookup"><span data-stu-id="e167d-272">WCF supports the Security Context Token (SCT) introduced in WS-SecureCoversation.</span></span> <span data-ttu-id="e167d-273">Le SCT est utilisé pour représenter un contexte de sécurité établi dans SecureConversation ainsi que les protocoles de négociation binaire TLS et SSPI, tel que décrit ci-après.</span><span class="sxs-lookup"><span data-stu-id="e167d-273">SCT is used to represent a security context established in SecureConversation as well as the binary negotiation protocols TLS and SSPI, described below.</span></span>  
  
## <a name="2-common-message-security-parameters"></a><span data-ttu-id="e167d-274">2. Paramètres de sécurité de message courants</span><span class="sxs-lookup"><span data-stu-id="e167d-274">2. Common Message Security Parameters</span></span>  
  
### <a name="21-timestamp"></a><span data-ttu-id="e167d-275">2.1 TimeStamp</span><span class="sxs-lookup"><span data-stu-id="e167d-275">2.1 TimeStamp</span></span>  
 <span data-ttu-id="e167d-276">La présence de l'horodatage est contrôlée à l'aide de la propriété <xref:System.ServiceModel.Channels.SecurityBindingElement.IncludeTimestamp%2A> de la classe <xref:System.ServiceModel.Channels.SecurityBindingElement> .</span><span class="sxs-lookup"><span data-stu-id="e167d-276">Timestamp presence is controlled using the <xref:System.ServiceModel.Channels.SecurityBindingElement.IncludeTimestamp%2A> property of the <xref:System.ServiceModel.Channels.SecurityBindingElement> class.</span></span> <span data-ttu-id="e167d-277">WCF sérialise systématiquement wsse : timestamp avec wsse : créé et wsse : expiration de champs.</span><span class="sxs-lookup"><span data-stu-id="e167d-277">WCF always serializes wsse:TimeStamp with wsse:Created and wsse:Expires fields.</span></span> <span data-ttu-id="e167d-278">wsse:TimeStamp est systématiquement signé en cas de signature.</span><span class="sxs-lookup"><span data-stu-id="e167d-278">The wsse:TimeStamp is always signed when signing is used.</span></span>  
  
### <a name="22-protection-order"></a><span data-ttu-id="e167d-279">2.2 Ordre de protection</span><span class="sxs-lookup"><span data-stu-id="e167d-279">2.2 Protection Order</span></span>  
 <span data-ttu-id="e167d-280">WCF prend en charge l’ordre de protection des messages « Sign Before Encrypt » et « Chiffrer avant de se connecter » (Security Policy 1.1).</span><span class="sxs-lookup"><span data-stu-id="e167d-280">WCF supports the message protection order "Sign Before Encrypt" and "Encrypt Before Sign" (Security Policy 1.1).</span></span> <span data-ttu-id="e167d-281">« Sign Before Encrypt » est recommandé dans les cas suivants : les messages protégés à l'aide de Encrypt Before Sign sont ouverts aux attaques par substitution de signature, sauf si le mécanisme WS-Security 1.1 SignatureConfirmation est utilisé et qu'une signature sur contenu chiffré rend l'audit plus difficile.</span><span class="sxs-lookup"><span data-stu-id="e167d-281">"Sign Before Encrypt" is recommended for reasons including: messages protected with Encrypt Before Sign are open to signature substitution attacks unless the WS-Security 1.1 SignatureConfirmation mechanism is used, and a signature over encrypted content makes auditing harder.</span></span>  
  
### <a name="23-signature-protection"></a><span data-ttu-id="e167d-282">2.3 Protection de la signature</span><span class="sxs-lookup"><span data-stu-id="e167d-282">2.3 Signature Protection</span></span>  
 <span data-ttu-id="e167d-283">Lorsque Encrypt Before Sign est utilisé, il est recommandé de protéger la signature afin d'empêcher les attaques par force brute de découvrir le contenu chiffré ou la clé de signature (en particulier lorsqu'un jeton personnalisé est utilisé avec du matériel de clé faible).</span><span class="sxs-lookup"><span data-stu-id="e167d-283">When Encrypt Before Sign is used, it is recommended to protect the signature to prevent brute force attacks for guessing the encrypted content or the signing key (especially when a custom token is used with weak key material).</span></span>  
  
### <a name="24-algorithm-suite"></a><span data-ttu-id="e167d-284">2.4 Suite algorithmique</span><span class="sxs-lookup"><span data-stu-id="e167d-284">2.4 Algorithm Suite</span></span>  
 <span data-ttu-id="e167d-285">WCF prend en charge toutes les suites algorithmiques répertoriées dans Security Policy 1.1.</span><span class="sxs-lookup"><span data-stu-id="e167d-285">WCF supports all algorithm suites listed in Security Policy 1.1.</span></span>  
  
### <a name="25-key-derivation"></a><span data-ttu-id="e167d-286">2.5 Dérivation de clé</span><span class="sxs-lookup"><span data-stu-id="e167d-286">2.5 Key Derivation</span></span>  
 <span data-ttu-id="e167d-287">WCF utilise « Dérivation de clé pour les clés symétriques », comme décrit dans WS-SecureConversation.</span><span class="sxs-lookup"><span data-stu-id="e167d-287">WCF uses "Key Derivation for symmetric keys" as described in WS-SecureConversation.</span></span>  
  
### <a name="26-signature-confirmation"></a><span data-ttu-id="e167d-288">2.6 Confirmation de signature</span><span class="sxs-lookup"><span data-stu-id="e167d-288">2.6 Signature Confirmation</span></span>  
 <span data-ttu-id="e167d-289">La confirmation de signature peut se résumer à la protection contre les attaques de type « homme du milieu » afin de protéger le jeu de signatures.</span><span class="sxs-lookup"><span data-stu-id="e167d-289">Signature confirmation can be as protection from middle man attacks to protect the set of signatures.</span></span>  
  
### <a name="27-security-header-layout"></a><span data-ttu-id="e167d-290">2.7 Disposition de l'en-tête de sécurité</span><span class="sxs-lookup"><span data-stu-id="e167d-290">2.7 Security Header Layout</span></span>  
 <span data-ttu-id="e167d-291">Chaque mode d'authentification décrit une certaine disposition de l'en-tête de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e167d-291">Each authentication mode describes a certain layout for the security header.</span></span> <span data-ttu-id="e167d-292">Ses éléments sont semi-organisés.</span><span class="sxs-lookup"><span data-stu-id="e167d-292">Elements within the security header are semi-ordered.</span></span> <span data-ttu-id="e167d-293">Pour définir l'ordre des éléments enfants, WS-Security Policy définit les modes de disposition suivants :</span><span class="sxs-lookup"><span data-stu-id="e167d-293">To define the order of security header child elements, WS-Security Policy defines the following security header layout modes:</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e167d-294">Strict</span><span class="sxs-lookup"><span data-stu-id="e167d-294">Strict</span></span>|<span data-ttu-id="e167d-295">Les éléments sont ajoutés à l'en-tête de sécurité selon les règles de disposition numérotée décrites dans Stratégie de sécurité à la section 7.7.1 conformément à un principe général de « déclaration avant utilisation ».</span><span class="sxs-lookup"><span data-stu-id="e167d-295">Items are added to the security header following the numbered layout rules described in Security Policy section 7.7.1 according to a general principle of "declare before use".</span></span>|  
|<span data-ttu-id="e167d-296">Lax</span><span class="sxs-lookup"><span data-stu-id="e167d-296">Lax</span></span>|<span data-ttu-id="e167d-297">Les éléments sont ajoutés à l’en-tête de sécurité dans n’importe quel ordre conforme à WSS : Sécurité des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="e167d-297">Items are added to the security header in any order that conforms to WSS: SOAP Message Security.</span></span>|  
|<span data-ttu-id="e167d-298">LaxTimestampFirst</span><span class="sxs-lookup"><span data-stu-id="e167d-298">LaxTimestampFirst</span></span>|<span data-ttu-id="e167d-299">Identique à Lax, excepté que le premier élément dans l'en-tête de sécurité doit être un wsse:Timestamp</span><span class="sxs-lookup"><span data-stu-id="e167d-299">Same as Lax except that the first item in the security header must be a wsse:Timestamp</span></span>|  
|<span data-ttu-id="e167d-300">LaxTimestampLast</span><span class="sxs-lookup"><span data-stu-id="e167d-300">LaxTimestampLast</span></span>|<span data-ttu-id="e167d-301">Identique à Lax, excepté que le dernier élément dans l'en-tête de sécurité doit être un wsse:Timestamp</span><span class="sxs-lookup"><span data-stu-id="e167d-301">Same as lax except that the last item in the security header must be a wsse:Timestamp</span></span>|  
  
 <span data-ttu-id="e167d-302">WCF prend en charge toutes les quatre modes de disposition d’en-tête de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e167d-302">WCF supports all four modes for security header layout.</span></span> <span data-ttu-id="e167d-303">Les exemples de message et de structure d'en-tête de sécurité fournis pour les modes d'authentification ci-après suivent le mode « Strict ».</span><span class="sxs-lookup"><span data-stu-id="e167d-303">Security header structure and message examples for authentication modes below follow the "Strict" mode.</span></span>  
  
## <a name="2-common-message-security-parameters"></a><span data-ttu-id="e167d-304">2. Paramètres de sécurité de message courants</span><span class="sxs-lookup"><span data-stu-id="e167d-304">2. Common Message Security Parameters</span></span>  
 <span data-ttu-id="e167d-305">Cette section fournit des exemples de stratégie pour chaque mode d'authentification ainsi que des exemples qui présentent la structure d'entête de sécurité dans les messages échangés par le client et le service.</span><span class="sxs-lookup"><span data-stu-id="e167d-305">This section provides example policies for each authentication mode along with examples showing security header structure in messages exchanged by client and service.</span></span>  
  
### <a name="61-transport-protection"></a><span data-ttu-id="e167d-306">6.1 Protection du transport</span><span class="sxs-lookup"><span data-stu-id="e167d-306">6.1 Transport Protection</span></span>  
 <span data-ttu-id="e167d-307">WCF fournit cinq modes d’authentification qui utilisent le transport sécurisé pour protéger les messages ; UserNameOverTransport, CertificateOverTransport, KerberosOverTransport, IssuedTokenOverTransport et SspiNegotiatedOverTransport.</span><span class="sxs-lookup"><span data-stu-id="e167d-307">WCF provides five authentication modes that use secure transport to protect messages; UserNameOverTransport, CertificateOverTransport, KerberosOverTransport, IssuedTokenOverTransport and SspiNegotiatedOverTransport.</span></span>  
  
 <span data-ttu-id="e167d-308">Ces modes d’authentification sont construits à l’aide de la liaison de transport décrite dans SecurityPolicy.</span><span class="sxs-lookup"><span data-stu-id="e167d-308">These authentication modes are constructed using the transport binding described in SecurityPolicy.</span></span> <span data-ttu-id="e167d-309">Pour le mode d'authentification UserNameOverTransport, UsernameToken est un jeton de prise en charge signé.</span><span class="sxs-lookup"><span data-stu-id="e167d-309">For the UserNameOverTransport authentication mode the UsernameToken is a signed supporting token.</span></span> <span data-ttu-id="e167d-310">Pour les autres modes d'authentification, le jeton apparaît sous forme d'un jeton d'endossement signé.</span><span class="sxs-lookup"><span data-stu-id="e167d-310">For the other authentication modes the token appears as a signed endorsing token.</span></span> <span data-ttu-id="e167d-311">Les annexes C.1.2 et C.1.3 de SecurityPolicy décrivent en détail la disposition de l'en-tête de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e167d-311">Appendix C.1.2 and C.1.3 of SecurityPolicy describe the security header layout in detail.</span></span> <span data-ttu-id="e167d-312">Les exemples suivants affichent la disposition Strict pour un mode d'authentification donné.</span><span class="sxs-lookup"><span data-stu-id="e167d-312">The following example security headers show the Strict layout for a given authentication mode.</span></span>  
  
 <span data-ttu-id="e167d-313">La valeur de la propriété « Derived Keys » pour les jetons est dans tous les cas « false ».</span><span class="sxs-lookup"><span data-stu-id="e167d-313">The value of the "Derived Keys" property for the tokens in all cases is "false".</span></span>  
  
 <span data-ttu-id="e167d-314">Les valeurs des diverses propriétés de la liaison de transport sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-314">The values of the various properties of the transport binding are as follows:</span></span>  
  
 <span data-ttu-id="e167d-315">Horodateur : true</span><span class="sxs-lookup"><span data-stu-id="e167d-315">Timestamp: true</span></span>  
  
 <span data-ttu-id="e167d-316">Disposition d’en-tête de sécurité : Strict</span><span class="sxs-lookup"><span data-stu-id="e167d-316">Security Header Layout: Strict</span></span>  
  
 <span data-ttu-id="e167d-317">Suite d’algorithmes : Basic256</span><span class="sxs-lookup"><span data-stu-id="e167d-317">Algorithm Suite: Basic256</span></span>  
  
#### <a name="611-usernameovertransport"></a><span data-ttu-id="e167d-318">6.1.1 UsernameOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-318">6.1.1 UsernameOverTransport</span></span>  
 <span data-ttu-id="e167d-319">Avec ce mode d'authentification, le client s'authentifie à l'aide d'un jeton de nom d'utilisateur qui apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge signé qui est systématiquement envoyé de l'initiateur au destinataire.</span><span class="sxs-lookup"><span data-stu-id="e167d-319">With this authentication mode, the client authenticates with a Username Token which appears at the SOAP layer as a signed supporting token that is always sent from the initiator to the recipient.</span></span> <span data-ttu-id="e167d-320">Le service est authentifié à l'aide d'un certificat X.509 au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-320">The service is authenticated using an X.509 certificate at the transport layer.</span></span> <span data-ttu-id="e167d-321">La liaison utilisée est une liaison de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-321">The binding used is a transport binding.</span></span>  
  
 <span data-ttu-id="e167d-322">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-322">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='UsernameOverTransport_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:TransportBinding >  
        <wsp:Policy>  
          <sp:TransportToken>  
            <wsp:Policy>  
              <sp:HttpsToken RequireClientCertificate='false' />   
            </wsp:Policy>  
          </sp:TransportToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
        </wsp:Policy>  
      </sp:TransportBinding>  
      <sp:SignedSupportingTokens >  
        <wsp:Policy>  
          <sp:UsernameToken   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
            <wsp:Policy>  
              <sp:WssUsernameToken10 />   
            </wsp:Policy>  
          </sp:UsernameToken>  
        </wsp:Policy>  
      </sp:SignedSupportingTokens>  
      <sp:Wss11 >  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10 >  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
 <span data-ttu-id="e167d-323">Disposition de l'en-tête de sécurité</span><span class="sxs-lookup"><span data-stu-id="e167d-323">Security Header Layout</span></span>  
  
 <span data-ttu-id="e167d-324">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-324">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wsse:UsernameToken ... >  
  ...  
  </wsse:UsernameToken>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-325">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-325">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
</wsse:Security>  
```  
  
#### <a name="612-certificateovertransport"></a><span data-ttu-id="e167d-326">6.1.2 CertificateOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-326">6.1.2 CertificateOverTransport</span></span>  
 <span data-ttu-id="e167d-327">Avec ce mode d'authentification, le client s'authentifie à l'aide d'un certificat X.509 qui apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge d'endossement qui est systématiquement envoyé de l'initiateur au destinataire.</span><span class="sxs-lookup"><span data-stu-id="e167d-327">With this authentication mode the client authenticates using an X.509 certificate which appears at the SOAP layer as an endorsing supporting token that is always sent from the initiator to the recipient.</span></span> <span data-ttu-id="e167d-328">Le service est authentifié à l'aide d'un certificat X.509 au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-328">The service is authenticated using an X.509 certificate at the transport layer.</span></span> <span data-ttu-id="e167d-329">La liaison utilisée est une liaison de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-329">The binding used is a transport binding.</span></span>  
  
 <span data-ttu-id="e167d-330">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-330">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='CertificateOverTransport_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:TransportBinding xmlns:sp='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy' >  
        <wsp:Policy>  
          <sp:TransportToken>  
            <wsp:Policy>  
             <sp:HttpsToken RequireClientCertificate='false' />   
            </wsp:Policy>  
          </sp:TransportToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
        </wsp:Policy>  
      </sp:TransportBinding>  
      <sp:EndorsingSupportingTokens>  
        <wsp:Policy>  
          <sp:X509Token   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
            <wsp:Policy>  
              <sp:RequireThumbprintReference />   
              <sp:WssX509V3Token10 />   
            </wsp:Policy>  
          </sp:X509Token>  
          <sp:SignedParts>  
            <sp:Header Name='To'   
Namespace='http://www.w3.org/2005/08/addressing' />   
          </sp:SignedParts>  
        </wsp:Policy>  
      </sp:EndorsingSupportingTokens>  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
 <span data-ttu-id="e167d-331">Disposition de l'en-tête de sécurité</span><span class="sxs-lookup"><span data-stu-id="e167d-331">Security Header Layout</span></span>  
  
 <span data-ttu-id="e167d-332">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-332">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wse:Timestamp u:Id="_0">  
  ...  
  </wse:Timestamp>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-333">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-333">Response</span></span>  
  
```xml  
<o:Security>  
  <u:Timestamp u:Id="_0">  
  ...  
  </u:Timestamp>  
</o:Security>  
```  
  
#### <a name="613-issuedtokenovertransport"></a><span data-ttu-id="e167d-334">6.1.3 IssuedTokenOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-334">6.1.3 IssuedTokenOverTransport</span></span>  
 <span data-ttu-id="e167d-335">Avec ce mode d'authentification, le client ne s'authentifie pas auprès du service, en tant que tel, mais présente à la place un jeton émis par un service d'émission de jeton de sécurité (STS) et prouve qu'il connaît une clé partagée.</span><span class="sxs-lookup"><span data-stu-id="e167d-335">With this authentication mode the client does not authenticate to the service, as such, but rather presents a token issued by a Security Token Service (STS) and proves knowledge of a shared key.</span></span> <span data-ttu-id="e167d-336">Le jeton émis apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge d'endossement qui est systématiquement envoyé de l'initiateur au destinataire.</span><span class="sxs-lookup"><span data-stu-id="e167d-336">The issued token appears at the SOAP layer as an endorsing supporting token that is always sent from the initiator to the recipient.</span></span> <span data-ttu-id="e167d-337">Le service est authentifié à l'aide d'un certificat X.509 au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-337">The service is authenticated using an X.509 certificate at the transport layer.</span></span> <span data-ttu-id="e167d-338">La liaison utilisée est une liaison de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-338">The binding is a transport binding.</span></span>  
  
 <span data-ttu-id="e167d-339">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-339">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='IssuedTokenOverTransport_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:TransportBinding >  
        <wsp:Policy>  
          <sp:TransportToken>  
            <wsp:Policy>  
              <sp:HttpsToken RequireClientCertificate='false' />   
            </wsp:Policy>  
          </sp:TransportToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
        </wsp:Policy>  
      </sp:TransportBinding>  
      <sp:EndorsingSupportingTokens>  
        <wsp:Policy>  
          <sp:IssuedToken   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
            <sp:RequestSecurityTokenTemplate>  
              <wst:KeyType>  
              http://schemas.xmlsoap.org/ws/2005/02/trust/SymmetricKey  
              </wst:KeyType>   
            </sp:RequestSecurityTokenTemplate>  
            <wsp:Policy>  
              <sp:RequireInternalReference />   
            </wsp:Policy>  
          </sp:IssuedToken>  
          <sp:SignedParts>  
            <sp:Header Name='To'   
Namespace='http://www.w3.org/2005/08/addressing' />   
          </sp:SignedParts>  
        </wsp:Policy>  
      </sp:EndorsingSupportingTokens>  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
 <span data-ttu-id="e167d-340">Disposition de l'en-tête de sécurité</span><span class="sxs-lookup"><span data-stu-id="e167d-340">Security Header Layout</span></span>  
  
 <span data-ttu-id="e167d-341">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-341">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1" >  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <saml:Assertion ...>  
  ...  
  </saml:Assertion>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-342">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-342">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
</wsse:Security>  
```  
  
#### <a name="614-kerberosovertransport"></a><span data-ttu-id="e167d-343">6.1.4 KerberosOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-343">6.1.4 KerberosOverTransport</span></span>  
 <span data-ttu-id="e167d-344">Avec ce mode d'authentification, le client s'authentifie auprès du service à l'aide d'un ticket Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e167d-344">With this authentication mode the client authenticates to the service using a Kerberos ticket.</span></span> <span data-ttu-id="e167d-345">Le jeton Kerberos apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge d'endossement.</span><span class="sxs-lookup"><span data-stu-id="e167d-345">The Kerberos token appears at the SOAP layer as an endorsing supporting token.</span></span> <span data-ttu-id="e167d-346">Le service est authentifié à l'aide d'un certificat X.509 au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-346">The service is authenticated using an X.509 certificate at the transport layer.</span></span> <span data-ttu-id="e167d-347">La liaison utilisée est une liaison de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-347">The binding is a transport binding.</span></span>  
  
 <span data-ttu-id="e167d-348">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-348">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='KerberosOverTransport_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:TransportBinding>  
        <wsp:Policy>  
          <sp:TransportToken>  
            <wsp:Policy>  
              <sp:HttpsToken RequireClientCertificate='false' />   
            </wsp:Policy>  
          </sp:TransportToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic128 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
        </wsp:Policy>  
      </sp:TransportBinding>  
      <sp:EndorsingSupportingTokens>  
        <wsp:Policy>  
          <sp:KerberosToken  
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/Once' >  
            <wsp:Policy>  
              <sp:WssGssKerberosV5ApReqToken11 />   
            </wsp:Policy>  
          </sp:KerberosToken>  
          <sp:SignedParts>  
            <sp:Header Name='To'   
Namespace='http://www.w3.org/2005/08/addressing' />   
          </sp:SignedParts>  
        </wsp:Policy>  
      </sp:EndorsingSupportingTokens>  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
 <span data-ttu-id="e167d-349">Disposition de l'en-tête de sécurité</span><span class="sxs-lookup"><span data-stu-id="e167d-349">Security Header Layout</span></span>  
  
 <span data-ttu-id="e167d-350">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-350">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1" >  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wsse:BinarySecurityToken ValueType="...#GSS_Kerberosv5_AP_REQ">  
  ...  
  </wsse:BinarySecurityToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-351">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-351">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
</wsse:Security>  
```  
  
#### <a name="615-sspinegotiatedovertransport"></a><span data-ttu-id="e167d-352">6.1.5 SspiNegotiatedOverTransport</span><span class="sxs-lookup"><span data-stu-id="e167d-352">6.1.5 SspiNegotiatedOverTransport</span></span>  
 <span data-ttu-id="e167d-353">Avec ce mode, un protocole de négociation est utilisé pour effectuer l'authentification du client et du serveur.</span><span class="sxs-lookup"><span data-stu-id="e167d-353">With this mode a negotiation protocol is used to perform client and server authentication.</span></span> <span data-ttu-id="e167d-354">Le protocole Kerberos est dans la mesure du possible utilisé, sinon c'est NTLM.</span><span class="sxs-lookup"><span data-stu-id="e167d-354">Kerberos is used if possible, otherwise NTLM.</span></span> <span data-ttu-id="e167d-355">Le SCT résultant apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge d'endossement qui est systématiquement envoyé de l'initiateur au destinataire.</span><span class="sxs-lookup"><span data-stu-id="e167d-355">The resulting SCT appears at the SOAP layer as an endorsing supporting token that is always sent from initiator to recipient.</span></span> <span data-ttu-id="e167d-356">Le service est en outre authentifié au niveau de la couche de transport par un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-356">The service is additionally authenticated at the transport layer by an X.509 certificate.</span></span> <span data-ttu-id="e167d-357">La liaison utilisée est une liaison de transport.</span><span class="sxs-lookup"><span data-stu-id="e167d-357">The binding used is a transport binding.</span></span> <span data-ttu-id="e167d-358">« SPNEGO » (négociation) décrit la manière dont WCF utilise le protocole de négociation binaire SSPI avec WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="e167d-358">"SPNEGO" (negotiation) describes how WCF uses SSPI binary negotiation protocol with WS-Trust.</span></span> <span data-ttu-id="e167d-359">Les exemples d'en-tête de sécurité présentés dans cette section supposent que le SCT a déjà été établi via la négociation SPNEGO.</span><span class="sxs-lookup"><span data-stu-id="e167d-359">Security header examples in this section are after the SCT has been established through the SPNEGO handshake.</span></span>  
  
 <span data-ttu-id="e167d-360">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-360">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='SspiNegotiatedOverTransport_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:TransportBinding>  
        <wsp:Policy>  
          <sp:TransportToken>  
            <wsp:Policy>  
              <sp:HttpsToken RequireClientCertificate='false' />   
            </wsp:Policy>  
          </sp:TransportToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
        </wsp:Policy>  
      </sp:TransportBinding>  
      <sp:EndorsingSupportingTokens>  
        <wsp:Policy>  
          <sp:SpnegoContextToken   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
            <wsp:Policy />   
          </sp:SpnegoContextToken>  
          <sp:SignedParts>  
            <sp:Header Name='To'   
Namespace='http://www.w3.org/2005/08/addressing' />   
          </sp:SignedParts>  
        </wsp:Policy>  
      </sp:EndorsingSupportingTokens>  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
### <a name="security-header-examples"></a><span data-ttu-id="e167d-361">Exemples d'en-tête de sécurité</span><span class="sxs-lookup"><span data-stu-id="e167d-361">Security Header Examples</span></span>  
 <span data-ttu-id="e167d-362">Une fois que le jeton de contexte de sécurité est établi via la négociation SPNEGO à l'aide de WS-Trust Binary Negotiation, les messages d'application ont des en-têtes de sécurité présentant la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="e167d-362">Once the Security Context Token is established through SPNEGO handshake using WS-Trust Binary Negotiation, the application messages have security headers with the following structure.</span></span>  
  
 <span data-ttu-id="e167d-363">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-363">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wssc:SecurityContextToken u:Id="uuid-2202746a-7725-453d-8747-809cb718dab0-29" >  
  ...  
  </wssc:SecurityContextToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-364">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-364">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
</wsse:Security>  
```  
  
### <a name="62-using-x509-certificates-for-service-authentication"></a><span data-ttu-id="e167d-365">6.2 Utilisation des certificats X.509 pour l'authentification de service</span><span class="sxs-lookup"><span data-stu-id="e167d-365">6.2 Using X.509 Certificates for Service Authentication</span></span>  
 <span data-ttu-id="e167d-366">Cette section décrit les modes d’authentification suivants : MutualCertificate WSS1.0, Mutual CertificateDuplex, MutualCertificate WSS1.1, AnonymousForCertificate, UserNameForCertificate et IssuedTokenForCertificate.</span><span class="sxs-lookup"><span data-stu-id="e167d-366">This section describes the following authentication modes: MutualCertificate WSS1.0, Mutual CertificateDuplex, MutualCertificate WSS1.1, AnonymousForCertificate, UserNameForCertificate and IssuedTokenForCertificate.</span></span>  
  
#### <a name="621-mutualcertificate-wss10"></a><span data-ttu-id="e167d-367">6.2.1 MutualCertificate WSS1.0</span><span class="sxs-lookup"><span data-stu-id="e167d-367">6.2.1 MutualCertificate WSS1.0</span></span>  
 <span data-ttu-id="e167d-368">Avec ce mode d'authentification, le client s'authentifie à l'aide d'un certificat X.509 qui apparaît au niveau de la couche SOAP sous forme de jeton d'initiateur.</span><span class="sxs-lookup"><span data-stu-id="e167d-368">With this authentication mode the client authenticates using an X.509 certificate which appears at the SOAP layer as the initiator token.</span></span> <span data-ttu-id="e167d-369">Le service est également authentifié à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-369">The service is also authenticated using an X.509 certificate.</span></span>  
  
 <span data-ttu-id="e167d-370">La liaison utilisée est une liaison asymétrique avec les valeurs de propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-370">The binding used is an asymmetric binding with the following property values:</span></span>  
  
 <span data-ttu-id="e167d-371">Jeton d'initiateur : certificat X.509 du client, avec mode d'inclusion défini à …/IncludeToken/AlwaysToRecipient</span><span class="sxs-lookup"><span data-stu-id="e167d-371">Initiator Token: the client’s X.509 certificate, with inclusion mode set to …/IncludeToken/AlwaysToRecipient</span></span>  
  
 <span data-ttu-id="e167d-372">Jeton de destinataire : Certificat X.509 du serveur, avec mode d’inclusion a la valeur .../IncludeToken/Never</span><span class="sxs-lookup"><span data-stu-id="e167d-372">Recipient Token: Server’s X.509 Certificate, with inclusion mode is set …/IncludeToken/Never</span></span>  
  
 <span data-ttu-id="e167d-373">Protection de jeton : False</span><span class="sxs-lookup"><span data-stu-id="e167d-373">Token Protection: False</span></span>  
  
 <span data-ttu-id="e167d-374">Intégralité de l’en-tête et corps Signatures : True</span><span class="sxs-lookup"><span data-stu-id="e167d-374">Entire Header And Body Signatures: True</span></span>  
  
 <span data-ttu-id="e167d-375">Ordre de protection : SignBeforeEncrypt</span><span class="sxs-lookup"><span data-stu-id="e167d-375">Protection Order: SignBeforeEncrypt</span></span>  
  
 <span data-ttu-id="e167d-376">Chiffrement de la Signature : True</span><span class="sxs-lookup"><span data-stu-id="e167d-376">Encrypt Signature: True</span></span>  
  
 <span data-ttu-id="e167d-377">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-377">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='MutualCertificate_WSS10_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:AsymmetricBinding>  
        <wsp:Policy>  
          <sp:InitiatorToken>  
            <wsp:Policy>  
              <sp:X509Token   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
                <wsp:Policy>  
                  <sp:WssX509V3Token10 />   
                </wsp:Policy>  
              </sp:X509Token>  
            </wsp:Policy>  
          </sp:InitiatorToken>  
          <sp:RecipientToken>  
            <wsp:Policy>  
              <sp:X509Token   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/Never' >  
                <wsp:Policy>  
                  <sp:WssX509V3Token10 />   
                </wsp:Policy>  
              </sp:X509Token>  
            </wsp:Policy>  
          </sp:RecipientToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
          <sp:EncryptSignature />   
          <sp:OnlySignEntireHeadersAndBody />   
        </wsp:Policy>  
      </sp:AsymmetricBinding>  
      <sp:Wss10>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
        </wsp:Policy>  
      </sp:Wss10>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-378">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-378">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-379">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-379">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <xenc:EncryptedKey>  
  ...  
    <xenc:ReferenceList>  
    ...  
    </xenc:ReferenceList>  
  </xenc:EncryptedKey>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-380">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-380">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
    <xenc:ReferenceList>  
    ...  
    </xenc:ReferenceList>  
  </xenc:EncryptedKey>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-381">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-381">Security Header Examples: EncryptBeforeSign</span></span>  
  
 <span data-ttu-id="e167d-382">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-382">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-383">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-383">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
#### <a name="622-mutualcertificateduplex"></a><span data-ttu-id="e167d-384">6.2.2 MutualCertificateDuplex</span><span class="sxs-lookup"><span data-stu-id="e167d-384">6.2.2 MutualCertificateDuplex</span></span>  
 <span data-ttu-id="e167d-385">Avec ce mode d'authentification, le client s'authentifie à l'aide d'un certificat X.509 qui apparaît au niveau de la couche SOAP sous forme de jeton d'initiateur.</span><span class="sxs-lookup"><span data-stu-id="e167d-385">With this authentication mode the client authenticates using an X.509 certificate which appears at the SOAP layer as the initiator token.</span></span> <span data-ttu-id="e167d-386">Le service est également authentifié à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-386">The service is also authenticated using an X.509 certificate.</span></span>  
  
 <span data-ttu-id="e167d-387">La liaison utilisée est une liaison asymétrique avec les valeurs de propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-387">The binding used is an asymmetric binding with the following property values:</span></span>  
  
 <span data-ttu-id="e167d-388">Jeton d’initiateur : X509 du client certificat, mode d’inclusion défini à .../IncludeToken/AlwaysToRecipient</span><span class="sxs-lookup"><span data-stu-id="e167d-388">Initiator Token: Client’s X509 Certificate, inclusion mode is set to …/IncludeToken/AlwaysToRecipient</span></span>  
  
 <span data-ttu-id="e167d-389">Jeton de destinataire : X509 du serveur certificat, mode d’inclusion défini à .../IncludeToken/AlwaysToInitiator</span><span class="sxs-lookup"><span data-stu-id="e167d-389">Recipient Token: Server’s X509 Certificate, inclusion mode is set to …/IncludeToken/AlwaysToInitiator</span></span>  
  
 <span data-ttu-id="e167d-390">Protection de jeton : False</span><span class="sxs-lookup"><span data-stu-id="e167d-390">Token Protection: False</span></span>  
  
 <span data-ttu-id="e167d-391">Intégralité de l’en-tête et corps Signatures : True</span><span class="sxs-lookup"><span data-stu-id="e167d-391">Entire Header And Body Signatures: True</span></span>  
  
 <span data-ttu-id="e167d-392">Ordre de protection : SignBeforeEncrypt</span><span class="sxs-lookup"><span data-stu-id="e167d-392">Protection Order: SignBeforeEncrypt</span></span>  
  
 <span data-ttu-id="e167d-393">Chiffrement de la Signature : True</span><span class="sxs-lookup"><span data-stu-id="e167d-393">Encrypt Signature: True</span></span>  
  
 <span data-ttu-id="e167d-394">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-394">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='MutualCertificateDuplex_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:AsymmetricBinding>  
        <wsp:Policy>  
          <sp:InitiatorToken>  
            <wsp:Policy>  
              <sp:X509Token   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
                <wsp:Policy>  
                  <sp:WssX509V3Token10 />   
                </wsp:Policy>  
              </sp:X509Token>  
            </wsp:Policy>  
          </sp:InitiatorToken>  
          <sp:RecipientToken>  
            <wsp:Policy>  
              <sp:X509Token   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToInitiator' >  
                <wsp:Policy>  
                  <sp:WssX509V3Token10 />   
                </wsp:Policy>  
              </sp:X509Token>  
            </wsp:Policy>  
          </sp:RecipientToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
          <sp:EncryptSignature />   
          <sp:OnlySignEntireHeadersAndBody />   
        </wsp:Policy>  
      </sp:AsymmetricBinding>  
      <sp:Wss10>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
        </wsp:Policy>  
      </sp:Wss10>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-395">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-395">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-396">Demande et réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-396">Request and Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <xenc:EncryptedKey>  
  ...  
    <xenc:ReferenceList>  
    ...  
    </xenc:ReferenceList>  
  </xenc:EncryptedKey>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-397">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-397">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-398">Demande et réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-398">Request and Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
#### <a name="623-using-symmetricbinding-with-x509-service-authentication"></a><span data-ttu-id="e167d-399">6.2.3 Utilisation de SymmetricBinding avec l'authentification de service X.509</span><span class="sxs-lookup"><span data-stu-id="e167d-399">6.2.3 Using SymmetricBinding with X.509 Service Authentication</span></span>  
 <span data-ttu-id="e167d-400">« WSS10 » a fourni un support limité aux scénarios avec jetons X509.</span><span class="sxs-lookup"><span data-stu-id="e167d-400">"WSS10" provided limited support for scenarios with X509 tokens.</span></span> <span data-ttu-id="e167d-401">Par exemple, il n'était pas possible d'assurer la protection des signatures et du chiffrement des messages qui utilisent uniquement le jeton X509 du service.</span><span class="sxs-lookup"><span data-stu-id="e167d-401">For example, there was no way to provide signature and encryption protection for messages using only service X509 token.</span></span> <span data-ttu-id="e167d-402">« WSS11 » a introduit l'utilisation de EncryptedKey sous forme d'un jeton symétrique.</span><span class="sxs-lookup"><span data-stu-id="e167d-402">"WSS11" introduced the usage of EncryptedKey as a symmetric token.</span></span> <span data-ttu-id="e167d-403">Une clé temporaire chiffrée pour le certificat X.509 du service peut maintenant être utilisée à la fois pour la protection des messages de demande et de réponse.</span><span class="sxs-lookup"><span data-stu-id="e167d-403">Now a temporary key encrypted for the service's X.509 certificate could be used for both request and response messages protection.</span></span> <span data-ttu-id="e167d-404">Les modes d'authentification décrits dans la section 6.4 ci-après utilisent ce modèle.</span><span class="sxs-lookup"><span data-stu-id="e167d-404">The authentication modes described in the section 6.4 below use this pattern.</span></span>  
  
 <span data-ttu-id="e167d-405">WS-SecurityPolicy décrit ce modèle à l'aide de SymmetricBinding avec le jeton X509 du service sous forme de jeton de protection.</span><span class="sxs-lookup"><span data-stu-id="e167d-405">WS-SecurityPolicy describes this pattern using SymmetricBinding with Service X509 token as the protection token.</span></span>  
  
 <span data-ttu-id="e167d-406">Les modes d'authentification AnonymousForCertificate, UsernameForCertificate, MutualCertificate WSS11 et IssuedTokenForCertificate utilisent tous une instance similaire de sp:SymmetricBinding avec les valeurs de propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-406">Authentication modes AnonymousForCertificate, UsernameForCertificate, MutualCertificate WSS11 and IssuedTokenForCertificate all use a similar instance of sp:SymmetricBinding with the following property values:</span></span>  
  
 <span data-ttu-id="e167d-407">Jeton de protection : X509 du serveur certificat, mode d’inclusion défini à .../IncludeToken/Never</span><span class="sxs-lookup"><span data-stu-id="e167d-407">Protection Token: Server’s X509 Certificate, inclusion mode is set to .../IncludeToken/Never</span></span>  
<span data-ttu-id="e167d-408">Protection de jeton : False</span><span class="sxs-lookup"><span data-stu-id="e167d-408">Token Protection: False</span></span>  
  
 <span data-ttu-id="e167d-409">Intégralité de l’en-tête et corps Signatures : True</span><span class="sxs-lookup"><span data-stu-id="e167d-409">Entire Header And Body Signatures: True</span></span>  
  
 <span data-ttu-id="e167d-410">Ordre de protection : SignBeforeEncrypt</span><span class="sxs-lookup"><span data-stu-id="e167d-410">Protection Order: SignBeforeEncrypt</span></span>  
  
 <span data-ttu-id="e167d-411">Chiffrement de la Signature : True</span><span class="sxs-lookup"><span data-stu-id="e167d-411">Encrypt Signature: True</span></span>  
  
 <span data-ttu-id="e167d-412">Les modes d'authentification précédemment cités diffèrent uniquement par les jetons de prise en charge qu'ils utilisent.</span><span class="sxs-lookup"><span data-stu-id="e167d-412">The above authentication modes only differ by the supporting tokens they use.</span></span> <span data-ttu-id="e167d-413">AnonymousForCertificate n'a pas de jeton de prise en charge, MutualCertificate WSS 1.1 a le certificat X509 du client comme jeton de prise en charge d'endossement, UserNameForCertificate a un jeton de nom d'utilisateur comme jeton de prise en charge signé, et IssuedTokenForCertificate a le jeton émis sous forme d'un jeton de prise en charge d'endossement.</span><span class="sxs-lookup"><span data-stu-id="e167d-413">AnonymousForCertificate does not have any supporting tokens, MutualCertificate WSS 1.1 has the client’s X509 certificate as an endorsing supporting tokens, UserNameForCertificate has a UserName Token as a signed supporting token and IssuedTokenForCertificate has the issued token as an endorsing supporting token.</span></span>  
  
 <span data-ttu-id="e167d-414">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-414">Policy</span></span>  
  
 <span data-ttu-id="e167d-415">Liaison symétrique</span><span class="sxs-lookup"><span data-stu-id="e167d-415">Symmetric Binding</span></span>  
  
```xml  
<wsp:Policy wsu:Id='SymmetricCert_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:SymmetricBinding>  
        <wsp:Policy>  
          <sp:ProtectionToken>  
            <wsp:Policy>  
              <sp:X509Token   
sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/Never' >  
                <wsp:Policy>  
                  <sp:RequireDerivedKeys />   
                  <sp:RequireThumbprintReference />   
                  <sp:WssX509V3Token10 />   
                </wsp:Policy>  
              </sp:X509Token>  
            </wsp:Policy>  
          </sp:ProtectionToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
          <sp:EncryptSignature />   
          <sp:OnlySignEntireHeadersAndBody />  
        </wsp:Policy>  
      </sp:SymmetricBinding>  
      <!-- Supporting Token Assertions appear here -->  
      ...  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
          <sp:RequireSignatureConfirmation />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
#### <a name="624-anonymousforcertificate"></a><span data-ttu-id="e167d-416">6.2.4 AnonymousForCertificate</span><span class="sxs-lookup"><span data-stu-id="e167d-416">6.2.4 AnonymousForCertificate</span></span>  
 <span data-ttu-id="e167d-417">Avec ce mode d'authentification, le client est anonyme et le service est authentifié à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-417">With this authentication mode the client is anonymous and the service is authenticated using an X.509 certificate.</span></span> <span data-ttu-id="e167d-418">La liaison utilisée est une instance de liaison symétrique, tel que décrit à la section 6.4.2.</span><span class="sxs-lookup"><span data-stu-id="e167d-418">The binding used is an instance of symmetric binding as described in 6.4.2.</span></span>  
  
 <span data-ttu-id="e167d-419">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-419">Policy</span></span>  
  
 <span data-ttu-id="e167d-420">Consultez « Stratégie » à la section 6.2.3 ci-dessus pour plus d’informations sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e167d-420">See "Policy" in 6.2.3 above for binding details</span></span>  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-421">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-421">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-422">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-422">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-423">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-423">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-424">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-424">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-425">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-425">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-426">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-426">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wsse11:SignatureConfirmation />  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
#### <a name="625-usernameforcertificate"></a><span data-ttu-id="e167d-427">6.2.5 UserNameForCertificate</span><span class="sxs-lookup"><span data-stu-id="e167d-427">6.2.5 UserNameForCertificate</span></span>  
 <span data-ttu-id="e167d-428">Avec ce mode d'authentification, le client s'authentifie auprès du service à l'aide d'un jeton de nom d'utilisateur qui apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge signé.</span><span class="sxs-lookup"><span data-stu-id="e167d-428">With this authentication mode the client authenticates to the service using a Username Token which appears at the SOAP layer as a signed supporting token.</span></span> <span data-ttu-id="e167d-429">Le service s'authentifie auprès du client à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-429">The service authenticates to the client using an X.509 certificate.</span></span> <span data-ttu-id="e167d-430">La liaison utilisée est une liaison symétrique, le jeton de protection étant une clé générée par le client, chiffrée avec la clé publique du service.</span><span class="sxs-lookup"><span data-stu-id="e167d-430">The binding used is a symmetric binding with the protection token being a key generated by the client, encrypted with the public key of the service.</span></span>  
  
 <span data-ttu-id="e167d-431">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-431">Policy</span></span>  
  
 <span data-ttu-id="e167d-432">Consultez « Stratégie » à la section 6.2.3 ci-dessus pour plus d’informations sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e167d-432">See "Policy" in 6.2.3 above for binding details</span></span>  
  
 <span data-ttu-id="e167d-433">Jeton de prise en charge signé</span><span class="sxs-lookup"><span data-stu-id="e167d-433">Signed Supporting Token</span></span>  
  
```xml  
<sp:SignedSupportingTokens>  
  <wsp:Policy>  
    <sp:UsernameToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
      <wsp:Policy>  
        <sp:WssUsernameToken10 />   
      </wsp:Policy>  
    </sp:UsernameToken>  
  </wsp:Policy>  
</sp:SignedSupportingTokens>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-434">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-434">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-435">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-435">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-436">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-436">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-437">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-437">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-438">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-438">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-439">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-439">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
#### <a name="626-mutualcertificate-wss-11"></a><span data-ttu-id="e167d-440">6.2.6 MutualCertificate (WSS 1.1)</span><span class="sxs-lookup"><span data-stu-id="e167d-440">6.2.6 MutualCertificate (WSS 1.1)</span></span>  
 <span data-ttu-id="e167d-441">Avec ce mode d'authentification, le client s'authentifie à l'aide d'un certificat X.509 qui apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge d'endossement.</span><span class="sxs-lookup"><span data-stu-id="e167d-441">With this authentication mode the client authenticates using an X.509 certificate which appears at the SOAP layer as an endorsing supporting token.</span></span> <span data-ttu-id="e167d-442">Le service est également authentifié à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-442">The service is also authenticated using an X.509 certificate.</span></span> <span data-ttu-id="e167d-443">La liaison utilisée est une liaison symétrique, le jeton de protection étant une clé générée par le client, chiffrée avec la clé publique du service.</span><span class="sxs-lookup"><span data-stu-id="e167d-443">The binding used is a symmetric binding with the protection token being a key generated by the client, encrypted with the public key of the service.</span></span>  
  
 <span data-ttu-id="e167d-444">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-444">Policy</span></span>  
  
 <span data-ttu-id="e167d-445">Consultez « Stratégie » à la section 6.2.3 ci-dessus pour plus d'informations sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e167d-445">See Policy in 6.2.3 for binding details</span></span>  
  
 <span data-ttu-id="e167d-446">Jeton de prise en charge d'endossement</span><span class="sxs-lookup"><span data-stu-id="e167d-446">Endorsing Supporting Token</span></span>  
  
```xml  
<sp:EndorsingSupportingTokens>  
  <wsp:Policy>  
    <sp:X509Token sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
      <wsp:Policy>  
        <sp:RequireThumbprintReference />   
        <sp:WssX509V3Token10 />   
      </wsp:Policy>  
    </sp:X509Token>  
  </wsp:Policy>  
</sp:EndorsingSupportingTokens>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-447">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-447">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-448">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-448">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-449">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-449">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-450">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-450">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-451">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-451">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-452">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-452">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wsse11:SignatureConfirmation />  
  <wsse11:SignatureConfirmation />  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
#### <a name="627-issuedtokenforcertificate"></a><span data-ttu-id="e167d-453">6.2.7 IssuedTokenForCertificate</span><span class="sxs-lookup"><span data-stu-id="e167d-453">6.2.7 IssuedTokenForCertificate</span></span>  
 <span data-ttu-id="e167d-454">Avec ce mode d'authentification, le client ne s'authentifie pas auprès du service, en tant que tel, mais présente à la place un jeton émis par un STS et prouve qu'il connaît une clé partagée.</span><span class="sxs-lookup"><span data-stu-id="e167d-454">With this authentication mode the client does not authenticate to the service, as such, but instead presents a token issued by a STS and proves knowledge of a shared key.</span></span> <span data-ttu-id="e167d-455">Le jeton émis apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge d'endossement.</span><span class="sxs-lookup"><span data-stu-id="e167d-455">The issued token appears at the SOAP layer as an endorsing supporting token.</span></span> <span data-ttu-id="e167d-456">Le service s'authentifie auprès du client à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-456">The service authenticates to the client using an X.509 certificate.</span></span> <span data-ttu-id="e167d-457">La liaison utilisée est une liaison symétrique, le jeton de protection étant une clé générée par le client, chiffrée avec la clé publique du service.</span><span class="sxs-lookup"><span data-stu-id="e167d-457">The binding used is a symmetric binding with the protection token being a key generated by the client, encrypted with the public key of the service.</span></span>  
  
 <span data-ttu-id="e167d-458">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-458">Policy</span></span>  
  
 <span data-ttu-id="e167d-459">Consultez « Stratégie » à la section 6.2.3 ci-dessus pour plus d’informations sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e167d-459">See Policy in 6.2.3 above for binding details</span></span>  
  
 <span data-ttu-id="e167d-460">Jeton de prise en charge d'endossement</span><span class="sxs-lookup"><span data-stu-id="e167d-460">Endorsing Supporting Token</span></span>  
  
```xml  
<sp:EndorsingSupportingTokens>  
  <wsp:Policy>  
    <sp:IssuedToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
      <sp:RequestSecurityTokenTemplate>  
        <wst:KeyType>  
http://schemas.xmlsoap.org/ws/2005/02/trust/SymmetricKey  
       </wst:KeyType>  
     </sp:RequestSecurityTokenTemplate>  
     <wsp:Policy>  
       <sp:RequireDerivedKeys />   
       <sp:RequireInternalReference />   
     </wsp:Policy>  
   </sp:IssuedToken>  
  </wsp:Policy>  
</sp:EndorsingSupportingTokens>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-461">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-461">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-462">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-462">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <saml:Assertion>  
  ...  
  </saml:Assertion>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-463">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-463">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-464">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-464">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-465">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-465">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <xenc:EncryptedKey>  
  ...  
  </xenc:EncryptedKey>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <saml:Assertion>  
  ...  
  </saml:Assertion>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-466">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-466">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp u:Id="_0">  
  ...  
  </wsu:Timestamp>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wssc:DerivedKeyToken>  
  ...  
  </wssc:DerivedKeyToken>  
  <wsse11:SignatureConfirmation />  
  <wsse11:SignatureConfirmation />  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
## <a name="63-kerberos"></a><span data-ttu-id="e167d-467">6.3 Kerberos</span><span class="sxs-lookup"><span data-stu-id="e167d-467">6.3 Kerberos</span></span>  
 <span data-ttu-id="e167d-468">Avec ce mode d'authentification, le client s'authentifie auprès du service à l'aide d'un ticket Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e167d-468">With this authentication mode the client authenticates to the service using a Kerberos ticket.</span></span> <span data-ttu-id="e167d-469">Ce même ticket fournit également l'authentification de serveur.</span><span class="sxs-lookup"><span data-stu-id="e167d-469">That same ticket also provides server authentication.</span></span> <span data-ttu-id="e167d-470">La liaison utilisée est une liaison symétrique avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-470">The binding used is a symmetric binding with the following properties;</span></span>  
  
 <span data-ttu-id="e167d-471">Jeton de protection : Kerberos Ticket, avec mode d’inclusion a la valeur .../IncludeToken/Once</span><span class="sxs-lookup"><span data-stu-id="e167d-471">Protection Token: Kerberos Ticket, inclusion mode is set to .../IncludeToken/Once</span></span>  
<span data-ttu-id="e167d-472">Protection de jeton : False</span><span class="sxs-lookup"><span data-stu-id="e167d-472">Token Protection: False</span></span>  
  
 <span data-ttu-id="e167d-473">Intégralité de l’en-tête et corps Signatures : True</span><span class="sxs-lookup"><span data-stu-id="e167d-473">Entire Header And Body Signatures: True</span></span>  
  
 <span data-ttu-id="e167d-474">Ordre de protection : SignBeforeEncrypt</span><span class="sxs-lookup"><span data-stu-id="e167d-474">Protection Order: SignBeforeEncrypt</span></span>  
  
 <span data-ttu-id="e167d-475">Chiffrement de la Signature : True</span><span class="sxs-lookup"><span data-stu-id="e167d-475">Encrypt Signature: True</span></span>  
  
 <span data-ttu-id="e167d-476">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-476">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='Kerberos_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:SymmetricBinding>  
        <wsp:Policy>  
          <sp:ProtectionToken>  
            <wsp:Policy>  
              <sp:KerberosToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/Once' >  
                <wsp:Policy>  
                  <sp:RequireDerivedKeys />   
                  <sp:WssGssKerberosV5ApReqToken11 />   
                </wsp:Policy>  
              </sp:KerberosToken>  
            </wsp:Policy>  
          </sp:ProtectionToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic128 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
          <sp:EncryptSignature />   
          <sp:OnlySignEntireHeadersAndBody />   
        </wsp:Policy>  
      </sp:SymmetricBinding>  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-477">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-477">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-478">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-478">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsse:BinarySecurityToken>  
  ...  
  </wsse:BinarySecurityToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-479">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-479">Response</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>    
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-480">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-480">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-481">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-481">Request</span></span>  
  
```xml  
<wsse:Security>  
TBD  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-482">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-482">Response</span></span>  
  
```xml  
<wsse:Security>  
TBD  
</wsse:Security>  
```  
  
#### <a name="64-issuedtoken"></a><span data-ttu-id="e167d-483">6.4 IssuedToken</span><span class="sxs-lookup"><span data-stu-id="e167d-483">6.4 IssuedToken</span></span>  
 <span data-ttu-id="e167d-484">Avec ce mode d'authentification, le client ne s'authentifie pas auprès du service, en tant que tel, mais présente à la place un jeton émis par un STS et prouve qu'il connaît une clé partagée.</span><span class="sxs-lookup"><span data-stu-id="e167d-484">With this authentication mode the client does not authenticate to the service, as such, rather the client presents a token issued by an STS and proves knowledge of a shared key.</span></span> <span data-ttu-id="e167d-485">Le service n'est pas authentifié auprès du client, en tant que tel, mais le STS chiffre la clé partagée dans le cadre du jeton émis afin que seul le service puisse déchiffrer la clé.</span><span class="sxs-lookup"><span data-stu-id="e167d-485">The service is not authenticated to the client, as such, instead the STS encrypts the shared key as part of the issued token such that only the service can decrypt the key.</span></span> <span data-ttu-id="e167d-486">La liaison utilisée est une liaison symétrique avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-486">The binding used is as symmetric binding with the following properties;</span></span>  
  
 <span data-ttu-id="e167d-487">Jeton de protection : Jeton émis, mode d’inclusion défini à .../IncludeToken/AlwaysToRecipient</span><span class="sxs-lookup"><span data-stu-id="e167d-487">Protection Token: Issued Token, inclusion mode is set to .../IncludeToken/AlwaysToRecipient</span></span>  
<span data-ttu-id="e167d-488">Protection de jeton : False</span><span class="sxs-lookup"><span data-stu-id="e167d-488">Token Protection: False</span></span>  
  
 <span data-ttu-id="e167d-489">Intégralité de l’en-tête et corps Signatures : True</span><span class="sxs-lookup"><span data-stu-id="e167d-489">Entire Header And Body Signatures: True</span></span>  
  
 <span data-ttu-id="e167d-490">Ordre de protection : SignBeforeEncrypt</span><span class="sxs-lookup"><span data-stu-id="e167d-490">Protection Order: SignBeforeEncrypt</span></span>  
  
 <span data-ttu-id="e167d-491">Chiffrement de la Signature : True</span><span class="sxs-lookup"><span data-stu-id="e167d-491">Encrypt Signature: True</span></span>  
  
 <span data-ttu-id="e167d-492">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-492">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='CustomBinding_ISimple3_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:SymmetricBinding>  
        <wsp:Policy>  
          <sp:ProtectionToken>  
            <wsp:Policy>  
              <sp:IssuedToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
                <sp:RequestSecurityTokenTemplate>  
                  <wst:KeyType>  
http://schemas.xmlsoap.org/ws/2005/02/trust/SymmetricKey  
                  </wst:KeyType>   
                </sp:RequestSecurityTokenTemplate>  
                <wsp:Policy>  
                  <sp:RequireDerivedKeys />   
                  <sp:RequireInternalReference />   
                </wsp:Policy>  
              </sp:IssuedToken>  
            </wsp:Policy>  
          </sp:ProtectionToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
          <sp:EncryptSignature />   
          <sp:OnlySignEntireHeadersAndBody />   
        </wsp:Policy>  
      </sp:SymmetricBinding>  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-493">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-493">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-494">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-494">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <saml:Assertion>  
  ...  
  </saml:Assertion>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-495">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-495">Response</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>    
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-496">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-496">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-497">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-497">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <saml:Assertion>  
  ...  
  </saml:Assertion>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-498">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-498">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
### <a name="65-using-sslnegotiated-for-service-authentication"></a><span data-ttu-id="e167d-499">6.5 Utilisation de SslNegotiated pour l'authentification de service</span><span class="sxs-lookup"><span data-stu-id="e167d-499">6.5 Using SslNegotiated for Service Authentication</span></span>  
 <span data-ttu-id="e167d-500">Cette section décrit un groupe de modes d’authentification qui utilisent une liaison symétrique, le jeton de protection étant un jeton de contexte de sécurité tel que défini dans WS-SC (WS-SecureConversation) dont la valeur de clé est négociée en exécutant le protocole TLS sur les messages WS-T (WS-Trust) RST/RSTR.</span><span class="sxs-lookup"><span data-stu-id="e167d-500">This section describes a group of authentication modes that use a symmetric binding with the protection token being a Security Context Token per WS-SecureConversation (WS-SC) whose key value is negotiated by executing the TLS protocol over WS-Trust (WS-T) RST/RSTR messages.</span></span> <span data-ttu-id="e167d-501">Les détails de l'implémentation de la négociation TLS à l'aide de WS-Trust sont décrits dans TLSNEGO.</span><span class="sxs-lookup"><span data-stu-id="e167d-501">Details of the TLS handshake implementation using WS-Trust are described in TLSNEGO.</span></span> <span data-ttu-id="e167d-502">Dans les exemples de message présentés, nous supposerons que le SCT avec un contexte de sécurité associé est déjà établi via une négociation.</span><span class="sxs-lookup"><span data-stu-id="e167d-502">Here in the message examples we will assume that SCT with an associated security context is already established through a handshake.</span></span>  
  
 <span data-ttu-id="e167d-503">La liaison utilisée est une liaison symétrique avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-503">The binding used is a symmetric binding with the following properties;</span></span>  
  
 <span data-ttu-id="e167d-504">Jeton de protection : SslContextToken, avec mode d’inclusion défini à .../IncludeToken/Never</span><span class="sxs-lookup"><span data-stu-id="e167d-504">Protection Token: SslContextToken, inclusion mode is set to .../IncludeToken/Never</span></span>  
<span data-ttu-id="e167d-505">Protection de jeton : False</span><span class="sxs-lookup"><span data-stu-id="e167d-505">Token Protection: False</span></span>  
  
 <span data-ttu-id="e167d-506">Intégralité de l’en-tête et corps Signatures : True</span><span class="sxs-lookup"><span data-stu-id="e167d-506">Entire Header And Body Signatures: True</span></span>  
  
 <span data-ttu-id="e167d-507">Ordre de protection : SignBeforeEncrypt</span><span class="sxs-lookup"><span data-stu-id="e167d-507">Protection Order: SignBeforeEncrypt</span></span>  
  
 <span data-ttu-id="e167d-508">Chiffrement de la Signature : True</span><span class="sxs-lookup"><span data-stu-id="e167d-508">Encrypt Signature: True</span></span>  
  
#### <a name="651-policy-for-sslnegotiated-service-authentication"></a><span data-ttu-id="e167d-509">6.5.1 Stratégie d'authentification de service SslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-509">6.5.1 Policy for SslNegotiated service authentication</span></span>  
 <span data-ttu-id="e167d-510">La stratégie utilisée pour tous les modes d'authentification présentés dans cette section est similaire et diffère uniquement par les jetons d'endossement ou de prise en charge signés spécifiques utilisés.</span><span class="sxs-lookup"><span data-stu-id="e167d-510">Policy for all authentication modes in this section are similar and differ only by specific signed supporting or endorsing tokens used.</span></span>  
  
```xml  
<wsp:Policy wsu:Id='SslNegotiated_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:SymmetricBinding>  
        <wsp:Policy>  
          <sp:ProtectionToken>  
            <wsp:Policy>  
              <mssp:SslContextToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' />  
                <wsp:Policy>  
                  <sp:RequireDerivedKeys />   
                </wsp:Policy>  
              </mssp:SslContextToken>  
            </wsp:Policy>  
          </sp:ProtectionToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
          <sp:EncryptSignature />   
          <sp:OnlySignEntireHeadersAndBody />   
        </wsp:Policy>  
      </sp:SymmetricBinding>  
      <!-- Supporting token assertions go here -->  
      ..  
      <sp:Wss11>   
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
#### <a name="652-anonymousforsslnegotiated"></a><span data-ttu-id="e167d-511">6.5.2 AnonymousForSslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-511">6.5.2 AnonymousForSslNegotiated</span></span>  
 <span data-ttu-id="e167d-512">Avec ce mode d'authentification, le client est anonyme et le service est authentifié à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-512">With this authentication mode the client is anonymous and the service is authenticated using an X.509 certificate.</span></span> <span data-ttu-id="e167d-513">La liaison utilisée est une instance de liaison symétrique, tel que décrit à la section 6.5.1 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e167d-513">The binding used is an instance of symmetric binding as described in 6.5.1 above.</span></span>  
  
 <span data-ttu-id="e167d-514">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-514">Policy</span></span>  
  
 <span data-ttu-id="e167d-515">Consultez « Stratégie » à la section 6.5.1 ci-dessus pour plus d'informations sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e167d-515">See Policy in 6.5.1 above for binding details.</span></span>  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-516">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-516">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-517">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-517">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-518">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-518">Response</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>    
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-519">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-519">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-520">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-520">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-521">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-521">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
#### <a name="653-usernameforsslnegotiated"></a><span data-ttu-id="e167d-522">6.5.3 UserNameForSslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-522">6.5.3 UserNameForSslNegotiated</span></span>  
 <span data-ttu-id="e167d-523">Avec ce mode d'authentification, le client s'authentifie auprès du service à l'aide d'un jeton de nom d'utilisateur qui apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge signé.</span><span class="sxs-lookup"><span data-stu-id="e167d-523">With this authentication mode the client is authenticates using a Username Token which appears at the SOAP layer as a signed supporting token.</span></span> <span data-ttu-id="e167d-524">Le service est authentifié à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-524">The service is authenticated using an X.509 certificate.</span></span> <span data-ttu-id="e167d-525">La liaison utilisée est une instance de liaison symétrique, tel que décrit à la section 6.5.1.</span><span class="sxs-lookup"><span data-stu-id="e167d-525">The binding used is an instance of symmetric binding as described in 6.5.1.</span></span>  
  
 <span data-ttu-id="e167d-526">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-526">Policy</span></span>  
  
 <span data-ttu-id="e167d-527">Consultez la section 6.5.1 ci-dessus pour plus d'informations sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e167d-527">See section 6.5.1 above for binding details</span></span>  
  
 <span data-ttu-id="e167d-528">Jeton de prise en charge signé</span><span class="sxs-lookup"><span data-stu-id="e167d-528">Signed Supporting Token</span></span>  
  
```xml  
<sp:SignedSupportingTokens>  
  <wsp:Policy>  
    <sp:UsernameToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
      <wsp:Policy>  
        <sp:WssUsernameToken10 />   
      </wsp:Policy>  
    </sp:UsernameToken>  
  </wsp:Policy>  
</sp:SignedSupportingTokens>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-529">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-529">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-530">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-530">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-531">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-531">Response</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>    
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-532">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-532">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-533">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-533">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-534">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-534">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
#### <a name="654-issuedtokenforsslnegotiated"></a><span data-ttu-id="e167d-535">6.5.4 IssuedTokenForSslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-535">6.5.4 IssuedTokenForSslNegotiated</span></span>  
 <span data-ttu-id="e167d-536">Avec ce mode d'authentification, le client ne s'authentifie pas auprès du service, en tant que tel, mais présente à la place un jeton émis par un STS et prouve qu'il connaît une clé partagée.</span><span class="sxs-lookup"><span data-stu-id="e167d-536">With this authentication mode the client does not authenticate to the service, as such, but instead presents a token issued by an STS and proves knowledge of a shared key.</span></span> <span data-ttu-id="e167d-537">Le jeton émis apparaît au niveau de la couche SOAP sous forme d'un jeton de prise en charge d'endossement.</span><span class="sxs-lookup"><span data-stu-id="e167d-537">The issued token appears at the SOAP layer as an endorsing supporting token.</span></span> <span data-ttu-id="e167d-538">Le service est authentifié à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-538">The service is authenticated using an X.509 certificate.</span></span> <span data-ttu-id="e167d-539">La liaison utilisée est une instance de liaison symétrique, tel que décrit à la section 6.5.1 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e167d-539">The binding used is an instance of symmetric binding as described in 6.5.1 above.</span></span>  
  
 <span data-ttu-id="e167d-540">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-540">Policy</span></span>  
  
 <span data-ttu-id="e167d-541">Consultez la section 6.5.1 ci-dessus pour plus d'informations sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e167d-541">See section 6.5.1 above for binding details</span></span>  
  
 <span data-ttu-id="e167d-542">Jeton de prise en charge d'endossement</span><span class="sxs-lookup"><span data-stu-id="e167d-542">Endorsing Supporting Token</span></span>  
  
```xml  
<sp:EndorsingSupportingTokens>  
  <wsp:Policy>  
    <sp:IssuedToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
      <sp:RequestSecurityTokenTemplate>  
        <wst:KeyType>  
http://schemas.xmlsoap.org/ws/2005/02/trust/SymmetricKey  
        </wst:KeyType>   
      </sp:RequestSecurityTokenTemplate>  
      <wsp:Policy>  
        <sp:RequireDerivedKeys />   
        <sp:RequireInternalReference />   
      </wsp:Policy>  
    </sp:IssuedToken>  
  </wsp:Policy>  
</sp:EndorsingSupportingTokens>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-543">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-543">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-544">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-544">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <saml:Assertion>  
  ...  
  </saml:Assertion>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-545">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-545">Response</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>    
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-546">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-546">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-547">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-547">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <saml:Assertion>  
  ...  
  </saml:Assertion>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-548">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-548">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsse11:SignatureConfirmation />  
  <wsse11:SignatureConfirmation />  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
#### <a name="655-mutualsslnegotiated"></a><span data-ttu-id="e167d-549">6.5.5 MutualSslNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-549">6.5.5 MutualSslNegotiated</span></span>  
 <span data-ttu-id="e167d-550">Avec ce mode d'authentification, le client et le service s'authentifient à l'aide de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="e167d-550">With this authentication mode the client and the service authenticate using X.509 certificates.</span></span> <span data-ttu-id="e167d-551">La liaison utilisée est une instance de liaison symétrique, tel que décrit à la section 6.5.1 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e167d-551">The binding used is an instance of symmetric binding as described in 6.5.1 above.</span></span>  
  
 <span data-ttu-id="e167d-552">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-552">Policy</span></span>  
  
 <span data-ttu-id="e167d-553">Consultez la section 6.5.1 ci-dessus pour plus d'informations sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e167d-553">See section 6.5.1 above for binding details</span></span>  
  
 <span data-ttu-id="e167d-554">Jeton de prise en charge d'endossement</span><span class="sxs-lookup"><span data-stu-id="e167d-554">Endorsing Supporting Token</span></span>  
  
```xml  
<sp:EndorsingSupportingTokens>  
  <wsp:Policy>  
    <sp:X509Token sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
      <wsp:Policy>  
        <sp:RequireThumbprintReference />   
        <sp:WssX509V3Token10 />   
      </wsp:Policy>  
    </sp:X509Token>  
  </wsp:Policy>  
</sp:EndorsingSupportingTokens>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-555">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-555">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-556">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-556">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-557">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-557">Response</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>    
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-558">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-558">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-559">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-559">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-560">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-560">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
### <a name="66-sspinegotiated"></a><span data-ttu-id="e167d-561">6.6 SspiNegotiated</span><span class="sxs-lookup"><span data-stu-id="e167d-561">6.6 SspiNegotiated</span></span>  
 <span data-ttu-id="e167d-562">Avec ce mode d'authentification, un protocole de négociation est utilisé pour effectuer l'authentification du client et du serveur.</span><span class="sxs-lookup"><span data-stu-id="e167d-562">With this authentication mode a negotiation protocol is used to perform client and server authentication.</span></span> <span data-ttu-id="e167d-563">Le protocole Kerberos est dans la mesure du possible utilisé, sinon c'est NTLM.</span><span class="sxs-lookup"><span data-stu-id="e167d-563">Kerberos is used if possible, otherwise NTLM.</span></span> <span data-ttu-id="e167d-564">La liaison utilisée est une liaison symétrique avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e167d-564">The binding used is a symmetric binding with the following properties;</span></span>  
  
 <span data-ttu-id="e167d-565">Jeton de protection : SpnegoContextToken, avec mode d’inclusion défini à .../IncludeToken/AlwaysToRecipient</span><span class="sxs-lookup"><span data-stu-id="e167d-565">Protection Token: SpnegoContextToken, inclusion mode is set to .../IncludeToken/AlwaysToRecipient</span></span>  
<span data-ttu-id="e167d-566">Protection de jeton : False</span><span class="sxs-lookup"><span data-stu-id="e167d-566">Token Protection: False</span></span>  
  
 <span data-ttu-id="e167d-567">Intégralité de l’en-tête et corps Signatures : True</span><span class="sxs-lookup"><span data-stu-id="e167d-567">Entire Header And Body Signatures: True</span></span>  
  
 <span data-ttu-id="e167d-568">Ordre de protection : SignBeforeEncrypt</span><span class="sxs-lookup"><span data-stu-id="e167d-568">Protection Order: SignBeforeEncrypt</span></span>  
  
 <span data-ttu-id="e167d-569">Chiffrement de la Signature : True</span><span class="sxs-lookup"><span data-stu-id="e167d-569">Encrypt Signature: True</span></span>  
  
 <span data-ttu-id="e167d-570">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-570">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='CustomBinding_ISimple13_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:SymmetricBinding>  
        <wsp:Policy>  
          <sp:ProtectionToken>  
            <wsp:Policy>  
              <sp:SpnegoContextToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
                <wsp:Policy>  
                  <sp:RequireDerivedKeys />   
                </wsp:Policy>  
              </sp:SpnegoContextToken>  
            </wsp:Policy>  
          </sp:ProtectionToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
          <sp:EncryptSignature />   
          <sp:OnlySignEntireHeadersAndBody />   
        </wsp:Policy>  
      </sp:SymmetricBinding>  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-571">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-571">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-572">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-572">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-573">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-573">Response</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>    
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-574">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-574">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-575">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-575">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-576">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-576">Response</span></span>  
  
```xml  
<wsse:Security>  
<wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
### <a name="67-secureconversation"></a><span data-ttu-id="e167d-577">6.7 SecureConversation</span><span class="sxs-lookup"><span data-stu-id="e167d-577">6.7 SecureConversation</span></span>  
 <span data-ttu-id="e167d-578">La liaison utilisée est une liaison symétrique, le jeton de protection étant un SCT tel que défini dans WS-SC (WS-SecureConversation).</span><span class="sxs-lookup"><span data-stu-id="e167d-578">The binding used is a symmetric binding with the protection token being a SCT per WS-SecureConversation (WS-SC).</span></span> <span data-ttu-id="e167d-579">Le SCT est négocié à l’aide de WS-T (WS-Trust) ou WS-SC (WS-SecureConversation) d’après une liaison imbriquée, qui est elle-même une liaison symétrique utilisant un protocole de négociation.</span><span class="sxs-lookup"><span data-stu-id="e167d-579">The SCT is negotiated using WS-Trust (WS-Trust) or WS-SecureConversation (WS-SC) according to a nested binding, which is itself a symmetric binding that uses a negotiation protocol.</span></span> <span data-ttu-id="e167d-580">Le protocole de négociation utilisera Kerberos pour effectuer l'authentification du client et du serveur, si possible.</span><span class="sxs-lookup"><span data-stu-id="e167d-580">The negotiation protocol will use Kerberos to perform client and server authentication if possible.</span></span> <span data-ttu-id="e167d-581">Si Kerberos ne peut pas être utilisé, ce sera NTLM.</span><span class="sxs-lookup"><span data-stu-id="e167d-581">If Kerberos cannot be used, it will fall back to NTLM.</span></span>  
  
 <span data-ttu-id="e167d-582">Stratégie</span><span class="sxs-lookup"><span data-stu-id="e167d-582">Policy</span></span>  
  
```xml  
<wsp:Policy wsu:Id='SecureConversation_policy' >  
  <wsp:ExactlyOne>  
    <wsp:All>  
      <sp:SymmetricBinding>  
        <wsp:Policy>  
          <sp:ProtectionToken>  
            <wsp:Policy>  
              <sp:SecureConversationToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
                <wsp:Policy>  
                  <sp:RequireDerivedKeys />   
                  <sp:BootstrapPolicy>  
                    <wsp:Policy>  
                      <sp:SignedParts>  
                        <sp:Body />   
                        <sp:Header Name='To' Namespace='http://www.w3.org/2005/08/addressing' />   
                        <sp:Header Name='From' Namespace='http://www.w3.org/2005/08/addressing' />   
                        <sp:Header Name='FaultTo' Namespace='http://www.w3.org/2005/08/addressing' />   
                        <sp:Header Name='ReplyTo' Namespace='http://www.w3.org/2005/08/addressing' />   
                        <sp:Header Name='MessageID' Namespace='http://www.w3.org/2005/08/addressing' />   
                        <sp:Header Name='RelatesTo' Namespace='http://www.w3.org/2005/08/addressing' />   
                        <sp:Header Name='Action' Namespace='http://www.w3.org/2005/08/addressing' />   
                      </sp:SignedParts>  
                      <sp:EncryptedParts>  
                        <sp:Body />   
                      </sp:EncryptedParts>  
                      <sp:SymmetricBinding>  
                        <wsp:Policy>  
                          <sp:ProtectionToken>  
                            <wsp:Policy>  
                              <sp:SpnegoContextToken sp:IncludeToken='http://schemas.xmlsoap.org/ws/2005/07/securitypolicy/IncludeToken/AlwaysToRecipient' >  
                                <wsp:Policy>  
                                  <sp:RequireDerivedKeys />   
                                </wsp:Policy>  
                              </sp:SpnegoContextToken>  
                            </wsp:Policy>  
                          </sp:ProtectionToken>  
                          <sp:AlgorithmSuite>  
                            <wsp:Policy>  
                              <sp:Basic256 />   
                            </wsp:Policy>  
                          </sp:AlgorithmSuite>  
                          <sp:Layout>  
                            <wsp:Policy>  
                              <sp:Strict />   
                            </wsp:Policy>  
                          </sp:Layout>  
                          <sp:IncludeTimestamp />   
                          <sp:EncryptSignature />   
                          <sp:OnlySignEntireHeadersAndBody />   
                        </wsp:Policy>  
                      </sp:SymmetricBinding>  
                      <sp:Wss11>  
                        <wsp:Policy>  
                          <sp:MustSupportRefKeyIdentifier />   
                          <sp:MustSupportRefIssuerSerial />   
                          <sp:MustSupportRefThumbprint />   
                          <sp:MustSupportRefEncryptedKey />   
                        </wsp:Policy>  
                      </sp:Wss11>  
                      <sp:Trust10>  
                        <wsp:Policy>  
                          <sp:MustSupportIssuedTokens />   
                          <sp:RequireClientEntropy />   
                          <sp:RequireServerEntropy />   
                        </wsp:Policy>  
                      </sp:Trust10>  
                    </wsp:Policy>  
                  </sp:BootstrapPolicy>  
                </wsp:Policy>  
              </sp:SecureConversationToken>  
            </wsp:Policy>  
          </sp:ProtectionToken>  
          <sp:AlgorithmSuite>  
            <wsp:Policy>  
              <sp:Basic256 />   
            </wsp:Policy>  
          </sp:AlgorithmSuite>  
          <sp:Layout>  
            <wsp:Policy>  
              <sp:Strict />   
            </wsp:Policy>  
          </sp:Layout>  
          <sp:IncludeTimestamp />   
          <sp:EncryptSignature />   
          <sp:OnlySignEntireHeadersAndBody />   
        </wsp:Policy>  
      </sp:SymmetricBinding>  
      <sp:Wss11>  
        <wsp:Policy>  
          <sp:MustSupportRefKeyIdentifier />   
          <sp:MustSupportRefIssuerSerial />   
          <sp:MustSupportRefThumbprint />   
          <sp:MustSupportRefEncryptedKey />   
        </wsp:Policy>  
      </sp:Wss11>  
      <sp:Trust10>  
        <wsp:Policy>  
          <sp:MustSupportIssuedTokens />   
          <sp:RequireClientEntropy />   
          <sp:RequireServerEntropy />   
        </wsp:Policy>  
      </sp:Trust10>  
      <wsaw:UsingAddressing />   
    </wsp:All>  
  </wsp:ExactlyOne>  
</wsp:Policy>  
```  
  
### <a name="security-header-examples-signbeforeencrypt-encryptsignature"></a><span data-ttu-id="e167d-583">Exemples d’en-tête de sécurité : SignBeforeEncrypt, EncryptSignature</span><span class="sxs-lookup"><span data-stu-id="e167d-583">Security Header Examples: SignBeforeEncrypt, EncryptSignature</span></span>  
 <span data-ttu-id="e167d-584">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-584">Request</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-585">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-585">Response</span></span>  
  
```xml  
<wsse:Security s:mustUnderstand="1">  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
  <xenc:EncryptedData>  
  ...  
  </xenc:EncryptedData>  
</wsse:Security>    
```  
  
### <a name="security-header-examples-encryptbeforesign"></a><span data-ttu-id="e167d-586">Exemples d’en-tête de sécurité : EncryptBeforeSign</span><span class="sxs-lookup"><span data-stu-id="e167d-586">Security Header Examples: EncryptBeforeSign</span></span>  
 <span data-ttu-id="e167d-587">Demande</span><span class="sxs-lookup"><span data-stu-id="e167d-587">Request</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:SecurityContextToken>  
  ...  
  </wsc:SecurityContextToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```  
  
 <span data-ttu-id="e167d-588">Réponse</span><span class="sxs-lookup"><span data-stu-id="e167d-588">Response</span></span>  
  
```xml  
<wsse:Security>  
  <wsu:Timestamp>  
  ...  
  </wsu:Timestamp>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <wsc:DerivedKeyToken>  
  ...  
  </wsc:DerivedKeyToken>  
  <ds:Signature>  
  ...  
  </ds:Signature>  
  <xenc:ReferenceList>  
  ...  
  </xenc:ReferenceList>  
</wsse:Security>  
```
