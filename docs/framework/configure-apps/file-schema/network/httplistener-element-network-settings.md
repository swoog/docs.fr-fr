---
title: '&lt;httpListener&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
ms.assetid: 62f121fd-3f2e-4033-bb39-48ae996bfbd9
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 7a8fbf172548ea68874f3e6c6c6c7a04bf17be19
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47078602"
---
# <a name="lthttplistenergt-element-network-settings"></a><span data-ttu-id="f4a35-102">&lt;httpListener&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="f4a35-102">&lt;httpListener&gt; Element (Network Settings)</span></span>
<span data-ttu-id="f4a35-103">Personnalise les paramètres utilisés par la <xref:System.Net.HttpListener> classe.</span><span class="sxs-lookup"><span data-stu-id="f4a35-103">Customizes parameters used by the <xref:System.Net.HttpListener> class.</span></span>  
  
 <span data-ttu-id="f4a35-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="f4a35-104">\<configuration></span></span>  
<span data-ttu-id="f4a35-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="f4a35-105">\<system.net></span></span>  
<span data-ttu-id="f4a35-106">\<Paramètres ></span><span class="sxs-lookup"><span data-stu-id="f4a35-106">\<settings></span></span>  
<span data-ttu-id="f4a35-107">\<httpListener ></span><span class="sxs-lookup"><span data-stu-id="f4a35-107">\<httpListener></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4a35-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4a35-108">Syntax</span></span>  
  
```xml  
<httpListener  
  unescapeRequestUrl="true|false"  
/>  
```  
  
## <a name="type"></a><span data-ttu-id="f4a35-109">Type</span><span class="sxs-lookup"><span data-stu-id="f4a35-109">Type</span></span>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f4a35-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f4a35-110">Attributes and Elements</span></span>  
 <span data-ttu-id="f4a35-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f4a35-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f4a35-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="f4a35-112">Attributes</span></span>  
  
|<span data-ttu-id="f4a35-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="f4a35-113">Attribute</span></span>|<span data-ttu-id="f4a35-114">Description</span><span class="sxs-lookup"><span data-stu-id="f4a35-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f4a35-115">unescapeRequestUrl</span><span class="sxs-lookup"><span data-stu-id="f4a35-115">unescapeRequestUrl</span></span>|<span data-ttu-id="f4a35-116">Valeur booléenne qui indique si un <xref:System.Net.HttpListener> instance utilise l’URI brut sans séquence d’échappement plutôt que l’URI converti.</span><span class="sxs-lookup"><span data-stu-id="f4a35-116">A Boolean value that indicates if a <xref:System.Net.HttpListener> instance uses the raw unescaped URI instead of the converted URI.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f4a35-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f4a35-117">Child Elements</span></span>  
 <span data-ttu-id="f4a35-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f4a35-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f4a35-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f4a35-119">Parent Elements</span></span>  
  
|<span data-ttu-id="f4a35-120">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f4a35-120">**Element**</span></span>|<span data-ttu-id="f4a35-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4a35-121">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="f4a35-122">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4a35-122">settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|<span data-ttu-id="f4a35-123">Configure les options réseau de base pour l’espace de noms <xref:System.Net>.</span><span class="sxs-lookup"><span data-stu-id="f4a35-123">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f4a35-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f4a35-124">Remarks</span></span>  
 <span data-ttu-id="f4a35-125">Le **unescapeRequestUrl** attribut indique si <xref:System.Net.HttpListener> utilise l’URI brut sans séquence d’échappement plutôt que l’URI converti où toutes les valeurs encodées de pourcentage sont converties et autres étapes de normalisation sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="f4a35-125">The **unescapeRequestUrl** attribute indicates if <xref:System.Net.HttpListener> uses the raw unescaped URI instead of the converted URI where any percent-encoded values are converted and other normalization steps are taken.</span></span>  
  
 <span data-ttu-id="f4a35-126">Quand un <xref:System.Net.HttpListener> instance reçoit une demande via le `http.sys` service, il crée une instance de la chaîne d’URI fournie par `http.sys`et l’expose en tant que le <xref:System.Net.HttpListenerRequest.Url%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="f4a35-126">When a <xref:System.Net.HttpListener> instance receives a request through the `http.sys` service, it creates an instance of the URI string provided by `http.sys`, and exposes it as the <xref:System.Net.HttpListenerRequest.Url%2A?displayProperty=nameWithType> property.</span></span>  
  
 <span data-ttu-id="f4a35-127">Le `http.sys` service expose deux chaînes d’URI de demande :</span><span class="sxs-lookup"><span data-stu-id="f4a35-127">The `http.sys` service exposes two request URI strings:</span></span>  
  
