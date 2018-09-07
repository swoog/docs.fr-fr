---
title: Enregistrement et restauration de fuseaux horaires
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- restoring time zones
- deserialization [.NET Framework], time zones
- serialization [.NET Framework], time zones
- time zone objects [.NET Framework], restoring
- saving time zones
- time zone objects [.NET Framework], deserializing
- time zones [.NET Framework], saving
- time zones [.NET Framework], restoring
- time zone objects [.NET Framework], serializing
- time zone objects [.NET Framework], saving
ms.assetid: 4028b310-e7ce-49d4-a646-1e83bfaf6f9d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1dc983f1f0b2405f207d69c62b800ee854fcd409
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44081766"
---
# <a name="saving-and-restoring-time-zones"></a>Enregistrement et restauration de fuseaux horaires

Le <xref:System.TimeZoneInfo> classe s’appuie sur le Registre pour récupérer des données de fuseau horaire prédéfini. Toutefois, le Registre est une structure dynamique. En outre, les informations de fuseau horaire qui contient le Registre sont utilisées par le système d’exploitation principalement à gérer les conversions et le réglage de l’heure de l’année en cours. Cela a deux conséquences principales pour les applications qui s’appuient sur des données de fuseau horaire exactes :

* Un fuseau horaire qui est requis par une application ne peut pas être défini dans le Registre, ou peut avoir été renommé ou supprimé le Registre.

* Un fuseau horaire qui est défini dans le Registre ne disposent parfois pas d’informations sur les règles d’ajustement particulier qui sont nécessaires pour les conversions de fuseau horaire historiques.

Le <xref:System.TimeZoneInfo> classe traite de ces limites en prenant en charge la sérialisation (enregistrement) et la désérialisation (restauration) des données de fuseau horaire.

## <a name="time-zone-serialization-and-deserialization"></a>La désérialisation et la sérialisation de fuseau horaire

Enregistrement et restauration d’un fuseau horaire à sérialiser et désérialiser des données de fuseau horaire impliquent deux appels de méthode :

* Vous pouvez sérialiser un <xref:System.TimeZoneInfo> objet en appelant l’objet <xref:System.TimeZoneInfo.ToSerializedString%2A> (méthode). La méthode n’accepte aucun paramètre et retourne une chaîne qui contient les informations de fuseau horaire.

* Vous pouvez désérialiser un <xref:System.TimeZoneInfo> objet à partir d’une chaîne sérialisée en passant cette chaîne à la `static` (`Shared` en Visual Basic) <xref:System.TimeZoneInfo.FromSerializedString%2A?displayProperty=nameWithType> (méthode).

## <a name="serialization-and-deserialization-scenarios"></a>Scénarios de sérialisation et désérialisation

La possibilité d’enregistrer (ou de sérialiser) un <xref:System.TimeZoneInfo> objet en une chaîne et de restauration (ou désérialiser) pour une utilisation ultérieure augmente l’utilitaire et la flexibilité de la <xref:System.TimeZoneInfo> classe. Cette section examine certaines des situations dans lesquelles la sérialisation et la désérialisation sont très utiles.

### <a name="serializing-and-deserializing-time-zone-data-in-an-application"></a>Sérialiser et désérialiser des données de fuseau horaire dans une application

Lorsqu’il est nécessaire, un fuseau horaire sérialisé peut être restauré à partir d’une chaîne. Une application peut faire si le fuseau horaire récupéré à partir du Registre est impossible de convertir correctement une date et une heure dans une plage de dates. Par exemple, les données de fuseau horaire dans le Registre de Windows XP prend en charge une règle d’ajustement unique, tandis que les fuseaux horaires définis dans le Registre de Windows Vista généralement fournissent des informations sur deux règles d’ajustement. Cela signifie que les conversions d’heures historiques peuvent être inexactes. Sérialisation et désérialisation des données de fuseau horaire peuvent gérer cette limitation.

