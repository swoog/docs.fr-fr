---
ms.openlocfilehash: de79182e326082786c1e0691f8888e30cd410f5d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235221"
---
### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a><span data-ttu-id="3c60d-101">Le nombre maximal d’annulations d’opérations pour une zone de texte WPF est de 100 par défaut</span><span class="sxs-lookup"><span data-stu-id="3c60d-101">WPF TextBox defaults to undo limit of 100</span></span>

|   |   |
|---|---|
|<span data-ttu-id="3c60d-102">Détails</span><span class="sxs-lookup"><span data-stu-id="3c60d-102">Details</span></span>|<span data-ttu-id="3c60d-103">Dans .NET Framework 4.5, le nombre maximal d’annulations d’opérations pour une zone de texte WPF est de 100 par défaut (dans .NET Framework 4.0, ce nombre était illimité).</span><span class="sxs-lookup"><span data-stu-id="3c60d-103">In .NET Framework 4.5, the default undo limit for a WPF textbox is 100 (as opposed to being unlimited in .NET Framework 4.0)</span></span>|
|<span data-ttu-id="3c60d-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="3c60d-104">Suggestion</span></span>|<span data-ttu-id="3c60d-105">Si une limite de 100 n’est pas suffisante, il est possible de définir explicitement cette valeur avec</span><span class="sxs-lookup"><span data-stu-id="3c60d-105">If an undo limit of 100 is too low, the limit can be set explicitly with</span></span> <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|<span data-ttu-id="3c60d-106">Portée</span><span class="sxs-lookup"><span data-stu-id="3c60d-106">Scope</span></span>|<span data-ttu-id="3c60d-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3c60d-107">Edge</span></span>|
|<span data-ttu-id="3c60d-108">Version</span><span class="sxs-lookup"><span data-stu-id="3c60d-108">Version</span></span>|<span data-ttu-id="3c60d-109">4.5</span><span class="sxs-lookup"><span data-stu-id="3c60d-109">4.5</span></span>|
|<span data-ttu-id="3c60d-110">Type</span><span class="sxs-lookup"><span data-stu-id="3c60d-110">Type</span></span>|<span data-ttu-id="3c60d-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="3c60d-111">Runtime</span></span>|
|<span data-ttu-id="3c60d-112">API affectées</span><span class="sxs-lookup"><span data-stu-id="3c60d-112">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|
