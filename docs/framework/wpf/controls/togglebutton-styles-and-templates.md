---
title: Styles et modèles ToggleButton
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], ToggleButton
- ToggleButton [WPF], styles and templates
- ControlTemplate [WPF], ToggleButton
- styles [WPF], ToggleButton
- templates [WPF], ToggleButton
- parts [WPF], ToggleButton
ms.assetid: 54f23f30-4bcb-4f09-8ce4-376a13a255a1
ms.openlocfilehash: 46fd7d07c3904ee752ae3f467f65af4b0c031c84
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790752"
---
# <a name="togglebutton-styles-and-templates"></a>Styles et modèles ToggleButton

Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Primitives.ToggleButton> contrôle. Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique. Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).

## <a name="togglebutton-parts"></a>Composants de ToggleButton

Le <xref:System.Windows.Controls.Primitives.ToggleButton> contrôle n’a pas de composants nommés.

## <a name="togglebutton-states"></a>États de contrôle ToggleButton

Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Primitives.ToggleButton> contrôle.

|Nom VisualState|Nom VisualStateGroup|Description|
|-|-|-|
|Normale|CommonStates|État par défaut.|
|MouseOver|CommonStates|Le pointeur de la souris est positionné sur le contrôle.|
|Appuyé|CommonStates|Le contrôle est enfoncé.|
|Désactivé|CommonStates|Le contrôle est désactivé.|
|Avec focus|FocusStates|Le contrôle a le focus.|
|Sans focus|FocusStates|Le contrôle n’a pas le focus.|
|Activé|CheckStates|<xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> a la valeur `true`.|
|Elle est désactivée|CheckStates|<xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> a la valeur `false`.|
|Indeterminate|CheckStates|<xref:System.Windows.Controls.Primitives.ToggleButton.IsThreeState%2A> est `true`, et <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> est `null`.|
|Valide|ValidationStates|Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.|
|InvalidFocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.|
|InvalidUnfocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.|

> [!NOTE]
> Si l’état visuel indéterminé n’existe pas dans votre modèle de contrôle, l’état visuel Unchecked sera être utilisé en tant qu’état visuel par défaut.

## <a name="togglebutton-controltemplate-example"></a>Exemple de ControlTemplate ToggleButton

L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Primitives.ToggleButton> contrôle.

[!code-xaml[ControlTemplateExamples#ToggleButton](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/combobox.xaml#togglebutton)]

L’exemple précédent utilise une ou plusieurs des ressources suivantes.

[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]

Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [Styles et modèles Control](control-styles-and-templates.md)
- [Personnalisation des contrôles](control-customization.md)
- [Application d’un style et création de modèles](styling-and-templating.md)
- [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md)
