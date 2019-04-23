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
ms.openlocfilehash: 59fe1a5492b34d2aef88e81b86307498e3a5dc2c
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59612288"
---
# <a name="whats-new-in-accessibility-in-the-net-framework"></a>Nouveautés du .NET Framework dans le domaine de l’accessibilité

Le .NET Framework vise à rendre les applications plus accessibles pour vos utilisateurs. Les fonctionnalités d’accessibilité permettent à une application de fournir une expérience appropriée pour les utilisateurs des technologies d’assistance. À compter de .NET Framework 4.7.1, le .NET Framework inclut un grand nombre d’améliorations en matière d’accessibilité qui permettent aux développeurs de créer des applications accessibles.

## <a name="accessibility-switches"></a>Commutateurs d’accessibilité

Si votre application cible .NET Framework 4.7 ou une version antérieure, mais est exécutée sur .NET Framework 4.7.1 ou une version ultérieure, vous pouvez la configurer pour qu’elle active les fonctionnalités d’accessibilité. Si elle cible .NET Framework 4.7.1 ou une version ultérieure, vous pouvez également la configurer afin qu’elle utilise les fonctionnalités héritées (et ainsi qu’elle n’active pas les fonctionnalités d’accessibilité). Chaque version du .NET Framework qui inclut des fonctionnalités d’accessibilité a son propre commutateur d’accessibilité, que vous ajoutez à l’élément [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) dans la section [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) du fichier de configuration de l’application. Les commutateurs pris en charge sont les suivants :

|Version|Basculer|
|---|---|
|.NET Framework 4.7.1|"Switch.UseLegacyAccessibilityFeatures"|
|.NET Framework 4.7.2|"Switch.UseLegacyAccessibilityFeatures.2"|

### <a name="taking-advantage-of-accessibility-enhancements"></a>Activation des nouvelles fonctionnalités d’accessibilité

Les nouvelles fonctionnalités d’accessibilité sont activées par défaut pour les applications qui ciblent .NET Framework 4.7.1 ou version ultérieure. De plus, pour les applications qui ciblent une version antérieure du .NET Framework mais qui sont exécutées sur .NET Framework 4.7.1 ou une version ultérieure, vous pouvez désactiver les comportements d’accessibilité hérités (et ainsi utiliser les nouvelles fonctionnalités d’accessibilité) en ajoutant des commutateurs à l’élément [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) dans la section [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) du fichier de configuration de l’application et en les définissant à la valeur `false`. Le code ci-dessous montre comment activer les nouvelles fonctionnalités d’accessibilité de .NET Framework 4.7.1 :

```xml
<runtime>
    <!-- AppContextSwitchOverrides value attribute is in the form of 'key1=true|false;key2=true|false  -->
    <AppContextSwitchOverrides value="Switch.UseLegacyAccessibilityFeatures=false" />
</runtime>
```

