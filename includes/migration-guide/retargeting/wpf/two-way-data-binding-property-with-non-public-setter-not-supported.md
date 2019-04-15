---
ms.openlocfilehash: a70aca33d0830f3b23ff985f17c469cb7c4ff35c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234722"
---
### <a name="two-way-data-binding-to-a-property-with-a-non-public-setter-is-not-supported"></a>La liaison de données bidirectionnelle avec une propriété ayant un accesseur Set non public n’est pas prise en charge

|   |   |
|---|---|
|Détails|La liaison de données avec une propriété sans accesseur Set public n’a jamais été prise en charge. À compter de .NET Framework 4.5.1, ce scénario lève une exception <xref:System.InvalidOperationException?displayProperty=name>. Notez que cette nouvelle exception sera levée uniquement pour les applications qui ciblent spécifiquement le .NET Framework 4.5.1. Si une application cible le .NET Framework 4.5, l’appel sera autorisé. Si l’application ne cible pas une version particulière du .NET Framework, la liaison sera traitée comme étant unidirectionnelle.|
|Suggestion|L’application doit être mise à jour pour utiliser une liaison unidirectionnelle ou exposer publiquement l’accesseur Set de la propriété. Vous pouvez également cibler le .NET Framework 4.5 pour obtenir l’ancien comportement de l’application.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType></li></ul>|
