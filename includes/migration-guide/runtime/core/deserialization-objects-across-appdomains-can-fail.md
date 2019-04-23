---
ms.openlocfilehash: 891c29b731214fb0028e960256b79cfc267d86b9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235248"
---
### <a name="deserialization-of-objects-across-appdomains-can-fail"></a><span data-ttu-id="1285a-101">La désérialisation d’objets entre les domaines d’application peut échouer</span><span class="sxs-lookup"><span data-stu-id="1285a-101">Deserialization of objects across appdomains can fail</span></span>

|   |   |
|---|---|
|<span data-ttu-id="1285a-102">Détails</span><span class="sxs-lookup"><span data-stu-id="1285a-102">Details</span></span>|<span data-ttu-id="1285a-103">Dans certains cas, quand une application utilise deux domaines d'application ou plus avec des bases d'application différentes, une tentative de désérialisation des objets dans le contexte d'appel logique entre les domaines d'application lève une exception.</span><span class="sxs-lookup"><span data-stu-id="1285a-103">In some cases, when an app uses two or more app domains with different application bases, trying to deserialize objects in the logical call context across app domains throws an exception.</span></span>|
|<span data-ttu-id="1285a-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="1285a-104">Suggestion</span></span>|<span data-ttu-id="1285a-105">Voir [Prévention : désérialisation d’objets sur plusieurs domaines d’application](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md).</span><span class="sxs-lookup"><span data-stu-id="1285a-105">See [Mitigation: Deserialization of Objects Across App Domains](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md)</span></span>|
|<span data-ttu-id="1285a-106">Portée</span><span class="sxs-lookup"><span data-stu-id="1285a-106">Scope</span></span>|<span data-ttu-id="1285a-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1285a-107">Edge</span></span>|
|<span data-ttu-id="1285a-108">Version</span><span class="sxs-lookup"><span data-stu-id="1285a-108">Version</span></span>|<span data-ttu-id="1285a-109">4.5.1</span><span class="sxs-lookup"><span data-stu-id="1285a-109">4.5.1</span></span>|
|<span data-ttu-id="1285a-110">Type</span><span class="sxs-lookup"><span data-stu-id="1285a-110">Type</span></span>|<span data-ttu-id="1285a-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="1285a-111">Runtime</span></span>|
