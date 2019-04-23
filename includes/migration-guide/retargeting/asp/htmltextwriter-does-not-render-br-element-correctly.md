---
ms.openlocfilehash: e600b8249096eecb13f63ea00343a771a8c12b60
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803913"
---
### <a name="htmltextwriter-does-not-render-br-element-correctly"></a><span data-ttu-id="1f9cd-101">HtmlTextWriter n’effectue pas correctement le rendu de l’élément `<br/>`</span><span class="sxs-lookup"><span data-stu-id="1f9cd-101">HtmlTextWriter does not render `<br/>` element correctly</span></span>

|   |   |
|---|---|
|<span data-ttu-id="1f9cd-102">Détails</span><span class="sxs-lookup"><span data-stu-id="1f9cd-102">Details</span></span>|<span data-ttu-id="1f9cd-103">À compter de la version 4.6 du .NET Framework, l’appel de <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> et <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> avec un élément <code>&lt;BR /&gt;</code> aboutit à l’insertion d’un seul <code>&lt;BR /&gt;</code> (au lieu de deux).</span><span class="sxs-lookup"><span data-stu-id="1f9cd-103">Beginning in the .NET Framework 4.6, calling <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> and <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> with a <code>&lt;BR /&gt;</code> element will correctly insert only one <code>&lt;BR /&gt;</code> (instead of two)</span></span>|
|<span data-ttu-id="1f9cd-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="1f9cd-104">Suggestion</span></span>|<span data-ttu-id="1f9cd-105">Si une application dépendait de la balise <code>&lt;BR /&gt;</code> supplémentaire, <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> doit être appelé une deuxième fois.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-105">If an app depended on the extra <code>&lt;BR /&gt;</code> tag, <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> should be called a second time.</span></span> <span data-ttu-id="1f9cd-106">Notez que ce changement de comportement affecte uniquement les applications qui ciblent .NET Framework 4.6 ou les versions ultérieures. Vous pouvez donc également cibler une version antérieure du .NET Framework pour obtenir l’ancien comportement.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-106">Note that this behavior change only affects apps that target the .NET Framework 4.6 or later, so another option is to target a previous version of the .NET Framework in order to get the old behavior.</span></span>|
|<span data-ttu-id="1f9cd-107">Portée</span><span class="sxs-lookup"><span data-stu-id="1f9cd-107">Scope</span></span>|<span data-ttu-id="1f9cd-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1f9cd-108">Edge</span></span>|
|<span data-ttu-id="1f9cd-109">Version</span><span class="sxs-lookup"><span data-stu-id="1f9cd-109">Version</span></span>|<span data-ttu-id="1f9cd-110">4.6</span><span class="sxs-lookup"><span data-stu-id="1f9cd-110">4.6</span></span>|
|<span data-ttu-id="1f9cd-111">Type</span><span class="sxs-lookup"><span data-stu-id="1f9cd-111">Type</span></span>|<span data-ttu-id="1f9cd-112">Reciblage</span><span class="sxs-lookup"><span data-stu-id="1f9cd-112">Retargeting</span></span>|
|<span data-ttu-id="1f9cd-113">API affectées</span><span class="sxs-lookup"><span data-stu-id="1f9cd-113">Affected APIs</span></span>|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|