-   <span data-ttu-id="f4a35-128">URI brut</span><span class="sxs-lookup"><span data-stu-id="f4a35-128">Raw URI</span></span>  
  
-   <span data-ttu-id="f4a35-129">URI converti</span><span class="sxs-lookup"><span data-stu-id="f4a35-129">Converted URI</span></span>  
  
 <span data-ttu-id="f4a35-130">L’URI brut est le <xref:System.Uri?displayProperty=nameWithType> fourni dans la ligne de demande d’une demande HTTP :</span><span class="sxs-lookup"><span data-stu-id="f4a35-130">The raw URI is the <xref:System.Uri?displayProperty=nameWithType> provided in the request line of a HTTP request:</span></span>  
  
 `GET /path/`  
  
 `Host: www.contoso.com`  
  
 <span data-ttu-id="f4a35-131">L’URI brut fourni par `http.sys` pour la requête mentionnée ci-dessus, est « / path / ».</span><span class="sxs-lookup"><span data-stu-id="f4a35-131">The raw URI provided by `http.sys` for the request mentioned above, is "/path/".</span></span> <span data-ttu-id="f4a35-132">Cela représente la chaîne qui suit le verbe HTTP lorsqu’il a été envoyé sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="f4a35-132">This represents the string following the HTTP verb as it was sent over the network.</span></span>  
  
 <span data-ttu-id="f4a35-133">Le `http.sys` service crée un URI converti à partir des informations fournies dans la demande à l’aide de l’URI fourni dans la ligne de la requête HTTP et l’en-tête d’hôte pour déterminer le serveur d’origine la demande doit être transférée à.</span><span class="sxs-lookup"><span data-stu-id="f4a35-133">The `http.sys` service creates a converted URI from the information provided in the request by using the URI provided in the HTTP request line and the Host header to determine the origin server the request should be forwarded to.</span></span> <span data-ttu-id="f4a35-134">Cela est effectué en comparant les informations à partir de la demande avec un ensemble de préfixes URI enregistrés.</span><span class="sxs-lookup"><span data-stu-id="f4a35-134">This is done by comparing the information from the request with a set of registered URI prefixes.</span></span> <span data-ttu-id="f4a35-135">La documentation du SDK du serveur HTTP fait référence à cet URI converti en tant que structure HTTP_COOKED_URL.</span><span class="sxs-lookup"><span data-stu-id="f4a35-135">The HTTP Server SDK documentation refers to this converted URI as the HTTP_COOKED_URL structure.</span></span>  
  
 <span data-ttu-id="f4a35-136">Pour être en mesure de comparer la demande avec les préfixes URI enregistrés, une normalisation de la demande doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="f4a35-136">In order to be able to compare the request with registered URI prefixes, some normalization to the request needs to be done.</span></span> <span data-ttu-id="f4a35-137">Pour l’exemple ci-dessus, l’URI converti est comme suit :</span><span class="sxs-lookup"><span data-stu-id="f4a35-137">For the sample above the converted URI would be as follows:</span></span>  
  
 `http://www.contoso.com/path/`  
  
 <span data-ttu-id="f4a35-138">Le `http.sys` service combine le <xref:System.Uri.Host%2A?displayProperty=nameWithType> valeur de propriété et la chaîne dans la ligne de demande de création d’un URI converti.</span><span class="sxs-lookup"><span data-stu-id="f4a35-138">The `http.sys` service combines the <xref:System.Uri.Host%2A?displayProperty=nameWithType> property value and the string in the request line to create a converted URI.</span></span> <span data-ttu-id="f4a35-139">En outre, `http.sys` et <xref:System.Uri?displayProperty=nameWithType> classe effectue également les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4a35-139">In addition, `http.sys` and the <xref:System.Uri?displayProperty=nameWithType> class also does the following:</span></span>  
  
-   <span data-ttu-id="f4a35-140">N’échappe pas pourcentage de toutes les valeurs encodées.</span><span class="sxs-lookup"><span data-stu-id="f4a35-140">Un-escapes all percent encoded values.</span></span>  
  
-   <span data-ttu-id="f4a35-141">Convertit encodés en pourcentage des caractères non ASCII en une représentation de caractères UTF-16.</span><span class="sxs-lookup"><span data-stu-id="f4a35-141">Converts percent-encoded non-ASCII characters into a UTF-16 character representation.</span></span> <span data-ttu-id="f4a35-142">Notez que les caractères UTF-8 et ANSI ou DBCS sont pris en charge, ainsi que des caractères Unicode (encodage Unicode en utilisant le format d’uXXXX %).</span><span class="sxs-lookup"><span data-stu-id="f4a35-142">Note that UTF-8 and ANSI/DBCS characters are supported as well as Unicode characters (Unicode encoding using the %uXXXX format).</span></span>  
  
