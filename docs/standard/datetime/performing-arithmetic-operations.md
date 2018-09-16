---
title: Exécution d’opérations arithmétiques avec des dates et heures
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- times [.NET Framework], arithmetic operations
- dates [.NET Framework], arithmetic operations
- time zones [.NET Framework], arithmetic operations
- arithmetic operations [.NET Framework], dates and times
- dates [.NET Framework], comparing
- DateTime structure, arithmetic operations
- DateTimeOffset structure, arithmetic operations
ms.assetid: 87c7ddf2-f15e-48af-8602-b3642237e6d0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c2a50823b812541786cf1bebfd6b1262ce2e9314
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45669014"
---
# <a name="performing-arithmetic-operations-with-dates-and-times"></a>Exécution d’opérations arithmétiques avec des dates et heures

Bien qu’à la fois le <xref:System.DateTime> et <xref:System.DateTimeOffset> structures fournissent des membres qui effectuent des opérations arithmétiques sur leurs valeurs, les résultats des opérations arithmétiques sont très différents. Cette rubrique examine ces différences, concerne les degrés de fuseaux horaires dans les données de date et d’heure et explique comment effectuer entièrement fuseau horaire prenant en charge les opérations en utilisant les données de date et d’heure.

## <a name="comparisons-and-arithmetic-operations-with-datetime-values"></a>Comparaisons et opérations arithmétiques avec des valeurs DateTime

Le <xref:System.DateTime.Kind%2A?displayProperty=nameWithType> propriété permet à un <xref:System.DateTimeKind> valeur à assigner à la date et l’heure pour indiquer si elle représente l’heure locale, temps universel coordonné (UTC) ou l’heure dans un fuseau horaire non spécifié. Toutefois, ces informations limitées de fuseau horaire sont ignorées lors de la comparaison ou l’exécution de date et heure arithmétique sur <xref:System.DateTimeKind> valeurs. Ceci est illustré dans l’exemple suivant, qui compare l’heure locale actuelle à l’heure UTC actuelle.

