---
ms.openlocfilehash: ac929a8b3e9a7d56122f5699c51819ad483d1f5e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235301"
---
### <a name="binaryformatter-can-fail-to-find-type-from-loadfrom-context"></a>BinaryFormatter peut ne pas parvenir à trouver le type dans le contexte LoadFrom

|   |   |
|---|---|
|Détails|Depuis .NET Framework 4.5, un certain nombre de modifications de <xref:System.Xml.Serialization.XmlSerializer?displayProperty=name> peuvent entraîner des différences de désérialisation quand vous utilisez <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> pour désérialiser des types qui avaient été chargés dans le contexte LoadFrom. Ces modifications sont dues aux nouvelles façons dont <xref:System.Xml.Serialization.XmlSerializer?displayProperty=name> charge maintenant un type qui provoque un comportement différent quand un <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> tente plus tard une désérialisation en ce type. Le binder de sérialisation par défaut n’effectue pas automatiquement des recherches dans le contexte LoadFrom, bien qu’il ait pu fonctionner dans certains cas en fonction de l’ancien comportement de XmlSerializer. En raison des modifications, quand un type est chargé à partir d’un assembly chargé dans un contexte différent, une <xref:System.IO.FileNotFoundException?displayProperty=name> peut être levée.|
|Suggestion|Si cette exception se produit, la propriété <code>Binder</code> de <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> peut être définie sur un binder personnalisé qui va rechercher le type approprié.<pre><code class="lang-csharp">var formatter = new BinaryFormatter { Binder = new TypeFinderBinder() }&#13;&#10;</code></pre>Puis le binder personnalisé :<pre><code class="lang-csharp">public class TypeFinderBinder : SerializationBinder&#13;&#10;{&#13;&#10;private static readonly string s_assemblyName = Assembly.GetExecutingAssembly().FullName;&#13;&#10;&#13;&#10;public override Type BindToType(string assemblyName, string typeName)&#13;&#10;{&#13;&#10;return Type.GetType(String.Format(CultureInfo.InvariantCulture, &quot;{0}, {1}&quot;, typeName, s_assemblyName));&#13;&#10;}&#13;&#10;}&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|
