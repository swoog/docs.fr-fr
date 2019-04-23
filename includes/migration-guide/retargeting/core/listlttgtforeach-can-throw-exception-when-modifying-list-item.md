---
ms.openlocfilehash: 4e81087431091dfa4d5432d5ea5e2b665be2b130
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234746"
---
### <a name="listtforeach-can-throw-exception-when-modifying-list-item"></a><span data-ttu-id="73c84-101">List\<T>.ForEach risque de lever une exception en cas de modification d’un élément de liste</span><span class="sxs-lookup"><span data-stu-id="73c84-101">List\<T>.ForEach can throw exception when modifying list item</span></span>

|   |   |
|---|---|
|<span data-ttu-id="73c84-102">Détails</span><span class="sxs-lookup"><span data-stu-id="73c84-102">Details</span></span>|<span data-ttu-id="73c84-103">À compter de .NET Framework 4.5, un énumérateur <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> lève une exception <xref:System.InvalidOperationException?displayProperty=name> si un élément de la collection appelante est modifié.</span><span class="sxs-lookup"><span data-stu-id="73c84-103">Beginning in .NET Framework 4.5, a <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> enumerator will throw an <xref:System.InvalidOperationException?displayProperty=name> exception if an element in the calling collection is modified.</span></span> <span data-ttu-id="73c84-104">Avant, il ne levait pas d’exception, mais pouvait entraîner des conditions de concurrence.</span><span class="sxs-lookup"><span data-stu-id="73c84-104">Previously, this would not throw an exception but could lead to race conditions.</span></span>|
|<span data-ttu-id="73c84-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="73c84-105">Suggestion</span></span>|<span data-ttu-id="73c84-106">Dans l’idéal, le code doit être corrigé de manière à ne pas modifier les listes pendant l’énumération de leurs éléments, car cela n’est jamais une opération sûre.</span><span class="sxs-lookup"><span data-stu-id="73c84-106">Ideally, code should be fixed to not modify lists while enumerating their elements because that is never a safe operation.</span></span> <span data-ttu-id="73c84-107">Cependant, pour restaurer le comportement précédent, une application peut cibler .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="73c84-107">To revert to the previous behavior, though, an app may target .NET Framework 4.0.</span></span>|
|<span data-ttu-id="73c84-108">Portée</span><span class="sxs-lookup"><span data-stu-id="73c84-108">Scope</span></span>|<span data-ttu-id="73c84-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73c84-109">Edge</span></span>|
|<span data-ttu-id="73c84-110">Version</span><span class="sxs-lookup"><span data-stu-id="73c84-110">Version</span></span>|<span data-ttu-id="73c84-111">4.5</span><span class="sxs-lookup"><span data-stu-id="73c84-111">4.5</span></span>|
|<span data-ttu-id="73c84-112">Type</span><span class="sxs-lookup"><span data-stu-id="73c84-112">Type</span></span>|<span data-ttu-id="73c84-113">Reciblage</span><span class="sxs-lookup"><span data-stu-id="73c84-113">Retargeting</span></span>|
|<span data-ttu-id="73c84-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="73c84-114">Affected APIs</span></span>|<ul><li><xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})?displayProperty=nameWithType></li></ul>|