-   <span data-ttu-id="f4a35-143">Exécute les autres étapes de normalisation, comme la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f4a35-143">Executes other normalization steps, like path compression.</span></span>  
  
 <span data-ttu-id="f4a35-144">Étant donné que la demande ne contient pas toutes les informations concernant l’encodage utilisé pour les valeurs encodées en pourcentage, il n’est peut-être pas possible de déterminer l’encodage correct seulement en analysant les valeurs encodées en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="f4a35-144">Since the request doesn't contain any information about the encoding used for percent-encoded values, it may not be possible to determine the correct encoding just by parsing the percent-encoded values.</span></span>  
  
 <span data-ttu-id="f4a35-145">Par conséquent `http.sys` fournit deux clés de Registre pour la modification du processus :</span><span class="sxs-lookup"><span data-stu-id="f4a35-145">Therefore `http.sys` provides two registry keys for modifying the process:</span></span>  
  
|<span data-ttu-id="f4a35-146">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="f4a35-146">Registry Key</span></span>|<span data-ttu-id="f4a35-147">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f4a35-147">Default Value</span></span>|<span data-ttu-id="f4a35-148">Description</span><span class="sxs-lookup"><span data-stu-id="f4a35-148">Description</span></span>|  
|------------------|-------------------|-----------------|  
|<span data-ttu-id="f4a35-149">EnableNonUTF8 n'</span><span class="sxs-lookup"><span data-stu-id="f4a35-149">EnableNonUTF8</span></span>|<span data-ttu-id="f4a35-150">1</span><span class="sxs-lookup"><span data-stu-id="f4a35-150">1</span></span>|<span data-ttu-id="f4a35-151">Si zéro, `http.sys` accepte uniquement les URL encodée en UTF-8.</span><span class="sxs-lookup"><span data-stu-id="f4a35-151">If zero, `http.sys` accepts only UTF-8-encoded URLs.</span></span><br /><br /> <span data-ttu-id="f4a35-152">Si non nul, `http.sys` accepte également des URL ANSI ou DBCS dans les requêtes.</span><span class="sxs-lookup"><span data-stu-id="f4a35-152">If non-zero, `http.sys` also accepts ANSI-encoded or DBCS-encoded URLs in requests.</span></span>|  
|<span data-ttu-id="f4a35-153">FavorUTF8</span><span class="sxs-lookup"><span data-stu-id="f4a35-153">FavorUTF8</span></span>|<span data-ttu-id="f4a35-154">1</span><span class="sxs-lookup"><span data-stu-id="f4a35-154">1</span></span>|<span data-ttu-id="f4a35-155">Si non nul, `http.sys` essaie toujours de décoder une URL au format UTF-8 tout d’abord ; si cette conversion échoue et EnableNonUTF8 n’est pas nulle, Http.sys, puis tente de décoder comme ANSI ou DBCS.</span><span class="sxs-lookup"><span data-stu-id="f4a35-155">If non-zero, `http.sys` always tries to decode a URL as UTF-8 first; if that conversion fails and EnableNonUTF8 is non-zero, Http.sys then tries to decode it as ANSI or DBCS.</span></span><br /><br /> <span data-ttu-id="f4a35-156">Si zéro (et EnableNonUTF8 n’est pas nulle), `http.sys` tente de décoder comme ANSI ou DBCS ; si ce n’est pas réussie, il essaie une conversion UTF-8.</span><span class="sxs-lookup"><span data-stu-id="f4a35-156">If zero (and EnableNonUTF8 is non-zero), `http.sys` tries to decode it as ANSI or DBCS; if that is not successful, it tries a UTF-8 conversion.</span></span>|  
  
 <span data-ttu-id="f4a35-157">Lorsque <xref:System.Net.HttpListener> reçoit une demande, il utilise l’URI converti à partir de `http.sys` comme entrée pour le <xref:System.Net.HttpListenerRequest.Url%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f4a35-157">When <xref:System.Net.HttpListener> receives a request, it uses the converted URI from `http.sys` as input to the <xref:System.Net.HttpListenerRequest.Url%2A> property.</span></span>  
  
 <span data-ttu-id="f4a35-158">Il est nécessaire pour prendre en charge des caractères en plus des caractères et les nombres dans les URI.</span><span class="sxs-lookup"><span data-stu-id="f4a35-158">There is a need for supporting characters besides characters and numbers in URIs.</span></span> <span data-ttu-id="f4a35-159">Un exemple est l’URI suivant, qui est utilisée pour récupérer des informations sur le client pour le client numéro « 1/3812 » :</span><span class="sxs-lookup"><span data-stu-id="f4a35-159">An example is the following URI, which is used to retrieve customer information for customer number "1/3812":</span></span>  
  
 `http://www.contoso.com/Customer('1%2F3812')/`  
  
 <span data-ttu-id="f4a35-160">Notez la barre oblique d’encodée en pourcentage dans l’Uri (% 2F).</span><span class="sxs-lookup"><span data-stu-id="f4a35-160">Note the percent-encoded slash in the Uri (%2F).</span></span> <span data-ttu-id="f4a35-161">Cela est nécessaire, puisque dans ce cas la barre oblique représente des données et non un délimiteur de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f4a35-161">This is necessary, since in this case the slash character represents data and not a path delimiter.</span></span>  
  
 <span data-ttu-id="f4a35-162">En passant la chaîne au constructeur d’Uri entraîne l’URI suivant :</span><span class="sxs-lookup"><span data-stu-id="f4a35-162">Passing the string to Uri constructor will lead to the following URI:</span></span>  
  
 `http://www.contoso.com/Customer('1/3812')/`  
  
 <span data-ttu-id="f4a35-163">Fractionner le chemin d’accès en ses segments génère les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f4a35-163">Splitting the path into its segments would result in the following elements:</span></span>  
  
 `Customer('1`  
  
 `3812')`  
  
 <span data-ttu-id="f4a35-164">Cela n’est pas l’intention de l’expéditeur de la demande.</span><span class="sxs-lookup"><span data-stu-id="f4a35-164">This is not the intent of the sender of the request.</span></span>  
  
 <span data-ttu-id="f4a35-165">Si le **unescapeRequestUrl** attribut a la valeur **false**, lorsque le <xref:System.Net.HttpListener> reçoit une demande, il utilise l’URI brut au lieu de l’URI converti à partir de `http.sys` en tant qu’entrée pour le <xref:System.Net.HttpListenerRequest.Url%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f4a35-165">If the **unescapeRequestUrl** attribute is set to **false**, then when the <xref:System.Net.HttpListener> receives a request, it uses the raw URI instead of the converted URI from `http.sys` as input to the <xref:System.Net.HttpListenerRequest.Url%2A> property.</span></span>  
  
 <span data-ttu-id="f4a35-166">La valeur par défaut pour le **unescapeRequestUrl** attribut est **true**.</span><span class="sxs-lookup"><span data-stu-id="f4a35-166">The default value for the **unescapeRequestUrl** attribute is **true**.</span></span>  
  
 <span data-ttu-id="f4a35-167">Le <xref:System.Net.Configuration.HttpListenerElement.UnescapeRequestUrl%2A> propriété peut être utilisée pour obtenir la valeur actuelle de la **unescapeRequestUrl** attribut à partir des fichiers de configuration applicables.</span><span class="sxs-lookup"><span data-stu-id="f4a35-167">The <xref:System.Net.Configuration.HttpListenerElement.UnescapeRequestUrl%2A> property can be used to get the current value of the **unescapeRequestUrl** attribute from applicable configuration files.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f4a35-168">Exemple</span><span class="sxs-lookup"><span data-stu-id="f4a35-168">Example</span></span>  
 <span data-ttu-id="f4a35-169">L’exemple suivant montre comment configurer le <xref:System.Net.HttpListener> lorsqu’il reçoit une demande pour utiliser l’URI brut au lieu de l’URI converti à partir de la classe `http.sys` comme entrée pour le <xref:System.Net.HttpListenerRequest.Url%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f4a35-169">The following example shows how to configure the <xref:System.Net.HttpListener> class when it receives a request to use the raw URI instead of the converted URI from `http.sys` as input to the <xref:System.Net.HttpListenerRequest.Url%2A> property.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <httpListener  
        unescapeRequestUrl="false"  
      />  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="element-information"></a><span data-ttu-id="f4a35-170">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f4a35-170">Element Information</span></span>  
  
|||
|-|-|  
|<span data-ttu-id="f4a35-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f4a35-171">Namespace</span></span>|<span data-ttu-id="f4a35-172">System.Net</span><span class="sxs-lookup"><span data-stu-id="f4a35-172">System.Net</span></span>|  
|<span data-ttu-id="f4a35-173">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="f4a35-173">Schema Name</span></span>||  
|<span data-ttu-id="f4a35-174">Fichier de validation</span><span class="sxs-lookup"><span data-stu-id="f4a35-174">Validation File</span></span>||  
|<span data-ttu-id="f4a35-175">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="f4a35-175">Can be Empty</span></span>||  
  
## <a name="see-also"></a><span data-ttu-id="f4a35-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4a35-176">See Also</span></span>  
 <xref:System.Net.Configuration.HttpListenerElement>  
 <xref:System.Net.HttpListener>  
 <xref:System.Net.HttpListenerRequest.Url%2A>  
 [<span data-ttu-id="f4a35-177">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="f4a35-177">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
