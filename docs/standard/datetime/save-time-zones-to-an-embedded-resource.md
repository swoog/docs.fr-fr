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
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44211851"
---
# <a name="how-to-save-time-zones-to-an-embedded-resource"></a><span data-ttu-id="3f2ac-102">Comment : enregistrer des fuseaux horaires dans une ressource incorporée</span><span class="sxs-lookup"><span data-stu-id="3f2ac-102">How to: Save time zones to an embedded resource</span></span>

<span data-ttu-id="3f2ac-103">Une application prenant en charge de fuseau horaire souvent nécessite la présence d’un fuseau horaire particulier.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-103">A time zone-aware application often requires the presence of a particular time zone.</span></span> <span data-ttu-id="3f2ac-104">Toutefois, étant donné que la disponibilité de l’individu <xref:System.TimeZoneInfo> objets dépend des informations stockées dans le Registre du système local, les fuseaux horaires même habituellement disponibles peuvent être absents.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-104">However, because the availability of individual <xref:System.TimeZoneInfo> objects depends on information stored in the local system's registry, even customarily available time zones may be absent.</span></span> <span data-ttu-id="3f2ac-105">En outre, les informations sur les fuseaux horaires personnalisés instancié à l’aide du <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> (méthode) n’est pas stockée avec d’autres informations de fuseau horaire dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-105">In addition, information about custom time zones instantiated by using the <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> method is not stored with other time zone information in the registry.</span></span> <span data-ttu-id="3f2ac-106">Pour vous assurer que ces fuseaux horaires sont disponibles lorsqu’ils sont nécessaires, vous pouvez les enregistrer en les sérialisant et les restaurer ultérieurement en désérialisant les.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-106">To ensure that these time zones are available when they are needed, you can save them by serializing them, and later restore them by deserializing them.</span></span>

<span data-ttu-id="3f2ac-107">En règle générale, la sérialisation un <xref:System.TimeZoneInfo> objet se trouve en dehors de l’application prenant en charge de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-107">Typically, serializing a <xref:System.TimeZoneInfo> object occurs apart from the time zone-aware application.</span></span> <span data-ttu-id="3f2ac-108">Selon le magasin de données utilisé pour contenir sérialisée <xref:System.TimeZoneInfo> objets, les données de fuseau horaire peuvent être sérialisées en tant que partie d’une routine d’installation (par exemple, lorsque les données sont stockées dans une clé d’application du Registre), ou dans le cadre d’une routine d’utilitaire qui s’exécute avant que l’application finale est compilée (par exemple, lorsque les données sérialisées sont stockées dans un fichier de ressources (.resx) .NET XML).</span><span class="sxs-lookup"><span data-stu-id="3f2ac-108">Depending on the data store used to hold serialized <xref:System.TimeZoneInfo> objects, time zone data may be serialized as part of a setup or installation routine (for example, when the data is stored in an application key of the registry), or as part of a utility routine that runs before the final application is compiled (for example, when the serialized data is stored in a .NET XML resource (.resx) file).</span></span>

<span data-ttu-id="3f2ac-109">En plus d’un fichier de ressources qui est compilé avec l’application, plusieurs autres magasins de données utilisable pour les informations de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-109">In addition to a resource file that is compiled with the application, several other data stores can be used for time zone information.</span></span> <span data-ttu-id="3f2ac-110">Notamment :</span><span class="sxs-lookup"><span data-stu-id="3f2ac-110">These include the following:</span></span>

* <span data-ttu-id="3f2ac-111">Le Registre.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-111">The registry.</span></span> <span data-ttu-id="3f2ac-112">Notez qu’une application doit utiliser les sous-clés de sa propre clé d’application pour stocker des données de fuseau horaire personnalisé, plutôt que d’utiliser les sous-clés de HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Time Zones.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-112">Note that an application should use the subkeys of its own application key to store custom time zone data rather than using the subkeys of HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Time Zones.</span></span>

* <span data-ttu-id="3f2ac-113">Fichiers de configuration.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-113">Configuration files.</span></span>

* <span data-ttu-id="3f2ac-114">Autres fichiers système.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-114">Other system files.</span></span>

### <a name="to-save-a-time-zone-by-serializing-it-to-a-resx-file"></a><span data-ttu-id="3f2ac-115">Pour enregistrer un fuseau horaire en le sérialisant dans un fichier .resx</span><span class="sxs-lookup"><span data-stu-id="3f2ac-115">To save a time zone by serializing it to a .resx file</span></span>

