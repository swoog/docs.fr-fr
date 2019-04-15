---
ms.openlocfilehash: 0056baa1e5f0cdc5bfcf8b0e83c9490ec5722926
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235356"
---
### <a name="httputilityjavascriptstringencode-escapes-ampersand"></a><span data-ttu-id="04e7c-101">HttpUtility.JavaScriptStringEncode place le caractère esperluette (&) dans une séquence d’échappement</span><span class="sxs-lookup"><span data-stu-id="04e7c-101">HttpUtility.JavaScriptStringEncode escapes ampersand</span></span>

|   |   |
|---|---|
|<span data-ttu-id="04e7c-102">Détails</span><span class="sxs-lookup"><span data-stu-id="04e7c-102">Details</span></span>|<span data-ttu-id="04e7c-103">Depuis .NET Framework 4.5, <xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name> place le caractère esperluette (&amp;) dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="04e7c-103">Starting with the .NET Framework 4.5, <xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name> escapes the ampersand (&amp;) character.</span></span>|
|<span data-ttu-id="04e7c-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="04e7c-104">Suggestion</span></span>|<span data-ttu-id="04e7c-105">Si votre application dépend du comportement précédent de cette méthode, vous pouvez ajouter un paramètre aspnet:JavaScriptDoNotEncodeAmpersand à l’[élément appSettings ASP.NET](https://docs.microsoft.com/previous-versions/aspnet/hh975440(v=vs.120)) dans votre fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="04e7c-105">If your app depends on the previous behavior of this method, you can add an aspnet:JavaScriptDoNotEncodeAmpersand setting to the [ASP.NET appSettings element](https://docs.microsoft.com/previous-versions/aspnet/hh975440(v=vs.120)) in your configuration file.</span></span>|
|<span data-ttu-id="04e7c-106">Portée</span><span class="sxs-lookup"><span data-stu-id="04e7c-106">Scope</span></span>|<span data-ttu-id="04e7c-107">Mineur</span><span class="sxs-lookup"><span data-stu-id="04e7c-107">Minor</span></span>|
|<span data-ttu-id="04e7c-108">Version</span><span class="sxs-lookup"><span data-stu-id="04e7c-108">Version</span></span>|<span data-ttu-id="04e7c-109">4.5</span><span class="sxs-lookup"><span data-stu-id="04e7c-109">4.5</span></span>|
|<span data-ttu-id="04e7c-110">Type</span><span class="sxs-lookup"><span data-stu-id="04e7c-110">Type</span></span>|<span data-ttu-id="04e7c-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="04e7c-111">Runtime</span></span>|
|<span data-ttu-id="04e7c-112">API affectées</span><span class="sxs-lookup"><span data-stu-id="04e7c-112">Affected APIs</span></span>|<ul><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|
