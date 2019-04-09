---
title: <idn> Élément (paramètres d’Uri)
ms.date: 03/30/2017
ms.assetid: 16c8e869-1791-4cf5-9244-3d3c738f60ec
ms.openlocfilehash: 3940f30f2ef90a77560a82edc909071f0ee8e130
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59129400"
---
# <a name="idn-element-uri-settings"></a>\<IDN >, élément (paramètres d’Uri)
Spécifie si l’analyse du nom de domaine international (IDN) est appliqué à un nom de domaine.  
  
## <a name="schema-hierarchy"></a>Hiérarchie de schéma  
 [\<configuration > élément](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [\<URI >, élément (paramètres d’Uri)](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)  
  
 [\<idn>](../../../../../docs/framework/configure-apps/file-schema/network/idn-element-uri-settings.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<idn  
  enabled="All|AllExceptIntranet|None"  
/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|`enabled`|Spécifie que si l’analyse du nom de domaine international (IDN) est appliqué à un nom de domaine la valeur par défaut est none.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[uri](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)|Contient des paramètres qui spécifient la façon dont le .NET Framework gère les adresses web exprimées à l’aide d’identificateurs de ressource uniforme (URI).|  
  
## <a name="remarks"></a>Notes  
 Existant <xref:System.Uri> classe a été étendue dans .NET Framework 3.5. 3.0 SP1 et 2.0 SP1 avec prise en charge pour les identificateurs IRI (International Resource) et les noms de domaine international (IDN). Les utilisateurs actuels ne verront pas de toute modification du comportement de .NET Framework 2.0, sauf si ils activent spécifiquement les IRI et des IDN prennent en charge. Cela garantit la compatibilité des applications avec les versions antérieures de .NET Framework.  
  
 Pour activer la prise en charge des IRI, les deux modifications suivantes sont requises :  
  
1.  Ajoutez la ligne suivante au fichier machine.config sous le répertoire .NET Framework 2.0  
  
    ```xml  
    <section name="uri" type="System.Configuration.UriSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
    ```  
  
2.  Spécifiez si vous souhaitez que l’analyse de nom de domaine international (IDN) appliquée au nom de domaine et si les règles d’analyse IRI doivent être appliquée. Cela est spécifié dans le fichier machine.config ou app.config.  
  
 Il existe trois valeurs possibles pour l’IDN selon les serveurs DNS qui sont utilisés :  
  
-   IDN activé = All  
  
     Cette valeur convertit les noms de domaine Unicode en leurs équivalents Punycode (noms IDN).  
  
-   IDN activé = AllExceptIntranet  
  
     Cette valeur convertit tous les noms de domaine Unicode pas sur l’Intranet local pour utiliser les équivalents Punycode (noms IDN). Dans ce cas pour gérer des noms internationaux sur l’Intranet local, les serveurs DNS qui sont utilisés pour l’Intranet doivent prendre en charge résolution de noms Unicode.  
  
-   IDN activé = None  
  
     Cette valeur ne convertira pas les noms de domaine Unicode pour utiliser Punycode. Il s’agit de la valeur par défaut qui est cohérente avec le comportement de .NET Framework 2.0.  
  
 L’activation des IDN entraîne la conversion de toutes les étiquettes Unicode d’un nom de domaine en leurs équivalents Punycode. Les noms Punycode contiennent uniquement des caractères ASCII et commencent toujours par le préfixe xn--. Cela permet de garantir la prise en charge des serveurs DNS existants sur Internet, la plupart d’entre eux prenant uniquement en charge les caractères ASCII (consultez la norme RFC 3940).  
  
### <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 L’exemple suivant montre une configuration utilisée par la <xref:System.Uri> classe pour prendre en charge l’analyse des IRI et les noms IDN.  
  
### <a name="code"></a>Code  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Configuration.IdnElement?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
