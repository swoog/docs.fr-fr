---
title: '&lt;démarrage&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup
- http://schemas.microsoft.com/.NetConfiguration/v2.0#startup
helpviewer_keywords:
- container tags, <startup> element
- <startup> element
- startup element
ms.assetid: 536acfd8-f827-452f-838a-e14fa3b87621
ms.openlocfilehash: 9fc5a555085369cdec249eb9b5b247f403bd12ed
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083715"
---
# <a name="ltstartupgt-element"></a>&lt;démarrage&gt; élément

Spécifie les informations de démarrage de common language runtime.

 \<configuration> \<startup>

## <a name="syntax"></a>Syntaxe

```xml
<startup useLegacyV2RuntimeActivationPolicy="true|false" > 
</startup>
```

## <a name="attributes-and-elements"></a>Attributs et éléments

 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.

### <a name="attributes"></a>Attributs

|Attribut|Description|
|---------------|-----------------|
|`useLegacyV2RuntimeActivationPolicy`|Attribut facultatif.<br /><br /> Spécifie s’il faut activer la [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] stratégie d’activation du runtime ou à utiliser le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] stratégie d’activation.|

## <a name="uselegacyv2runtimeactivationpolicy-attribute"></a>useLegacyV2RuntimeActivationPolicy attribute

|Value|Description|
|-----------|-----------------|
|`true`|Activer [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] stratégie d’activation du runtime pour le runtime choisi, qui consiste à lier les techniques d’activation runtime hérité (telles que la [fonction CorBindToRuntimeEx](../../../unmanaged-api/hosting/corbindtoruntimeex-function.md)) au runtime choisi dans le fichier de configuration au lieu de coupe les CLR version 2.0. Par conséquent, si la version CLR 4 ou version ultérieure est choisie dans le fichier de configuration, les assemblys en mode mixte créés avec les versions antérieures du .NET Framework sont chargés avec la version du CLR choisie. Définition de cette valeur empêche CLR version 1.1 ou CLR version 2.0 le chargement dans le même processus, en désactivant efficacement la fonctionnalité côte à côte in-process.|
|`false`|Utiliser la stratégie d’activation par défaut pour le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] et version ultérieure, qui consiste à autoriser runtime hérité techniques charger le CLR version 1.1 ou 2.0 dans le processus d’activation. Ce paramètre empêche les assemblys en mode mixte de charger dans le .NET Framework 4 ou version ultérieure, sauf si elles ont été générées avec le .NET Framework 4 ou version ultérieure. Cette valeur est la valeur par défaut.|

### <a name="child-elements"></a>Éléments enfants

|Élément|Description|
|-------------|-----------------|
|[\<requiredRuntime>](requiredruntime-element.md)|Spécifie que l’application prend en charge uniquement la version 1.0 du common language runtime. Les applications générées avec la version 1.1 ou ultérieure du runtime doivent utiliser le  **\<supportedRuntime >** élément.|
|[\<supportedRuntime>](supportedruntime-element.md)|Spécifie quelles versions du Common Language Runtime sont prises en charge par l'application.|

### <a name="parent-elements"></a>Éléments parents

|Élément|Description|
|-------------|-----------------|
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|

## <a name="remarks"></a>Notes

 Le  **\<supportedRuntime >** élément doit être utilisé par toutes les applications générées à l’aide de la version 1.1 ou ultérieure du runtime. Les applications générées pour prendre en charge uniquement la version 1.0 du runtime doivent utiliser le  **\<requiredRuntime >** élément.

 Le code de démarrage d’une application hébergée dans Microsoft Internet Explorer ignore les  **\<démarrage >** élément et ses éléments enfants.

## <a name="the-uselegacyv2runtimeactivationpolicy-attribute"></a>L’attribut useLegacyV2RuntimeActivationPolicy

 Cet attribut est utile si votre application utilise des chemins d’accès d’activation héritée, telle que la [fonction CorBindToRuntimeEx](../../../unmanaged-api/hosting/corbindtoruntimeex-function.md), et vous souhaitez que ces chemins activent la version 4 du CLR au lieu d’une version antérieure, ou si votre application est intègrent la [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] mais a une dépendance sur un assembly en mode mixte généré avec une version antérieure du .NET Framework. Dans ces scénarios, la valeur est l’attribut `true`.

> [!NOTE]
> Définition de l’attribut sur `true` empêche le chargement dans le même processus, en désactivant efficacement la fonctionnalité côte à côte in-process de CLR version 1.1 ou CLR version 2.0 (consultez [l’exécution côte à côte pour COM Interop](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)).

## <a name="example"></a>Exemple

 L’exemple suivant montre comment spécifier la version du runtime dans un fichier de configuration.

```xml
<!-- When used with version 1.0 of the .NET Framework runtime -->
<configuration>
   <startup>
      <requiredRuntime version="v1.0.3705" safemode="true"/>
   </startup>
</configuration>
<!-- When used with version 1.1 (or later) of the runtime -->
<configuration>
   <startup>
      <supportedRuntime version="v1.1.4322"/>
      <supportedRuntime version="v1.0.3705"/>
   </startup>
</configuration>
```

## <a name="see-also"></a>Voir aussi

- [Schéma des paramètres de démarrage](index.md)
- [Schéma des fichiers de configuration](../index.md)
- [Guide pratique pour configurer une application en vue de prendre en charge le .NET Framework 4 ou versions ultérieures](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)
- [Exécution côte à côte pour COM Interop](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)
- [Exécution côte à côte in-process](../../../deployment/in-process-side-by-side-execution.md)