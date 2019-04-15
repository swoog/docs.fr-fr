---
ms.openlocfilehash: 2278d82d5362fe217ca4bce02a052d4b440843c2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236652"
---
### <a name="aspnet-mvc-now-escapes-spaces-in-strings-passed-in-via-route-parameters"></a><span data-ttu-id="6cae7-101">ASP.NET MVC place désormais dans une séquence d’échappement les espaces dans les chaînes passées via des paramètres d’itinéraire</span><span class="sxs-lookup"><span data-stu-id="6cae7-101">ASP.NET MVC now escapes spaces in strings passed in via route parameters</span></span>

|   |   |
|---|---|
|<span data-ttu-id="6cae7-102">Détails</span><span class="sxs-lookup"><span data-stu-id="6cae7-102">Details</span></span>|<span data-ttu-id="6cae7-103">Pour des raisons de conformité à la norme RFC 2396, les espaces situés dans les itinéraires de routage sont désormais échappés lors du remplissage des paramètres d’action à partir d’un itinéraire.</span><span class="sxs-lookup"><span data-stu-id="6cae7-103">In order to conform to RFC 2396, spaces in route paths are now escaped when populating action parameters from a route.</span></span> <span data-ttu-id="6cae7-104">Dans les versions précédentes, <code>/controller/action/some data</code> correspondait à l’itinéraire <code>/controller/action/{data}</code> et fournissait <code>some data</code> comme paramètre de données. Désormais, il fournit <code>some%20data</code> à la place.</span><span class="sxs-lookup"><span data-stu-id="6cae7-104">So, whereas  <code>/controller/action/some data</code> would previously match the route <code>/controller/action/{data}</code> and provide <code>some data</code> as the data parameter, it will now provide <code>some%20data</code> instead.</span></span>|
|<span data-ttu-id="6cae7-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="6cae7-105">Suggestion</span></span>|<span data-ttu-id="6cae7-106">Le code doit être mis à jour pour ne plus échapper les paramètres de chaîne à partir d’un itinéraire.</span><span class="sxs-lookup"><span data-stu-id="6cae7-106">Code should be updated to unescape string parameters from a route.</span></span> <span data-ttu-id="6cae7-107">Si l’URI d’origine est nécessaire, vous pouvez y accéder avec l’API <xref:System.Net.HttpWebRequest.RequestUri>.OriginalString.</span><span class="sxs-lookup"><span data-stu-id="6cae7-107">If the original URI is needed, it can be accessed with the <xref:System.Net.HttpWebRequest.RequestUri>.OriginalString API.</span></span>|
|<span data-ttu-id="6cae7-108">Portée</span><span class="sxs-lookup"><span data-stu-id="6cae7-108">Scope</span></span>|<span data-ttu-id="6cae7-109">Mineur</span><span class="sxs-lookup"><span data-stu-id="6cae7-109">Minor</span></span>|
|<span data-ttu-id="6cae7-110">Version</span><span class="sxs-lookup"><span data-stu-id="6cae7-110">Version</span></span>|<span data-ttu-id="6cae7-111">4.5.2</span><span class="sxs-lookup"><span data-stu-id="6cae7-111">4.5.2</span></span>|
|<span data-ttu-id="6cae7-112">Type</span><span class="sxs-lookup"><span data-stu-id="6cae7-112">Type</span></span>|<span data-ttu-id="6cae7-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="6cae7-113">Runtime</span></span>|
|<span data-ttu-id="6cae7-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="6cae7-114">Affected APIs</span></span>|<ul><li><xref:System.Web.Mvc.RouteAttribute.%23ctor(System.String)?displayProperty=nameWithType></li></ul>|
