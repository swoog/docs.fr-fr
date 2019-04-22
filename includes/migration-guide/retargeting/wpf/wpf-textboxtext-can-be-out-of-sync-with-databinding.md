---
ms.openlocfilehash: 8b0617d8f021a9534289fd7ae8539cd054684862
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774339"
---
### <a name="wpf-textboxtext-can-be-out-of-sync-with-databinding"></a><span data-ttu-id="f825d-101">Dans WPF, TextBox.Text et la liaison de données peuvent être désynchronisés</span><span class="sxs-lookup"><span data-stu-id="f825d-101">WPF TextBox.Text can be out-of-sync with databinding</span></span>

|   |   |
|---|---|
|<span data-ttu-id="f825d-102">Détails</span><span class="sxs-lookup"><span data-stu-id="f825d-102">Details</span></span>|<span data-ttu-id="f825d-103">Dans certains cas, la propriété <xref:System.Windows.Controls.TextBox.Text> reflète une valeur précédente de la propriété liée aux données si cette propriété est modifiée au cours d'une opération d'écriture de liaison de données.</span><span class="sxs-lookup"><span data-stu-id="f825d-103">In some cases, the <xref:System.Windows.Controls.TextBox.Text> property reflects a previous value of the databound property value if the property is modified during a databinding write operation.</span></span>|
|<span data-ttu-id="f825d-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="f825d-104">Suggestion</span></span>|<span data-ttu-id="f825d-105">Cela ne doit pas avoir d'impact négatif.</span><span class="sxs-lookup"><span data-stu-id="f825d-105">This should have no negative impact.</span></span> <span data-ttu-id="f825d-106">Vous pouvez, cependant, restaurer le comportement précédent en affectant à la propriété <xref:System.Windows.FrameworkCompatibilityPreferences.KeepTextBoxDisplaySynchronizedWithTextProperty> la valeur <code>false</code>.</span><span class="sxs-lookup"><span data-stu-id="f825d-106">However, you can restore the previous behavior by setting the <xref:System.Windows.FrameworkCompatibilityPreferences.KeepTextBoxDisplaySynchronizedWithTextProperty> property to <code>false</code>.</span></span>|
|<span data-ttu-id="f825d-107">Portée</span><span class="sxs-lookup"><span data-stu-id="f825d-107">Scope</span></span>|<span data-ttu-id="f825d-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f825d-108">Edge</span></span>|
|<span data-ttu-id="f825d-109">Version</span><span class="sxs-lookup"><span data-stu-id="f825d-109">Version</span></span>|<span data-ttu-id="f825d-110">4.5</span><span class="sxs-lookup"><span data-stu-id="f825d-110">4.5</span></span>|
|<span data-ttu-id="f825d-111">Type</span><span class="sxs-lookup"><span data-stu-id="f825d-111">Type</span></span>|<span data-ttu-id="f825d-112">Reciblage</span><span class="sxs-lookup"><span data-stu-id="f825d-112">Retargeting</span></span>|
|<span data-ttu-id="f825d-113">API affectées</span><span class="sxs-lookup"><span data-stu-id="f825d-113">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.TextBox.Text?displayProperty=nameWithType></li></ul>|
