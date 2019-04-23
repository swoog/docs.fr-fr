---
title: Élément <listeners> pour <trace>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners
helpviewer_keywords:
- <listeners> element
- listeners element
ms.assetid: 1394c2c3-6304-46db-87c1-8e8b16f5ad5b
ms.openlocfilehash: f9f12d9e61e2472b897169727bbb4fbf9833efd6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59179112"
---
# <a name="listeners-element-for-trace"></a>\<écouteurs >, élément pour \<trace >
Spécifie un écouteur qui collecte, stocke et achemine les messages. Les écouteurs dirigent la sortie de traçage vers une cible appropriée.  
  
 \<configuration > élément  
\<System.Diagnostics > élément  
\<trace > élément  
\<écouteurs >, élément pour \<trace >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<listeners>   
  <add>...</add>  
  <clear/>  
  <remove ... />  
</listeners>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/add-element-for-listeners-for-trace.md)|Ajoute un écouteur à la collection `Listeners`.|  
|[\<clear>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/clear-element-for-listeners-for-trace.md)|Efface la collection `Listeners` de la trace.|  
|[\<remove>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/remove-element-for-listeners-for-trace.md)|Supprime un écouteur de la `Listeners` collection.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`system.diagnostics`|Spécifie l'élément racine de la section de configuration ASP.NET.|  
|`trace`|Contient les écouteurs qui collectent, stockent et acheminent les messages de traçage.|  
  
## <a name="remarks"></a>Notes  
 Le <xref:System.Diagnostics.Debug> et <xref:System.Diagnostics.Trace> classes partagent le même **écouteurs** collection. Si vous ajoutez un objet écouteur à la collection dans un de ces classes, l’autre classe utilise le même écouteur. Les classes de l’écouteur fournis avec le .NET Framework dérivent la <xref:System.Diagnostics.TraceListener> classe.  
  
## <a name="configuration-file"></a>Fichier de configuration  
 Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le  **\<écouteurs >** élément pour ajouter les écouteurs `MyListener` et `MyEventListener` à la **écouteurs** collection. `MyListener` Crée un fichier appelé `MyListener.log` et écrit la sortie dans le fichier. `MyEventListener` Crée une entrée dans le journal des événements.  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="true" indentsize="0">  
      <listeners>  
        <add name="myListener"   
          type="System.Diagnostics.TextWriterTraceListener,   
            system, version=1.0.3300.0, Culture=neutral,   
            PublicKeyToken=b77a5c561934e089"   
          initializeData="c:\myListener.log" />  
        <add name="MyEventListener"  
          type="System.Diagnostics.EventLogTraceListener,   
            system, version=1.0.3300.0, Culture=neutral,   
            PublicKeyToken=b77a5c561934e089"  
          initializeData="MyConfigEventLog"/>  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Diagnostics.TraceListener>
- [Schéma des paramètres de trace et de débogage](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
