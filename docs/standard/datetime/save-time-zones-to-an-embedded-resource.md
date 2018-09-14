---
title: 'Comment : enregistrer des fuseaux horaires dans une ressource incorporée'
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time zones [.NET Framework], saving
- time zone objects [.NET Framework], serializing
- time zone objects [.NET Framework], saving
ms.assetid: 3c96d83a-a057-4496-abb0-8f4b12712558
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 921874e774d18751c29db495dac1bc53d10cc8ad
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "44778626"
---
# <a name="how-to-save-time-zones-to-an-embedded-resource"></a>Comment : enregistrer des fuseaux horaires dans une ressource incorporée

Une application prenant en charge de fuseau horaire souvent nécessite la présence d’un fuseau horaire particulier. Toutefois, étant donné que la disponibilité de l’individu <xref:System.TimeZoneInfo> objets dépend des informations stockées dans le Registre du système local, les fuseaux horaires même habituellement disponibles peuvent être absents. En outre, les informations sur les fuseaux horaires personnalisés instancié à l’aide du <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> (méthode) n’est pas stockée avec d’autres informations de fuseau horaire dans le Registre. Pour vous assurer que ces fuseaux horaires sont disponibles lorsqu’ils sont nécessaires, vous pouvez les enregistrer en les sérialisant et les restaurer ultérieurement en désérialisant les.

En règle générale, la sérialisation un <xref:System.TimeZoneInfo> objet se trouve en dehors de l’application prenant en charge de fuseau horaire. Selon le magasin de données utilisé pour contenir sérialisée <xref:System.TimeZoneInfo> objets, les données de fuseau horaire peuvent être sérialisées en tant que partie d’une routine d’installation (par exemple, lorsque les données sont stockées dans une clé d’application du Registre), ou dans le cadre d’une routine d’utilitaire qui s’exécute avant que l’application finale est compilée (par exemple, lorsque les données sérialisées sont stockées dans un fichier de ressources (.resx) .NET XML).

En plus d’un fichier de ressources qui est compilé avec l’application, plusieurs autres magasins de données utilisable pour les informations de fuseau horaire. Notamment :

* Le Registre. Notez qu’une application doit utiliser les sous-clés de sa propre clé d’application pour stocker des données de fuseau horaire personnalisé, plutôt que d’utiliser les sous-clés de HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Time Zones.

* Fichiers de configuration.

* Autres fichiers système.

### <a name="to-save-a-time-zone-by-serializing-it-to-a-resx-file"></a>Pour enregistrer un fuseau horaire en le sérialisant dans un fichier .resx

1. Récupérer un fuseau horaire existant ou créer un nouveau fuseau horaire.

   Pour récupérer un fuseau horaire existant, consultez [Comment : accéder aux objets de fuseau UTC et l’heure locale prédéfinis](../../../docs/standard/datetime/access-utc-and-local.md) et [Comment : instancier un objet TimeZoneInfo](../../../docs/standard/datetime/instantiate-time-zone-info.md).

   Pour créer un nouveau fuseau horaire, appelez l’une des surcharges de la <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> (méthode). Pour plus d’informations, consultez [Comment : créer des fuseaux horaires sans règles d’ajustement](../../../docs/standard/datetime/create-time-zones-without-adjustment-rules.md) et [Comment : créer des fuseaux horaires avec des règles d’ajustement](../../../docs/standard/datetime/create-time-zones-with-adjustment-rules.md).

2. Appelez le <xref:System.TimeZoneInfo.ToSerializedString%2A> méthode pour créer une chaîne qui contient les données du fuseau horaire.

3. Instancier un <xref:System.IO.StreamWriter> objet en fournissant le nom et éventuellement le chemin d’accès du fichier .resx à la <xref:System.IO.StreamWriter> constructeur de classe.

4. Instancier un <xref:System.Resources.ResXResourceWriter> en passant le <xref:System.IO.StreamWriter> de l’objet à le <xref:System.Resources.ResXResourceWriter> constructeur de classe.

5. Passez le fuseau horaire chaîne sérialisée à le <xref:System.Resources.ResXResourceWriter.AddResource%2A?displayProperty=nameWithType> (méthode).

6. Appelez la méthode <xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType>.

7. Appelez la méthode <xref:System.Resources.ResXResourceWriter.Close%2A?displayProperty=nameWithType>.

8. Fermer le <xref:System.IO.StreamWriter> objet en appelant son <xref:System.IO.StreamWriter.Close%2A> (méthode).

9. Ajoutez le fichier .resx généré au projet de l’application Visual Studio.

10. À l’aide de la **propriétés** fenêtre dans Visual Studio, assurez-vous que le fichier .resx **Action de génération** propriété est définie sur **ressource incorporée**.

## <a name="example"></a>Exemple

L’exemple suivant sérialise un <xref:System.TimeZoneInfo> objet qui représente l’heure et un <xref:System.TimeZoneInfo> objet qui représente le Palmer Station, l’heure de l’Antarctique dans un fichier de ressources .NET XML nommé SerializedTimeZones.resx. Heure d’hiver Central est généralement défini dans le Registre ; Palmer Station, Antarctique est un fuseau horaire personnalisé.

[!code-csharp[TimeZone2.Serialization#1](../../../samples/snippets/csharp/VS_Snippets_CLR/TimeZone2.Serialization/cs/SerializeTimeZoneData.cs#1)]
[!code-vb[TimeZone2.Serialization#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/TimeZone2.Serialization/vb/SerializeTimeZoneData.vb#1)]

Cet exemple sérialise <xref:System.TimeZoneInfo> objets de sorte qu’ils sont disponibles dans un fichier de ressources au moment de la compilation.

Étant donné que le <xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType> méthode ajoute des informations d’en-tête complètes à un fichier de ressources .NET XML, il ne peut pas être utilisé pour ajouter des ressources à un fichier existant. L’exemple gère cela en recherchant le fichier SerializedTimeZones.resx et, si elle existe, toutes ses ressources stockage autre que les deux sérialisé fuseaux horaires générique <xref:System.Collections.Generic.Dictionary%602> objet. Le fichier existant est ensuite supprimé et les ressources existantes sont ajoutés à un nouveau fichier SerializedTimeZones.resx. Les données de fuseau horaire sérialisé sont également ajoutées à ce fichier.

La clé (ou **nom**) champs de ressources ne doivent pas contenir des espaces incorporés. Le <xref:System.String.Replace%28System.String%2CSystem.String%29> méthode est appelée pour supprimer tous les espaces incorporés dans les identificateurs de fuseau horaire avant qu’ils sont affectés au fichier de ressources.

## <a name="compiling-the-code"></a>Compilation du code

Cet exemple nécessite :

* Une référence à System.Windows.Forms.dll et System.Core.dll être ajouté au projet.

* Que les espaces de noms suivants soient importés :

  [!code-csharp[TimeZone2.Serialization#2](../../../samples/snippets/csharp/VS_Snippets_CLR/TimeZone2.Serialization/cs/SerializeTimeZoneData.cs#2)]
  [!code-vb[TimeZone2.Serialization#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/TimeZone2.Serialization/vb/SerializeTimeZoneData.vb#2)]

## <a name="see-also"></a>Voir aussi

* [Dates, heures et fuseaux horaires](../../../docs/standard/datetime/index.md)
* [Vue d’ensemble des fuseaux horaires](../../../docs/standard/datetime/time-zone-overview.md)
* [Guide pratique pour restaurer des fuseaux horaires dans une ressource incorporée](../../../docs/standard/datetime/restore-time-zones-from-an-embedded-resource.md)
