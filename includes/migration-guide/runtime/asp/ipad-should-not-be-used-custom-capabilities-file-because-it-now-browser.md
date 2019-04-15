---
ms.openlocfilehash: 84f570cbbd97be79426e117d4c97ec182a397fd4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235276"
---
### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a><span data-ttu-id="58f96-101">IPad ne doit pas servir dans le fichier de fonctionnalités personnalisé, car il est désormais une fonctionnalité du navigateur</span><span class="sxs-lookup"><span data-stu-id="58f96-101">IPad should not be used in custom capabilities file because it is now a browser capability</span></span>

|   |   |
|---|---|
|<span data-ttu-id="58f96-102">Détails</span><span class="sxs-lookup"><span data-stu-id="58f96-102">Details</span></span>|<span data-ttu-id="58f96-103">À compter de .NET Framework 4.5, iPad étant un identificateur dans le fichier de fonctionnalités du navigateur ASP.NET par défaut, il ne doit pas être utilisé dans un fichier de fonctionnalités personnalisé</span><span class="sxs-lookup"><span data-stu-id="58f96-103">Beginning in .NET Framework 4.5, iPad is an identifier in the default ASP.NET browser capabilities file, so it should not be used in a custom capabilities file</span></span>|
|<span data-ttu-id="58f96-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="58f96-104">Suggestion</span></span>|<span data-ttu-id="58f96-105">Si des fonctionnalités spécifiques à l’iPad sont requises, il est nécessaire de modifier le comportement de l’iPad en définissant des fonctionnalités sur la passerelle prédéfinie refID &quot;IPad&quot; et non en générant un ID &quot;IPad&quot; par mise en correspondance de l’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58f96-105">If iPad-specific capabilities are required, it is necessary to modify iPad behavior by setting capabilities on the pre-defined gateway refID &quot;IPad&quot; instead of by generating a new &quot;IPad&quot; ID by user agent matching.</span></span>|
|<span data-ttu-id="58f96-106">Portée</span><span class="sxs-lookup"><span data-stu-id="58f96-106">Scope</span></span>|<span data-ttu-id="58f96-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="58f96-107">Edge</span></span>|
|<span data-ttu-id="58f96-108">Version</span><span class="sxs-lookup"><span data-stu-id="58f96-108">Version</span></span>|<span data-ttu-id="58f96-109">4.5</span><span class="sxs-lookup"><span data-stu-id="58f96-109">4.5</span></span>|
|<span data-ttu-id="58f96-110">Type</span><span class="sxs-lookup"><span data-stu-id="58f96-110">Type</span></span>|<span data-ttu-id="58f96-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="58f96-111">Runtime</span></span>|
