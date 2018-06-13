---
title: Nouveautés du .NET Framework dans le domaine de l’accessibilité
ms.custom: updateeachrelease
ms.date: 04/10/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- what's new [.NET Framework]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7fe7e15e482028b9988d7e560b98be19b6c07427
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33509214"
---
# <a name="whats-new-in-accessibility-in-the-net-framework"></a><span data-ttu-id="120cb-102">Nouveautés du .NET Framework dans le domaine de l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="120cb-102">What's new in accessibility in the .NET Framework</span></span>

<span data-ttu-id="120cb-103">Le .NET Framework vise à rendre les applications plus accessibles pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="120cb-103">The .NET Framework aims at making applications more accessible for your users.</span></span> <span data-ttu-id="120cb-104">Les fonctionnalités d’accessibilité permettent à une application de fournir une expérience appropriée pour les utilisateurs des technologies d’assistance.</span><span class="sxs-lookup"><span data-stu-id="120cb-104">Accessibility features allow an application to provide an appropriate experience for users of Assistive Technology.</span></span> <span data-ttu-id="120cb-105">À compter de .NET Framework 4.7.1, le .NET Framework inclut un grand nombre d’améliorations en matière d’accessibilité qui permettent aux développeurs de créer des applications accessibles.</span><span class="sxs-lookup"><span data-stu-id="120cb-105">Starting with the .NET Framework 4.7.1, the .NET Framework includes a large number of accessibility improvements that allow developers to create accessible applications.</span></span> 

## <a name="accessibility-switches"></a><span data-ttu-id="120cb-106">Commutateurs d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="120cb-106">Accessibility switches</span></span>

<span data-ttu-id="120cb-107">Si votre application cible .NET Framework 4.7 ou une version antérieure, mais est exécutée sur .NET Framework 4.7.1 ou une version ultérieure, vous pouvez la configurer pour qu’elle active les fonctionnalités d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="120cb-107">You can configure your app to opt into accessibility features if it targets the .NET Framework 4.7 or an earlier version but is running on the .NET Framework 4.7.1 or later.</span></span> <span data-ttu-id="120cb-108">Si elle cible .NET Framework 4.7.1 ou une version ultérieure, vous pouvez également la configurer afin qu’elle utilise les fonctionnalités héritées (et ainsi qu’elle n’active pas les fonctionnalités d’accessibilité).</span><span class="sxs-lookup"><span data-stu-id="120cb-108">You can also configure your app to use legacy features (and not take advantage of accessibility features) if it targets the .NET Framework 4.7.1 or later.</span></span> <span data-ttu-id="120cb-109">Chaque version du .NET Framework qui inclut des fonctionnalités d’accessibilité a son propre commutateur d’accessibilité, que vous ajoutez à l’élément [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) dans la section [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) du fichier de configuration de l’application.</span><span class="sxs-lookup"><span data-stu-id="120cb-109">Each version of the .NET Framework that includes accessibility features has a version-specific accessibility switch, which you add to the [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) element in the [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) section of the application's configuration file.</span></span> <span data-ttu-id="120cb-110">Les commutateurs pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="120cb-110">The following are the supported switches:</span></span>

|<span data-ttu-id="120cb-111">Version</span><span class="sxs-lookup"><span data-stu-id="120cb-111">Version</span></span>|<span data-ttu-id="120cb-112">Basculer</span><span class="sxs-lookup"><span data-stu-id="120cb-112">Switch</span></span>|
|---|---|
|<span data-ttu-id="120cb-113">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="120cb-113">.NET Framework 4.7.1</span></span>|<span data-ttu-id="120cb-114">"Switch.UseLegacyAccessibilityFeatures"</span><span class="sxs-lookup"><span data-stu-id="120cb-114">"Switch.UseLegacyAccessibilityFeatures"</span></span>|
|<span data-ttu-id="120cb-115">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="120cb-115">.NET Framework 4.7.2</span></span>|<span data-ttu-id="120cb-116">"Switch.UseLegacyAccessibilityFeatures.2"</span><span class="sxs-lookup"><span data-stu-id="120cb-116">"Switch.UseLegacyAccessibilityFeatures.2"</span></span>|

### <a name="taking-advantage-of-accessibility-enhancements"></a><span data-ttu-id="120cb-117">Activation des nouvelles fonctionnalités d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="120cb-117">Taking advantage of accessibility enhancements</span></span>

<span data-ttu-id="120cb-118">Les nouvelles fonctionnalités d’accessibilité sont activées par défaut pour les applications qui ciblent .NET Framework 4.7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="120cb-118">The new accessibility features are enabled by default for applications that target the .NET Framework 4.7.1 or later.</span></span> <span data-ttu-id="120cb-119">De plus, pour les applications qui ciblent une version antérieure du .NET Framework mais qui sont exécutées sur .NET Framework 4.7.1 ou une version ultérieure, vous pouvez désactiver les comportements d’accessibilité hérités (et ainsi utiliser les nouvelles fonctionnalités d’accessibilité) en ajoutant des commutateurs à l’élément [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) dans la section [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) du fichier de configuration de l’application et en les définissant à la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="120cb-119">In addition, applications that target an earlier version of the .NET Framework but are running on the .NET Framework 4.7.1 or later can opt out of legacy accessibility behaviors (and thereby take advantage of accessibility improvements) by adding switches to the [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) element in the [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) section of the application's configuration file and setting their value to `false`.</span></span> <span data-ttu-id="120cb-120">Le code ci-dessous montre comment activer les nouvelles fonctionnalités d’accessibilité de .NET Framework 4.7.1 :</span><span class="sxs-lookup"><span data-stu-id="120cb-120">The following shows how to opt in to accessibility enhancements introduced in the .NET Framework 4.7.1:</span></span>

```xml
<runtime>
    <!-- AppContextSwitchOverrides value attribute is in the form of 'key1=true|false;key2=true|false  -->
    <AppContextSwitchOverrides value="Switch.UseLegacyAccessibilityFeatures=false" />
</runtime>
```

