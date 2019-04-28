---
title: 'Procédure : créer des fuseaux horaires sans règles d’ajustement'
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time zones [.NET Framework], adjustment rule
- time zones [.NET Framework], creating
- adjustment rule [.NET Framework]
ms.assetid: a6af8647-7893-4f29-95a9-d94c65a6e8dd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cb3ffc7b6f1f7baec7ce6beb5a50b706ff78bfa1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62026547"
---
# <a name="how-to-create-time-zones-without-adjustment-rules"></a>Procédure : créer des fuseaux horaires sans règles d’ajustement

Les informations de fuseau horaire précises qui sont requis par une application ne peuvent pas être présentes sur un système particulier pour plusieurs raisons :

* Le fuseau horaire n’a jamais été défini dans le Registre du système local.

* Données sur le fuseau horaire a été modifiées ou supprimées à partir du Registre.

* Le fuseau horaire existe mais n’a pas d’informations précises sur les ajustements de fuseau horaire pour une période donnée.

Dans ce cas, vous pouvez appeler la <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> méthode pour définir le fuseau horaire requis par votre application. Vous pouvez utiliser les surcharges de cette méthode pour créer un fuseau horaire avec ou sans règles d’ajustement. Si le fuseau horaire prend en charge l’heure d’été, vous pouvez définir des ajustements avec des règles d’ajustement fixe ou flottante. (Pour les définitions de ces termes, consultez la section « Terminologie de fuseau horaire » dans [vue d’ensemble du fuseau horaire](../../../docs/standard/datetime/time-zone-overview.md).)

> [!IMPORTANT]
> Les fuseaux horaires personnalisés créés en appelant le <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> méthode ne sont pas ajoutés au Registre. Au lieu de cela, ils sont accessibles uniquement par le biais de la référence d’objet retournée par la <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> appel de méthode.

Cette rubrique montre comment créer un fuseau horaire sans règles d’ajustement. Pour créer un fuseau horaire qui prend en charge des règles d’ajustement de l’heure d’été, consultez [Comment : Créer des fuseaux horaires avec des règles d’ajustement](../../../docs/standard/datetime/create-time-zones-with-adjustment-rules.md).

### <a name="to-create-a-time-zone-without-adjustment-rules"></a>Pour créer un fuseau horaire sans règles d’ajustement

1. Définir le nom d’affichage du fuseau horaire.

   Le nom d’affichage suit un format relativement standard dans lequel l’offset du fuseau horaire par rapport au temps universel coordonné (UTC) est placée entre parenthèses et est suivie d’une chaîne qui identifie le fuseau horaire, une ou plusieurs des villes dans le fuseau horaire, ou l’un ou plusieurs du cou gra ou des régions dans le fuseau horaire.

2. Définir le nom de l’heure d’hiver du fuseau horaire. En règle générale, cette chaîne est également utilisée comme identificateur de fuseau horaire.

3. Si vous souhaitez utiliser un identificateur autre que le nom standard du fuseau horaire, définissez l’identificateur de fuseau horaire.

4. Instancier un <xref:System.TimeSpan> objet qui définit le décalage du fuseau horaire à l’heure UTC. Fuseaux horaires avec des heures sont ultérieures à l’heure UTC ont un décalage positif. Fuseaux horaires avec des temps d’antérieures à UTC ont un offset négatif.

5. Appelez le <xref:System.TimeZoneInfo.CreateCustomTimeZone%28System.String%2CSystem.TimeSpan%2CSystem.String%2CSystem.String%29?displayProperty=nameWithType> méthode pour instancier le nouveau fuseau horaire.

## <a name="example"></a>Exemple

L’exemple suivant définit un fuseau horaire personnalisé pour Mawson, en Antarctique sans règles d’ajustement.

[!code-csharp[System.TimeZone2.CreateTimeZone#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/cs/System.TimeZone2.CreateTimeZone.cs#1)]
[!code-vb[System.TimeZone2.CreateTimeZone#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/vb/System.TimeZone2.CreateTimeZone.vb#1)]

La chaîne assignée à la <xref:System.TimeZoneInfo.DisplayName%2A> propriété suit un format standard dans lequel décalage du fuseau horaire à l’heure UTC est suivie d’une description conviviale du fuseau horaire.

## <a name="compiling-the-code"></a>Compilation du code

Cet exemple nécessite :

* Qu’une référence à System.Core.dll soit ajoutée au projet.

* Que les espaces de noms suivants soient importés :

  [!code-csharp[System.TimeZone2.CreateTimeZone#6](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/cs/System.TimeZone2.CreateTimeZone.cs#6)]
  [!code-vb[System.TimeZone2.CreateTimeZone#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/vb/System.TimeZone2.CreateTimeZone.vb#6)]

## <a name="see-also"></a>Voir aussi

- [Dates, heures et fuseaux horaires](../../../docs/standard/datetime/index.md)
- [Vue d’ensemble des fuseaux horaires](../../../docs/standard/datetime/time-zone-overview.md)
- [Guide pratique pour Créer des fuseaux horaires avec des règles d’ajustement](../../../docs/standard/datetime/create-time-zones-with-adjustment-rules.md)