1. <span data-ttu-id="3f2ac-116">Récupérer un fuseau horaire existant ou créer un nouveau fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-116">Retrieve an existing time zone or create a new time zone.</span></span>

   <span data-ttu-id="3f2ac-117">Pour récupérer un fuseau horaire existant, consultez [Comment : accéder aux objets de fuseau UTC et l’heure locale prédéfinis](../../../docs/standard/datetime/access-utc-and-local.md) et [Comment : instancier un objet TimeZoneInfo](../../../docs/standard/datetime/instantiate-time-zone-info.md).</span><span class="sxs-lookup"><span data-stu-id="3f2ac-117">To retrieve an existing time zone, see [How to: Access the predefined UTC and local time zone objects](../../../docs/standard/datetime/access-utc-and-local.md) and [How to: Instantiate a TimeZoneInfo object](../../../docs/standard/datetime/instantiate-time-zone-info.md).</span></span>

   <span data-ttu-id="3f2ac-118">Pour créer un nouveau fuseau horaire, appelez l’une des surcharges de la <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="3f2ac-118">To create a new time zone, call one of the overloads of the <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> method.</span></span> <span data-ttu-id="3f2ac-119">Pour plus d’informations, consultez [Comment : créer des fuseaux horaires sans règles d’ajustement](../../../docs/standard/datetime/create-time-zones-without-adjustment-rules.md) et [Comment : créer des fuseaux horaires avec des règles d’ajustement](../../../docs/standard/datetime/create-time-zones-with-adjustment-rules.md).</span><span class="sxs-lookup"><span data-stu-id="3f2ac-119">For more information, see [How to: Create time zones without adjustment rules](../../../docs/standard/datetime/create-time-zones-without-adjustment-rules.md) and [How to: Create time zones with adjustment rules](../../../docs/standard/datetime/create-time-zones-with-adjustment-rules.md).</span></span>

2. <span data-ttu-id="3f2ac-120">Appelez le <xref:System.TimeZoneInfo.ToSerializedString%2A> méthode pour créer une chaîne qui contient les données du fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-120">Call the <xref:System.TimeZoneInfo.ToSerializedString%2A> method to create a string that contains the time zone's data.</span></span>

3. <span data-ttu-id="3f2ac-121">Instancier un <xref:System.IO.StreamWriter> objet en fournissant le nom et éventuellement le chemin d’accès du fichier .resx à la <xref:System.IO.StreamWriter> constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-121">Instantiate a <xref:System.IO.StreamWriter> object by providing the name and optionally the path of the .resx file to the <xref:System.IO.StreamWriter> class constructor.</span></span>

4. <span data-ttu-id="3f2ac-122">Instancier un <xref:System.Resources.ResXResourceWriter> en passant le <xref:System.IO.StreamWriter> de l’objet à le <xref:System.Resources.ResXResourceWriter> constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-122">Instantiate a <xref:System.Resources.ResXResourceWriter> object by passing the <xref:System.IO.StreamWriter> object to the <xref:System.Resources.ResXResourceWriter> class constructor.</span></span>

5. <span data-ttu-id="3f2ac-123">Passez le fuseau horaire chaîne sérialisée à le <xref:System.Resources.ResXResourceWriter.AddResource%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="3f2ac-123">Pass the time zone's serialized string to the <xref:System.Resources.ResXResourceWriter.AddResource%2A?displayProperty=nameWithType> method.</span></span>

6. <span data-ttu-id="3f2ac-124">Appelez la méthode <xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-124">Call the <xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType> method.</span></span>

7. <span data-ttu-id="3f2ac-125">Appelez la méthode <xref:System.Resources.ResXResourceWriter.Close%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-125">Call the <xref:System.Resources.ResXResourceWriter.Close%2A?displayProperty=nameWithType> method.</span></span>

8. <span data-ttu-id="3f2ac-126">Fermer le <xref:System.IO.StreamWriter> objet en appelant son <xref:System.IO.StreamWriter.Close%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="3f2ac-126">Close the <xref:System.IO.StreamWriter> object by calling its <xref:System.IO.StreamWriter.Close%2A> method.</span></span>

9. <span data-ttu-id="3f2ac-127">Ajoutez le fichier .resx généré au projet de l’application Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-127">Add the generated .resx file to the application's Visual Studio project.</span></span>

10. <span data-ttu-id="3f2ac-128">À l’aide de la **propriétés** fenêtre dans Visual Studio, assurez-vous que le fichier .resx **Action de génération** propriété est définie sur **ressource incorporée**.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-128">Using the **Properties** window in Visual Studio, make sure that the .resx file's **Build Action** property is set to **Embedded Resource**.</span></span>

## <a name="example"></a><span data-ttu-id="3f2ac-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f2ac-129">Example</span></span>

<span data-ttu-id="3f2ac-130">L’exemple suivant sérialise un <xref:System.TimeZoneInfo> objet qui représente l’heure et un <xref:System.TimeZoneInfo> objet qui représente le Palmer Station, l’heure de l’Antarctique dans un fichier de ressources .NET XML nommé SerializedTimeZones.resx.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-130">The following example serializes a <xref:System.TimeZoneInfo> object that represents Central Standard Time and a <xref:System.TimeZoneInfo> object that represents the Palmer Station, Antarctica time to a .NET XML resource file that is named SerializedTimeZones.resx.</span></span> <span data-ttu-id="3f2ac-131">Heure d’hiver Central est généralement défini dans le Registre ; Palmer Station, Antarctique est un fuseau horaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-131">Central Standard Time is typically defined in the registry; Palmer Station, Antarctica is a custom time zone.</span></span>

