---
title: 'Procédure : accéder aux objets de fuseau horaire UTC et local prédéfinis'
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time zones [.NET Framework], local
- predefined time zones
- UTC times, predefined
- local time zone access
- time zones [.NET Framework], retrieving
- time zones [.NET Framework], UTC
ms.assetid: 961fb70b-83f0-4dab-a042-cb5fcd817cf5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c10c07c08a4e676cf3c84a5722814eaed85f74a9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62026604"
---
# <a name="how-to-access-the-predefined-utc-and-local-time-zone-objects"></a>Procédure : accéder aux objets de fuseau horaire UTC et local prédéfinis

Le <xref:System.TimeZoneInfo> classe fournit deux propriétés, <xref:System.TimeZoneInfo.Utc%2A> et <xref:System.TimeZoneInfo.Local%2A>, qui vous offrent votre code d’accéder aux objets de fuseau horaire prédéfini. Cette rubrique explique comment accéder aux objets <xref:System.TimeZoneInfo> retournés par ces propriétés.

### <a name="to-access-the-coordinated-universal-time-utc-timezoneinfo-object"></a>Pour accéder à l’objet TimeZoneInfo de temps universel coordonné (UTC)

1. Utilisez le `static` (`Shared` en Visual Basic) <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> propriété à laquelle accéder temps universel coordonné.

2. Au lieu d’affecter le <xref:System.TimeZoneInfo> objet retourné par la propriété à une variable objet, continuer à accéder au temps universel coordonné via la <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> propriété.

### <a name="to-access-the-local-time-zone"></a>Pour accéder au fuseau horaire local

1. Utilisez le `static` (`Shared` en Visual Basic) <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> propriété pour accéder au fuseau horaire de système local.

2. Au lieu d’affecter le <xref:System.TimeZoneInfo> objet retourné par la propriété à une variable objet, continuer à accéder au fuseau horaire local via le <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> propriété.

## <a name="example"></a>Exemple

Le code suivant utilise la <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> et <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> propriétés pour convertir une heure du fuseau horaire des États-Unis et Canada est Standard, ainsi que pour afficher le nom de fuseau horaire dans la console.

[!code-csharp[System.TimeZone2.Concepts#13](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Concepts/CS/TimeZone2Concepts.cs#13)]
[!code-vb[System.TimeZone2.Concepts#13](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Concepts/VB/TimeZone2Concepts.vb#13)]

Vous devez toujours accéder au fuseau horaire local via le <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> propriété plutôt qu’en affectant l’heure locale de la zone à une <xref:System.TimeZoneInfo> variable objet. De même, vous devez toujours accéder à temps universel coordonné via la <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> propriété plutôt qu’en affectant l’heure UTC de la zone à une <xref:System.TimeZoneInfo> variable objet. Cela empêche le <xref:System.TimeZoneInfo> variable objet d’être invalidée par un appel à la <xref:System.TimeZoneInfo.ClearCachedData%2A?displayProperty=nameWithType> (méthode).

## <a name="compiling-the-code"></a>Compilation du code

Cet exemple nécessite :

* Qu’une référence à System.Core.dll soit ajoutée au projet.

* Que l'espace de noms <xref:System> soit importé avec l'instruction `using` (obligatoire en C#).

## <a name="see-also"></a>Voir aussi

- [Dates, heures et fuseaux horaires](../../../docs/standard/datetime/index.md)
- [Recherche des fuseaux horaires définis sur un système local](../../../docs/standard/datetime/finding-the-time-zones-on-local-system.md)
- [Guide pratique pour Instancier un objet TimeZoneInfo](../../../docs/standard/datetime/instantiate-time-zone-info.md)
