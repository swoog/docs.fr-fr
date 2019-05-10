---
title: <httpListener>, élément (paramètres réseau)
ms.date: 03/30/2017
ms.assetid: 62f121fd-3f2e-4033-bb39-48ae996bfbd9
ms.openlocfilehash: 8257b0311e18a21fbc04185f8297ee8e5f38b86b
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64592736"
---
# <a name="httplistener-element-network-settings"></a>\<httpListener >, élément (paramètres réseau)
Personnalise les paramètres utilisés par la <xref:System.Net.HttpListener> classe.  
  
 \<configuration>  
\<system.net>  
\<settings>  
\<httpListener>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<httpListener  
  unescapeRequestUrl="true|false"  
/>  
```  
  
## <a name="type"></a>Type  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|unescapeRequestUrl|Valeur booléenne qui indique si un <xref:System.Net.HttpListener> instance utilise l’URI brut sans séquence d’échappement plutôt que l’URI converti.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[settings](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|Configure les options réseau de base pour l’espace de noms <xref:System.Net>.|  
  
## <a name="remarks"></a>Notes  
 Le **unescapeRequestUrl** attribut indique si <xref:System.Net.HttpListener> utilise l’URI brut sans séquence d’échappement plutôt que l’URI converti où toutes les valeurs encodées de pourcentage sont converties et autres étapes de normalisation sont exécutées.  
  
 Quand un <xref:System.Net.HttpListener> instance reçoit une demande via le `http.sys` service, il crée une instance de la chaîne d’URI fournie par `http.sys`et l’expose en tant que le <xref:System.Net.HttpListenerRequest.Url%2A?displayProperty=nameWithType> propriété.  
  
 Le `http.sys` service expose deux chaînes d’URI de demande :  
  
- URI brut  
  
- URI converti  
  
 L’URI brut est le <xref:System.Uri?displayProperty=nameWithType> fourni dans la ligne de demande d’une demande HTTP :  
  
 `GET /path/`  
  
 `Host: www.contoso.com`  
  
 L’URI brut fourni par `http.sys` pour la requête mentionnée ci-dessus, est « / path / ». Cela représente la chaîne qui suit le verbe HTTP lorsqu’il a été envoyé sur le réseau.  
  
 Le `http.sys` service crée un URI converti à partir des informations fournies dans la demande à l’aide de l’URI fourni dans la ligne de la requête HTTP et l’en-tête d’hôte pour déterminer le serveur d’origine la demande doit être transférée à. Cela est effectué en comparant les informations à partir de la demande avec un ensemble de préfixes URI enregistrés. La documentation du SDK du serveur HTTP fait référence à cet URI converti en tant que structure HTTP_COOKED_URL.  
  
 Pour être en mesure de comparer la demande avec les préfixes URI enregistrés, une normalisation de la demande doit être effectuée. Pour l’exemple ci-dessus, l’URI converti est comme suit :  
  
 `http://www.contoso.com/path/`  
  
 Le `http.sys` service combine le <xref:System.Uri.Host%2A?displayProperty=nameWithType> valeur de propriété et la chaîne dans la ligne de demande de création d’un URI converti. En outre, `http.sys` et <xref:System.Uri?displayProperty=nameWithType> classe effectue également les opérations suivantes :  
  
- N’échappe pas pourcentage de toutes les valeurs encodées.  
  
- Convertit encodés en pourcentage des caractères non ASCII en une représentation de caractères UTF-16. Notez que les caractères UTF-8 et ANSI ou DBCS sont pris en charge, ainsi que des caractères Unicode (encodage Unicode en utilisant le format d’uXXXX %).  
  
- Exécute les autres étapes de normalisation, comme la compression de chemin d’accès.  
  
 Étant donné que la demande ne contient pas toutes les informations concernant l’encodage utilisé pour les valeurs encodées en pourcentage, il n’est peut-être pas possible de déterminer l’encodage correct seulement en analysant les valeurs encodées en pourcentage.  
  
 Par conséquent `http.sys` fournit deux clés de Registre pour la modification du processus :  
  
|Clé de Registre|Valeur par défaut|Description|  
|------------------|-------------------|-----------------|  
|EnableNonUTF8|1|Si zéro, `http.sys` accepte uniquement les URL encodée en UTF-8.<br /><br /> Si non nul, `http.sys` accepte également des URL ANSI ou DBCS dans les requêtes.|  
|FavorUTF8|1|Si non nul, `http.sys` essaie toujours de décoder une URL au format UTF-8 tout d’abord ; si cette conversion échoue et EnableNonUTF8 n’est pas nulle, Http.sys, puis tente de décoder comme ANSI ou DBCS.<br /><br /> Si zéro (et EnableNonUTF8 n’est pas nulle), `http.sys` tente de décoder comme ANSI ou DBCS ; si ce n’est pas réussie, il essaie une conversion UTF-8.|  
  
 Lorsque <xref:System.Net.HttpListener> reçoit une demande, il utilise l’URI converti à partir de `http.sys` comme entrée pour le <xref:System.Net.HttpListenerRequest.Url%2A> propriété.  
  
 Il est nécessaire pour prendre en charge des caractères en plus des caractères et les nombres dans les URI. Un exemple est l’URI suivant, qui est utilisée pour récupérer des informations sur le client pour le client numéro « 1/3812 » :  
  
 `http://www.contoso.com/Customer('1%2F3812')/`  
  
 Notez la barre oblique d’encodée en pourcentage dans l’Uri (% 2F). Cela est nécessaire, puisque dans ce cas la barre oblique représente des données et non un délimiteur de chemin d’accès.  
  
 En passant la chaîne au constructeur d’Uri entraîne l’URI suivant :  
  
 `http://www.contoso.com/Customer('1/3812')/`  
  
 Fractionner le chemin d’accès en ses segments génère les éléments suivants :  
  
 `Customer('1`  
  
 `3812')`  
  
 Cela n’est pas l’intention de l’expéditeur de la demande.  
  
 Si le **unescapeRequestUrl** attribut a la valeur **false**, lorsque le <xref:System.Net.HttpListener> reçoit une demande, il utilise l’URI brut au lieu de l’URI converti à partir de `http.sys` en tant qu’entrée pour le <xref:System.Net.HttpListenerRequest.Url%2A> propriété.  
  
 La valeur par défaut pour le **unescapeRequestUrl** attribut est **true**.  
  
 Le <xref:System.Net.Configuration.HttpListenerElement.UnescapeRequestUrl%2A> propriété peut être utilisée pour obtenir la valeur actuelle de la **unescapeRequestUrl** attribut à partir des fichiers de configuration applicables.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment configurer le <xref:System.Net.HttpListener> lorsqu’il reçoit une demande pour utiliser l’URI brut au lieu de l’URI converti à partir de la classe `http.sys` comme entrée pour le <xref:System.Net.HttpListenerRequest.Url%2A> propriété.  
  
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
  
## <a name="element-information"></a>Informations sur les éléments  
  
|||
|-|-|  
|Espace de noms|System.Net|  
|Nom du schéma||  
|Fichier de validation||  
|Peut être vide||  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Net.Configuration.HttpListenerElement>
- <xref:System.Net.HttpListener>
- <xref:System.Net.HttpListenerRequest.Url%2A>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
