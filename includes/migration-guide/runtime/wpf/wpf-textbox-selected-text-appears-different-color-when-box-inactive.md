---
ms.openlocfilehash: 74ce1bbc9a887aee3a33eaf05084e8c2000967c2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235386"
---
### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a><span data-ttu-id="8262b-101">Le texte sélectionné dans la zone de texte WPF sélectionnée s’affiche dans une autre couleur quand la zone de texte est inactive</span><span class="sxs-lookup"><span data-stu-id="8262b-101">WPF TextBox selected text appears a different color when the text box is inactive</span></span>

|   |   |
|---|---|
|<span data-ttu-id="8262b-102">Détails</span><span class="sxs-lookup"><span data-stu-id="8262b-102">Details</span></span>|<span data-ttu-id="8262b-103">Dans .NET Framework 4.5, quand un contrôle de zone de texte WPF est inactif (c’est-à-dire qu’il n’a pas le focus), le texte sélectionné dans la zone s’affiche dans une couleur différente de celle utilisée quand le contrôle est actif.</span><span class="sxs-lookup"><span data-stu-id="8262b-103">In .NET Framework 4.5, when a WPF text box control is inactive (it doesn't have focus), the selected text inside the box will appear a different color than when the control is active.</span></span>|
|<span data-ttu-id="8262b-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="8262b-104">Suggestion</span></span>|<span data-ttu-id="8262b-105">Vous pouvez restaurer le comportement précédent (.NET Framework 4.0) en affectant la valeur <code>false</code> à la propriété <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported>.</span><span class="sxs-lookup"><span data-stu-id="8262b-105">The previous (.NET Framework 4.0) behavior may be restored by setting the <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> property to <code>false</code>.</span></span>|
|<span data-ttu-id="8262b-106">Portée</span><span class="sxs-lookup"><span data-stu-id="8262b-106">Scope</span></span>|<span data-ttu-id="8262b-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8262b-107">Edge</span></span>|
|<span data-ttu-id="8262b-108">Version</span><span class="sxs-lookup"><span data-stu-id="8262b-108">Version</span></span>|<span data-ttu-id="8262b-109">4.5</span><span class="sxs-lookup"><span data-stu-id="8262b-109">4.5</span></span>|
|<span data-ttu-id="8262b-110">Type</span><span class="sxs-lookup"><span data-stu-id="8262b-110">Type</span></span>|<span data-ttu-id="8262b-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="8262b-111">Runtime</span></span>|
|<span data-ttu-id="8262b-112">API affectées</span><span class="sxs-lookup"><span data-stu-id="8262b-112">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|
