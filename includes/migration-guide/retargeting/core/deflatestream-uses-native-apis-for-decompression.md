---
ms.openlocfilehash: 897bb0b0650c633b87a792516c62566f491ec3fd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59233979"
---
### <a name="deflatestream-uses-native-apis-for-decompression"></a>DeflateStream utilise des API natives pour la décompression

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.7.2, l’implémentation de la décompression de la classe <code>T:System.IO.Compression.DeflateStream</code> a été changée de façon à utiliser des API Windows natives par défaut. En règle générale, cela entraîne une amélioration sensible des performances. Toutes les applications .NET ciblant .NET Framework versions 4.7.2 ou ultérieures utilisent l’implémentation native. Ce changement peut entraîner certaines différences de comportement, notamment les suivantes :<ul><li>Les messages d’exception peuvent être différents. Toutefois, le type d’exception levée reste le même.</li><li>Certaines situations particulières, telles que le manque de mémoire pour effectuer une opération, peuvent être traitées différemment.</li><li>Il existe des différences connues pour l’analyse de l’en-tête gzip (remarque : seul <code>GZipStream</code> défini pour la décompression est affecté) :</li><li>Les exceptions pendant l’analyse d’en-têtes non valides peuvent être levées à des moments différents.</li><li>L’implémentation native impose que les valeurs de certains indicateurs réservés à l’intérieur de l’en-tête gzip (c’est-à-dire, [FLG](http://www.zlib.org/rfc-gzip.html#header-trailer)) soient définies en fonction de la spécification ; elle risque donc de lever une exception au lieu d’ignorer les valeurs non valides.</li></ul>|
|Suggestion|Si la décompression avec des API natives a affecté le comportement de votre application, vous pouvez refuser cette fonctionnalité en ajoutant le commutateur <code>Switch.System.IO.Compression.DoNotUseNativeZipLibraryForDecompression</code> à la section <code>runtime</code> de votre fichier app.config et en le définissant sur <code>true</code> :<pre><code class="lang-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot; ?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.IO.Compression.DoNotUseNativeZipLibraryForDecompression=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IO.Compression.DeflateStream?displayProperty=nameWithType></li><li><xref:System.IO.Compression.GZipStream?displayProperty=nameWithType></li></ul>|