[!code-csharp[System.DateTimeOffset.Conceptual#2](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/cs/Conceptual2.cs#2)]
[!code-vb[System.DateTimeOffset.Conceptual#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/vb/Conceptual2.vb#2)]

Le <xref:System.DateTime.CompareTo%28System.DateTime%29> méthode signale que l’heure locale est antérieure à (ou inférieur à) l’heure UTC et l’opération de soustraction indique que la différence entre l’heure UTC et l’heure locale pour un système dans le fuseau horaire du Pacifique est de sept heures. Toutefois, comme ces deux valeurs donnent des représentations différentes d’un même point dans le temps, il apparaît clairement dans ce cas que cet intervalle de temps est totalement attribuable au décalage du fuseau horaire local par rapport à l’heure UTC.

En règle générale, le <xref:System.DateTime.Kind%2A?displayProperty=nameWithType> propriété n’affecte pas les résultats retournés par <xref:System.DateTime.Kind> les méthodes de comparaison et d’arithmétique (comme la comparaison de deux points identiques dans le temps indique), mais elle peut affecter l’interprétation de ces résultats. Exemple :

* Le résultat de toute opération arithmétique exécutée sur deux valeurs de date et d’heure dont la propriété <xref:System.DateTime.Kind%2A?displayProperty=nameWithType> égale à deux propriétés <xref:System.DateTimeKind> reflète l’intervalle de temps réel entre les deux valeurs. De même, la comparaison de deux valeurs de date et d’heure de ce type indique précisément la relation entre les heures.

* Le résultat de toutes les opérations arithmétiques ou de comparaison exécutée sur deux valeurs de date et d’heure dont la propriété <xref:System.DateTime.Kind%2A?displayProperty=nameWithType> égale à deux propriétés <xref:System.DateTimeKind> ou sur deux valeurs de date et d’heure avec différents <xref:System.DateTime.Kind%2A?displayProperty=nameWithType> valeurs de propriété reflète la différence de l’horloge entre les deux valeurs.

* Les opérations arithmétiques ou de comparaison sur des valeurs de date et d’heure locales ne prennent pas en compte le fait qu’une valeur particulière soit ambiguë ou non valide, ni l’incidence de règles d’ajustement quelconques résultant du passage du fuseau horaire local à l’heure d’été ou à l’heure d’hiver.

* Toute opération qui compare ou calcule la différence entre l’heure UTC et une heure locale inclut dans le résultat un intervalle de temps égal au décalage du fuseau horaire local par rapport à l’heure UTC.

* Toute opération qui compare ou calcule la différence entre une heure non spécifiée et l’heure UTC ou l’heure locale reflète le temps horloge simple. Les décalages entre les fuseaux horaires ne sont pas pris en compte et le résultat ne reflète pas l’application des règles d’ajustement des fuseaux horaires.

* Toute opération qui compare ou calcule la différence entre deux heures non spécifiées peut inclure un intervalle inconnu qui reflète la différence d’heure entre deux fuseaux horaires différents.

Il existe plusieurs scénarios dans quel fuseau horaire différences n’affectent pas les calculs de date et d’heure (pour une présentation de certains d'entre eux, consultez [choix entre DateTime, DateTimeOffset, TimeSpan et TimeZoneInfo](../../../docs/standard/datetime/choosing-between-datetime.md)) ou dans lequel le contexte de la date et l’heure données définissent la signification des opérations de comparaison ou arithmétique.

## <a name="comparisons-and-arithmetic-operations-with-datetimeoffset-values"></a>Comparaisons et opérations arithmétiques avec des valeurs DateTimeOffset

Un <xref:System.DateTimeOffset> valeur inclut non seulement une date et une heure, mais également un décalage qui définit clairement cette date et cette heure par rapport à l’heure UTC. Cela permet de définir une égalité quelque peu différemment pour <xref:System.DateTimeOffset> valeurs. Tandis que <xref:System.DateTime> valeurs sont égales si elles ont la même date et heure, <xref:System.DateTimeOffset> valeurs sont égales si toutes deux font référence au même point dans le temps. Cela rend une <xref:System.DateTimeOffset> valeur plus précise et nécessite moins d’interprétation lorsqu’il est utilisé dans les comparaisons et dans la plupart des opérations arithmétiques qui déterminent l’intervalle entre deux dates et heures. L’exemple suivant, qui est la <xref:System.DateTimeOffset> équivalent à l’exemple précédent qui comparée local et l’heure UTC <xref:System.DateTimeOffset> valeurs, illustre cette différence de comportement.

[!code-csharp[System.DateTimeOffset.Conceptual#3](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/cs/Conceptual3.cs#3)]
[!code-vb[System.DateTimeOffset.Conceptual#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/vb/Conceptual3.vb#3)]

Dans cet exemple, le <xref:System.DateTimeOffset.CompareTo%2A> méthode indique que l’heure locale actuelle et l’heure UTC actuelle sont égales et la soustraction de <xref:System.DateTimeOffset.CompareTo(System.DateTimeOffset)> valeurs indique que la différence entre les deux heures est <xref:System.TimeSpan.Zero?displayProperty=nameWithType>.

La limitation en chef de l’utilisation de <xref:System.DateTimeOffset> valeurs date / heure arithmétique est que, bien que <xref:System.DateTimeOffset> valeurs ont certains fuseaux horaires, ils ne sont pas entièrement fuseau horaire prenant en charge. Bien que le <xref:System.DateTimeOffset> reflète le décalage de la du valeur décalage d’un fuseau horaire à l’heure UTC lorsqu’une <xref:System.DateTimeOffset> variable est d’abord affectée une valeur, il se dissocie par la suite du fuseau horaire. Comme il n’est plus directement associé à une heure identifiable, l’addition et la soustraction d’intervalles de dates et d’heures ne prennent pas en compte les règles d’ajustement des fuseaux horaires.

Pour illustrer cela, la passage à l’heure d’été dans le fuseau horaire du Centre (États-Unis) se produit à 2:00, le 9 mars 2008. Cela signifie que l’ajout d’un intervalle de deux heures trente à l’heure de 1:30 dans le fuseau horaire du Centre des États-Unis, le 9 mars 2008, doit avoir pour résultat 5:00, le 9 mars 2008. Toutefois, comme le montre l’exemple suivant, le résultat de l’addition est 4:00, le 9 mars 2008. Notez que le résultat de cette opération représente l’heure correcte, même s’il ne s’agit pas de l’heure dans le fuseau horaire qui nous intéresse (autrement dit, elle n’a pas le décalage horaire attendu).

[!code-csharp[System.DateTimeOffset.Conceptual#4](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/cs/Conceptual4.cs#4)]
[!code-vb[System.DateTimeOffset.Conceptual#4](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/vb/Conceptual4.vb#4)]

## <a name="arithmetic-operations-with-times-in-time-zones"></a>Opérations arithmétiques avec des heures dans des fuseaux horaires

Le <xref:System.TimeZoneInfo> classe inclut plusieurs méthodes de conversion qui appliquent automatiquement des ajustements lorsqu’elles convertissent des heures d’un fuseau horaire à un autre. Notamment :

* Le <xref:System.TimeZoneInfo.ConvertTime%2A> et <xref:System.TimeZoneInfo.ConvertTimeBySystemTimeZoneId%2A> méthodes qui convertissent des heures entre deux fuseaux horaires quelconques.

* Le <xref:System.TimeZoneInfo.ConvertTimeFromUtc%2A> et <xref:System.TimeZoneInfo.ConvertTimeToUtc%2A> méthodes qui convertissent l’heure d’un fuseau horaire particulier en heure UTC, ou convertissent l’heure UTC en heure d’un fuseau horaire particulier.

Pour plus d’informations, consultez [conversion d’heures entre fuseaux horaires](../../../docs/standard/datetime/converting-between-time-zones.md).

Le <xref:System.TimeZoneInfo.ConvertTimeToUtc(System.DateTime)> classe ne fournit pas de méthodes qui appliquent automatiquement des règles d’ajustement lorsque vous effectuez la date et l’heure arithmétique. Toutefois, vous pouvez convertir l’heure d’un fuseau horaire en heure UTC, effectuer l’opération arithmétique, puis reconvertir l’heure UTC dans l’heure du fuseau horaire. Pour plus d’informations, consultez [Comment : utiliser des fuseaux horaires dans les date et heure arithmétique](../../../docs/standard/datetime/use-time-zones-in-arithmetic.md).

Par exemple, le code suivant est semblable au code précédent qui ajoutait deux heures trente à 2:00, le 9 mars 2008. Toutefois, comme il convertit l’heure du Centre des États-Unis en heure UTC avant d’effectuer les opérations arithmétiques de date et d’heure, puis reconvertit le résultat UTC en heure du Centre, l’heure résultante reflète le passage du fuseau horaire du Centre des États-Unis à l’heure d’été.

[!code-csharp[System.DateTimeOffset.Conceptual#5](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/cs/Conceptual5.cs#5)]
[!code-vb[System.DateTimeOffset.Conceptual#5](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/vb/Conceptual5.vb#5)]

## <a name="see-also"></a>Voir aussi

* [Dates, heures et fuseaux horaires](../../../docs/standard/datetime/index.md)
* [Guide pratique pour utiliser des fuseaux horaires dans des opérations arithmétiques de date et d’heure](../../../docs/standard/datetime/use-time-zones-in-arithmetic.md)
