---
title: 'Comment : accéder aux objets de fuseau UTC et l’heure locale prédéfinis'
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
ms.openlocfilehash: f074e6f6d9b11cc7d7405adced3a4523a31676fa
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44086911"
---
# <a name="how-to-access-the-predefined-utc-and-local-time-zone-objects"></a><span data-ttu-id="dc87b-102">Comment : accéder aux objets de fuseau UTC et l’heure locale prédéfinis</span><span class="sxs-lookup"><span data-stu-id="dc87b-102">How to: Access the predefined UTC and local time zone objects</span></span>

<span data-ttu-id="dc87b-103">Le <xref:System.TimeZoneInfo> classe fournit deux propriétés, <xref:System.TimeZoneInfo.Utc%2A> et <xref:System.TimeZoneInfo.Local%2A>, qui vous offrent votre code d’accéder aux objets de fuseau horaire prédéfini.</span><span class="sxs-lookup"><span data-stu-id="dc87b-103">The <xref:System.TimeZoneInfo> class provides two properties, <xref:System.TimeZoneInfo.Utc%2A> and <xref:System.TimeZoneInfo.Local%2A>, that give your code access to predefined time zone objects.</span></span> <span data-ttu-id="dc87b-104">Cette rubrique explique comment accéder aux objets <xref:System.TimeZoneInfo> retournés par ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dc87b-104">This topic discusses how to access the <xref:System.TimeZoneInfo> objects returned by those properties.</span></span>

### <a name="to-access-the-coordinated-universal-time-utc-timezoneinfo-object"></a><span data-ttu-id="dc87b-105">Pour accéder à l’objet TimeZoneInfo de temps universel coordonné (UTC)</span><span class="sxs-lookup"><span data-stu-id="dc87b-105">To access the Coordinated Universal Time (UTC) TimeZoneInfo object</span></span>

1. <span data-ttu-id="dc87b-106">Utilisez le `static` (`Shared` en Visual Basic) <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> propriété à laquelle accéder temps universel coordonné.</span><span class="sxs-lookup"><span data-stu-id="dc87b-106">Use the `static` (`Shared` in Visual Basic) <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> property to access Coordinated Universal Time.</span></span>

2. <span data-ttu-id="dc87b-107">Au lieu d’affecter le <xref:System.TimeZoneInfo> objet retourné par la propriété à une variable objet, continuer à accéder au temps universel coordonné via la <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="dc87b-107">Rather than assigning the <xref:System.TimeZoneInfo> object returned by the property to an object variable, continue to access Coordinated Universal Time through the <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> property.</span></span>

### <a name="to-access-the-local-time-zone"></a><span data-ttu-id="dc87b-108">Pour accéder au fuseau horaire local</span><span class="sxs-lookup"><span data-stu-id="dc87b-108">To access the local time zone</span></span>

1. <span data-ttu-id="dc87b-109">Utilisez le `static` (`Shared` en Visual Basic) <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> propriété pour accéder au fuseau horaire de système local.</span><span class="sxs-lookup"><span data-stu-id="dc87b-109">Use the `static` (`Shared` in Visual Basic) <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> property to access the local system time zone.</span></span>

2. <span data-ttu-id="dc87b-110">Au lieu d’affecter le <xref:System.TimeZoneInfo> objet retourné par la propriété à une variable objet, continuer à accéder au fuseau horaire local via le <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="dc87b-110">Rather than assigning the <xref:System.TimeZoneInfo> object returned by the property to an object variable, continue to access the local time zone through the <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> property.</span></span>

## <a name="example"></a><span data-ttu-id="dc87b-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc87b-111">Example</span></span>

<span data-ttu-id="dc87b-112">Le code suivant utilise la <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> et <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> propriétés pour convertir une heure du fuseau horaire des États-Unis et Canada est Standard, ainsi que pour afficher le nom de fuseau horaire dans la console.</span><span class="sxs-lookup"><span data-stu-id="dc87b-112">The following code uses the <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> and <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> properties to convert a time from the U.S. and Canadian Eastern Standard time zone, as well as to display the time zone name to the console.</span></span>

[!code-csharp[System.TimeZone2.Concepts#13](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Concepts/CS/TimeZone2Concepts.cs#13)]
[!code-vb[System.TimeZone2.Concepts#13](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Concepts/VB/TimeZone2Concepts.vb#13)]

<span data-ttu-id="dc87b-113">Vous devez toujours accéder au fuseau horaire local via le <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> propriété plutôt qu’en affectant l’heure locale de la zone à une <xref:System.TimeZoneInfo> variable objet.</span><span class="sxs-lookup"><span data-stu-id="dc87b-113">You should always access the local time zone through the <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> property rather than assigning the local time zone to a <xref:System.TimeZoneInfo> object variable.</span></span> <span data-ttu-id="dc87b-114">De même, vous devez toujours accéder à temps universel coordonné via la <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> propriété plutôt qu’en affectant l’heure UTC de la zone à une <xref:System.TimeZoneInfo> variable objet.</span><span class="sxs-lookup"><span data-stu-id="dc87b-114">Similarly, you should always access Coordinated Universal Time through the <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> property rather than assigning the UTC zone to a <xref:System.TimeZoneInfo> object variable.</span></span> <span data-ttu-id="dc87b-115">Cela empêche le <xref:System.TimeZoneInfo> variable objet d’être invalidée par un appel à la <xref:System.TimeZoneInfo.ClearCachedData%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="dc87b-115">This prevents the <xref:System.TimeZoneInfo> object variable from being invalidated by a call to the <xref:System.TimeZoneInfo.ClearCachedData%2A?displayProperty=nameWithType> method.</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="dc87b-116">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="dc87b-116">Compiling the code</span></span>

<span data-ttu-id="dc87b-117">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="dc87b-117">This example requires:</span></span>

* <span data-ttu-id="dc87b-118">Qu’une référence à System.Core.dll être ajoutée au projet.</span><span class="sxs-lookup"><span data-stu-id="dc87b-118">That a reference to System.Core.dll be added to the project.</span></span>

* <span data-ttu-id="dc87b-119">Que le <xref:System> espace de noms importés avec le `using` instruction (requise en code c#).</span><span class="sxs-lookup"><span data-stu-id="dc87b-119">That the <xref:System> namespace be imported with the `using` statement (required in C# code).</span></span>

## <a name="see-also"></a><span data-ttu-id="dc87b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc87b-120">See also</span></span>

* [<span data-ttu-id="dc87b-121">Dates, heures et fuseaux horaires</span><span class="sxs-lookup"><span data-stu-id="dc87b-121">Dates, times, and time zones</span></span>](../../../docs/standard/datetime/index.md)
* [<span data-ttu-id="dc87b-122">Recherche des fuseaux horaires définis sur un système local</span><span class="sxs-lookup"><span data-stu-id="dc87b-122">Finding the time zones defined on a local system</span></span>](../../../docs/standard/datetime/finding-the-time-zones-on-local-system.md)
* [<span data-ttu-id="dc87b-123">Guide pratique pour instancier un objet TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="dc87b-123">How to: Instantiate a TimeZoneInfo object</span></span>](../../../docs/standard/datetime/instantiate-time-zone-info.md)
