---
title: '&lt;ajouter&gt; élément pour &lt;écouteurs&gt; pour &lt;source&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/add
helpviewer_keywords:
- initializeData attribute
- add element for <listeners> for <source>
- <add> element for <listeners> for <source>
ms.assetid: 4ce36ac1-81ef-48e8-b8b2-b5a5b0e2adcb
author: mcleblanc
ms.author: markl
ms.openlocfilehash: c0ab15f6eca8b20653530583016eb849273c4ce1
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47216862"
---
# <a name="ltaddgt-element-for-ltlistenersgt-for-ltsourcegt"></a>&lt;ajouter&gt; élément pour &lt;écouteurs&gt; pour &lt;source&gt;
Ajoute un écouteur à la collection `Listeners` pour une source de trace.  
  
 \<configuration>  
\<System.Diagnostics >  
\<sources >  
\<source >  
\<écouteurs >  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<add name="name"   
  type="TraceListenerClassName, Version, Culture, PublicKeyToken"  
  initializeData="data"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`type`|Attribut, requis, sauf si vous référencez un écouteur dans la `sharedListeners` regroupement, dans lequel cas vous suffit de faire référence par nom (voir la [exemple](#example)).<br /><br /> Spécifie le type de l’écouteur. Vous devez utiliser une chaîne conforme aux exigences spécifiées dans [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).|  
|`initializeData`|Attribut facultatif.<br /><br /> La chaîne passée au constructeur pour la classe spécifiée. Un <xref:System.Configuration.ConfigurationException> est levée si la classe n’a pas de constructeur qui accepte une chaîne.|  
|`name`|Attribut facultatif.<br /><br /> Spécifie le nom de l’écouteur.|  
|`traceOutputOptions`|Attribut facultatif.<br /><br /> Spécifie le <xref:System.Diagnostics.TraceListener.TraceOutputOptions%2A> valeur de propriété pour l’écouteur de suivi.|  
|[attributs personnalisés]|Attributs facultatifs.<br /><br /> Spécifie la valeur pour les attributs spécifiques à l’écouteur identifiés par la <xref:System.Diagnostics.TraceListener.GetSupportedAttributes%2A> méthode pour cet écouteur. <xref:System.Diagnostics.DelimitedListTraceListener.Delimiter%2A> est un exemple d’attribut supplémentaire unique à la <xref:System.Diagnostics.DelimitedListTraceListener> classe.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<filter>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/filter-element-for-add-for-listeners-for-source.md)|Ajoute un filtre à un écouteur dans la collection `Listeners` pour une source de trace.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`system.diagnostics`|Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.|  
|`sources`|Contient les sources de trace qui lancent des messages de traçage.|  
|`source`|Spécifie une source de trace qui lance des messages de traçage.|  
|`listeners`|Spécifie des écouteurs qui collectent, stockent et acheminent les messages.|  
  
## <a name="remarks"></a>Notes  
 Les classes de l’écouteur fournis avec le .NET Framework dérivent la <xref:System.Diagnostics.TraceListener> classe.  
  
 Si vous ne spécifiez pas le `name` attribut de l’écouteur de suivi, le <xref:System.Diagnostics.TraceListener.Name%2A> propriété de l’écouteur de trace par défaut est une chaîne vide (« »). Si votre application comporte un seul écouteur, vous pouvez l’ajouter sans spécifier de nom, et vous pouvez le supprimer en spécifiant une chaîne vide pour le nom. Toutefois, si votre application a plusieurs écouteurs, vous devez spécifier un nom unique pour chaque écouteur de trace, qui vous permet d’identifier et de gérer des écouteurs de trace individuels dans le <xref:System.Diagnostics.TraceSource.Listeners%2A?displayProperty=nameWithType> collection.  
  
> [!NOTE]
>  Ajout de plusieurs écouteurs de trace du même type et avec le même nommez entraîne l’écouteur de suivi qu’un seul de ce type et ajouté à la `Listeners` collection. Toutefois, vous pouvez ajouter par programmation plusieurs écouteurs identiques à la `Listeners` collection.  
  
 La valeur de la `initializeData` attribut varie selon le type d’écouteur que vous créez. Pas tous les écouteurs de trace nécessitent que vous spécifiez `initializeData`.  
  
> [!NOTE]
>  Lorsque vous utilisez le `initializeData` attribut, vous risquez d’obtenir le compilateur Avertissement : « l’attribut 'initializeData' n’est pas déclaré. ». Cet avertissement se produit parce que les paramètres de configuration sont validés par rapport à la classe de base abstraite <xref:System.Diagnostics.TraceListener>, qui ne reconnaît pas le `initializeData` attribut. En règle générale, vous pouvez ignorer cet avertissement pour les implémentations d’écouteur de trace qui ont un constructeur qui accepte un paramètre.  
  
 Le tableau suivant présente les écouteurs de trace qui sont inclus avec le .NET Framework et décrit la valeur de leur `initializeData` attributs.  
  
|Classe d’écouteur de trace|valeur de l’attribut initializeData|  
|--------------------------|------------------------------------|  
|<xref:System.Diagnostics.ConsoleTraceListener?displayProperty=nameWithType>|Le `useErrorStream` valeur pour le <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructeur.  Définir le `initializeData` l’attribut «`true`« écrire trace et debug de sortie pour le flux d’erreurs standard ; affectez-lui la valeur »`false`» à écrire dans le flux de sortie standard.|  
|<xref:System.Diagnostics.DelimitedListTraceListener?displayProperty=nameWithType>|Le nom du fichier le <xref:System.Diagnostics.DelimitedListTraceListener> écrit dans.|  
|<xref:System.Diagnostics.EventLogTraceListener?displayProperty=nameWithType>|Le nom d’une source existante de journal des événements.|  
|<xref:System.Diagnostics.EventSchemaTraceListener?displayProperty=nameWithType>|Le nom du fichier qui le <xref:System.Diagnostics.EventSchemaTraceListener> écrit dans.|  
|<xref:System.Diagnostics.TextWriterTraceListener?displayProperty=nameWithType>|Le nom du fichier qui le <xref:System.Diagnostics.TextWriterTraceListener> écrit dans.|  
|<xref:System.Diagnostics.XmlWriterTraceListener?displayProperty=nameWithType>|Le nom du fichier qui le <xref:System.Diagnostics.XmlWriterTraceListener> écrit dans.|  
  
## <a name="configuration-file"></a>Fichier de configuration  
 Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser `<add>` éléments à ajouter les écouteurs `console` et `textListener` à la `Listeners` collection pour la source de suivi `TraceSourceApp`. Le `textListener` écouteur écrit la sortie de trace dans le fichier myListener.log.  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"   
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
          <remove name="Default"/>  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="textListener"   
        type="System.Diagnostics.TextWriterTraceListener"   
        initializeData="myListener.log"/>  
    </sharedListeners>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Diagnostics.TraceSource>  
 <xref:System.Diagnostics.TraceListener>  
 [Schéma des paramètres de trace et de débogage](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [Écouteurs de suivi](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
