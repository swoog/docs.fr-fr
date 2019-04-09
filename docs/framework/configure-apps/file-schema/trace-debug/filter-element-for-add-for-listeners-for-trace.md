---
title: <filter> Élément pour <add> pour <listeners> pour <trace>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/add/filter
helpviewer_keywords:
- initializeData attribute
- filter element for <add> for <listeners> for <trace>
- <filter> element for <add> for <listeners> for <trace>
ms.assetid: eb9c18f5-dfa8-47c5-b91b-e4b93e76e1cc
ms.openlocfilehash: 5961125e1b8d0d0f5711f8b942b68ba71d61888f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59143427"
---
# <a name="filter-element-for-add-for-listeners-for-trace"></a>\<Filtre >, élément pour \<Ajouter > pour \<écouteurs > pour \<trace >
Ajoute un filtre à un écouteur dans la `Listeners` collection pour une trace.  
  
 \<configuration>  
\<system.diagnostics>  
\<trace>  
\<listeners>  
\<add>  
\<filter>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<filter   
  type="traceFilterClassName"   
  initializeData="data" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`type`|Attribut requis.<br /><br /> Spécifie le type du filtre, qui doit hériter la <xref:System.Diagnostics.TraceFilter> classe. Vous pouvez utiliser le nom qualifié d’espace de noms du type, qui correspond à du type <xref:System.Type.FullName%2A> propriété, ou vous pouvez utiliser le nom de type qualifié complet, y compris les informations d’assembly, qui correspondant à la <xref:System.Type.AssemblyQualifiedName%2A> propriété. Pour plus d’informations sur les noms de types qualifiés complets, consultez [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).|  
|`initializeData`|Attribut facultatif.<br /><br /> La chaîne passée au constructeur pour la classe de filtre spécifié.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`system.diagnostics`|Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.|  
|`trace`|Contient les écouteurs qui collectent, stockent et acheminent les messages de traçage.|  
|`listeners`|Contient des écouteurs qui collectent, stockent et acheminent les messages. Les écouteurs dirigent la sortie de traçage vers une cible appropriée.|  
|`add`|Ajoute un écouteur à la collection `Listeners`.|  
  
## <a name="remarks"></a>Notes  
 Le `<filter>` élément doit être contenu dans un `<add>` élément pour un écouteur de trace qui spécifie le type de l’écouteur, pas seulement le nom d’un écouteur défini dans un [ \<sharedListeners >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md). Si l’écouteur est défini dans un [ \<sharedListeners >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md), le filtre de cet écouteur doit être défini dans cet élément.  
  
 Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le `<filter>` élément pour ajouter un filtre à l’écouteur `console` dans le `Listeners` collection de la trace, en spécifiant le niveau d’événement de filtre en tant que `Error`.  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="false" indentsize="4">  
      <listeners>  
        <add name="console"   
          type="System.Diagnostics.ConsoleTraceListener" >  
          <filter type="System.Diagnostics.EventTypeFilter"   
            initializeData="Error" />  
        </add>  
        <remove name="Default" />  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Diagnostics.Trace>
- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.TraceListener.Filter%2A?displayProperty=nameWithType>
- <xref:System.Diagnostics.TraceFilter>
- [Schéma des paramètres de traçage et de débogage](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
