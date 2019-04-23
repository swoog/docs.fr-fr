---
ms.openlocfilehash: 9ec5fa379556dedeaa7a35e34f004340ab47a39c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59234369"
---
### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>L’appel de CreateDefaultAuthorizationContext avec un argument null a été modifié

|   |   |
|---|---|
|Détails|L’implémentation de la valeur <xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name> retournée par un appel à <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name> avec un argument authorizationPolicies null est maintenant différente dans .NET Framework 4.6.|
|Suggestion|Dans de rares cas, les applications WCF qui utilisent l'authentification personnalisée peuvent voir les différences de comportement. Dans ce cas, vous pouvez restaurer l’ancien comportement de deux manières :<ol><li>Recompiler l'application pour cibler une version antérieure du .NET Framework autre que 4.6. Pour les services hébergés dans IIS, utilisez l’élément &lt;httpRuntime targetFramework=&quot;x.x&quot; /&gt; pour cibler une version antérieure du .NET Framework.</li><li>Ajoutez la ligne suivante à la section <code>&lt;appSettings&gt;</code> de votre fichier app.config : <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code></li></ol>|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|
