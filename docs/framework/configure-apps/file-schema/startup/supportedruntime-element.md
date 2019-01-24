---
title: '&lt;supportedRuntime&gt; élément'
ms.date: 04/10/2018
ms.custom: updateeachrelease
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#supportedRuntime
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup/supportedRuntime
helpviewer_keywords:
- supportedRuntime element
- <supportedRuntime> element
ms.assetid: 1ae16e23-afbe-4de4-b413-bc457f37b69f
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 93084b34e5795ef35e8c433f50646e5da088adfd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54600516"
---
# <a name="ltsupportedruntimegt-element"></a>&lt;supportedRuntime&gt; élément

Spécifie quelles versions du Common Language Runtime sont prises en charge par l'application. Cet élément doit être utilisé par toutes les applications créées avec la version 1.1 ou ultérieure du .NET Framework.  
  
[\<configuration>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
&nbsp;&nbsp;[\<startup>](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<supportedRuntime>**  
  
## <a name="syntax"></a>Syntaxe
  
```xml  
<supportedRuntime version="runtime version" sku="sku id"/>  
```  
  
## <a name="attributes"></a>Attributs
  
|Attribut|Description|  
|---------------|-----------------|  
|**version**|Attribut facultatif.<br /><br /> Valeur de chaîne qui spécifie la version du Common Language Runtime (CLR) prise en charge par cette application. Pour les valeurs valides de la `version` d’attribut, consultez le [les valeurs de « version du runtime »](#version) section. **Remarque :**  Via le .NET Framework 3.5, le «*version du runtime*» valeur prend la forme *majeure*. *mineure*. *build*. Depuis [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], seuls les numéros de version principale et secondaire sont nécessaires (c'est-à-dire "v4.0" au lieu de "v4.0.30319"). La chaîne courte est recommandée.|  
|**sku**|Attribut facultatif.<br /><br /> Valeur de chaîne qui spécifie la référence (SKU), qui à son tour spécifie quelle version du .NET Framework cette application prend en charge.<br /><br /> À compter du .NET Framework 4.0, l’utilisation de l’attribut `sku` est recommandée.  Quand il est présent, il indique la version du .NET Framework ciblée par l’application.<br /><br /> Pour obtenir des valeurs valides de l’attribut de référence (SKU), consultez le [les valeurs « id de référence (SKU) »](#sku) section.|  
  
## <a name="remarks"></a>Notes

Si le  **\<supportedRuntime >** élément n’est pas présent dans le fichier de configuration d’application, la version du runtime utilisée pour générer l’application est utilisée.  

Le  **\<supportedRuntime >** élément doit être utilisé par toutes les applications générées à l’aide de la version 1.1 ou ultérieure du runtime. Les applications générées pour prendre en charge uniquement la version 1.0 du runtime doivent utiliser le [ \<requiredRuntime >](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md) élément.  
  
> [!NOTE]
>  Si vous utilisez le [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md) de fonction pour spécifier le fichier de configuration, vous devez utiliser le `<requiredRuntime>` élément pour toutes les versions du runtime. Le `<supportedRuntime>` élément est ignoré lorsque vous utilisez [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md).  
  
Pour les applications prenant en charge les versions du runtime du .NET Framework 1.1 à 3.5, quand plusieurs versions du runtime sont prises en charge, le premier élément doit spécifier la version du runtime préférée en premier tandis que le dernier élément doit spécifier la version préférée en dernier. Pour les applications prenant en charge le .NET Framework 4.0 ou ultérieur, l’attribut `version` indique la version du CLR, qui est commune au .NET Framework 4 et aux versions ultérieures tandis que l’attribut `sku` indique la seule version du .NET Framework ciblée par l’application.  
  
> [!NOTE]
>  Si votre application utilise des chemins d’accès d’activation héritée, tel que le [fonction CorBindToRuntimeEx](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md), et vous souhaitez que ces chemins activent la version 4 du CLR au lieu d’une version antérieure, ou si votre application est générée avec le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]mais a une dépendance sur un assembly en mode mixte généré avec une version antérieure du .NET Framework, il n’est pas suffisant spécifier le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] dans la liste des runtimes pris en charge. En outre, dans le [ \<démarrage > élément](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) dans votre fichier de configuration, vous devez définir le `useLegacyV2RuntimeActivationPolicy` attribut `true`. Toutefois, l'affectation de la valeur `true` à cet attribut signifie que tous les composants générés avec des versions antérieures du .NET Framework sont exécutés à l'aide de [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] plutôt qu'à l'aide des runtimes avec lesquels ils ont été générés.  
  
Nous vous recommandons de tester les applications avec toutes les versions du .NET Framework sur lesquelles elles peuvent s'exécuter.  
  
<a name="version"></a>   
## <a name="runtime-version-values"></a>valeurs de "runtime version"  
Le `runtime` attribut spécifie la version du Common Language Runtime (CLR) qui est requise pour une application donnée. Notez que toutes les versions de .NET Framework 4.x spécifient le `v4.0` CLR. Le tableau suivant répertorie les valeurs valides pour le *version du runtime* valeur de la `version` attribut.  

|Version du .NET Framework|Attribut `version`|  
|----------------------------|-------------------------|  
|1.0|"v1.0.3705"|  
|1.1|"v1.1.4322"|  
|2.0|"v2.0.50727"|  
|3.0|"v2.0.50727"|  
|3.5|"v2.0.50727"|  
|4.0-4.7.2|"v4.0"|  

<a name="sku"></a>   
## <a name="sku-id-values"></a>valeurs de "sku id"

Le `sku` attribut utilise un moniker du framework cible (TFM) pour indiquer la version du .NET Framework que l’application cible et nécessaires à l’exécution. Le tableau suivant répertorie les valeurs valides sont pris en charge par le `sku` attribut, en commençant par le .NET Framework 4.
  
|Version du .NET Framework|Attribut `sku`|  
|----------------------------|---------------------|  
|4.0|".NETFramework,Version=v4.0"|  
|4.0, Client Profile|".NETFramework,Version=v4.0,Profile=Client"|  
|4.0, Platform Update 1|".NETFramework,Version=v4.0.1"|  
|4.0, Client Profile, Update 1|". NETFramework, Version = v4.0.1, profil = Client »|  
|4.0, Platform Update 2|".NETFramework,Version=v4.0.2"|  
|4.0, Client Profile, Update 2|". NETFramework, Version = version 4.0.2, profil = Client »|  
|4.0, Platform Update 3|".NETFramework,Version=v4.0.3"|  
|4.0, Client Profile, Update 3|". NETFramework, Version = verze 4.0.3, profil = Client »|  
|4.5|".NETFramework,Version=v4.5"|  
|4.5.1|".NETFramework,Version=v4.5.1"|  
|4.5.2|".NETFramework,Version=v4.5.2"|  
|4.6|".NETFramework,Version=v4.6"|  
|4.6.1|".NETFramework,Version=v4.6.1"|  
|4.6.2|". NETFramework, Version = v4.6.2 »|  
|4.7|". NETFramework, Version = v4.7 »|
|4.7.1|". NETFramework, Version = v4.7.1 »|
|4.7.2|". NETFramework, Version = v4.7.2 »|

## <a name="example"></a>Exemple  
 L’exemple suivant montre comment spécifier la version du runtime prise en charge dans un fichier de configuration. Le fichier de configuration indique que l’application cible le .NET Framework 4.7.  
  
```xml  
<configuration>  
   <startup>  
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7" />  
   </startup>  
</configuration>  
```  
  
## <a name="configuration-file"></a>fichier de configuration

Cet élément peut être utilisé dans le fichier de configuration de l'application.

## <a name="see-also"></a>Voir aussi

- [Schéma des paramètres de démarrage](../../../../../docs/framework/configure-apps/file-schema/startup/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [Exécution côte à côte in-process](../../../../../docs/framework/deployment/in-process-side-by-side-execution.md)
