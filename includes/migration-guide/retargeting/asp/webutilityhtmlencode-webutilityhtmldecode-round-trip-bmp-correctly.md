---
ms.openlocfilehash: ca662b57fae9b1d0d41290f3052f71bca66e9bf3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234749"
---
### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode et WebUtility.HtmlDecode font un aller-retour correct au plan BMP

|   |   |
|---|---|
|Détails|Pour les applications qui ciblent .NET Framework 4.5, les caractères extérieurs au plan BMP (Basic Multilingual Plane) font un aller-retour correct quand ils sont passés à la méthode <xref:System.Net.WebUtility.HtmlDecode(System.String)>.|
|Suggestion|Ce changement ne doit avoir aucun effet sur les applications actuelles. Toutefois, pour rétablir le comportement d’origine, affectez à l’attribut <code>targetFramework</code> de l’élément <code>&lt;httpRuntime&gt;</code> la valeur d’une chaîne autre que &quot;4.5&quot;. Vous pouvez également définir les attributs <code>unicodeEncodingConformance</code> et <code>unicodeDecodingConformance</code> de l'élément de configuration <code>&lt;webUtility&gt;</code> pour contrôler ce comportement indépendamment de la version ciblée du .NET Framework.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|
