---
ms.openlocfilehash: 4c6a89f9753989a5ad061e847dff70d2af0b3cf4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774342"
---
### <a name="entity-framework-version-must-match-the-net-framework-version"></a><span data-ttu-id="67b0b-101">La version d’Entity Framework doit correspondre à la version du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="67b0b-101">Entity Framework version must match the .NET Framework version</span></span>

|   |   |
|---|---|
|<span data-ttu-id="67b0b-102">Détails</span><span class="sxs-lookup"><span data-stu-id="67b0b-102">Details</span></span>|<span data-ttu-id="67b0b-103">La version d’Entity Framework doit être mise en correspondance avec la version du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="67b0b-103">The entity framework version should be matched with the .NET framework version.</span></span> <span data-ttu-id="67b0b-104">Entity Framework 5 est recommandé pour .NET Framework 4.5.</span><span class="sxs-lookup"><span data-stu-id="67b0b-104">Entity Framework 5 is recommended for .NET Framework 4.5.</span></span> <span data-ttu-id="67b0b-105">Il existe certains problèmes connus avec EF 4.x dans un projet .NET Framework 4.5 concernant <xref:System.ComponentModel.DataAnnotations>.</span><span class="sxs-lookup"><span data-stu-id="67b0b-105">There are some known issues with EF 4.x in a .NET Framework 4.5 project around <xref:System.ComponentModel.DataAnnotations>.</span></span> <span data-ttu-id="67b0b-106">Dans .NET 4.5, les annotations ont été déplacées vers un autre assembly. De ce fait, la détermination des annotations à utiliser pose problème.</span><span class="sxs-lookup"><span data-stu-id="67b0b-106">In .NET 4.5, these were moved to a different assembly, so there are issues determining which annotations to use.</span></span>|
|<span data-ttu-id="67b0b-107">Suggestion</span><span class="sxs-lookup"><span data-stu-id="67b0b-107">Suggestion</span></span>|<span data-ttu-id="67b0b-108">Mise à niveau vers Entity Framework 5 pour .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="67b0b-108">Upgrade to Entity Framework 5 for .NET Framework 4.5</span></span>|
|<span data-ttu-id="67b0b-109">Portée</span><span class="sxs-lookup"><span data-stu-id="67b0b-109">Scope</span></span>|<span data-ttu-id="67b0b-110">Majeur</span><span class="sxs-lookup"><span data-stu-id="67b0b-110">Major</span></span>|
|<span data-ttu-id="67b0b-111">Version</span><span class="sxs-lookup"><span data-stu-id="67b0b-111">Version</span></span>|<span data-ttu-id="67b0b-112">4.5</span><span class="sxs-lookup"><span data-stu-id="67b0b-112">4.5</span></span>|
|<span data-ttu-id="67b0b-113">Type</span><span class="sxs-lookup"><span data-stu-id="67b0b-113">Type</span></span>|<span data-ttu-id="67b0b-114">Reciblage</span><span class="sxs-lookup"><span data-stu-id="67b0b-114">Retargeting</span></span>|
