---
title: 'Procédure : Résoudre des heures ambiguës'
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time zones [.NET Framework], ambiguous time
- ambiguous time [.NET Framework]
ms.assetid: 2cf5fb25-492c-4875-9245-98cac8348e97
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: aae3e5145d2fa85cd55fc5b1288ef4aaa0fef48f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569290"
---
# <a name="how-to-resolve-ambiguous-times"></a><span data-ttu-id="b3303-102">Procédure : Résoudre des heures ambiguës</span><span class="sxs-lookup"><span data-stu-id="b3303-102">How to: Resolve ambiguous times</span></span>

<span data-ttu-id="b3303-103">Une heure ambiguë est une heure qui correspond à plusieurs heures UTC.</span><span class="sxs-lookup"><span data-stu-id="b3303-103">An ambiguous time is a time that maps to more than one Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="b3303-104">Cela se produit quand l’heure de l’horloge est retardée, comme lors du passage de l’heure d’été à l'heure d'hiver dans un fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="b3303-104">It occurs when the clock time is adjusted back in time, such as during the transition from a time zone's daylight saving time to its standard time.</span></span> <span data-ttu-id="b3303-105">Quand vous gérez une heure ambiguë, vous pouvez procéder de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3303-105">When handling an ambiguous time, you can do one of the following:</span></span>

* <span data-ttu-id="b3303-106">Proposez une méthode de mappage à l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="b3303-106">Make an assumption about how the time maps to UTC.</span></span> <span data-ttu-id="b3303-107">Par exemple, vous pouvez supposer qu’une heure ambiguë est toujours exprimée à l'heure d’hiver du fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="b3303-107">For example, you can assume that an ambiguous time is always expressed in the time zone's standard time.</span></span>

* <span data-ttu-id="b3303-108">Si l’heure ambiguë est un élément de données entré par l’utilisateur, vous pouvez laisser l’utilisateur résoudre l’ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="b3303-108">If the ambiguous time is an item of data entered by the user, you can leave it to the user to resolve the ambiguity.</span></span>

<span data-ttu-id="b3303-109">Cette rubrique montre comment résoudre une heure ambiguë en supposant qu’elle représente l’heure d’hiver du fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="b3303-109">This topic shows how to resolve an ambiguous time by assuming that it represents the time zone's standard time.</span></span>

### <a name="to-map-an-ambiguous-time-to-a-time-zones-standard-time"></a><span data-ttu-id="b3303-110">Pour mapper une heure ambiguë à l’heure d’hiver d’un fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="b3303-110">To map an ambiguous time to a time zone's standard time</span></span>

1. <span data-ttu-id="b3303-111">Appelez le <xref:System.TimeZoneInfo.IsAmbiguousTime%2A> méthode pour déterminer si l’heure est ambiguë.</span><span class="sxs-lookup"><span data-stu-id="b3303-111">Call the <xref:System.TimeZoneInfo.IsAmbiguousTime%2A> method to determine whether the time is ambiguous.</span></span>

2. <span data-ttu-id="b3303-112">Si l’heure est ambiguë, soustrayez l’heure de la <xref:System.TimeSpan> objet retourné par le fuseau horaire <xref:System.TimeZoneInfo.BaseUtcOffset%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="b3303-112">If the time is ambiguous, subtract the time from the <xref:System.TimeSpan> object returned by the time zone's <xref:System.TimeZoneInfo.BaseUtcOffset%2A> property.</span></span>

3. <span data-ttu-id="b3303-113">Appelez le `static` (`Shared` dans Visual Basic .NET) <xref:System.DateTime.SpecifyKind%2A> méthode pour définir la date et l’heure valeur UTC <xref:System.DateTime.Kind%2A> propriété <xref:System.DateTimeKind.Utc?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="b3303-113">Call the `static` (`Shared` in Visual Basic .NET) <xref:System.DateTime.SpecifyKind%2A> method to set the UTC date and time value's <xref:System.DateTime.Kind%2A> property to <xref:System.DateTimeKind.Utc?displayProperty=nameWithType>.</span></span>

## <a name="example"></a><span data-ttu-id="b3303-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="b3303-114">Example</span></span>

<span data-ttu-id="b3303-115">L’exemple suivant illustre comment convertir une heure ambiguë en heure UTC en supposant qu’elle représente l’heure d’hiver du fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="b3303-115">The following example illustrates how to convert an ambiguous time to UTC by assuming that it represents the local time zone's standard time.</span></span>