Si vous choisissez d’activer les fonctionnalités d’accessibilité d’une version ultérieure du .NET Framework, vous devez aussi activer explicitement les fonctionnalités des versions antérieures du .NET Framework. Pour configurer votre application afin qu’elle utilise les nouvelles fonctionnalités d’accessibilité des deux versions du .NET Framework (4.7.1 et 4.7.2), vous devez ajouter l’élément [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant :

```xml
<runtime>
    <!-- AppContextSwitchOverrides value attribute is in the form of 'key1=true|false;key2=true|false  -->
    <AppContextSwitchOverrides value="Switch.UseLegacyAccessibilityFeatures=false;Switch.UseLegacyAccessibilityFeatures.2=false" />
</runtime>
```

### <a name="restoring-legacy-behavior"></a>Restauration du comportement hérité

Pour les applications ciblant la version 4.7.1 ou des versions ultérieures du .NET Framework, vous pouvez désactiver les fonctionnalités d’accessibilité en ajoutant des commutateurs à l’élément [`<AppContextSwitchOverrides>`](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) dans la section [`<runtime>`](~/docs/framework/configure-apps/file-schema/runtime/index.md) du fichier de configuration de l’application et en les définissant à la valeur `true`. Par exemple, la configuration suivante active les nouvelles fonctionnalités d’accessibilité de .NET Framework 4.7.2 :

```xml
<runtime>
    <!-- AppContextSwitchOverrides value attribute is in the form of 'key1=true|false;key2=true|false  -->
    <AppContextSwitchOverrides value="Switch.UseLegacyAccessibilityFeatures.2=true" />
</runtime>
```

## <a name="whats-new-in-accessibility-in-the-net-framework-472"></a>Nouveautés de .NET Framework 4.7.2 dans le domaine de l’accessibilité

.NET Framework 4.7.2 apporte de nouvelles fonctionnalités d’accessibilité dans les domaines suivants :

- [Windows Forms](#winforms472)

- [Windows Presentation Foundation (WPF)](#wpf472)

<a name="winforms472"></a>

### <a name="windows-forms"></a>Windows Forms

**Couleurs définies par le système d’exploitation dans les thèmes à contraste élevé**

À compter de .NET Framework 4.7.2, Windows Forms utilise les couleurs définies par le système d’exploitation dans les thèmes à contraste élevé. Cela concerne les contrôles suivants :

- Flèche déroulante du contrôle <xref:System.Windows.Forms.ToolStripDropDownButton>.

- Contrôles <xref:System.Windows.Forms.Button>, <xref:System.Windows.Forms.RadioButton> et <xref:System.Windows.Forms.CheckBox> dont la propriété <xref:System.Windows.Forms.ButtonBase.FlatStyle> est définie sur <xref:System.Windows.Forms.FlatStyle.Flat?displayProperty=nameWithType> ou <xref:System.Windows.Forms.FlatStyle.Popup?displayProperty=nameWithType>. Auparavant, les couleurs du texte sélectionné et de l’arrière-plan étaient sans contraste, ce qui nuisait à la lisibilité.

- Contrôles contenus dans un <xref:System.Windows.Forms.GroupBox> dont la propriété <xref:System.Windows.Forms.Control.Enabled> est définie sur `false`.

- Contrôles <xref:System.Windows.Forms.ToolStripButton>, <xref:System.Windows.Forms.ToolStripComboBox> et <xref:System.Windows.Forms.ToolStripDropDownButton> ayant un ratio contraste/luminosité accru dans le mode à contraste élevé.

- Propriété <xref:System.Windows.Forms.DataGridViewLinkCell.LinkColor> de <xref:System.Windows.Forms.DataGridViewLinkCell>.

**Améliorations du Narrateur**

.NET Framework 4.7.2 et les versions ultérieures améliorent la prise en charge du Narrateur de la façon suivante :

- Le Narrateur annonce la valeur de la propriété <xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeys?displayProperty=nameWithType> quand il annonce le texte d’un <xref:System.Windows.Forms.ToolStripMenuItem>.

- Il indique quand un <xref:System.Windows.Forms.ToolStripMenuItem> a sa propriété <xref:System.Windows.Forms.Control.Enabled> définie sur `false`.

- Il fournit des commentaires sur l’état d’une case à cocher quand la propriété <xref:System.Windows.Forms.ListView.CheckBoxes?displayProperty=nameWithType> est définie sur `true`.

- L’ordre de focus du mode balayage du Narrateur est cohérent avec l’ordre d’affichage des contrôles dans la fenêtre de la boîte de dialogue de téléchargement ClickOnce.

**Améliorations du contrôle DataGridView**

À compter de .NET Framework 4.7.2, le contrôle <xref:System.Windows.Forms.DataGridView> présente les améliorations d’accessibilité suivantes :

- Les lignes peuvent être triées à l’aide du clavier. Un utilisateur peut utiliser la touche F3 pour trier la colonne active.

- Quand <xref:System.Windows.Forms.DataGridView.SelectionMode?displayProperty=nameWithType> est défini sur <xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect?displayProperty=nameWithType>, l’en-tête de colonne change de couleur pour indiquer la colonne active quand l’utilisateur se déplace entre les cellules de la ligne active à l’aide de la touche Tab.

- La propriété <xref:System.Windows.Forms.AccessibleObject.Parent?displayProperty=nameWithType> d’un <xref:System.Windows.Forms.DataGridViewLinkCell.DataGridViewLinkCellAccessibleObject?displayProperty=nameWithType> retourne le bon contrôle parent.

**Amélioration des signaux visuels**

- Les contrôles <xref:System.Windows.Forms.RadioButton> et <xref:System.Windows.Forms.CheckBox> avec une propriété <xref:System.Windows.Forms.ButtonBase.Text> vide affichent un indicateur de focus quand ils deviennent actifs.

**Prise en charge améliorée de la grille des propriétés**

- Les éléments enfants du contrôle <xref:System.Windows.Forms.PropertyGrid> retournent désormais un `true` pour la propriété <xref:System.Windows.Automation.ValuePattern.IsReadOnlyProperty> uniquement quand un élément PropertyGrid est activé.

- Les éléments enfants du contrôle <xref:System.Windows.Forms.PropertyGrid> retournent un `false` pour la propriété <xref:System.Windows.Automation.AutomationElement.IsEnabledProperty> uniquement quand un élément PropertyGrid peut être changé par l’utilisateur.

**Navigation au clavier améliorée**

- Le contrôle <xref:System.Windows.Forms.ToolStripButton> peut être activé quand il est contenu dans un <xref:System.Windows.Forms.ToolStripPanel> dont la propriété <xref:System.Windows.Forms.ToolStripPanel.TabStop> a la valeur `true`

<a name="wpf472"></a>

### <a name="windows-presentation-foundation-wpf"></a>Windows Presentation Foundation (WPF)

**Changements apportés aux contrôles CheckBox et RadioButton**

Dans .NET Framework 4.7.1 et les versions antérieures, les contrôles WPF <xref:System.Windows.Controls.CheckBox?displayProperty=nameWIthType> et <xref:System.Windows.Controls.RadioButton?displayProperty=nameWIthType> ont des visuels de focus incohérents et, dans les thèmes standard et à contraste élevé, des visuels de focus inappropriés.  Ces problèmes se produisent dans les cas où les contrôles n’ont pas de contenu défini.  Cela peut rendre la transition entre les thèmes confuse et le visuel de focus difficile à voir.

Dans .NET Framework 4.7.2, ces visuels sont désormais plus cohérents entre les thèmes et plus facilement visibles dans les thèmes classique et à contraste élevé.

**Contrôles WinForms hébergés dans une application WPF**

Dans .NET Framework 4.7.1 et les versions antérieures, les contrôles WinForms hébergés dans une application WPF ne permettaient pas aux utilisateurs de sortir de la couche WinForms à l’aide de la touche Tab quand le contrôle WPF <xref:System.Windows.Forms.Integration.ElementHost> était le premier ou dernier contrôle dans cette couche. Dans .NET Framework 4.7.2, les utilisateurs peuvent désormais sortir de la couche WinForms à l’aide de la touche Tab.

Toutefois, les applications automatisées qui s’attendent à ce que le focus ne quitte jamais la couche WinForms risquent de ne plus fonctionner comme prévu.

## <a name="whats-new-in-accessibility-in-the-net-framework-471"></a>Nouveautés de .NET Framework 4.7.1 dans le domaine de l’accessibilité

.NET Framework 4.7.1 apporte de nouvelles fonctionnalités d’accessibilité dans les domaines suivants :

- [Windows Presentation Foundation (WPF)](#wpf471)

- [Windows Forms](#winforms471)

- [Contrôles web ASP.NET](#aspnet471)

- [Outils du kit SDK .NET](#tools471)

- [Concepteur de flux de travail Windows Workflow Foundation (WF)](#wf471)

<a name="wpf471"></a>

### <a name="windows-presentation-foundation-wpf"></a>Windows Presentation Foundation (WPF)

**Améliorations du lecteur d’écran**

Si les améliorations apportées à l’accessibilité sont activées, .NET Framework 4.7.1 inclut les améliorations suivantes qui affectent les lecteurs d’écran :

- Dans .NET Framework 4.7 et versions antérieures, les contrôles <xref:System.Windows.Controls.Expander> étaient annoncés par des lecteurs d’écran sous forme de boutons. À compter de .NET Framework 4.7.1, ils sont correctement annoncés en tant que groupes extensibles/réductibles.

- Dans .NET Framework 4.7 et versions antérieures, les contrôles <xref:System.Windows.Controls.DataGridCell> étaient annoncés par des lecteurs d’écran comme étant « personnalisés ». À compter de .NET Framework 4.7.1, ils sont maintenant correctement annoncés en tant que cellule de grille de données (localisée).

- À compter de .NET Framework 4.7.1, les lecteurs d’écran annoncent le nom d’un élément <xref:System.Windows.Controls.ComboBox> modifiable.

- Dans .NET Framework 4.7 et versions antérieures, les contrôles <xref:System.Windows.Controls.PasswordBox> étaient annoncés comme « aucun élément dans la vue » ou avaient sinon un comportement incorrect. Ce problème est résolu depuis .NET Framework 4.7.1.

**Prise en charge de zones dynamiques UIAutomation**

Les lecteurs d’écran tels que le Narrateur aident les personnes à lire le contenu de l’interface utilisateur d’une application, généralement par une sortie conversion de texte par synthèse vocale du contenu de l’interface utilisateur actif. Toutefois, si un élément d’interface utilisateur change et n’est pas actif, l’utilisateur peut ne pas en être informé et manquer des informations importantes. Les zones dynamiques visent à résoudre ce problème. Un développeur peut les utiliser pour informer le lecteur d’écran ou tout autre client UIAutomation qu’une modification importante a été apportée à un élément d’interface utilisateur. Le lecteur d’écran peut ensuite décider comment et quand informer l’utilisateur de cette modification.

Pour prendre en charge les zones dynamiques, les API suivantes ont été ajoutées à WPF :

- Champs <xref:System.Windows.Automation.AutomationElementIdentifiers.LiveSettingProperty?displayProperty=nameWithType> et <xref:System.Windows.Automation.AutomationElementIdentifiers.LiveRegionChangedEvent?displayProperty=nameWithType>, qui identifient la propriété **LiveSetting** et l’événement **LiveRegionChanged**. Il peuvent être définis à l’aide de XAML.

- Propriété jointe **AutomationProperties.LiveSetting**, qui informe le lecteur d’écran de l’importance de la modification de l’interface utilisateur pour l’utilisateur.

- Propriété <xref:System.Windows.Automation.AutomationProperties.LiveSettingProperty?displayProperty=nameWithType>, qui identifie la propriété jointe **AutomationProperties.LiveSetting**.

- Méthode <xref:System.Windows.Automation.Peers.AutomationPeer.GetLiveSettingCore%2A?displayProperty=nameWithType>, qui peut être remplacée pour fournir une valeur **LiveSetting**.

- Méthodes <xref:System.Windows.Automation.AutomationProperties.GetLiveSetting%2A?displayProperty=nameWithType> et <xref:System.Windows.Automation.AutomationProperties.SetLiveSetting%2A?displayProperty=nameWithType>, qui obtiennent et définissent une valeur **LiveSetting**.

- Énumération <xref:System.Windows.Automation.AutomationLiveSetting?displayProperty=nameWithType>, qui définit les valeurs **LiveSetting** possibles suivantes :

   - <xref:System.Windows.Automation.AutomationLiveSetting.Off?displayProperty=nameWithType>. L’élément n’envoie pas de notification si le contenu de la zone dynamique a changé.
   - <xref:System.Windows.Automation.AutomationLiveSetting.Polite?displayProperty=nameWithType>. L’élément envoie des notifications qui ne provoquent pas d’interruption si le contenu de la zone dynamique a changé.

   - <xref:System.Windows.Automation.AutomationLiveSetting.Assertive?displayProperty=nameWithType>. L’élément envoie des notifications qui provoquent des interruptions si le contenu de la zone dynamique a changé.

Vous pouvez créer une zone dynamique en définissant la propriété **AutomationProperties.LiveSetting** sur l’élément qui vous intéresse, comme indiqué dans l’exemple suivant :

```xaml
<TextBlock Name="myTextBlock" AutomationProperties.LiveSetting="Assertive">announcement</TextBlock>
```

Quand les données de la zone dynamique sont modifiées et que vous devez informer un lecteur d’écran, vous déclenchez explicitement un événement, comme indiqué dans l’exemple suivant.

```csharp
var peer = FrameworkElementAutomationPeer.FromElement(myTextBlock);

peer.RaiseAutomationEvent(AutomationEvents.LiveRegionChanged);
```

```vb
Dim peer = FrameworkElementAutomationPeer.FromElement(myTextBlock)
peer.RaiseAutomationEvent(AutomationEvents.LiveRegionChanged)

```

**Contraste élevé**

À compter de .NET Framework 4.7.1, des améliorations en matière de contraste élevé ont été apportées à différents contrôles WPF. Elles sont désormais visibles quand le thème <xref:System.Windows.SystemParameters.HighContrast%2A> est défini. Elles incluent notamment :

- Contrôle <xref:System.Windows.Controls.Expander>

    L’élément visuel de focus pour le contrôle <xref:System.Windows.Controls.Expander> est désormais visible. Les éléments visuels de clavier pour les contrôles <xref:System.Windows.Controls.ComboBox>, <xref:System.Windows.Controls.ListBox> et <xref:System.Windows.Controls.RadioButton> sont également visibles. Par exemple :

    Avant : 

    ![Contrôle Expander avec focus avant les améliorations apportées à l’accessibilité](media/expander-before.png)

    Après : 

    ![Contrôle Expander avec focus après les améliorations apportées à l’accessibilité](media/expander-after.png)

- Contrôles <xref:System.Windows.Controls.CheckBox> et <xref:System.Windows.Controls.RadioButton>

    Le texte dans les contrôles <xref:System.Windows.Controls.CheckBox> et <xref:System.Windows.Controls.RadioButton> est désormais plus facile à voir quand il est sélectionné dans les thèmes à contraste élevé. Par exemple :

    Avant : 

    ![Case d’option à contraste élevé avec focus avant les améliorations apportées à l’accessibilité](media/radio-button-before.png)

    Après : 

    ![Case d’option à contraste élevé avec focus après les améliorations apportées à l’accessibilité](media/radio-button-after.png)

- Contrôle <xref:System.Windows.Controls.ComboBox>

    À compter de .NET Framework 4.7.1, la bordure d’un contrôle <xref:System.Windows.Controls.ComboBox> désactivé est de la même couleur que le texte désactivé. Par exemple :

    Avant : 

     ![Texte et bordure d’un contrôle ComboBox désactivé avant les améliorations apportées à l’accessibilité](media/combo-disabled-before.png)

    Après :   

     ![Texte et bordure d’un contrôle ComboBox désactivé après les améliorations apportées à l’accessibilité](media/combo-disabled-after.png)

    En outre, les boutons désactivés et actifs utilisent la couleur de thème correcte.

    Avant :

    ![Couleurs de thème des boutons avant les améliorations apportées à l’accessibilité](media/button-themes-before.png) 

    Après : 

    ![Couleurs de thème des boutons après les améliorations apportées à l’accessibilité](media/button-themes-after.png) 

    Enfin, dans .NET Framework 4.7 et versions antérieures, la définition du style d’un contrôle <xref:System.Windows.Controls.ComboBox> sur `Toolbar.ComboBoxStyleKey` rendait la flèche déroulante invisible. Ce problème est résolu depuis .NET Framework 4.7.1. Par exemple :

    Avant : 

    ![Toolbar.ComboBoxStyleKey avant les améliorations apportées à l’accessibilité](media/comboboxstylekey-before.png) 

    Après : 

    ![Toolbar.ComboBoxStyleKey après les améliorations apportées à l’accessibilité](media/comboboxstylekey-after.png) 

- Contrôle <xref:System.Windows.Controls.DataGrid>

    À compter de .NET Framework 4.7.1, la flèche d’indicateur de tri dans les contrôles <xref:System.Windows.Controls.DataGrid> utilise maintenant les couleurs de thème correctes. Par exemple :

    Avant : 

    ![Flèche d’indicateur de tri avant les améliorations apportées à l’accessibilité](media/sort-indicator-before.png) 

    Après :   

    ![Flèche d’indicateur de tri après les améliorations apportées à l’accessibilité](media/sort-indicator-after.png) 

    En outre, dans .NET Framework 4.7 et versions antérieures, le style de lien par défaut prenait une couleur incorrecte en pointant avec la souris dans des modes de contraste élevé. Ce problème est résolu depuis .NET Framework 4.7.1. De même, les colonnes de cases à cocher <xref:System.Windows.Controls.DataGrid> utilisent les couleurs attendues pour les commentaires de focus clavier depuis .NET Framework 4.7.1.

    Avant : 

    ![Style de lien par défaut DataGrid avant les améliorations apportées à l’accessibilité](media/default-link-style-before.png) 

    Après :    

    ![Style de lien par défaut DataGrid après les améliorations apportées à l’accessibilité](media/default-link-style-after.png) 

Pour plus d’informations sur les améliorations apportées à l’accessibilité dans WPF dans .NET Framework 4.7.1, consultez [Améliorations apportées à l’accessibilité dans WPF](../migration-guide/retargeting/4.7-4.7.1.md#accessibility-improvements-in-wpf).

<a name="winforms471"></a>

### <a name="windows-forms-accessibility-improvements"></a>Améliorations apportées à l’accessibilité dans les Windows Forms

Dans .NET Framework 4.7.1, WinForms (Windows Forms) présente des modifications de l’accessibilité dans les domaines suivants.

**Affichage amélioré en mode de contraste élevé**

À compter de .NET Framework 4.7.1, différents contrôles WinForms offrent un meilleur rendu dans les modes de contraste élevé disponibles dans le système d’exploitation. Windows 10 a modifié les valeurs de certaines couleurs système à contraste élevé et Windows Forms repose sur le framework Windows 10 Win32. Pour une expérience optimale, procédez à une exécution sur la dernière version de Windows et activez les dernières modifications du système d’exploitation en ajoutant un fichier app.manifest dans une application de test et supprimez les marques de commentaire de la ligne de système d’exploitation Windows 10 pour qu’elle ressemble à ce qui suit :

```xml
<!-- Windows 10 -->
<supportedOS Id=”{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}” />
```

Voici quelques exemples de modifications du contraste élevé :

- Les coches dans les éléments <xref:System.Windows.Forms.MenuStrip> sont plus faciles à afficher.

- Quand ils sont sélectionnés, les éléments <xref:System.Windows.Forms.MenuStrip> désactivés sont plus faciles à afficher.

- Le texte dans un contrôle <xref:System.Windows.Forms.Button> sélectionné contraste avec la couleur de sélection.

- Le texte désactivé est plus facile à lire. Par exemple :

    Avant :

    ![Texte désactivé avant les améliorations apportées à l’accessibilité](media/wf-disabled-before.png) 

    Après :

    ![Texte désactivé après les améliorations apportées à l’accessibilité](media/wf-disabled-after.png) 

- Améliorations du contraste élevé dans la boîte de dialogue Thread Exception (Exception de thread).

**Prise en charge améliorée du Narrateur**

Windows Forms dans .NET Framework 4.7.1 inclut les améliorations en matière d’accessibilité suivantes pour le Narrateur :

- Le contrôle <xref:System.Windows.Forms.MonthCalendar> est accessible par le Narrateur, ainsi que par d’autres outils UI Automation.

- Le contrôle <xref:System.Windows.Forms.CheckedListBox> avertit le Narrateur quand l’état de case à cocher d’un élément a changé pour que l’utilisateur sache que la valeur d’un élément de liste est modifiée.

- Le contrôle <xref:System.Windows.Forms.DataGridViewCell> signale l’état Lecture seule correct au Narrateur.

- Le Narrateur peut désormais lire le texte <xref:System.Windows.Forms.ToolStripMenuItem> désactivé, alors qu’il ignorait précédemment les éléments de menu désactivés.

**Prise en charge améliorée des modèles d’accessibilité UIAutomation**

À compter de .NET Framework 4.7.1, les développeurs d’outils technologiques d’accessibilité peuvent tirer parti des modèles d’accessibilité d’API courants et des propriétés de plusieurs contrôles WinForms. Ces améliorations en matière d’accessibilité sont notamment :

- <xref:System.Windows.Forms.ComboBox> et <xref:System.Windows.Forms.ToolStripSplitButton> prennent maintenant en charge le [modèle Développer/Réduire](../ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).

- <xref:System.Windows.Forms.DataGridViewCheckBoxCell> prend maintenant en charge le [modèle Basculer](../ui-automation/implementing-the-ui-automation-toggle-control-pattern.md).

- Le contrôle <xref:System.Windows.Forms.ToolStripItem> prend en charge la propriété <xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.Name> et le [modèle Développer/Réduire](../ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).

- Les contrôles <xref:System.Windows.Forms.NumericUpDown> et <xref:System.Windows.Forms.DomainUpDown> prennent en charge la propriété <xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.Name>.

**Expérience améliorée avec l’Explorateur de propriétés**

À compter de .NET Framework 4.7.1, Windows Forms propose :

- Une meilleure navigation au clavier via les différentes fenêtres de sélection de liste déroulante.
- Une réduction des taquets de tabulation inutiles.
- Des rapports plus élaborés sur les types de contrôles.
- Un comportement amélioré du Narrateur.

<a name="aspnet471"></a>

### <a name="aspnet-web-controls"></a>Contrôles web ASP.NET

À compter de .NET Framework 4.7.1 et de Visual Studio 2017 15.3, ASP.NET améliore le fonctionnement des contrôles web ASP.NET avec la technologie d’accessibilité de Visual Studio. Les changements apportés sont les suivants :

- Changements visant à implémenter les modèles d’accessibilité de l’interface utilisateur manquants dans les contrôles, comme la boîte de dialogue **Ajouter un champ** de l’Assistant **Vue Détails** ou la boîte de dialogue **Configurer ListView** de l’Assistant **ListView**.

- Changements visant à améliorer l’affichage en mode de contraste élevé, comme **l’éditeur de champs du pagineur de données**.

- Changements visant à améliorer les expériences de navigation au clavier pour les contrôles, comme la boîte de dialogue **Champs** de l’Assistant **Modifier les champs du pagineur** du contrôle DataPager, la boîte de dialogue **Configurer ObjectContext** ou la boîte de dialogue **Configurer la sélection de données** de l’Assistant **Configurer la source de données**.

<a name="tools471"></a>

### <a name="net-sdk-tools"></a>Outils du kit SDK . NET

Divers problèmes d’accessibilité ont été corrigés dans [l’outil Éditeur de Configuration (SvcConfigEditor.exe)](../wcf/configuration-editor-tool-svcconfigeditor-exe.md) et [l’outil Service Trace Viewer (SvcTraceViewer.exe)](../wcf/service-trace-viewer-tool-svctraceviewer-exe.md). La plupart étaient des problèmes sans gravité, par exemple, un nom non défini ou certains modèles d’automatisation de l’interface utilisateur non implémentés correctement. La majorité des utilisateurs ne remarqueront même pas ces problèmes, mais les clients qui utilisent des technologies d’assistance comme les lecteurs d’écran trouveront les outils de ce kit SDK plus accessibles.

Ces améliorations changent certains comportements précédents, comme l’ordre de focus du clavier.

<a name="wf471"></a>

### <a name="windows-workflow-foundation-wf-workflow-designer"></a>Concepteur de flux de travail Windows Workflow Foundation (WF)

Les changements apportés pour améliorer l’accessibilité dans le Concepteur de flux de travail sont les suivants :

- L’ordre de tabulation est maintenant de gauche à droite et de haut en bas dans certains contrôles :

  - La fenêtre d’initialisation de la corrélation pour définir les données de corrélation pour l’activité <xref:System.ServiceModel.Activities.InitializeCorrelation>.

  - La fenêtre de définition du contenu pour les activités <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.SendReply> et <xref:System.ServiceModel.Activities.ReceiveReply>.

- D’autres fonctions sont disponibles par le biais du clavier :

  - Quand vous modifiez les propriétés d’une activité, les groupes de propriétés peuvent être réduits à l’aide du clavier la première fois qu’ils ont le focus.

  - Les icônes d’avertissement sont accessibles à l’aide du clavier.

  - Le bouton **Plus de propriétés** de la fenêtre **Propriétés** est accessible à l’aide du clavier.

  - Les utilisateurs du clavier peuvent accéder aux éléments d’en-tête dans les volets **Arguments** et **Variables** du Concepteur de flux de travail.

- Une meilleure visibilité des éléments ayant le focus, par exemple dans les cas suivants :

  - Ajout de lignes dans des grilles de données utilisées par le Concepteur de flux de travail et les concepteurs d’activités.

  - Déplacement par tabulation dans les champs des activités <xref:System.ServiceModel.Activities.ReceiveReply> et <xref:System.ServiceModel.Activities.SendReply>.

  - Définition de valeurs par défaut pour les variables ou les arguments

- Les lecteurs d’écran peuvent désormais reconnaître correctement :

  - Les points d’arrêt définis dans le Concepteur de flux de travail.

  - Les activités <xref:System.Activities.Statements.FlowSwitch%601>, <xref:System.Activities.Statements.FlowDecision> et <xref:System.ServiceModel.Activities.CorrelationScope>.
  - Le contenu de l’activité <xref:System.ServiceModel.Activities.Receive>.

  - Le type cible pour l’activité <xref:System.Activities.Statements.InvokeMethod>.

  - Le contrôle zone de liste déroulante Exception et la section Finally de l’activité <xref:System.Activities.Statements.TryCatch>.

  - Le contrôle zone de liste déroulante Type de message, le séparateur dans la fenêtre Ajouter des initialiseurs de corrélation, la fenêtre de définition du contenu et la fenêtre Définition de CorrelatesOn dans les activités de messagerie (<xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.SendReply> et <xref:System.ServiceModel.Activities.ReceiveReply>).

  - Transitions d’ordinateur d’état et destination des transitions.

  - Annotations et connecteurs sur les activités <xref:System.Activities.Statements.FlowDecision>.

  - Les menus contextuels (accessibles en cliquant avec le bouton droit) pour les activités.

  - Les éditeurs de valeurs de propriété, le bouton Effacer la recherche, les boutons a catégorie par et boutons de tri Par catégorie et Ordre alphabétique et la boîte de dialogue Éditeur d’expressions dans la grille des propriétés.

  - Le pourcentage de zoom dans le Concepteur de flux de travail.

  - Le séparateur dans les activités <xref:System.Activities.Statements.Parallel> et <xref:System.Activities.Statements.Pick>.

  - L’activité <xref:System.Activities.Statements.InvokeDelegate>.

  - La fenêtre Sélectionner les types pour les activités de dictionnaire (`Microsoft.Activities.AddToDictionary<TKey,TValue>`, `Microsoft.Activities.RemoveFromDictionary<TKey,TValue>`, etc.).

  - La fenêtre Rechercher et sélectionner un type .NET.

  - Les barres de navigation dans le Concepteur de flux de travail.

- Les utilisateurs qui choisissent des thèmes à contraste élevé verront de nombreuses améliorations de la visibilité du Concepteur de flux de travail et de ses contrôles, notamment de meilleurs ratios de contraste entre les éléments et des zones de sélection plus visibles utilisées pour les éléments actifs.

## <a name="see-also"></a>Voir aussi

- [Nouveautés du .NET Framework](whats-new.md)
