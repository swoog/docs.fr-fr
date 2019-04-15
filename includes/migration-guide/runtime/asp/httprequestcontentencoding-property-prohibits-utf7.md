---
ms.openlocfilehash: 668d047d3247d64cb1400d4a9ea6887795fa0d44
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235227"
---
### <a name="httprequestcontentencoding-property-prohibits-utf7"></a><span data-ttu-id="b7dad-101">La propriété HttpRequest.ContentEncoding interdit UTF7</span><span class="sxs-lookup"><span data-stu-id="b7dad-101">HttpRequest.ContentEncoding property prohibits UTF7</span></span>

|   |   |
|---|---|
|<span data-ttu-id="b7dad-102">Détails</span><span class="sxs-lookup"><span data-stu-id="b7dad-102">Details</span></span>|<span data-ttu-id="b7dad-103">À compter de .NET Framework 4.5, l’encodage UTF-7 est interdit dans le corps des <xref:System.Web.HttpRequest?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="b7dad-103">Beginning in .NET Framework 4.5, UTF-7 encoding is prohibited in <xref:System.Web.HttpRequest?displayProperty=name>s' bodies.</span></span> <span data-ttu-id="b7dad-104">Les données des applications qui dépendent des données UTF-7 entrantes ne seront pas décodées correctement dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="b7dad-104">Data for applications that depend on incoming UTF-7 data will not decode properly in some cases.</span></span>|
|<span data-ttu-id="b7dad-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="b7dad-105">Suggestion</span></span>|<span data-ttu-id="b7dad-106">Dans l’idéal, les applications doivent être mises à jour pour ne pas utiliser l’encodage UTF-7 dans les <xref:System.Web.HttpRequest?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="b7dad-106">Ideally, applications should be updated to not use UTF-7 encoding in <xref:System.Web.HttpRequest?displayProperty=name>s.</span></span> <span data-ttu-id="b7dad-107">Vous pouvez aussi restaurer le comportement hérité à l’aide de l’attribut <code>aspnet:AllowUtf7RequestContentEncoding</code> de l’élément [appSettings](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="b7dad-107">Alternatively, legacy behavior can be restored by using the <code>aspnet:AllowUtf7RequestContentEncoding</code> attribute of the [appSettings](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) element.</span></span>|
|<span data-ttu-id="b7dad-108">Portée</span><span class="sxs-lookup"><span data-stu-id="b7dad-108">Scope</span></span>|<span data-ttu-id="b7dad-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b7dad-109">Edge</span></span>|
|<span data-ttu-id="b7dad-110">Version</span><span class="sxs-lookup"><span data-stu-id="b7dad-110">Version</span></span>|<span data-ttu-id="b7dad-111">4.5</span><span class="sxs-lookup"><span data-stu-id="b7dad-111">4.5</span></span>|
|<span data-ttu-id="b7dad-112">Type</span><span class="sxs-lookup"><span data-stu-id="b7dad-112">Type</span></span>|<span data-ttu-id="b7dad-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="b7dad-113">Runtime</span></span>|
|<span data-ttu-id="b7dad-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="b7dad-114">Affected APIs</span></span>|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|
