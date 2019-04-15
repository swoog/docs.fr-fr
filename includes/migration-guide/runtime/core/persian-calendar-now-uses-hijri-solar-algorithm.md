---
ms.openlocfilehash: bfe406161ac754124a2cc38c68a80c3b9fb2c7f6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234154"
---
### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>Le calendrier persan utilise désormais l’algorithme solaire hégirien

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.6, la classe <xref:System.Globalization.PersianCalendar?displayProperty=name> utilise l’algorithme solaire hégirien. La conversion de dates entre le calendrier <xref:System.Globalization.PersianCalendar?displayProperty=name> et les autres calendriers peut produire un résultat légèrement différent à compter de .NET Framework 4.6 pour les dates antérieures à 1800 ou postérieures à 2023 (calendrier grégorien). De plus, <xref:System.Globalization.PersianCalendar.MinSupportedDateTime?displayProperty=nameWithType> est désormais <code>March 22, 0622</code> au lieu de <code>March 21, 0622</code>.|
|Suggestion|Notez que certaines dates anciennes ou futures peuvent être légèrement différentes quand vous utilisez le calendrier persan dans .NET Framework 4.6. En outre, quand vous sérialisez des dates dans plusieurs processus qui peuvent s’exécuter sur des versions différentes du .NET Framework, ne les stockez pas sous forme de chaînes de date PersianCalendar (puisque ces valeurs peuvent être différentes).|
|Portée|Mineur|
|Version|4.6|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|
