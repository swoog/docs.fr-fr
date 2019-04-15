---
ms.openlocfilehash: 77e04333ed2b9a5ca8b900c1355fb5b12957772d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234705"
---
### <a name="machinekeyencode-and-machinekeydecode-methods-are-now-obsolete"></a><span data-ttu-id="35487-101">Les méthodes MachineKey.Encode et MachineKey.Decode sont maintenant obsolètes</span><span class="sxs-lookup"><span data-stu-id="35487-101">MachineKey.Encode and MachineKey.Decode methods are now obsolete</span></span>

|   |   |
|---|---|
|<span data-ttu-id="35487-102">Détails</span><span class="sxs-lookup"><span data-stu-id="35487-102">Details</span></span>|<span data-ttu-id="35487-103">Ces méthodes sont désormais obsolètes.</span><span class="sxs-lookup"><span data-stu-id="35487-103">These methods are now obsolete.</span></span> <span data-ttu-id="35487-104">La compilation du code qui appelle ces méthodes génère un avertissement du compilateur.</span><span class="sxs-lookup"><span data-stu-id="35487-104">Compilation of code that calls these methods produces a compiler warning.</span></span>|
|<span data-ttu-id="35487-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="35487-105">Suggestion</span></span>|<span data-ttu-id="35487-106">Les alternatives recommandées sont <xref:System.Web.Security.MachineKey.Protect(System.Byte[],System.String[])> et <xref:System.Web.Security.MachineKey.Unprotect(System.Byte[],System.String[])>.</span><span class="sxs-lookup"><span data-stu-id="35487-106">The recommended alternatives are <xref:System.Web.Security.MachineKey.Protect(System.Byte[],System.String[])> and <xref:System.Web.Security.MachineKey.Unprotect(System.Byte[],System.String[])>.</span></span> <span data-ttu-id="35487-107">Vous pouvez également supprimer les avertissements de génération, ou les éviter en utilisant un compilateur plus ancien.</span><span class="sxs-lookup"><span data-stu-id="35487-107">Alternatively, the build warnings can be suppressed, or they can be avoided by using an older compiler.</span></span> <span data-ttu-id="35487-108">Ces API sont toujours prises en charge.</span><span class="sxs-lookup"><span data-stu-id="35487-108">The APIs are still supported.</span></span>|
|<span data-ttu-id="35487-109">Portée</span><span class="sxs-lookup"><span data-stu-id="35487-109">Scope</span></span>|<span data-ttu-id="35487-110">Mineur</span><span class="sxs-lookup"><span data-stu-id="35487-110">Minor</span></span>|
|<span data-ttu-id="35487-111">Version</span><span class="sxs-lookup"><span data-stu-id="35487-111">Version</span></span>|<span data-ttu-id="35487-112">4.5</span><span class="sxs-lookup"><span data-stu-id="35487-112">4.5</span></span>|
|<span data-ttu-id="35487-113">Type</span><span class="sxs-lookup"><span data-stu-id="35487-113">Type</span></span>|<span data-ttu-id="35487-114">Reciblage</span><span class="sxs-lookup"><span data-stu-id="35487-114">Retargeting</span></span>|
|<span data-ttu-id="35487-115">API affectées</span><span class="sxs-lookup"><span data-stu-id="35487-115">Affected APIs</span></span>|<ul><li><xref:System.Web.Security.MachineKey.Encode(System.Byte[],System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li><li><xref:System.Web.Security.MachineKey.Decode(System.String,System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li></ul>|