Dans l’exemple suivant, un personnalisé <xref:System.TimeZoneInfo> classe qui a des règles d’ajustement est définie pour représenter le fuseau horaire Heure d’hiver fuseau de 1883 à 1917, avant l’introduction de l’heure d’été aux États-Unis. Le fuseau horaire personnalisé est sérialisé dans une variable qui a une portée globale. La méthode de conversion de fuseau horaire, `ConvertUtcTime`, est passée pour convertir le temps de temps universel coordonné (UTC). Si la date et l’heure se produit en 1917 ou une version antérieure, le fuseau horaire est des États-Unis personnalisé est restauré à partir d’une chaîne sérialisée et remplace le fuseau horaire récupéré à partir du Registre.

[!code-csharp[System.TimeZone2.Serialization.1#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Serialization.1/cs/Serialization.cs#1)]
[!code-vb[System.TimeZone2.Serialization.1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Serialization.1/vb/Serialization.vb#1)]

### <a name="handling-time-zone-exceptions"></a>Gestion des exceptions de fuseau horaire

Étant donné que le Registre est une structure dynamique, son contenu est sujet à modification accidentelle ou intentionnelle. Cela signifie qu’un fuseau horaire qui doit être défini dans le Registre et qui est nécessaire pour une application à s’exécuter avec succès peuvent être absent. Sans prise en charge pour la sérialisation de fuseau horaire et de la désérialisation, ne vous reste plus qu’à gérer résultant <xref:System.TimeZoneNotFoundException> en mettant fin à l’application. Toutefois, à l’aide de sérialisation de fuseau horaire et la désérialisation, vous pouvez gérer un inattendue <xref:System.TimeZoneNotFoundException> en restaurant le fuseau horaire requis à partir d’une chaîne sérialisée et l’application continuera à s’exécuter.

L’exemple suivant crée et sérialise un fuseau horaire Standard Central personnalisé. Ensuite, il tente de récupérer le fuseau horaire de la centrale à partir du Registre. Si l’opération de récupération lève soit une <xref:System.TimeZoneNotFoundException> ou un <xref:System.InvalidTimeZoneException>, le Gestionnaire d’exceptions désérialise le fuseau horaire.

[!code-csharp[System.TimeZone2.Serialization.2#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Serialization.2/cs/Serialization2.cs#1)]
[!code-vb[System.TimeZone2.Serialization.2#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Serialization.2/vb/Serialization2.vb#1)]

### <a name="storing-a-serialized-string-and-restoring-it-when-needed"></a>Stocker une chaîne sérialisée et la restauration en cas de besoin

Les exemples précédents ont stocké des informations de fuseau horaire à une variable de chaîne et restaurés en cas de besoin. Toutefois, la chaîne qui contient l’heure sérialisée des informations de zone peuvent être stockées dans un support de stockage, tel qu’un fichier externe, un fichier de ressources incorporées dans l’application ou le Registre. (Notez que les informations sur les fuseaux horaires personnalisés doivent être stockées en dehors des clés de fuseau horaire du système dans le Registre).

Stockage d’une chaîne de fuseau horaire sérialisées de cette manière sépare également la routine de création de fuseau horaire à partir de l’application elle-même. Par exemple, une routine de création de fuseau horaire peut exécuter et créer un fichier de données qui contient des informations de fuseau horaire historiques qu’une application peut utiliser. Le fichier de données peut ensuite être installé avec l’application et il peut être ouvert et un ou plusieurs de ses zones de temps peuvent être désérialisé lorsque l’application a besoin.

Pour obtenir un exemple qui utilise une ressource incorporée pour stocker les données de fuseau horaire sérialisées, consultez [Comment : enregistrer des fuseaux horaires dans une ressource incorporée](../../../docs/standard/datetime/save-time-zones-to-an-embedded-resource.md) et [Comment : restaurer des fuseaux horaires dans une ressource incorporée](../../../docs/standard/datetime/restore-time-zones-from-an-embedded-resource.md).

## <a name="see-also"></a>Voir aussi

* [Dates, heures et fuseaux horaires](../../../docs/standard/datetime/index.md)
