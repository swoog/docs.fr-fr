---
ms.openlocfilehash: 1721d32f8cdc9b6ea4b4732e38afa56a8a532600
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234730"
---
### <a name="dbparameterprecision-and-dbparameterscale-are-now-public-virtual-members"></a><span data-ttu-id="658c4-101">DbParameter.Precision et DbParameter.Scale sont maintenant des membres virtuels publics</span><span class="sxs-lookup"><span data-stu-id="658c4-101">DbParameter.Precision and DbParameter.Scale are now public virtual members</span></span>

|   |   |
|---|---|
|<span data-ttu-id="658c4-102">Détails</span><span class="sxs-lookup"><span data-stu-id="658c4-102">Details</span></span>|<xref:System.Data.Common.DbParameter.Precision> <span data-ttu-id="658c4-103">et <xref:System.Data.Common.DbParameter.Scale> sont implémentées en tant que propriétés virtuelles publiques.</span><span class="sxs-lookup"><span data-stu-id="658c4-103">and <xref:System.Data.Common.DbParameter.Scale> are implemented as public virtual properties.</span></span> <span data-ttu-id="658c4-104">Elles remplacent les implémentations d'interface explicites correspondantes, <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Precision> et <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Scale>.</span><span class="sxs-lookup"><span data-stu-id="658c4-104">They replace the corresponding explicit interface implementations, <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Precision> and <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Scale>.</span></span>|
|<span data-ttu-id="658c4-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="658c4-105">Suggestion</span></span>|<span data-ttu-id="658c4-106">Lorsque vous régénérez un fournisseur de base de données ADO.NET, vous devez désormais appliquer le mot clé « override » aux propriétés Precision et Scale.</span><span class="sxs-lookup"><span data-stu-id="658c4-106">When re-building an ADO.NET database provider, these differences will require the 'override' keyword to be applied to the Precision and Scale properties.</span></span> <span data-ttu-id="658c4-107">Cette opération est nécessaire uniquement si vous régénérez les composants. Les fichiers binaires existants continuent de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="658c4-107">This is only needed when re-building the components; existing binaries will continue to work.</span></span>|
|<span data-ttu-id="658c4-108">Portée</span><span class="sxs-lookup"><span data-stu-id="658c4-108">Scope</span></span>|<span data-ttu-id="658c4-109">Mineur</span><span class="sxs-lookup"><span data-stu-id="658c4-109">Minor</span></span>|
|<span data-ttu-id="658c4-110">Version</span><span class="sxs-lookup"><span data-stu-id="658c4-110">Version</span></span>|<span data-ttu-id="658c4-111">4.5.1</span><span class="sxs-lookup"><span data-stu-id="658c4-111">4.5.1</span></span>|
|<span data-ttu-id="658c4-112">Type</span><span class="sxs-lookup"><span data-stu-id="658c4-112">Type</span></span>|<span data-ttu-id="658c4-113">Reciblage</span><span class="sxs-lookup"><span data-stu-id="658c4-113">Retargeting</span></span>|
|<span data-ttu-id="658c4-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="658c4-114">Affected APIs</span></span>|<ul><li><xref:System.Data.Common.DbParameter.Precision?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbParameter.Scale?displayProperty=nameWithType></li></ul>|
