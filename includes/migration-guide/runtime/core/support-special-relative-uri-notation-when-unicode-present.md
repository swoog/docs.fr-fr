---
ms.openlocfilehash: 34d7395e72f6ef252ac68366bcd346cd8d464036
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59236125"
---
### <a name="support-special-relative-uri-notation-when-unicode-is-present"></a>Prise en charge d’une notation d’URI relatif spéciale quand des caractères Unicode sont présents

|   |   |
|---|---|
|Détails|<xref:System.Uri> ne lève plus une <xref:System.NullReferenceException> quand il appelle <xref:System.Uri.TryCreate%2A> sur certains URI relatifs contenant des caractères Unicode. La reproduction la plus simple du <xref:System.NullReferenceException> est indiquée ci-dessous, où les deux instructions sont équivalentes :<pre><code class="lang-csharp">bool success = Uri.TryCreate(&quot;http:%C3%A8&quot;, UriKind.RelativeOrAbsolute, out Uri href);&#13;&#10;bool success = Uri.TryCreate(&quot;http:&#232;&quot;, UriKind.RelativeOrAbsolute, out Uri href);&#13;&#10;</code></pre><xref:System.NullReferenceException> ne peut être reproduite que si les conditions suivantes sont réunies :<ul><li>Vous devez spécifier l’URI comme étant relatif en le faisant précéder de « http: » sans le faire suivre de « // ».</li><li>L’URI doit contenir des symboles non réservés ou Unicode encodés en pourcentage.</li></ul>|
|Suggestion|Les utilisateurs qui dépendent de ce comportement pour interdire les URI relatifs doivent spécifier <xref:System.UriKind.Absolute?displayProperty=nameWithType> à la place quand ils créent un URI.|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Uri.TryCreate(System.Uri,System.Uri,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.String,System.UriKind,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.String,System.Uri@)?displayProperty=nameWithType></li></ul>|
