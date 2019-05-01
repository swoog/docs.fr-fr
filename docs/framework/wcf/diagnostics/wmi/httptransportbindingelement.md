---
title: HttpTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 088a7bce-6bb2-4839-ad74-f68d4b1aa0f9
ms.openlocfilehash: 5e23342d57621554aaec67c5c568bb75202a9454
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61963486"
---
# <a name="httptransportbindingelement"></a><span data-ttu-id="5831c-102">HttpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="5831c-102">HttpTransportBindingElement</span></span>
<span data-ttu-id="5831c-103">HttpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="5831c-103">HttpTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5831c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5831c-104">Syntax</span></span>  
  
```csharp
class HttpTransportBindingElement : TransportBindingElement  
{  
  boolean AllowCookies;  
  string AuthenticationScheme;  
  boolean BypassProxyOnLocal;  
  string HostNameComparisonMode;  
  boolean KeepAliveEnabled;  
  sint32 MaxBufferSize;  
  string ProxyAddress;  
  string ProxyAuthenticationScheme;  
  string Realm;  
  string TransferMode;  
  boolean UnsafeConnectionNtlmAuthentication;  
  boolean UseDefaultWebProxy;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="5831c-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5831c-105">Methods</span></span>  
 <span data-ttu-id="5831c-106">La classe HttpTransportBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="5831c-106">The HttpTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="5831c-107">Properties</span><span class="sxs-lookup"><span data-stu-id="5831c-107">Properties</span></span>  
 <span data-ttu-id="5831c-108">La classe HttpTransportBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="5831c-108">The HttpTransportBindingElement class has the following properties:</span></span>  
  
### <a name="allowcookies"></a><span data-ttu-id="5831c-109">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="5831c-109">AllowCookies</span></span>  
 <span data-ttu-id="5831c-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="5831c-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="5831c-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-112">Valeur qui indique si le client accepte les cookies et les propage aux demandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5831c-112">A value that indicates whether the client accepts cookies and propagates them on future requests.</span></span>  
  
### <a name="authenticationscheme"></a><span data-ttu-id="5831c-113">AuthenticationScheme</span><span class="sxs-lookup"><span data-stu-id="5831c-113">AuthenticationScheme</span></span>  
 <span data-ttu-id="5831c-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5831c-114">Data type: string</span></span>  
  
 <span data-ttu-id="5831c-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-116">Schéma d'authentification utilisé pour authentifier les demandes d'un client traitées par un écouteur HTTP.</span><span class="sxs-lookup"><span data-stu-id="5831c-116">The authentication scheme used to authenticate client requests being processed by an HTTP listener.</span></span>  
  
### <a name="bypassproxyonlocal"></a><span data-ttu-id="5831c-117">BypassProxyOnLocal</span><span class="sxs-lookup"><span data-stu-id="5831c-117">BypassProxyOnLocal</span></span>  
 <span data-ttu-id="5831c-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="5831c-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="5831c-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-120">Valeur qui indique si les proxys sont ignorés pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="5831c-120">A value that indicates whether proxies are ignored for local addresses.</span></span>  
  
### <a name="hostnamecomparisonmode"></a><span data-ttu-id="5831c-121">HostNameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="5831c-121">HostNameComparisonMode</span></span>  
 <span data-ttu-id="5831c-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5831c-122">Data type: string</span></span>  
  
 <span data-ttu-id="5831c-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-124">Valeur qui indique si le nom d'hôte est utilisé pour atteindre le service lors de la correspondance avec l'URI.</span><span class="sxs-lookup"><span data-stu-id="5831c-124">A value that indicates whether the hostname is used to reach the service when matching on the URI.</span></span>  
  
### <a name="keepaliveenabled"></a><span data-ttu-id="5831c-125">KeepAliveEnabled</span><span class="sxs-lookup"><span data-stu-id="5831c-125">KeepAliveEnabled</span></span>  
 <span data-ttu-id="5831c-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="5831c-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="5831c-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-128">En cas d'activation, les connexions HTTP sont maintenues indépendamment du niveau d'activité.</span><span class="sxs-lookup"><span data-stu-id="5831c-128">When enabled, HTTP connections are kept alive regardless of activity level.</span></span>  
  
### <a name="maxbuffersize"></a><span data-ttu-id="5831c-129">MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="5831c-129">MaxBufferSize</span></span>  
 <span data-ttu-id="5831c-130">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="5831c-130">Data type: sint32</span></span>  
  
 <span data-ttu-id="5831c-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-132">La taille maximale du pool de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="5831c-132">The maximum size of the buffer pool.</span></span>  
  
### <a name="proxyaddress"></a><span data-ttu-id="5831c-133">ProxyAddress</span><span class="sxs-lookup"><span data-stu-id="5831c-133">ProxyAddress</span></span>  
 <span data-ttu-id="5831c-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5831c-134">Data type: string</span></span>  
  
 <span data-ttu-id="5831c-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-136">URI qui contient l'adresse du proxy à utiliser pour les requêtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="5831c-136">A URI that contains the address of the proxy to use for HTTP requests.</span></span>  
  
### <a name="proxyauthenticationscheme"></a><span data-ttu-id="5831c-137">ProxyAuthenticationScheme</span><span class="sxs-lookup"><span data-stu-id="5831c-137">ProxyAuthenticationScheme</span></span>  
 <span data-ttu-id="5831c-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5831c-138">Data type: string</span></span>  
  
 <span data-ttu-id="5831c-139">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-140">Schéma d'authentification utilisé pour authentifier les demandes d'un client traitées par un proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="5831c-140">The authentication scheme used to authenticate client requests being processed by an HTTP proxy.</span></span>  
  
### <a name="realm"></a><span data-ttu-id="5831c-141">Realm</span><span class="sxs-lookup"><span data-stu-id="5831c-141">Realm</span></span>  
 <span data-ttu-id="5831c-142">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5831c-142">Data type: string</span></span>  
  
 <span data-ttu-id="5831c-143">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-144">Domaine d'authentification.</span><span class="sxs-lookup"><span data-stu-id="5831c-144">The authentication realm.</span></span>  
  
### <a name="transfermode"></a><span data-ttu-id="5831c-145">TransferMode</span><span class="sxs-lookup"><span data-stu-id="5831c-145">TransferMode</span></span>  
 <span data-ttu-id="5831c-146">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5831c-146">Data type: string</span></span>  
  
 <span data-ttu-id="5831c-147">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-148">Valeur qui spécifie si les messages sont mis en mémoire tampon ou transmis en continu ou s'il s'agit d'une demande ou d'une réponse.</span><span class="sxs-lookup"><span data-stu-id="5831c-148">A value that specifies whether messages are buffered or streamed or a request or response.</span></span>  
  
### <a name="unsafeconnectionntlmauthentication"></a><span data-ttu-id="5831c-149">UnsafeConnectionNtlmAuthentication</span><span class="sxs-lookup"><span data-stu-id="5831c-149">UnsafeConnectionNtlmAuthentication</span></span>  
 <span data-ttu-id="5831c-150">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="5831c-150">Data type: boolean</span></span>  
  
 <span data-ttu-id="5831c-151">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-152">Valeur qui indique si le partage de connexion non sécurisé est activé sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="5831c-152">A value that indicates whether Unsafe Connection Sharing is enabled on the server.</span></span>  
  
### <a name="usedefaultwebproxy"></a><span data-ttu-id="5831c-153">UseDefaultWebProxy</span><span class="sxs-lookup"><span data-stu-id="5831c-153">UseDefaultWebProxy</span></span>  
 <span data-ttu-id="5831c-154">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="5831c-154">Data type: boolean</span></span>  
  
 <span data-ttu-id="5831c-155">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5831c-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5831c-156">Valeur qui indique si les paramètres de proxy à l'échelle de l'ordinateur sont utilisés à la place des paramètres propres à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5831c-156">A value that indicates whether the machine-wide proxy settings are used rather than the user specific settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5831c-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5831c-157">Requirements</span></span>  
  
|<span data-ttu-id="5831c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="5831c-158">MOF</span></span>|<span data-ttu-id="5831c-159">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="5831c-159">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="5831c-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5831c-160">Namespace</span></span>|<span data-ttu-id="5831c-161">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="5831c-161">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5831c-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5831c-162">See also</span></span>

- <xref:System.ServiceModel.Channels.HttpTransportBindingElement>
