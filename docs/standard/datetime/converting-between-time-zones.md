---
title: Conversion d’heures entre fuseaux horaires
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- times [.NET Framework], converting
- time zones [.NET Framework], conversions
- UTC times, converting
- converting times
- local time conversions
ms.assetid: a51e1a3b-c983-4320-b31a-1f9fa3cf824a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0c77832a4c578ddb2c8a427b133e53ab4ab5c5e3
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45529582"
---
# <a name="converting-times-between-time-zones"></a>Conversion d’heures entre fuseaux horaires

Il devient de plus en plus important pour une application qui fonctionne avec des dates et des heures de gérer les différences entre les fuseaux horaires. Une application ne peut plus supposer que toutes les heures peut être exprimée en heure locale, qui est la durée disponible à partir de la <xref:System.DateTime> structure. Par exemple, une page web qui affiche l’heure actuelle dans la partie Est des États-Unis ne sera pas crédible pour un client d’Asie orientale. Cette rubrique explique comment convertir les heures d’un fuseau horaire à un autre, ainsi que comment convertir <xref:System.DateTimeOffset> valeurs limitée fuseaux horaires.

## <a name="converting-to-coordinated-universal-time"></a>Conversion en heure UTC

Le temps universel coordonné (UTC) est une norme d’heure atomique de haute précision. Les fuseaux horaires du monde sont exprimés comme décalages positifs ou négatifs par rapport à l’heure UTC. Par conséquent, l’heure UTC fournit une sorte d’heure neutre du point de vue des fuseaux horaires. L’utilisation de l’heure UTC est recommandée lorsque la portabilité de la date et de l’heure entre les ordinateurs est importante. (Pour plus d’informations et d’autres meilleures pratiques à l’aide de dates et heures, consultez [de codage recommandées à l’aide de DateTime dans le .NET Framework](https://msdn.microsoft.com/library/ms973825.aspx).) La conversion de fuseaux horaires individuels en heure UTC facilite les comparaisons d’heures.

> [!NOTE]
> Vous pouvez également sérialiser un <xref:System.DateTimeOffset> structure pour représenter clairement un point unique dans le temps. Étant donné que <xref:System.DateTimeOffset> objets stockent une valeur de date et d’heure, ainsi que son décalage à l’heure UTC, ils représentent toujours un point particulier dans le temps par rapport au format UTC.

Pour convertir une heure en UTC le plus simple consiste à appeler le `static` (`Shared` en Visual Basic) <xref:System.TimeZoneInfo.ConvertTimeToUtc%28System.DateTime%29?displayProperty=nameWithType> (méthode). La conversion exacte effectuée par la méthode dépend de la valeur de la `dateTime` du paramètre <xref:System.DateTime.Kind%2A> propriété, comme le tableau suivant.

| `DateTime.Kind`            | Conversion                                                                     |
| -------------------------- | ------------------------------------------------------------------------------ |
| `DateTimeKind.Local`       | Convertit l’heure locale en heure UTC.                                                    |
| `DateTimeKind.Unspecified` | Suppose que le paramètre `dateTime` est l’heure locale et convertit l’heure locale en heure UTC. |
| `DateTimeKind.Utc`         | Retourne le paramètre `dateTime` inchangé.                                    |

Le code suivant convertit l’heure locale actuelle en heure UTC et affiche le résultat dans la console.

[!code-csharp[System.TimeZone2.Concepts#6](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Concepts/CS/TimeZone2Concepts.cs#6)]
[!code-vb[System.TimeZone2.Concepts#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Concepts/VB/TimeZone2Concepts.vb#6)]

> [!NOTE]
> Le <xref:System.TimeZoneInfo.ConvertTimeToUtc%28System.DateTime%29?displayProperty=nameWithType> méthode ne produit pas nécessairement les résultats sont identiques à la <xref:System.TimeZone.ToUniversalTime%2A?displayProperty=nameWithType> et <xref:System.DateTime.ToUniversalTime%2A?displayProperty=nameWithType> méthodes. Si le système hôte local de l’horaire inclut plusieurs règles d’ajustement, <xref:System.TimeZoneInfo.ConvertTimeToUtc%28System.DateTime%29?displayProperty=nameWithType> s’applique la règle appropriée à une date et heure particulière. Les deux autres méthodes appliquent toujours la dernière règle d’ajustement.

Si la valeur de date et d’heure ne représente pas l’heure locale ou UTC, la <xref:System.DateTime.ToUniversalTime%2A> méthode probablement retourne un résultat erroné. Toutefois, vous pouvez utiliser la <xref:System.TimeZoneInfo.ConvertTimeToUtc%2A?displayProperty=nameWithType> méthode pour convertir la date et l’heure à partir d’un fuseau horaire spécifié. (Pour plus d’informations sur la récupération d’un <xref:System.TimeZoneInfo> objet qui représente le fuseau horaire de destination, consultez [recherche des fuseaux horaires définis sur un système local](../../../docs/standard/datetime/finding-the-time-zones-on-local-system.md).) Le code suivant utilise la <xref:System.TimeZoneInfo.ConvertTimeToUtc%2A?displayProperty=nameWithType> méthode pour convertir l’heure UTC.

[!code-csharp[System.TimeZone2.Concepts#7](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Concepts/CS/TimeZone2Concepts.cs#7)]
[!code-vb[System.TimeZone2.Concepts#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Concepts/VB/TimeZone2Concepts.vb#7)]

Notez que cette méthode lève un <xref:System.ArgumentException> si le <xref:System.DateTime> l’objet <xref:System.DateTime.Kind%2A> propriété et le fuseau horaire ne correspondent pas. Une incompatibilité se produit si le <xref:System.DateTime.Kind%2A> propriété est <xref:System.DateTimeKind.Local?displayProperty=nameWithType> mais le <xref:System.TimeZoneInfo> objet ne représente pas le fuseau horaire local, ou si le <xref:System.DateTime.Kind%2A> propriété est <xref:System.DateTimeKind.Utc?displayProperty=nameWithType> mais le <xref:System.TimeZoneInfo> objet n’est pas égal <xref:System.TimeZoneInfo.Utc?displayProperty=nameWithType>.

Toutes ces méthodes prennent <xref:System.DateTime> valeurs comme paramètres et retournent un <xref:System.DateTime> valeur. Pour <xref:System.DateTimeOffset> valeurs, le <xref:System.DateTimeOffset> structure a une <xref:System.DateTimeOffset.ToUniversalTime%2A> méthode qui convertit la date et l’heure de l’instance actuelle en heure UTC d’instance. L’exemple suivant appelle la <xref:System.DateTimeOffset.ToUniversalTime%2A> méthode pour convertir une heure locale et plusieurs autres heures en temps universel coordonné (UTC).

[!code-csharp[System.DateTimeOffset.Methods#16](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Methods/cs/Methods.cs#16)]
[!code-vb[System.DateTimeOffset.Methods#16](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Methods/vb/Methods.vb#16)]

## <a name="converting-utc-to-a-designated-time-zone"></a>Conversion de l’heure UTC dans un fuseau horaire désigné

Pour convertir l’heure UTC en heure locale, consultez la section « conversion en heure UTC à Local » qui suit. Pour convertir l’heure UTC en heure d’un fuseau horaire que vous désignez, appelez le <xref:System.TimeZoneInfo.ConvertTimeFromUtc%2A> (méthode). Cette méthode accepte deux paramètres :

* L’heure UTC à convertir. Cela doit être un <xref:System.DateTime> valeur dont la propriété <xref:System.DateTime.Kind%2A> propriété est définie sur `Unspecified` ou `Utc`.

* Le fuseau horaire vers lequel convertir l’heure UTC.

Le code suivant convertit l’heure UTC en heure propre au fuseau horaire Centre.

[!code-csharp[System.TimeZone2.Concepts#8](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Concepts/CS/TimeZone2Concepts.cs#8)]
[!code-vb[System.TimeZone2.Concepts#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Concepts/VB/TimeZone2Concepts.vb#8)]

## <a name="converting-utc-to-local-time"></a>Conversion de l’heure UTC en heure locale

Pour convertir l’heure UTC en heure locale, appelez le <xref:System.DateTime.ToLocalTime%2A> méthode de la <xref:System.DateTime> objet dont vous souhaitez convertir l’heure. Le comportement exact de la méthode dépend de la valeur de l’objet <xref:System.DateTime.Kind%2A> propriété, comme le tableau suivant.

| `DateTime.Kind`            | Conversion                                                                               |
| -------------------------- | ---------------------------------------------------------------------------------------- |
| `DateTimeKind.Local`       | Retourne le <xref:System.DateTime> valeur inchangée.                                      |
| `DateTimeKind.Unspecified` | Suppose que le <xref:System.DateTime> valeur est une heure UTC et convertit l’heure UTC en heure locale. |
| `DateTimeKind.Utc`         | Convertit la <xref:System.DateTime> valeur en heure locale.                                 |

> [!NOTE]
> Le <xref:System.TimeZone.ToLocalTime%2A?displayProperty=nameWithType> méthode se comporte comme le `DateTime.ToLocalTime` (méthode). Il prend un seul paramètre, qui est la valeur de date et l’heure à convertir.

Vous pouvez également régler l’heure dans n’importe quel fuseau horaire désigné en heure locale à l’aide de la `static` (`Shared` en Visual Basic) <xref:System.TimeZoneInfo.ConvertTime%2A?displayProperty=nameWithType> (méthode). Cette technique est décrite dans la section suivante.

## <a name="converting-between-any-two-time-zones"></a>Conversion entre deux fuseaux horaires quelconques

Vous pouvez convertir entre deux fuseaux horaires quelconques à l’aide d’une des deux suivantes `static` (`Shared` en Visual Basic) les méthodes de la <xref:System.TimeZoneInfo> classe :

* <xref:System.TimeZoneInfo.ConvertTime%2A>

  Paramètres de cette méthode sont la valeur de date et l’heure à convertir, un `TimeZoneInfo` objet qui représente le fuseau horaire de la valeur de date et d’heure, et un `TimeZoneInfo` objet qui représente le fuseau horaire pour convertir la valeur de date et heure.

* <xref:System.TimeZoneInfo.ConvertTimeBySystemTimeZoneId%2A>

  Paramètres de cette méthode sont la date et valeur d’heure à convertir l’identificateur de la date et de fuseau horaire de valeur d’heure et l’identificateur du fuseau horaire pour convertir la valeur de date et heure.

Les deux méthodes requièrent que le <xref:System.DateTime.Kind%2A> propriété de la valeur de date et l’heure à convertir et le <xref:System.TimeZoneInfo> identificateur d’objet ou le fuseau horaire qui représente son fuseau horaire correspondent entre eux. Sinon, une exception <xref:System.ArgumentException> est levée. Par exemple, si le `Kind` propriété de la valeur de date et d’heure est `DateTimeKind.Local`, une exception est levée si le `TimeZoneInfo` objet passé en tant que paramètre à la méthode n’est pas égal à `TimeZoneInfo.Local`. Une exception est également levée si l’identificateur passé comme paramètre à la méthode n’est pas égal à `TimeZoneInfo.Local.Id`.

L’exemple suivant utilise la <xref:System.TimeZoneInfo.ConvertTime%2A> méthode pour convertir l’heure Standard d’Hawaï en heure locale.

[!code-csharp[System.TimeZone2.Concepts#9](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Concepts/CS/TimeZone2Concepts.cs#9)]
[!code-vb[System.TimeZone2.Concepts#9](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Concepts/VB/TimeZone2Concepts.vb#9)]

## <a name="converting-datetimeoffset-values"></a>Conversion de valeurs DateTimeOffset

Les valeurs de date et d’heure représentées par <xref:System.DateTimeOffset> objets ne sont pas entièrement horaire prenant en charge, car l’objet est dissocié de son fuseau horaire au moment où il est instancié. Toutefois, dans de nombreux cas, une application doit simplement convertir une date et une heure en fonction de deux décalages différents par rapport à l’heure UTC plutôt qu’en fonction de l’heure dans des fuseaux horaires particuliers. Pour effectuer cette conversion, vous pouvez appeler l’instance en cours <xref:System.DateTimeOffset.ToOffset%2A> (méthode). Paramètre unique de la méthode est le décalage de la nouvelle valeur date et heure que la méthode consiste à retourner.

Par exemple, si la date et l’heure d’une demande de page web de l’utilisateur sont connues et sont sérialisées comme chaîne au format MM/jj/aaaa hh:mm:ss zzzz, la méthode `ReturnTimeOnServer` qui suit convertit cette valeur de date et d’heure en date et heure sur le serveur web.

[!code-csharp[System.DateTimeOffset.Conceptual.OffsetConversions#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual.OffsetConversions/cs/TimeConversions.cs#1)]
[!code-vb[System.DateTimeOffset.Conceptual.OffsetConversions#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual.OffsetConversions/vb/TimeConversions.vb#1)] 

Si la chaîne « 1/9/2007 5:32:07 -05:00 » est transmise à la méthode, représentant la date et l’heure dans un fuseau horaire en retard de cinq heures par rapport à l’heure UTC, elle retourne 1/9/2007 3:32:07 AM -07:00 pour un serveur situé dans le fuseau horaire horaire Pacifique (É.-U.).

Le <xref:System.TimeZoneInfo> classe inclut également une surcharge de la <xref:System.TimeZoneInfo.ConvertTime%28System.DateTimeOffset%2CSystem.TimeZoneInfo%29?displayProperty=nameWithType> méthode qui effectue des conversions de fuseau horaire avec <xref:System.DateTimeOffset.ToOffset(System.TimeSpan)> valeurs. Paramètres de la méthode sont une <xref:System.DateTimeOffset> valeur et une référence au fuseau horaire à laquelle l’heure doit être converti. L’appel de méthode retourne un <xref:System.DateTimeOffset> valeur. Par exemple, le `ReturnTimeOnServer` méthode dans l’exemple précédent peut être réécrit comme suit pour appeler le <xref:System.TimeZoneInfo.ConvertTime%28System.DateTimeOffset%2CSystem.TimeZoneInfo%29> (méthode).

[!code-csharp[System.DateTimeOffset.Conceptual.OffsetConversions#2](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual.OffsetConversions/cs/timeconversions2.cs#2)]
[!code-vb[System.DateTimeOffset.Conceptual.OffsetConversions#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual.OffsetConversions/vb/TimeConversions2.vb#2)]

## <a name="see-also"></a>Voir aussi

* <xref:System.TimeZoneInfo>
* [Dates, heures et fuseaux horaires](../../../docs/standard/datetime/index.md)
* [Recherche des fuseaux horaires définis sur un système local](../../../docs/standard/datetime/finding-the-time-zones-on-local-system.md)