[!code-csharp[TimeZone2.Serialization#1](../../../samples/snippets/csharp/VS_Snippets_CLR/TimeZone2.Serialization/cs/SerializeTimeZoneData.cs#1)]
[!code-vb[TimeZone2.Serialization#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/TimeZone2.Serialization/vb/SerializeTimeZoneData.vb#1)]

<span data-ttu-id="3f2ac-132">Cet exemple sérialise <xref:System.TimeZoneInfo> objets de sorte qu’ils sont disponibles dans un fichier de ressources au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-132">This example serializes <xref:System.TimeZoneInfo> objects so that they are available in a resource file at compile time.</span></span>

<span data-ttu-id="3f2ac-133">Étant donné que le <xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType> méthode ajoute des informations d’en-tête complètes à un fichier de ressources .NET XML, il ne peut pas être utilisé pour ajouter des ressources à un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-133">Because the <xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType> method adds complete header information to a .NET XML resource file, it cannot be used to add resources to an existing file.</span></span> <span data-ttu-id="3f2ac-134">L’exemple gère cela en recherchant le fichier SerializedTimeZones.resx et, si elle existe, toutes ses ressources stockage autre que les deux sérialisé fuseaux horaires générique <xref:System.Collections.Generic.Dictionary%602> objet.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-134">The example handles this by checking for the SerializedTimeZones.resx file and, if it exists, storing all of its resources other than the two serialized time zones to a generic <xref:System.Collections.Generic.Dictionary%602> object.</span></span> <span data-ttu-id="3f2ac-135">Le fichier existant est ensuite supprimé et les ressources existantes sont ajoutés à un nouveau fichier SerializedTimeZones.resx.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-135">The existing file is then deleted and the existing resources are added to a new SerializedTimeZones.resx file.</span></span> <span data-ttu-id="3f2ac-136">Les données de fuseau horaire sérialisé sont également ajoutées à ce fichier.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-136">The serialized time zone data is also added to this file.</span></span>

<span data-ttu-id="3f2ac-137">La clé (ou **nom**) champs de ressources ne doivent pas contenir des espaces incorporés.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-137">The key (or **Name**) fields of resources should not contain embedded spaces.</span></span> <span data-ttu-id="3f2ac-138">Le <xref:System.String.Replace%28System.String%2CSystem.String%29> méthode est appelée pour supprimer tous les espaces incorporés dans les identificateurs de fuseau horaire avant qu’ils sont affectés au fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-138">The <xref:System.String.Replace%28System.String%2CSystem.String%29> method is called to remove all embedded spaces in the time zone identifiers before they are assigned to the resource file.</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="3f2ac-139">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="3f2ac-139">Compiling the code</span></span>

<span data-ttu-id="3f2ac-140">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="3f2ac-140">This example requires:</span></span>

* <span data-ttu-id="3f2ac-141">Une référence à System.Windows.Forms.dll et System.Core.dll être ajouté au projet.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-141">That a reference to System.Windows.Forms.dll and System.Core.dll be added to the project.</span></span>

* <span data-ttu-id="3f2ac-142">Que les espaces de noms suivants soient importés :</span><span class="sxs-lookup"><span data-stu-id="3f2ac-142">That the following namespaces be imported:</span></span>

  [!code-csharp[TimeZone2.Serialization#2](../../../samples/snippets/csharp/VS_Snippets_CLR/TimeZone2.Serialization/cs/SerializeTimeZoneData.cs#2)]
  [!code-vb[TimeZone2.Serialization#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/TimeZone2.Serialization/vb/SerializeTimeZoneData.vb#2)]

## <a name="see-also"></a><span data-ttu-id="3f2ac-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f2ac-143">See also</span></span>

* [<span data-ttu-id="3f2ac-144">Dates, heures et fuseaux horaires</span><span class="sxs-lookup"><span data-stu-id="3f2ac-144">Dates, times, and time zones</span></span>](../../../docs/standard/datetime/index.md)
* [<span data-ttu-id="3f2ac-145">Vue d’ensemble des fuseaux horaires</span><span class="sxs-lookup"><span data-stu-id="3f2ac-145">Time zone overview</span></span>](../../../docs/standard/datetime/time-zone-overview.md)
* [<span data-ttu-id="3f2ac-146">Guide pratique pour restaurer des fuseaux horaires dans une ressource incorporée</span><span class="sxs-lookup"><span data-stu-id="3f2ac-146">How to: Restore time zones from an embedded resource</span></span>](../../../docs/standard/datetime/restore-time-zones-from-an-embedded-resource.md)
