---
title: <add>, élément de <sharedListeners>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners/add
helpviewer_keywords:
- initializeData attribute
- <add> element for <sharedListeners>
- add element for <sharedListeners>
ms.assetid: 1595e1bc-2492-421f-8384-7f382eb8eb57
ms.openlocfilehash: cbce115c6a485c5642a60528614480324e3e5665
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274017"
---
# <a name="add-element-for-sharedlisteners"></a>\<Ajouter > élément pour \<sharedListeners >
Ajoute un écouteur à la collection `sharedListeners`. `sharedListeners` est une collection d’écouteurs que tout [ \<source >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) ou [ \<trace >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md) peut faire référence.  Par défaut, les écouteurs dans le `sharedListeners` collection ne sont pas placées dans un `Listeners` collection. Ils doivent être ajoutés par un nom pour le [ \<source >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) ou [ \<trace >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md). Il n’est pas possible d’obtenir les écouteurs de la `sharedListeners` collection dans le code en cours d’exécution.  
  
 \<configuration>  
&nbsp;&nbsp;\<system.diagnostics>  
&nbsp;&nbsp;&nbsp;&nbsp;\<sharedListeners > élément  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<add name="name"   
  type="TraceListenerClassName, Version, Culture, PublicKeyToken"  
  initializeData="data"
  traceOutputOptions = "None"
/>  
```
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`name`|Attribut requis.<br /><br /> Spécifie le nom de l’écouteur est utilisé pour ajouter l’écouteur partagé à une `Listeners` collection.|  
|`type`|Attribut requis.<br /><br /> Spécifie le type de l’écouteur. Vous devez utiliser une chaîne conforme aux exigences spécifiées dans [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).|  
|`initializeData`|Attribut facultatif.<br /><br /> La chaîne passée au constructeur pour la classe spécifiée.|  
|`traceOutputOptions`|Attribut facultatif.<br/><br/>La représentation sous forme de chaîne d’un ou plusieurs <xref:System.Diagnostics.TraceOptions> membres de l’énumération qui indique les données à écrire dans la sortie de trace. Plusieurs éléments sont séparés par des virgules. La valeur par défaut est « None ».|

### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<filter>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/filter-element-for-add-for-sharedlisteners.md)|Ajoute un filtre à un écouteur dans la collection `sharedListeners`.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`system.diagnostics`|Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.|  
|`sharedListeners`|Une collection d’écouteurs de n’importe quel élément trace ou une source peut faire référence.|  
  
## <a name="remarks"></a>Notes  
 Les classes de l’écouteur fournis avec le .NET Framework dérivent la <xref:System.Diagnostics.TraceListener> classe. La valeur de la `name` attribut est utilisé pour ajouter l’écouteur partagé à une `Listeners` collection pour une trace ou une source de suivi. La valeur de la `initializeData` attribut varie selon le type d’écouteur que vous créez. Pas tous les écouteurs de trace nécessitent que vous spécifiez `initializeData`.  
  
> [!NOTE]
>  Lorsque vous utilisez le `initializeData` attribut, vous risquez d’obtenir le compilateur Avertissement : « l’attribut 'initializeData' n’est pas déclaré. ». Cet avertissement se produit parce que les paramètres de configuration sont validés par rapport à la classe de base abstraite <xref:System.Diagnostics.TraceListener>, qui ne reconnaît pas le `initializeData` attribut. En règle générale, vous pouvez ignorer cet avertissement pour les implémentations d’écouteur de trace qui ont un constructeur qui accepte un paramètre.  
  
 Le tableau suivant présente les écouteurs de trace qui sont inclus avec le .NET Framework et décrit la valeur de leur `initializeData` attributs.  
  
|Classe d’écouteur de trace|valeur de l’attribut initializeData|  
|--------------------------|------------------------------------|  
|<xref:System.Diagnostics.ConsoleTraceListener>|Le `useErrorStream` valeur pour le <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructeur.  Définir le `initializeData` l’attribut «`true`« écrire trace et debug de sortie pour le flux d’erreurs standard ; affectez-lui la valeur »`false`» à écrire dans le flux de sortie standard.|  
|<xref:System.Diagnostics.DelimitedListTraceListener>|Le nom du fichier le <xref:System.Diagnostics.DelimitedListTraceListener> écrit dans.|  
|<xref:System.Diagnostics.EventLogTraceListener?displayProperty=nameWithType>|Le nom d’une source existante de journal des événements.|  
|<xref:System.Diagnostics.EventSchemaTraceListener?displayProperty=nameWithType>|Le nom du fichier qui le <xref:System.Diagnostics.EventSchemaTraceListener> écrit dans.|  
|<xref:System.Diagnostics.TextWriterTraceListener?displayProperty=nameWithType>|Le nom du fichier qui le <xref:System.Diagnostics.TextWriterTraceListener> écrit dans.|  
|<xref:System.Diagnostics.XmlWriterTraceListener>|Le nom du fichier qui le <xref:System.Diagnostics.XmlWriterTraceListener> écrit dans.|  
  
## <a name="configuration-file"></a>Fichier de configuration  
 Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser `<add>` éléments à ajouter le <xref:System.Diagnostics.TextWriterTraceListener> `textListener` à la `sharedListeners` collection.   `textListener` est ajouté par nom à la `Listeners` collection pour la source de suivi `TraceSourceApp`. Le `textListener` écouteur écrit la sortie de trace dans le fichier myListener.log.  
  
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
- <xref:System.Diagnostics.TraceSource>
- <xref:System.Diagnostics.TraceListener>
- [Schéma des paramètres de trace et de débogage](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [Écouteurs de suivi](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