[!code-csharp[System.TimeZone2.Concepts#10](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Concepts/CS/TimeZone2Concepts.cs#10)]
[!code-vb[System.TimeZone2.Concepts#10](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Concepts/VB/TimeZone2Concepts.vb#10)]

<span data-ttu-id="b3303-116">L’exemple se compose d’une méthode nommée `ResolveAmbiguousTime` qui détermine si le <xref:System.DateTime> valeur passée à ce dernier est ambigu.</span><span class="sxs-lookup"><span data-stu-id="b3303-116">The example consists of a method named `ResolveAmbiguousTime` that determines whether the <xref:System.DateTime> value passed to it is ambiguous.</span></span> <span data-ttu-id="b3303-117">Si la valeur est ambiguë, la méthode retourne un <xref:System.DateTime> valeur qui représente l’heure UTC correspondante.</span><span class="sxs-lookup"><span data-stu-id="b3303-117">If the value is ambiguous, the method returns a <xref:System.DateTime> value that represents the corresponding UTC time.</span></span> <span data-ttu-id="b3303-118">La méthode gère cette conversion en soustrayant la valeur du fuseau horaire local <xref:System.TimeZoneInfo.BaseUtcOffset%2A> propriété à partir de l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="b3303-118">The method handles this conversion by subtracting the value of the local time zone's <xref:System.TimeZoneInfo.BaseUtcOffset%2A> property from the local time.</span></span>

<span data-ttu-id="b3303-119">En règle générale, une heure ambiguë est gérée en appelant le <xref:System.TimeZoneInfo.GetAmbiguousTimeOffsets%2A> méthode pour récupérer un tableau de <xref:System.TimeSpan> offsets des objets qui contiennent UTC possibles de l’heure ambiguë.</span><span class="sxs-lookup"><span data-stu-id="b3303-119">Ordinarily, an ambiguous time is handled by calling the <xref:System.TimeZoneInfo.GetAmbiguousTimeOffsets%2A> method to retrieve an array of <xref:System.TimeSpan> objects that contain the ambiguous time's possible UTC offsets.</span></span> <span data-ttu-id="b3303-120">Toutefois, cet exemple émet l’hypothèse arbitraire qu’une heure ambiguë devrait toujours être mappée à l’heure d’hiver du fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="b3303-120">However, this example makes the arbitrary assumption that an ambiguous time should always be mapped to the time zone's standard time.</span></span> <span data-ttu-id="b3303-121">Le <xref:System.TimeZoneInfo.BaseUtcOffset%2A> propriété retourne le décalage entre l’heure UTC et l’heure d’hiver d’un fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="b3303-121">The <xref:System.TimeZoneInfo.BaseUtcOffset%2A> property returns the offset between UTC and a time zone's standard time.</span></span>

<span data-ttu-id="b3303-122">Dans cet exemple, toutes les références au fuseau horaire local sont faites par le biais de la propriété <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> ; le fuseau horaire local n’est jamais affecté à une variable objet.</span><span class="sxs-lookup"><span data-stu-id="b3303-122">In this example, all references to the local time zone are made through the <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> property; the local time zone is never assigned to an object variable.</span></span> <span data-ttu-id="b3303-123">Cette pratique est recommandée, car un appel à la méthode <xref:System.TimeZoneInfo.ClearCachedData%2A?displayProperty=nameWithType> invalide tous les objets auxquels le fuseau horaire est affecté.</span><span class="sxs-lookup"><span data-stu-id="b3303-123">This is a recommended practice because a call to the <xref:System.TimeZoneInfo.ClearCachedData%2A?displayProperty=nameWithType> method invalidates any objects that the local time zone is assigned to.</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="b3303-124">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="b3303-124">Compiling the code</span></span>

<span data-ttu-id="b3303-125">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="b3303-125">This example requires:</span></span>

* <span data-ttu-id="b3303-126">Qu’une référence à System.Core.dll soit ajoutée au projet.</span><span class="sxs-lookup"><span data-stu-id="b3303-126">That a reference to System.Core.dll be added to the project.</span></span>

* <span data-ttu-id="b3303-127">Que l'espace de noms <xref:System> soit importé avec l'instruction `using` (obligatoire en C#).</span><span class="sxs-lookup"><span data-stu-id="b3303-127">That the <xref:System> namespace be imported with the `using` statement (required in C# code).</span></span>

## <a name="see-also"></a><span data-ttu-id="b3303-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3303-128">See also</span></span>

- [<span data-ttu-id="b3303-129">Dates, heures et fuseaux horaires</span><span class="sxs-lookup"><span data-stu-id="b3303-129">Dates, times, and time zones</span></span>](../../../docs/standard/datetime/index.md)
- [<span data-ttu-id="b3303-130">Guide pratique pour Permettre aux utilisateurs de résoudre des heures ambiguës</span><span class="sxs-lookup"><span data-stu-id="b3303-130">How to: Let users resolve ambiguous times</span></span>](../../../docs/standard/datetime/let-users-resolve-ambiguous-times.md)
