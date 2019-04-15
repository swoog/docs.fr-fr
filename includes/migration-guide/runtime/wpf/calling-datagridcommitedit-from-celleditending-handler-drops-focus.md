---
ms.openlocfilehash: e2d63d85adce64db6e00b62ec17f55ae71ce3052
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235368"
---
### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a><span data-ttu-id="3431a-101">L’appel de DataGrid.CommitEdit à partir d’un gestionnaire CellEditEnding supprime le focus</span><span class="sxs-lookup"><span data-stu-id="3431a-101">Calling DataGrid.CommitEdit from a CellEditEnding handler drops focus</span></span>

|   |   |
|---|---|
|<span data-ttu-id="3431a-102">Détails</span><span class="sxs-lookup"><span data-stu-id="3431a-102">Details</span></span>|<span data-ttu-id="3431a-103">L’appel de <xref:System.Windows.Controls.DataGrid.CommitEdit> depuis un des gestionnaires d’événements <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> de <xref:System.Windows.Controls.DataGrid?displayProperty=name> fait que <xref:System.Windows.Controls.DataGrid?displayProperty=name> perd le focus.</span><span class="sxs-lookup"><span data-stu-id="3431a-103">Calling <xref:System.Windows.Controls.DataGrid.CommitEdit> from one of the <xref:System.Windows.Controls.DataGrid?displayProperty=name>'s <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> event handlers causes the <xref:System.Windows.Controls.DataGrid?displayProperty=name> to lose focus.</span></span>|
|<span data-ttu-id="3431a-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="3431a-104">Suggestion</span></span>|<span data-ttu-id="3431a-105">Ce bogue a été résolu dans le .NET Framework 4.5.2. Vous pouvez donc l’éviter en mettant à niveau votre version du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3431a-105">This bug has been fixed in the .NET Framework 4.5.2, so it can be avoided by upgrading the .NET Framework.</span></span> <span data-ttu-id="3431a-106">Vous pouvez également contourner ce problème en resélectionnant explicitement <xref:System.Windows.Controls.DataGrid?displayProperty=name> après avoir appelé <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="3431a-106">Alternatively, it can be avoided by explicitly re-selecting the <xref:System.Windows.Controls.DataGrid?displayProperty=name> after calling <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.</span></span>|
|<span data-ttu-id="3431a-107">Portée</span><span class="sxs-lookup"><span data-stu-id="3431a-107">Scope</span></span>|<span data-ttu-id="3431a-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3431a-108">Edge</span></span>|
|<span data-ttu-id="3431a-109">Version</span><span class="sxs-lookup"><span data-stu-id="3431a-109">Version</span></span>|<span data-ttu-id="3431a-110">4.5</span><span class="sxs-lookup"><span data-stu-id="3431a-110">4.5</span></span>|
|<span data-ttu-id="3431a-111">Type</span><span class="sxs-lookup"><span data-stu-id="3431a-111">Type</span></span>|<span data-ttu-id="3431a-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="3431a-112">Runtime</span></span>|
|<span data-ttu-id="3431a-113">API affectées</span><span class="sxs-lookup"><span data-stu-id="3431a-113">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|