<span data-ttu-id="120cb-121">Si vous choisissez d’activer les fonctionnalités d’accessibilité d’une version ultérieure du .NET Framework, vous devez aussi activer explicitement les fonctionnalités des versions antérieures du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="120cb-121">If you choose to opt in to accessibility features in a later version of the .NET Framework, you must also explicitly opt in to the features from earlier versions of the .NET Framework.</span></span> <span data-ttu-id="120cb-122">Pour configurer votre application afin qu’elle utilise les nouvelles fonctionnalités d’accessibilité des deux versions du .NET Framework (4.7.1 et 4.7.2), vous devez ajouter l’élément [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant :</span><span class="sxs-lookup"><span data-stu-id="120cb-122">Configuring your app to take advantage of accessibility improvements in both the .NET Framework 4.7.1 and 4.7.2 requires the following [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) element:</span></span>

```xml
<runtime>
    <!-- AppContextSwitchOverrides value attribute is in the form of 'key1=true|false;key2=true|false  -->
    <AppContextSwitchOverrides value="Switch.UseLegacyAccessibilityFeatures=false;Switch.UseLegacyAccessibilityFeatures.2=false" />
</runtime>
```

### <a name="restoring-legacy-behavior"></a><span data-ttu-id="120cb-123">Restauration du comportement hérité</span><span class="sxs-lookup"><span data-stu-id="120cb-123">Restoring legacy behavior</span></span>

<span data-ttu-id="120cb-124">Pour les applications ciblant la version 4.7.1 ou des versions ultérieures du .NET Framework, vous pouvez désactiver les fonctionnalités d’accessibilité en ajoutant des commutateurs à l’élément [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) dans la section [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) du fichier de configuration de l’application et en les définissant à la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="120cb-124">Applications that target versions of the .NET Framework starting with 4.7.1 can disable accessibility features by adding switches to the [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) element in the [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) section of the application's configuration file and setting their value to `true`.</span></span> <span data-ttu-id="120cb-125">Par exemple, la configuration suivante active les nouvelles fonctionnalités d’accessibilité de .NET Framework 4.7.2 :</span><span class="sxs-lookup"><span data-stu-id="120cb-125">For example, the following configuration opts out of accessibility features introduced in .NET Framework 4.7.2:</span></span>  

```xml
<runtime>
    <!-- AppContextSwitchOverrides value attribute is in the form of 'key1=true|false;key2=true|false  -->
    <AppContextSwitchOverrides value="Switch.UseLegacyAccessibilityFeatures.2=true" />
</runtime>
```

## <a name="whats-new-in-accessibility-in-the-net-framework-472"></a><span data-ttu-id="120cb-126">Nouveautés de .NET Framework 4.7.2 dans le domaine de l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="120cb-126">What's new in accessibility in the .NET Framework 4.7.2</span></span>

<span data-ttu-id="120cb-127">.NET Framework 4.7.2 apporte de nouvelles fonctionnalités d’accessibilité dans les domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="120cb-127">The .NET Framework 4.7.2 includes new accessibility features in the following areas:</span></span>

- [<span data-ttu-id="120cb-128">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="120cb-128">Windows Forms</span></span>](#winforms472)

- [<span data-ttu-id="120cb-129">Windows Presentation Foundation (WPF)</span><span class="sxs-lookup"><span data-stu-id="120cb-129">Windows Presentation Foundation (WPF)</span></span>](#wpf472)

<a name="winforms472"></a>
### <a name="windows-forms"></a><span data-ttu-id="120cb-130">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="120cb-130">Windows Forms</span></span>

<span data-ttu-id="120cb-131">**Couleurs définies par le système d’exploitation dans les thèmes à contraste élevé**</span><span class="sxs-lookup"><span data-stu-id="120cb-131">**OS-defined colors in High Contrast themes**</span></span>

<span data-ttu-id="120cb-132">À compter de .NET Framework 4.7.2, Windows Forms utilise les couleurs définies par le système d’exploitation dans les thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="120cb-132">Starting with .NET Framework 4.7.2, Windows Forms uses colors defined by the operating system in High Contrast themes.</span></span> <span data-ttu-id="120cb-133">Cela concerne les contrôles suivants :</span><span class="sxs-lookup"><span data-stu-id="120cb-133">This affects the following controls:</span></span>

- <span data-ttu-id="120cb-134">Flèche déroulante du contrôle <xref:System.Windows.Forms.ToolStripDropDownButton>.</span><span class="sxs-lookup"><span data-stu-id="120cb-134">The drop-down arrow of the <xref:System.Windows.Forms.ToolStripDropDownButton> control.</span></span>

- <span data-ttu-id="120cb-135">Contrôles <xref:System.Windows.Forms.Button>, <xref:System.Windows.Forms.RadioButton> et <xref:System.Windows.Forms.CheckBox> dont la propriété <xref:System.Windows.Forms.ButtonBase.FlatStyle> est définie sur <xref:System.Windows.Forms.FlatStyle.Flat?displayProperty=nameWithType> ou <xref:System.Windows.Forms.FlatStyle.Popup?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="120cb-135">The <xref:System.Windows.Forms.Button>, <xref:System.Windows.Forms.RadioButton> and <xref:System.Windows.Forms.CheckBox> controls with <xref:System.Windows.Forms.ButtonBase.FlatStyle> set to <xref:System.Windows.Forms.FlatStyle.Flat?displayProperty=nameWithType> or <xref:System.Windows.Forms.FlatStyle.Popup?displayProperty=nameWithType>.</span></span> <span data-ttu-id="120cb-136">Auparavant, les couleurs du texte sélectionné et de l’arrière-plan étaient sans contraste, ce qui nuisait à la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="120cb-136">Previously, selected text and background colors were not contrasting and were hard to read.</span></span>

- <span data-ttu-id="120cb-137">Contrôles contenus dans un <xref:System.Windows.Forms.GroupBox> dont la propriété <xref:System.Windows.Forms.Control.Enabled> est définie sur `false`.</span><span class="sxs-lookup"><span data-stu-id="120cb-137">Controls contained within a <xref:System.Windows.Forms.GroupBox> that has its <xref:System.Windows.Forms.Control.Enabled> property set to `false`.</span></span>
 
- <span data-ttu-id="120cb-138">Contrôles <xref:System.Windows.Forms.ToolStripButton>, <xref:System.Windows.Forms.ToolStripComboBox> et <xref:System.Windows.Forms.ToolStripDropDownButton> ayant un ratio contraste/luminosité accru dans le mode à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="120cb-138">The <xref:System.Windows.Forms.ToolStripButton>, <xref:System.Windows.Forms.ToolStripComboBox>, and <xref:System.Windows.Forms.ToolStripDropDownButton> controls, which have an increased luminosity contrast ratio in High Contrast Mode.</span></span>

- <span data-ttu-id="120cb-139">Propriété <xref:System.Windows.Forms.DataGridViewLinkCell.LinkColor> de <xref:System.Windows.Forms.DataGridViewLinkCell>.</span><span class="sxs-lookup"><span data-stu-id="120cb-139">The <xref:System.Windows.Forms.DataGridViewLinkCell.LinkColor> property of the <xref:System.Windows.Forms.DataGridViewLinkCell>.</span></span>

<span data-ttu-id="120cb-140">**Améliorations du Narrateur**</span><span class="sxs-lookup"><span data-stu-id="120cb-140">**Narrator improvements**</span></span>

<span data-ttu-id="120cb-141">.NET Framework 4.7.2 et les versions ultérieures améliorent la prise en charge du Narrateur de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="120cb-141">Starting with the .NET Framework 4.7.2, Narrator support is enhanced as follows:</span></span>

- <span data-ttu-id="120cb-142">Le Narrateur annonce la valeur de la propriété <xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeys?displayProperty=nameWithType> quand il annonce le texte d’un <xref:System.Windows.Forms.ToolStripMenuItem>.</span><span class="sxs-lookup"><span data-stu-id="120cb-142">It announces the value of the <xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeys?displayProperty=nameWithType> property when announcing the text of a <xref:System.Windows.Forms.ToolStripMenuItem>.</span></span> 

- <span data-ttu-id="120cb-143">Il indique quand un <xref:System.Windows.Forms.ToolStripMenuItem> a sa propriété <xref:System.Windows.Forms.Control.Enabled> définie sur `false`.</span><span class="sxs-lookup"><span data-stu-id="120cb-143">It indicates when a <xref:System.Windows.Forms.ToolStripMenuItem> has its <xref:System.Windows.Forms.Control.Enabled> property set to `false`.</span></span>

- <span data-ttu-id="120cb-144">Il fournit des commentaires sur l’état d’une case à cocher quand la propriété <xref:System.Windows.Forms.ListView.CheckBoxes?displayProperty=nameWithType> est définie sur `true`.</span><span class="sxs-lookup"><span data-stu-id="120cb-144">It gives feedback on the state of a check box when the <xref:System.Windows.Forms.ListView.CheckBoxes?displayProperty=nameWithType> property is set to `true`.</span></span>

- <span data-ttu-id="120cb-145">L’ordre de focus du mode balayage du Narrateur est cohérent avec l’ordre d’affichage des contrôles dans la fenêtre de la boîte de dialogue de téléchargement ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="120cb-145">Narrator's Scan Mode focus order is consistent with the visual order of the controls on the ClickOnce download dialog window.</span></span>

<span data-ttu-id="120cb-146">**Améliorations du contrôle DataGridView**</span><span class="sxs-lookup"><span data-stu-id="120cb-146">**DataGridView improvements**</span></span>

<span data-ttu-id="120cb-147">À compter de .NET Framework 4.7.2, le contrôle <xref:System.Windows.Forms.DataGridView> présente les améliorations d’accessibilité suivantes :</span><span class="sxs-lookup"><span data-stu-id="120cb-147">Starting with the .NET Framework 4.7.2, the <xref:System.Windows.Forms.DataGridView> control has introduced the following accessibility improvements:</span></span>

- <span data-ttu-id="120cb-148">Les lignes peuvent être triées à l’aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="120cb-148">Rows can be sorted using the keyboard.</span></span> <span data-ttu-id="120cb-149">Un utilisateur peut utiliser la touche F3 pour trier la colonne active.</span><span class="sxs-lookup"><span data-stu-id="120cb-149">A user can use the F3 key in order to sort by the current column.</span></span>

- <span data-ttu-id="120cb-150">Quand <xref:System.Windows.Forms.DataGridView.SelectionMode?displayProperty=nameWithType> est défini sur <xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect?displayProperty=nameWithType>, l’en-tête de colonne change de couleur pour indiquer la colonne active quand l’utilisateur se déplace entre les cellules de la ligne active à l’aide de la touche Tab.</span><span class="sxs-lookup"><span data-stu-id="120cb-150">When the <xref:System.Windows.Forms.DataGridView.SelectionMode?displayProperty=nameWithType> is set to <xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect?displayProperty=nameWithType>, the column header changes color to indicate the current column as the user tabs through the cells in the current row.</span></span>

- <span data-ttu-id="120cb-151">La propriété <xref:System.Windows.Forms.AccessibleObject.Parent?displayProperty=nameWithType> d’un <xref:System.Windows.Forms.DataGridViewLinkCell.DataGridViewLinkCellAccessibleObject?displayProperty=nameWithType> retourne le bon contrôle parent.</span><span class="sxs-lookup"><span data-stu-id="120cb-151">The <xref:System.Windows.Forms.AccessibleObject.Parent?displayProperty=nameWithType> property of a  <xref:System.Windows.Forms.DataGridViewLinkCell.DataGridViewLinkCellAccessibleObject?displayProperty=nameWithType> returns the correct parent control.</span></span>

<span data-ttu-id="120cb-152">**Amélioration des signaux visuels**</span><span class="sxs-lookup"><span data-stu-id="120cb-152">**Improved visual cues**</span></span>

- <span data-ttu-id="120cb-153">Les contrôles <xref:System.Windows.Forms.RadioButton> et <xref:System.Windows.Forms.CheckBox> avec une propriété <xref:System.Windows.Forms.ButtonBase.Text> vide affichent un indicateur de focus quand ils deviennent actifs.</span><span class="sxs-lookup"><span data-stu-id="120cb-153">The <xref:System.Windows.Forms.RadioButton> and <xref:System.Windows.Forms.CheckBox> controls with an empty <xref:System.Windows.Forms.ButtonBase.Text> property  display a focus indicator when they receive the focus.</span></span>

<span data-ttu-id="120cb-154">**Prise en charge améliorée de la grille des propriétés**</span><span class="sxs-lookup"><span data-stu-id="120cb-154">**Improved Property Grid Support**</span></span>

- <span data-ttu-id="120cb-155">Les éléments enfants du contrôle <xref:System.Windows.Forms.PropertyGrid> retournent désormais un `true` pour la propriété <xref:System.Windows.Automation.ValuePattern.IsReadOnlyProperty> uniquement quand un élément PropertyGrid est activé.</span><span class="sxs-lookup"><span data-stu-id="120cb-155">The <xref:System.Windows.Forms.PropertyGrid> control child elements now return a `true` for the  <xref:System.Windows.Automation.ValuePattern.IsReadOnlyProperty> property only when a PropertyGrid element is enabled.</span></span>

- <span data-ttu-id="120cb-156">Les éléments enfants du contrôle <xref:System.Windows.Forms.PropertyGrid> retournent un `false` pour la propriété <xref:System.Windows.Automation.AutomationElement.IsEnabledProperty> uniquement quand un élément PropertyGrid peut être changé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="120cb-156">The <xref:System.Windows.Forms.PropertyGrid> control child elements return a `false` for the <xref:System.Windows.Automation.AutomationElement.IsEnabledProperty> property only when a PropertyGrid element can be changed by the user.</span></span>

<span data-ttu-id="120cb-157">**Navigation au clavier améliorée**</span><span class="sxs-lookup"><span data-stu-id="120cb-157">**Improved keyboard navigation**</span></span>

- <span data-ttu-id="120cb-158">Le contrôle <xref:System.Windows.Forms.ToolStripButton> peut être activé quand il est contenu dans un <xref:System.Windows.Forms.ToolStripPanel> dont la propriété <xref:System.Windows.Forms.ToolStripPanel.TabStop> a la valeur `true`</span><span class="sxs-lookup"><span data-stu-id="120cb-158">The <xref:System.Windows.Forms.ToolStripButton> control allows focus when contained within a <xref:System.Windows.Forms.ToolStripPanel> that has the <xref:System.Windows.Forms.ToolStripPanel.TabStop> property set to `true`</span></span>

<a name="wpf472"></a>
### <a name="windows-presentation-foundation-wpf"></a><span data-ttu-id="120cb-159">Windows Presentation Foundation (WPF)</span><span class="sxs-lookup"><span data-stu-id="120cb-159">Windows Presentation Foundation (WPF)</span></span>

<span data-ttu-id="120cb-160">**Changements apportés aux contrôles CheckBox et RadioButton**</span><span class="sxs-lookup"><span data-stu-id="120cb-160">**Changes to the CheckBox and RadioButton controls**</span></span>

<span data-ttu-id="120cb-161">Dans .NET Framework 4.7.1 et les versions antérieures, les contrôles WPF <xref:System.Windows.Controls.CheckBox?displayProperty=nameWIthType> et <xref:System.Windows.Controls.RadioButton?displayProperty=nameWIthType> ont des visuels de focus incohérents et, dans les thèmes standard et à contraste élevé, des visuels de focus inappropriés.</span><span class="sxs-lookup"><span data-stu-id="120cb-161">In the .NET Framework 4.7.1 and earlier versions, the WPF <xref:System.Windows.Controls.CheckBox?displayProperty=nameWIthType> and <xref:System.Windows.Controls.RadioButton?displayProperty=nameWIthType> controls have inconsistent and, in Classic and High Contrast themes, incorrect focus visuals.</span></span>  <span data-ttu-id="120cb-162">Ces problèmes se produisent dans les cas où les contrôles n’ont pas de contenu défini.</span><span class="sxs-lookup"><span data-stu-id="120cb-162">These issues occur in cases where the controls do not have any content set.</span></span>  <span data-ttu-id="120cb-163">Cela peut rendre la transition entre les thèmes confuse et le visuel de focus difficile à voir.</span><span class="sxs-lookup"><span data-stu-id="120cb-163">This can make the transition between themes confusing and the focus visual hard to see.</span></span>

<span data-ttu-id="120cb-164">Dans .NET Framework 4.7.2, ces visuels sont désormais plus cohérents entre les thèmes et plus facilement visibles dans les thèmes classique et à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="120cb-164">In the .NET Framework 4.7.2, these visuals are now more consistent across themes and more easily visible in Classic and High Contrast themes.</span></span>

<span data-ttu-id="120cb-165">**Contrôles WinForms hébergés dans une application WPF**</span><span class="sxs-lookup"><span data-stu-id="120cb-165">**WinForms controls hosted in a WPF application**</span></span>

<span data-ttu-id="120cb-166">Dans .NET Framework 4.7.1 et les versions antérieures, les contrôles WinForms hébergés dans une application WPF ne permettaient pas aux utilisateurs de sortir de la couche WinForms à l’aide de la touche Tab quand le contrôle WPF <xref:System.Windows.Forms.Integration.ElementHost> était le premier ou dernier contrôle dans cette couche.</span><span class="sxs-lookup"><span data-stu-id="120cb-166">For WinForms control hosted in a WPF application in the .NET Framework 4.7.1 and earlier versions, users couldn't tab out of the WinForms layer if the first or last control in that layer is the WPF <xref:System.Windows.Forms.Integration.ElementHost> control.</span></span> <span data-ttu-id="120cb-167">Dans .NET Framework 4.7.2, les utilisateurs peuvent désormais sortir de la couche WinForms à l’aide de la touche Tab.</span><span class="sxs-lookup"><span data-stu-id="120cb-167">In the .NET Framework 4.7.2, users are now able to tab out of the WinForms layer.</span></span>

<span data-ttu-id="120cb-168">Toutefois, les applications automatisées qui s’attendent à ce que le focus ne quitte jamais la couche WinForms risquent de ne plus fonctionner comme prévu.</span><span class="sxs-lookup"><span data-stu-id="120cb-168">However, automated applications that rely on focus never escaping the WinForms layer may no longer work as expected.</span></span>

## <a name="whats-new-in-accessibility-in-the-net-framework-471"></a><span data-ttu-id="120cb-169">Nouveautés de .NET Framework 4.7.1 dans le domaine de l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="120cb-169">What's new in accessibility in the .NET Framework 4.7.1</span></span>

<span data-ttu-id="120cb-170">.NET Framework 4.7.1 apporte de nouvelles fonctionnalités d’accessibilité dans les domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="120cb-170">The .NET Framework 4.7.1 includes new accessibility features in the following areas:</span></span>

- [<span data-ttu-id="120cb-171">Windows Presentation Foundation (WPF)</span><span class="sxs-lookup"><span data-stu-id="120cb-171">Windows Presentation Foundation (WPF)</span></span>](#wpf471)

- [<span data-ttu-id="120cb-172">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="120cb-172">Windows Forms</span></span>](#winforms471)

- [<span data-ttu-id="120cb-173">Contrôles web ASP.NET</span><span class="sxs-lookup"><span data-stu-id="120cb-173">ASP.NET web controls</span></span>](#aspnet471)

- [<span data-ttu-id="120cb-174">Outils du kit SDK .NET</span><span class="sxs-lookup"><span data-stu-id="120cb-174">.NET SDK Tools</span></span>](#tools471)

- [<span data-ttu-id="120cb-175">Concepteur de flux de travail Windows Workflow Foundation (WF)</span><span class="sxs-lookup"><span data-stu-id="120cb-175">Windows Workflow Foundation (WF) Workflow Designer</span></span>](#wf471)

<a name="wpf471"></a>
### <a name="windows-presentation-foundation-wpf"></a><span data-ttu-id="120cb-176">Windows Presentation Foundation (WPF)</span><span class="sxs-lookup"><span data-stu-id="120cb-176">Windows Presentation Foundation (WPF)</span></span>

<span data-ttu-id="120cb-177">**Améliorations du lecteur d’écran**</span><span class="sxs-lookup"><span data-stu-id="120cb-177">**Screen reader improvements**</span></span>

<span data-ttu-id="120cb-178">Si les améliorations apportées à l’accessibilité sont activées, .NET Framework 4.7.1 inclut les améliorations suivantes qui affectent les lecteurs d’écran :</span><span class="sxs-lookup"><span data-stu-id="120cb-178">If accessibility improvements are enabled, the .NET Framework 4.7.1 includes the following enhancements that affect screen readers:</span></span>

- <span data-ttu-id="120cb-179">Dans .NET Framework 4.7 et versions antérieures, les contrôles <xref:System.Windows.Controls.Expander> étaient annoncés par des lecteurs d’écran sous forme de boutons.</span><span class="sxs-lookup"><span data-stu-id="120cb-179">In the .NET Framework 4.7 and earlier versions, <xref:System.Windows.Controls.Expander> controls were announced by screen readers as buttons.</span></span> <span data-ttu-id="120cb-180">À compter de .NET Framework 4.7.1, ils sont correctement annoncés en tant que groupes extensibles/réductibles.</span><span class="sxs-lookup"><span data-stu-id="120cb-180">Starting with the .NET Framework 4.7.1, they are correctly announced as expandable/collapsible groups.</span></span>

- <span data-ttu-id="120cb-181">Dans .NET Framework 4.7 et versions antérieures, les contrôles <xref:System.Windows.Controls.DataGridCell> étaient annoncés par des lecteurs d’écran comme étant « personnalisés ».</span><span class="sxs-lookup"><span data-stu-id="120cb-181">In the .NET Framework 4.7 and earlier versions, <xref:System.Windows.Controls.DataGridCell> controls were announced by screen readers as “custom.”</span></span> <span data-ttu-id="120cb-182">À compter de .NET Framework 4.7.1, ils sont maintenant correctement annoncés en tant que cellule de grille de données (localisée).</span><span class="sxs-lookup"><span data-stu-id="120cb-182">Starting with the .NET Framework 4.7.1, they are now correctly announced as data grid cell (localized).</span></span>
 
- <span data-ttu-id="120cb-183">À compter de .NET Framework 4.7.1, les lecteurs d’écran annoncent le nom d’un élément <xref:System.Windows.Controls.ComboBox> modifiable.</span><span class="sxs-lookup"><span data-stu-id="120cb-183">Starting with the .NET Framework 4.7.1, screen readers announce the name of an editable <xref:System.Windows.Controls.ComboBox>.</span></span>

- <span data-ttu-id="120cb-184">Dans .NET Framework 4.7 et versions antérieures, les contrôles <xref:System.Windows.Controls.PasswordBox> étaient annoncés comme « aucun élément dans la vue » ou avaient sinon un comportement incorrect.</span><span class="sxs-lookup"><span data-stu-id="120cb-184">In the .NET Framework 4.7 and earlier versions, <xref:System.Windows.Controls.PasswordBox> controls were announced as “no item in view” or had otherwise incorrect behavior.</span></span> <span data-ttu-id="120cb-185">Ce problème est résolu depuis .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="120cb-185">This issue is fixed starting with the .NET Framework 4.7.1.</span></span>

<span data-ttu-id="120cb-186">**Prise en charge de zones dynamiques UIAutomation**</span><span class="sxs-lookup"><span data-stu-id="120cb-186">**UIAutomation LiveRegion support**</span></span>

<span data-ttu-id="120cb-187">Les lecteurs d’écran tels que le Narrateur aident les personnes à lire le contenu de l’interface utilisateur d’une application, généralement par une sortie conversion de texte par synthèse vocale du contenu de l’interface utilisateur actif.</span><span class="sxs-lookup"><span data-stu-id="120cb-187">Screen readers such as Narrator help people read the UI contents of an application, usually by text-to-speech output of the UI content that has the focus.</span></span> <span data-ttu-id="120cb-188">Toutefois, si un élément d’interface utilisateur change et n’est pas actif, l’utilisateur peut ne pas en être informé et manquer des informations importantes.</span><span class="sxs-lookup"><span data-stu-id="120cb-188">However, if a UI element changes and does not have the focus, the user may not be notified and may miss important information.</span></span> <span data-ttu-id="120cb-189">Les zones dynamiques visent à résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="120cb-189">Live regions aim at solving this problem.</span></span> <span data-ttu-id="120cb-190">Un développeur peut les utiliser pour informer le lecteur d’écran ou tout autre client UIAutomation qu’une modification importante a été apportée à un élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="120cb-190">A developer can use them to inform the screen reader or any other UIAutomation client that an important change has been made to a UI element.</span></span> <span data-ttu-id="120cb-191">Le lecteur d’écran peut ensuite décider comment et quand informer l’utilisateur de cette modification.</span><span class="sxs-lookup"><span data-stu-id="120cb-191">The screen reader can then decide how and when to inform the user of this change.</span></span> 

<span data-ttu-id="120cb-192">Pour prendre en charge les zones dynamiques, les API suivantes ont été ajoutées à WPF :</span><span class="sxs-lookup"><span data-stu-id="120cb-192">To support live regions, the following APIs have been added to WPF:</span></span>

- <span data-ttu-id="120cb-193">Champs <xref:System.Windows.Automation.AutomationElementIdentifiers.LiveSettingProperty?displayProperty=nameWithType> et <xref:System.Windows.Automation.AutomationElementIdentifiers.LiveRegionChangedEvent?displayProperty=nameWithType>, qui identifient la propriété **LiveSetting** et l’événement **LiveRegionChanged**.</span><span class="sxs-lookup"><span data-stu-id="120cb-193">The <xref:System.Windows.Automation.AutomationElementIdentifiers.LiveSettingProperty?displayProperty=nameWithType> and <xref:System.Windows.Automation.AutomationElementIdentifiers.LiveRegionChangedEvent?displayProperty=nameWithType> fields, which identify the **LiveSetting** property and the **LiveRegionChanged** event.</span></span> <span data-ttu-id="120cb-194">Ils peuvent être définis à l’aide de XAML.</span><span class="sxs-lookup"><span data-stu-id="120cb-194">They can be set by using XAML.</span></span>

- <span data-ttu-id="120cb-195">Propriété jointe **AutomationProperties.LiveSetting**, qui informe le lecteur d’écran de l’importance de la modification de l’interface utilisateur pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="120cb-195">The **AutomationProperties.LiveSetting** attached property, which informs the screen reader of the importance of the UI change to the user.</span></span>

- <span data-ttu-id="120cb-196">Propriété <xref:System.Windows.Automation.AutomationProperties.LiveSettingProperty?displayProperty=nameWithType>, qui identifie la propriété jointe **AutomationProperties.LiveSetting**.</span><span class="sxs-lookup"><span data-stu-id="120cb-196">The <xref:System.Windows.Automation.AutomationProperties.LiveSettingProperty?displayProperty=nameWithType> property, which identifies the **AutomationProperties.LiveSetting** attached property.</span></span>
 
- <span data-ttu-id="120cb-197">Méthode <xref:System.Windows.Automation.Peers.AutomationPeer.GetLiveSettingCore%2A?displayProperty=nameWithType>, qui peut être remplacée pour fournir une valeur **LiveSetting**.</span><span class="sxs-lookup"><span data-stu-id="120cb-197">The <xref:System.Windows.Automation.Peers.AutomationPeer.GetLiveSettingCore%2A?displayProperty=nameWithType> method, which can be overridden to provide a **LiveSetting** value.</span></span>

- <span data-ttu-id="120cb-198">Méthodes <xref:System.Windows.Automation.AutomationProperties.GetLiveSetting%2A?displayProperty=nameWithType> et <xref:System.Windows.Automation.AutomationProperties.SetLiveSetting%2A?displayProperty=nameWithType>, qui obtiennent et définissent une valeur **LiveSetting**.</span><span class="sxs-lookup"><span data-stu-id="120cb-198">The <xref:System.Windows.Automation.AutomationProperties.GetLiveSetting%2A?displayProperty=nameWithType> and <xref:System.Windows.Automation.AutomationProperties.SetLiveSetting%2A?displayProperty=nameWithType> methods, which get and set a **LiveSetting** value.</span></span>
 
- <span data-ttu-id="120cb-199">Énumération <xref:System.Windows.Automation.AutomationLiveSetting?displayProperty=nameWithType>, qui définit les valeurs **LiveSetting** possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="120cb-199">The <xref:System.Windows.Automation.AutomationLiveSetting?displayProperty=nameWithType> enumeration, which defines the following possible **LiveSetting** values:</span></span>

   - <span data-ttu-id="120cb-200"><xref:System.Windows.Automation.AutomationLiveSetting.Off?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="120cb-200"><xref:System.Windows.Automation.AutomationLiveSetting.Off?displayProperty=nameWithType>.</span></span> <span data-ttu-id="120cb-201">L’élément n’envoie pas de notification si le contenu de la zone dynamique a changé.</span><span class="sxs-lookup"><span data-stu-id="120cb-201">The element does not send notifications if the content of the live region has changed.</span></span>   
   - <span data-ttu-id="120cb-202"><xref:System.Windows.Automation.AutomationLiveSetting.Polite?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="120cb-202"><xref:System.Windows.Automation.AutomationLiveSetting.Polite?displayProperty=nameWithType>.</span></span> <span data-ttu-id="120cb-203">L’élément envoie des notifications qui ne provoquent pas d’interruption si le contenu de la zone dynamique a changé.</span><span class="sxs-lookup"><span data-stu-id="120cb-203">The element sends non-interruptive notifications if the content of the live region has changed.</span></span>   

  - <span data-ttu-id="120cb-204"><xref:System.Windows.Automation.AutomationLiveSetting.Assertive?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="120cb-204"><xref:System.Windows.Automation.AutomationLiveSetting.Assertive?displayProperty=nameWithType>.</span></span> <span data-ttu-id="120cb-205">L’élément envoie des notifications qui provoquent des interruptions si le contenu de la zone dynamique a changé.</span><span class="sxs-lookup"><span data-stu-id="120cb-205">The element sends interruptive notifications if the content of the live region has changed.</span></span>   

<span data-ttu-id="120cb-206">Vous pouvez créer une zone dynamique en définissant la propriété **AutomationProperties.LiveSetting** sur l’élément qui vous intéresse, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="120cb-206">You can create a LiveRegion by setting the **AutomationProperties.LiveSetting** property on the element of interest, as shown in the following example:</span></span>   

```xaml
<TextBlock Name="myTextBlock" AutomationProperties.LiveSetting="Assertive">announcement</TextBlock>
```

<span data-ttu-id="120cb-207">Quand les données de la zone dynamique sont modifiées et que vous devez informer un lecteur d’écran, vous déclenchez explicitement un événement, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="120cb-207">When the data in the live region changes and you need to inform a screen reader, you explicitly raise an event, as shown in the following sample.</span></span>

```csharp
var peer = FrameworkElementAutomationPeer.FromElement(myTextBlock);

peer.RaiseAutomationEvent(AutomationEvents.LiveRegionChanged);
```
```vb
Dim peer = FrameworkElementAutomationPeer.FromElement(myTextBlock)
peer.RaiseAutomationEvent(AutomationEvents.LiveRegionChanged)

```

<span data-ttu-id="120cb-208">**Contraste élevé**</span><span class="sxs-lookup"><span data-stu-id="120cb-208">**High contrast**</span></span>

<span data-ttu-id="120cb-209">À compter de .NET Framework 4.7.1, des améliorations en matière de contraste élevé ont été apportées à différents contrôles WPF.</span><span class="sxs-lookup"><span data-stu-id="120cb-209">Starting with the .NET Framework 4.7.1, improvements in high contrast have been made to various WPF controls.</span></span> <span data-ttu-id="120cb-210">Elles sont désormais visibles quand le thème <xref:System.Windows.SystemParameters.HighContrast%2A> est défini.</span><span class="sxs-lookup"><span data-stu-id="120cb-210">They are now visible when the <xref:System.Windows.SystemParameters.HighContrast%2A> theme is set.</span></span> <span data-ttu-id="120cb-211">Elles incluent notamment :</span><span class="sxs-lookup"><span data-stu-id="120cb-211">These include:</span></span>

- <span data-ttu-id="120cb-212">Contrôle <xref:System.Windows.Controls.Expander></span><span class="sxs-lookup"><span data-stu-id="120cb-212"><xref:System.Windows.Controls.Expander> control</span></span>

    <span data-ttu-id="120cb-213">L’élément visuel de focus pour le contrôle <xref:System.Windows.Controls.Expander> est désormais visible.</span><span class="sxs-lookup"><span data-stu-id="120cb-213">The focus visual for the  <xref:System.Windows.Controls.Expander> control is now visible.</span></span> <span data-ttu-id="120cb-214">Les éléments visuels de clavier pour les contrôles <xref:System.Windows.Controls.ComboBox>, <xref:System.Windows.Controls.ListBox> et <xref:System.Windows.Controls.RadioButton> sont également visibles.</span><span class="sxs-lookup"><span data-stu-id="120cb-214">The keyboard visuals for <xref:System.Windows.Controls.ComboBox>,<xref:System.Windows.Controls.ListBox>, and <xref:System.Windows.Controls.RadioButton> controls are visible as well.</span></span> <span data-ttu-id="120cb-215">Exemple :</span><span class="sxs-lookup"><span data-stu-id="120cb-215">For example:</span></span>

    <span data-ttu-id="120cb-216">Avant :</span><span class="sxs-lookup"><span data-stu-id="120cb-216">Before:</span></span> 
    
    ![Contrôle Expander avec focus avant les améliorations apportées à l’accessibilité](media/expander-before.png)

    <span data-ttu-id="120cb-218">Après :</span><span class="sxs-lookup"><span data-stu-id="120cb-218">After:</span></span> 

    ![Contrôle Expander avec focus après les améliorations apportées à l’accessibilité](media/expander-after.png)

- <span data-ttu-id="120cb-220">Contrôles <xref:System.Windows.Controls.CheckBox> et <xref:System.Windows.Controls.RadioButton></span><span class="sxs-lookup"><span data-stu-id="120cb-220"><xref:System.Windows.Controls.CheckBox> and <xref:System.Windows.Controls.RadioButton> controls</span></span>
 
    <span data-ttu-id="120cb-221">Le texte dans les contrôles <xref:System.Windows.Controls.CheckBox> et <xref:System.Windows.Controls.RadioButton> est désormais plus facile à voir quand il est sélectionné dans les thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="120cb-221">The text in the <xref:System.Windows.Controls.CheckBox> and <xref:System.Windows.Controls.RadioButton> controls is now easier to see when selected in high contrast themes.</span></span> <span data-ttu-id="120cb-222">Exemple :</span><span class="sxs-lookup"><span data-stu-id="120cb-222">For example:</span></span>

    <span data-ttu-id="120cb-223">Avant :</span><span class="sxs-lookup"><span data-stu-id="120cb-223">Before:</span></span> 

    ![Case d’option à contraste élevé avec focus avant les améliorations apportées à l’accessibilité](media/radio-button-before.png)
    
    <span data-ttu-id="120cb-225">Après :</span><span class="sxs-lookup"><span data-stu-id="120cb-225">After:</span></span> 

    ![Case d’option à contraste élevé avec focus après les améliorations apportées à l’accessibilité](media/radio-button-after.png)

- <span data-ttu-id="120cb-227">Contrôle <xref:System.Windows.Controls.ComboBox></span><span class="sxs-lookup"><span data-stu-id="120cb-227"><xref:System.Windows.Controls.ComboBox> control</span></span>
 
    <span data-ttu-id="120cb-228">À compter de .NET Framework 4.7.1, la bordure d’un contrôle <xref:System.Windows.Controls.ComboBox> désactivé est de la même couleur que le texte désactivé.</span><span class="sxs-lookup"><span data-stu-id="120cb-228">Starting with the .NET Framework 4.7.1, the border of a disabled <xref:System.Windows.Controls.ComboBox> control is the same color as disabled text.</span></span> <span data-ttu-id="120cb-229">Exemple :</span><span class="sxs-lookup"><span data-stu-id="120cb-229">For example:</span></span>
    
    <span data-ttu-id="120cb-230">Avant :</span><span class="sxs-lookup"><span data-stu-id="120cb-230">Before:</span></span> 

     ![Texte et bordure d’un contrôle ComboBox désactivé avant les améliorations apportées à l’accessibilité](media/combo-disabled-before.png)

    <span data-ttu-id="120cb-232">Après :</span><span class="sxs-lookup"><span data-stu-id="120cb-232">After:</span></span>   

     ![Texte et bordure d’un contrôle ComboBox désactivé après les améliorations apportées à l’accessibilité](media/combo-disabled-after.png)

    <span data-ttu-id="120cb-234">En outre, les boutons désactivés et actifs utilisent la couleur de thème correcte.</span><span class="sxs-lookup"><span data-stu-id="120cb-234">In addition, disabled and focused buttons use the correct theme color.</span></span>

    <span data-ttu-id="120cb-235">Avant :</span><span class="sxs-lookup"><span data-stu-id="120cb-235">Before:</span></span>

    ![Couleurs de thème des boutons avant les améliorations apportées à l’accessibilité](media/button-themes-before.png) 
    
    <span data-ttu-id="120cb-237">Après :</span><span class="sxs-lookup"><span data-stu-id="120cb-237">After:</span></span> 

    ![Couleurs de thème des boutons après les améliorations apportées à l’accessibilité](media/button-themes-after.png) 

    <span data-ttu-id="120cb-239">Enfin, dans .NET Framework 4.7 et versions antérieures, la définition du style d’un contrôle <xref:System.Windows.Controls.ComboBox> sur `Toolbar.ComboBoxStyleKey` rendait la flèche déroulante invisible.</span><span class="sxs-lookup"><span data-stu-id="120cb-239">Finally, in the .NET Framework 4.7 and earlier versions, setting a <xref:System.Windows.Controls.ComboBox> control’s style to `Toolbar.ComboBoxStyleKey` caused the drop-down arrow to be invisible.</span></span> <span data-ttu-id="120cb-240">Ce problème est résolu depuis .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="120cb-240">This issue is fixed starting with the .NET Framework 4.7.1.</span></span> <span data-ttu-id="120cb-241">Exemple :</span><span class="sxs-lookup"><span data-stu-id="120cb-241">For example:</span></span>

    <span data-ttu-id="120cb-242">Avant :</span><span class="sxs-lookup"><span data-stu-id="120cb-242">Before:</span></span> 

    ![Toolbar.ComboBoxStyleKey avant les améliorations apportées à l’accessibilité](media/comboboxstylekey-before.png) 
    
    <span data-ttu-id="120cb-244">Après :</span><span class="sxs-lookup"><span data-stu-id="120cb-244">After:</span></span> 

    ![Toolbar.ComboBoxStyleKey après les améliorations apportées à l’accessibilité](media/comboboxstylekey-after.png) 

- <span data-ttu-id="120cb-246">Contrôle <xref:System.Windows.Controls.DataGrid></span><span class="sxs-lookup"><span data-stu-id="120cb-246"><xref:System.Windows.Controls.DataGrid> control</span></span>

    <span data-ttu-id="120cb-247">À compter de .NET Framework 4.7.1, la flèche d’indicateur de tri dans les contrôles <xref:System.Windows.Controls.DataGrid> utilise maintenant les couleurs de thème correctes.</span><span class="sxs-lookup"><span data-stu-id="120cb-247">Starting with the .NET Framework 4.7.1, the sort indicator arrow in <xref:System.Windows.Controls.DataGrid> controls now uses correct theme colors.</span></span> <span data-ttu-id="120cb-248">Exemple :</span><span class="sxs-lookup"><span data-stu-id="120cb-248">For example:</span></span>

    <span data-ttu-id="120cb-249">Avant :</span><span class="sxs-lookup"><span data-stu-id="120cb-249">Before:</span></span> 

    ![Flèche d’indicateur de tri avant les améliorations apportées à l’accessibilité](media/sort-indicator-before.png) 
    
    <span data-ttu-id="120cb-251">Après :</span><span class="sxs-lookup"><span data-stu-id="120cb-251">After:</span></span>   
 
    ![Flèche d’indicateur de tri après les améliorations apportées à l’accessibilité](media/sort-indicator-after.png) 
    
    <span data-ttu-id="120cb-253">En outre, dans .NET Framework 4.7 et versions antérieures, le style de lien par défaut prenait une couleur incorrecte en pointant avec la souris dans des modes de contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="120cb-253">In addition, in the .NET Framework 4.7 and earlier versions, the default link style changed to an incorrect color on mouse over in high contrast modes.</span></span> <span data-ttu-id="120cb-254">Ce problème est résolu depuis .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="120cb-254">This is resolved starting with the .NET Framework 4.7.1.</span></span> <span data-ttu-id="120cb-255">De même, les colonnes de cases à cocher <xref:System.Windows.Controls.DataGrid> utilisent les couleurs attendues pour les commentaires de focus clavier depuis .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="120cb-255">Similarly, <xref:System.Windows.Controls.DataGrid> checkbox columns uses the expected colors for keyboard focus feedback starting with the .NET Framework 4.7.1.</span></span>

    <span data-ttu-id="120cb-256">Avant :</span><span class="sxs-lookup"><span data-stu-id="120cb-256">Before:</span></span> 

    ![Style de lien par défaut DataGrid avant les améliorations apportées à l’accessibilité](media/default-link-style-before.png) 
 
    <span data-ttu-id="120cb-258">Après :</span><span class="sxs-lookup"><span data-stu-id="120cb-258">After:</span></span>    
  
    ![Style de lien par défaut DataGrid après les améliorations apportées à l’accessibilité](media/default-link-style-after.png)  

<span data-ttu-id="120cb-260">Pour plus d’informations sur les améliorations apportées à l’accessibilité dans WPF dans .NET Framework 4.7.1, consultez [Améliorations apportées à l’accessibilité dans WPF](../migration-guide/retargeting/4.7-4.7.1.md#accessibility-improvements-in-wpf).</span><span class="sxs-lookup"><span data-stu-id="120cb-260">For more information on WPF accessibility improvements in the .NET Framework 4.7.1, see [Accessibility improvements in WPF](../migration-guide/retargeting/4.7-4.7.1.md#accessibility-improvements-in-wpf).</span></span>

<a name="winforms471"></a>
## <a name="windows-forms-accessibility-improvements"></a><span data-ttu-id="120cb-261">Améliorations apportées à l’accessibilité dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="120cb-261">Windows Forms accessibility improvements</span></span>

<span data-ttu-id="120cb-262">Dans .NET Framework 4.7.1, WinForms (Windows Forms) présente des modifications de l’accessibilité dans les domaines suivants.</span><span class="sxs-lookup"><span data-stu-id="120cb-262">In the .NET Framework 4.7.1, Windows Forms (WinForms) includes accessibility changes in the following areas.</span></span>

<span data-ttu-id="120cb-263">**Affichage amélioré en mode de contraste élevé**</span><span class="sxs-lookup"><span data-stu-id="120cb-263">**Improved display in High Contrast mode**</span></span>

<span data-ttu-id="120cb-264">À compter de .NET Framework 4.7.1, différents contrôles WinForms offrent un meilleur rendu dans les modes de contraste élevé disponibles dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="120cb-264">Starting with the .NET Framework 4.7.1, various WinForms controls offer improved rendering in the HighContrast modes available in the operating system.</span></span> <span data-ttu-id="120cb-265">Windows 10 a modifié les valeurs de certaines couleurs système à contraste élevé et Windows Forms repose sur le framework Windows 10 Win32.</span><span class="sxs-lookup"><span data-stu-id="120cb-265">Windows 10 has changed the values for some high contrast system colors, and Windows Forms is based on the Windows 10 Win32 framework.</span></span> <span data-ttu-id="120cb-266">Pour une expérience optimale, procédez à une exécution sur la dernière version de Windows et activez les dernières modifications du système d’exploitation en ajoutant un fichier app.manifest dans une application de test et supprimez les marques de commentaire de la ligne de système d’exploitation Windows 10 pour qu’elle ressemble à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="120cb-266">For the best experience, run on the latest version of Windows and opt in to the latest OS changes by adding an app.manifest file in a test application and un-comment the Windows 10 supported OS  line so that it looks the following:</span></span>

```xml
<!-- Windows 10 -->
<supportedOS Id=”{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}” />
```
<span data-ttu-id="120cb-267">Voici quelques exemples de modifications du contraste élevé :</span><span class="sxs-lookup"><span data-stu-id="120cb-267">Some examples of high contrast changes include:</span></span>

- <span data-ttu-id="120cb-268">Les coches dans les éléments <xref:System.Windows.Forms.MenuStrip> sont plus faciles à afficher.</span><span class="sxs-lookup"><span data-stu-id="120cb-268">Checkmarks in <xref:System.Windows.Forms.MenuStrip> items are easier to view.</span></span>

- <span data-ttu-id="120cb-269">Quand ils sont sélectionnés, les éléments <xref:System.Windows.Forms.MenuStrip> désactivés sont plus faciles à afficher.</span><span class="sxs-lookup"><span data-stu-id="120cb-269">When selected, disabled <xref:System.Windows.Forms.MenuStrip> items are easier to view.</span></span>

- <span data-ttu-id="120cb-270">Le texte dans un contrôle <xref:System.Windows.Forms.Button> sélectionné contraste avec la couleur de sélection.</span><span class="sxs-lookup"><span data-stu-id="120cb-270">Text in a selected <xref:System.Windows.Forms.Button> control contrasts with the selection color.</span></span>

- <span data-ttu-id="120cb-271">Le texte désactivé est plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="120cb-271">Disabled text is easier to read.</span></span> <span data-ttu-id="120cb-272">Exemple :</span><span class="sxs-lookup"><span data-stu-id="120cb-272">For example:</span></span>

    <span data-ttu-id="120cb-273">Avant :</span><span class="sxs-lookup"><span data-stu-id="120cb-273">Before:</span></span>

    ![Texte désactivé avant les améliorations apportées à l’accessibilité](media/wf-disabled-before.png) 

    <span data-ttu-id="120cb-275">Après :</span><span class="sxs-lookup"><span data-stu-id="120cb-275">After:</span></span>

    ![Texte désactivé après les améliorations apportées à l’accessibilité](media/wf-disabled-after.png) 

- <span data-ttu-id="120cb-277">Améliorations du contraste élevé dans la boîte de dialogue Thread Exception (Exception de thread).</span><span class="sxs-lookup"><span data-stu-id="120cb-277">High contrast improvements in the Thread Exception Dialog.</span></span>

<span data-ttu-id="120cb-278">**Prise en charge améliorée du Narrateur**</span><span class="sxs-lookup"><span data-stu-id="120cb-278">**Improved Narrator support**</span></span>

<span data-ttu-id="120cb-279">Windows Forms dans .NET Framework 4.7.1 inclut les améliorations en matière d’accessibilité suivantes pour le Narrateur :</span><span class="sxs-lookup"><span data-stu-id="120cb-279">Windows Forms in the .NET Framework 4.7.1 includes the following accessibility improvements for the Narrator:</span></span>

- <span data-ttu-id="120cb-280">Le contrôle <xref:System.Windows.Forms.MonthCalendar> est accessible par le Narrateur, ainsi que par d’autres outils UI Automation.</span><span class="sxs-lookup"><span data-stu-id="120cb-280">The <xref:System.Windows.Forms.MonthCalendar> control can be accessed by the Narrator, as well as by other UI automation tools.</span></span>

- <span data-ttu-id="120cb-281">Le contrôle <xref:System.Windows.Forms.CheckedListBox> avertit le Narrateur quand l’état de case à cocher d’un élément a changé pour que l’utilisateur sache que la valeur d’un élément de liste est modifiée.</span><span class="sxs-lookup"><span data-stu-id="120cb-281">The <xref:System.Windows.Forms.CheckedListBox> control notifies Narrator when an item's check state has changed so the user is notified that they’ve changed the value of a list item.</span></span>
 
- <span data-ttu-id="120cb-282">Le contrôle <xref:System.Windows.Forms.DataGridViewCell> signale l’état Lecture seule correct au Narrateur.</span><span class="sxs-lookup"><span data-stu-id="120cb-282">The <xref:System.Windows.Forms.DataGridViewCell> control reports the correct read-only status to Narrator.</span></span>
 
- <span data-ttu-id="120cb-283">Le Narrateur peut désormais lire le texte <xref:System.Windows.Forms.ToolStripMenuItem> désactivé, alors qu’il ignorait précédemment les éléments de menu désactivés.</span><span class="sxs-lookup"><span data-stu-id="120cb-283">Narrator can now read disabled <xref:System.Windows.Forms.ToolStripMenuItem> text, whereas previously it would skip over disabled menu items.</span></span>

<span data-ttu-id="120cb-284">**Prise en charge améliorée des modèles d’accessibilité UIAutomation**</span><span class="sxs-lookup"><span data-stu-id="120cb-284">**Enhanced support for UIAutomation accessibility patterns**</span></span>

<span data-ttu-id="120cb-285">À compter de .NET Framework 4.7.1, les développeurs d’outils technologiques d’accessibilité peuvent tirer parti des modèles d’accessibilité d’API courants et des propriétés de plusieurs contrôles WinForms.</span><span class="sxs-lookup"><span data-stu-id="120cb-285">Starting with the .NET Framework 4.7.1, developers of accessibility technology tools can leverage common API accessibility patterns and properties for several WinForms controls.</span></span> <span data-ttu-id="120cb-286">Ces améliorations en matière d’accessibilité sont notamment :</span><span class="sxs-lookup"><span data-stu-id="120cb-286">These accessibility improvements include:</span></span>

- <span data-ttu-id="120cb-287"><xref:System.Windows.Forms.ComboBox> et <xref:System.Windows.Forms.ToolStripSplitButton> prennent maintenant en charge le [modèle Développer/Réduire](../ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="120cb-287">The <xref:System.Windows.Forms.ComboBox> and <xref:System.Windows.Forms.ToolStripSplitButton> now support the [expand/collapse pattern](../ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span></span>
 
- <span data-ttu-id="120cb-288"><xref:System.Windows.Forms.DataGridViewCheckBoxCell> prend maintenant en charge le [modèle Basculer](../ui-automation/implementing-the-ui-automation-toggle-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="120cb-288">The <xref:System.Windows.Forms.DataGridViewCheckBoxCell> now supports the [toggle pattern](../ui-automation/implementing-the-ui-automation-toggle-control-pattern.md).</span></span>
 
- <span data-ttu-id="120cb-289">Le contrôle <xref:System.Windows.Forms.ToolStripItem> prend en charge la propriété <xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.Name> et le [modèle Développer/Réduire](../ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="120cb-289">The <xref:System.Windows.Forms.ToolStripItem> control supports the <xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.Name> property and the [expand/collapse pattern](../ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span></span>

- <span data-ttu-id="120cb-290">Les contrôles <xref:System.Windows.Forms.NumericUpDown> et <xref:System.Windows.Forms.DomainUpDown> prennent en charge la propriété <xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.Name>.</span><span class="sxs-lookup"><span data-stu-id="120cb-290">The <xref:System.Windows.Forms.NumericUpDown> and <xref:System.Windows.Forms.DomainUpDown> controls support the <xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.Name> property.</span></span>

<span data-ttu-id="120cb-291">**Expérience améliorée avec l’Explorateur de propriétés**</span><span class="sxs-lookup"><span data-stu-id="120cb-291">**Improved property browser experience**</span></span>

<span data-ttu-id="120cb-292">À compter de .NET Framework 4.7.1, Windows Forms propose :</span><span class="sxs-lookup"><span data-stu-id="120cb-292">Starting with the .NET Framework 4.7.1, Windows Forms includes:</span></span>

- <span data-ttu-id="120cb-293">Une meilleure navigation au clavier via les différentes fenêtres de sélection de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="120cb-293">Better keyboard navigation through the various drop-down selection windows.</span></span>
- <span data-ttu-id="120cb-294">Une réduction des taquets de tabulation inutiles.</span><span class="sxs-lookup"><span data-stu-id="120cb-294">A reduction of unnecessary tab stops.</span></span>
- <span data-ttu-id="120cb-295">Des rapports plus élaborés sur les types de contrôles.</span><span class="sxs-lookup"><span data-stu-id="120cb-295">Better reporting of control types.</span></span>
- <span data-ttu-id="120cb-296">Un comportement amélioré du Narrateur.</span><span class="sxs-lookup"><span data-stu-id="120cb-296">Improved narrator behavior.</span></span>
 
<a name="aspnet471"></a>
## <a name="aspnet-web-controls"></a><span data-ttu-id="120cb-297">Contrôles web ASP.NET</span><span class="sxs-lookup"><span data-stu-id="120cb-297">ASP.NET web controls</span></span>

<span data-ttu-id="120cb-298">À compter de .NET Framework 4.7.1 et de Visual Studio 2017 15.3, ASP.NET améliore le fonctionnement des contrôles web ASP.NET avec la technologie d’accessibilité de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="120cb-298">Starting with the .NET Framework 4.7.1 and Visual Studio 2017 15.3, ASP.NET improves how ASP.NET web controls work with accessibility technology in Visual Studio.</span></span> <span data-ttu-id="120cb-299">Les changements apportés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="120cb-299">Changes include the following:</span></span>

- <span data-ttu-id="120cb-300">Changements visant à implémenter les modèles d’accessibilité de l’interface utilisateur manquants dans les contrôles, comme la boîte de dialogue **Ajouter un champ** de l’Assistant **Vue Détails** ou la boîte de dialogue **Configurer ListView** de l’Assistant **ListView**.</span><span class="sxs-lookup"><span data-stu-id="120cb-300">Changes to implement missing UI accessibility patterns in controls, like the **Add Field** dialog in the **Details View** wizard, or the **Configure ListView** dialog of the **ListView** wizard.</span></span>

- <span data-ttu-id="120cb-301">Changements visant à améliorer l’affichage en mode de contraste élevé, comme **l’éditeur de champs du pagineur de données**.</span><span class="sxs-lookup"><span data-stu-id="120cb-301">Changes to improve the display in High Contrast mode, like the **Data Pager Fields Editor**.</span></span>

- <span data-ttu-id="120cb-302">Changements visant à améliorer les expériences de navigation au clavier pour les contrôles, comme la boîte de dialogue **Champs** de l’Assistant **Modifier les champs du pagineur** du contrôle DataPager, la boîte de dialogue **Configurer ObjectContext** ou la boîte de dialogue **Configurer la sélection de données** de l’Assistant **Configurer la source de données**.</span><span class="sxs-lookup"><span data-stu-id="120cb-302">Changes to improve the keyboard navigation experiences for controls, like the **Fields** dialog in the **Edit Pager Fields** wizard of the DataPager control, the **Configure ObjectContext** dialog, or the **Configure Data Selection** dialog of the **Configure Data Source** wizard.</span></span>

<a name="tools471"></a>
## <a name="net-sdk-tools"></a><span data-ttu-id="120cb-303">Outils du kit SDK . NET</span><span class="sxs-lookup"><span data-stu-id="120cb-303">.NET SDK Tools</span></span>

<span data-ttu-id="120cb-304">Divers problèmes d’accessibilité ont été corrigés dans [l’outil Éditeur de Configuration (SvcConfigEditor.exe)](../wcf/configuration-editor-tool-svcconfigeditor-exe.md) et [l’outil Service Trace Viewer (SvcTraceViewer.exe)](../wcf/service-trace-viewer-tool-svctraceviewer-exe.md).</span><span class="sxs-lookup"><span data-stu-id="120cb-304">The [Configuration Editor Tool (SvcConfigEditor.exe)](../wcf/configuration-editor-tool-svcconfigeditor-exe.md) and [Service Trace Viewer Tool (SvcTraceViewer.exe)](../wcf/service-trace-viewer-tool-svctraceviewer-exe.md) have been improved by fixing varied accessibility issues.</span></span> <span data-ttu-id="120cb-305">La plupart étaient des problèmes sans gravité, par exemple, un nom non défini ou certains modèles d’automatisation de l’interface utilisateur non implémentés correctement.</span><span class="sxs-lookup"><span data-stu-id="120cb-305">Most of these were small issues, like a name not being defined or certain UI automation patterns not being implemented correctly.</span></span> <span data-ttu-id="120cb-306">La majorité des utilisateurs ne remarqueront même pas ces problèmes, mais les clients qui utilisent des technologies d’assistance comme les lecteurs d’écran trouveront les outils de ce kit SDK plus accessibles.</span><span class="sxs-lookup"><span data-stu-id="120cb-306">While many users won’t be aware of these incorrect values, customers who use assistive technologies like screen readers will find these SDK tools more accessible.</span></span> 

<span data-ttu-id="120cb-307">Ces améliorations changent certains comportements précédents, comme l’ordre de focus du clavier.</span><span class="sxs-lookup"><span data-stu-id="120cb-307">These enhancements change some previous behaviors, such as keyboard focus order.</span></span>

<a name="wf471"></a>
## <a name="windows-workflow-foundation-wf-workflow-designer"></a><span data-ttu-id="120cb-308">Concepteur de flux de travail Windows Workflow Foundation (WF)</span><span class="sxs-lookup"><span data-stu-id="120cb-308">Windows Workflow Foundation (WF) Workflow Designer</span></span>

<span data-ttu-id="120cb-309">Les changements apportés pour améliorer l’accessibilité dans le Concepteur de flux de travail sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="120cb-309">Accessibility changes in the Workflow Designer include the following:</span></span>

- <span data-ttu-id="120cb-310">L’ordre de tabulation est maintenant de gauche à droite et de haut en bas dans certains contrôles :</span><span class="sxs-lookup"><span data-stu-id="120cb-310">The tab order changes to left to right and top to bottom in some controls:</span></span>

  - <span data-ttu-id="120cb-311">La fenêtre d’initialisation de la corrélation pour définir les données de corrélation pour l’activité <xref:System.ServiceModel.Activities.InitializeCorrelation>.</span><span class="sxs-lookup"><span data-stu-id="120cb-311">The initialize correlation window for setting correlation data for the <xref:System.ServiceModel.Activities.InitializeCorrelation> activity.</span></span>

  - <span data-ttu-id="120cb-312">La fenêtre de définition du contenu pour les activités <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.SendReply> et <xref:System.ServiceModel.Activities.ReceiveReply>.</span><span class="sxs-lookup"><span data-stu-id="120cb-312">The content definition window for the <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.SendReply>, and <xref:System.ServiceModel.Activities.ReceiveReply> activities.</span></span>

- <span data-ttu-id="120cb-313">D’autres fonctions sont disponibles par le biais du clavier :</span><span class="sxs-lookup"><span data-stu-id="120cb-313">More functions are available via the keyboard:</span></span>

  - <span data-ttu-id="120cb-314">Quand vous modifiez les propriétés d’une activité, les groupes de propriétés peuvent être réduits à l’aide du clavier la première fois qu’ils ont le focus.</span><span class="sxs-lookup"><span data-stu-id="120cb-314">When editing the properties of an activity, property groups can be collapsed by keyboard the first time they are focused.</span></span>

  - <span data-ttu-id="120cb-315">Les icônes d’avertissement sont accessibles à l’aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="120cb-315">Warning icons are accessible by keyboard.</span></span>

  - <span data-ttu-id="120cb-316">Le bouton **Plus de propriétés** de la fenêtre **Propriétés** est accessible à l’aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="120cb-316">The **More Properties** button in the **Properties** window is accessible by keyboard.</span></span>

  - <span data-ttu-id="120cb-317">Les utilisateurs du clavier peuvent accéder aux éléments d’en-tête dans les volets **Arguments** et **Variables** du Concepteur de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="120cb-317">Keyboard users can access the header items in the **Arguments** and **Variables** panes of the Workflow Designer.</span></span>

- <span data-ttu-id="120cb-318">Une meilleure visibilité des éléments ayant le focus, par exemple dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="120cb-318">Improved visibility of items with focus, such as when:</span></span>

  - <span data-ttu-id="120cb-319">Ajout de lignes dans des grilles de données utilisées par le Concepteur de flux de travail et les concepteurs d’activités.</span><span class="sxs-lookup"><span data-stu-id="120cb-319">Adding rows to data grids used by the Workflow Designer and activity designers.</span></span>

  - <span data-ttu-id="120cb-320">Déplacement par tabulation dans les champs des activités <xref:System.ServiceModel.Activities.ReceiveReply> et <xref:System.ServiceModel.Activities.SendReply>.</span><span class="sxs-lookup"><span data-stu-id="120cb-320">Tabbing through fields in the <xref:System.ServiceModel.Activities.ReceiveReply> and <xref:System.ServiceModel.Activities.SendReply> activities.</span></span>

  - <span data-ttu-id="120cb-321">Définition de valeurs par défaut pour les variables ou les arguments</span><span class="sxs-lookup"><span data-stu-id="120cb-321">Setting default values for variables or arguments</span></span>

- <span data-ttu-id="120cb-322">Les lecteurs d’écran peuvent désormais reconnaître correctement :</span><span class="sxs-lookup"><span data-stu-id="120cb-322">Screen readers can now correctly recognize:</span></span>

  - <span data-ttu-id="120cb-323">Les points d’arrêt définis dans le Concepteur de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="120cb-323">Breakpoints set in the workflow designer.</span></span>

  - <span data-ttu-id="120cb-324">Les activités <xref:System.Activities.Statements.FlowSwitch%601>, <xref:System.Activities.Statements.FlowDecision> et <xref:System.ServiceModel.Activities.CorrelationScope>.</span><span class="sxs-lookup"><span data-stu-id="120cb-324">The <xref:System.Activities.Statements.FlowSwitch%601>, <xref:System.Activities.Statements.FlowDecision>, and <xref:System.ServiceModel.Activities.CorrelationScope> activities.</span></span>
  - <span data-ttu-id="120cb-325">Le contenu de l’activité <xref:System.ServiceModel.Activities.Receive>.</span><span class="sxs-lookup"><span data-stu-id="120cb-325">The contents of the <xref:System.ServiceModel.Activities.Receive> activity.</span></span>

  - <span data-ttu-id="120cb-326">Le type cible pour l’activité <xref:System.Activities.Statements.InvokeMethod>.</span><span class="sxs-lookup"><span data-stu-id="120cb-326">The Target Type for the <xref:System.Activities.Statements.InvokeMethod> activity.</span></span>

  - <span data-ttu-id="120cb-327">Le contrôle zone de liste déroulante Exception et la section Finally de l’activité <xref:System.Activities.Statements.TryCatch>.</span><span class="sxs-lookup"><span data-stu-id="120cb-327">The Exception combo box and the Finally section in the <xref:System.Activities.Statements.TryCatch> activity.</span></span>

  - <span data-ttu-id="120cb-328">Le contrôle zone de liste déroulante Type de message, le séparateur dans la fenêtre Ajouter des initialiseurs de corrélation, la fenêtre de définition du contenu et la fenêtre Définition de CorrelatesOn dans les activités de messagerie (<xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.SendReply> et <xref:System.ServiceModel.Activities.ReceiveReply>).</span><span class="sxs-lookup"><span data-stu-id="120cb-328">The Message Type combo box, the splitter in the Add Correlation Initializers window, the Content Definition window, and the CorrelatesOn Definition window in the messaging activities (<xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.SendReply>, and <xref:System.ServiceModel.Activities.ReceiveReply>).</span></span>

  - <span data-ttu-id="120cb-329">Transitions d’ordinateur d’état et destination des transitions.</span><span class="sxs-lookup"><span data-stu-id="120cb-329">State machine transitions and transitions destinations.</span></span>

  - <span data-ttu-id="120cb-330">Annotations et connecteurs sur les activités <xref:System.Activities.Statements.FlowDecision>.</span><span class="sxs-lookup"><span data-stu-id="120cb-330">Annotations and connectors on <xref:System.Activities.Statements.FlowDecision> activities.</span></span>

  - <span data-ttu-id="120cb-331">Les menus contextuels (accessibles en cliquant avec le bouton droit) pour les activités.</span><span class="sxs-lookup"><span data-stu-id="120cb-331">The context (right-click) menus for activities.</span></span>

  - <span data-ttu-id="120cb-332">Les éditeurs de valeurs de propriété, le bouton Effacer la recherche, les boutons a catégorie par et boutons de tri Par catégorie et Ordre alphabétique et la boîte de dialogue Éditeur d’expressions dans la grille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="120cb-332">The property value editors, the Clear Search button, the By Category and Alphabetical sort buttons, and the Expression Editor dialog in the properties grid.</span></span>

  - <span data-ttu-id="120cb-333">Le pourcentage de zoom dans le Concepteur de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="120cb-333">The zoom percentage in the Workflow Designer.</span></span>

  - <span data-ttu-id="120cb-334">Le séparateur dans les activités <xref:System.Activities.Statements.Parallel> et <xref:System.Activities.Statements.Pick>.</span><span class="sxs-lookup"><span data-stu-id="120cb-334">The separator in <xref:System.Activities.Statements.Parallel> and <xref:System.Activities.Statements.Pick> activities.</span></span>

  - <span data-ttu-id="120cb-335">L’activité <xref:System.Activities.Statements.InvokeDelegate>.</span><span class="sxs-lookup"><span data-stu-id="120cb-335">The <xref:System.Activities.Statements.InvokeDelegate> activity.</span></span>

  - <span data-ttu-id="120cb-336">La fenêtre Sélectionner les types pour les activités de dictionnaire (`Microsoft.Activities.AddToDictionary<TKey,TValue>`, `Microsoft.Activities.RemoveFromDictionary<TKey,TValue>`, etc.).</span><span class="sxs-lookup"><span data-stu-id="120cb-336">The Select Types window for dictionary activities (`Microsoft.Activities.AddToDictionary<TKey,TValue>`, `Microsoft.Activities.RemoveFromDictionary<TKey,TValue>`, etc.).</span></span>

  - <span data-ttu-id="120cb-337">La fenêtre Rechercher et sélectionner un type .NET.</span><span class="sxs-lookup"><span data-stu-id="120cb-337">The Browse and Select .NET Type window.</span></span>

  - <span data-ttu-id="120cb-338">Les barres de navigation dans le Concepteur de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="120cb-338">Breadcrumbs in the Workflow Designer.</span></span>

- <span data-ttu-id="120cb-339">Les utilisateurs qui choisissent des thèmes à contraste élevé verront de nombreuses améliorations de la visibilité du Concepteur de flux de travail et de ses contrôles, notamment de meilleurs ratios de contraste entre les éléments et des zones de sélection plus visibles utilisées pour les éléments actifs.</span><span class="sxs-lookup"><span data-stu-id="120cb-339">Users who choose High Contrast themes will see many improvements in the visibility of the Workflow Designer and its controls, like better contrast ratios between elements and more noticeable selection boxes used for focus elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="120cb-340">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="120cb-340">See Also</span></span>

[<span data-ttu-id="120cb-341">Nouveautés du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="120cb-341">What's new in the .NET Framework</span></span>](whats-new.md)
 
