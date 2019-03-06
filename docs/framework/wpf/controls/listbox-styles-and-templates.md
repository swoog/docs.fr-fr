---
title: Styles et modèles ListBox
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], ListBox
- templates [WPF], ListBox
- states [WPF], ListBox
- ControlTemplate [WPF], ListBox
- parts [WPF], ListBox
- ListBox [WPF], styles and templates
ms.assetid: fc5764cb-c27b-495b-88d4-d969a8213ccb
ms.openlocfilehash: e3171322e0f24060422f54c74f4d2b4751433415
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357896"
---
# <a name="listbox-styles-and-templates"></a>Styles et modèles ListBox
Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.ListBox> contrôle. Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique. Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).  
  
## <a name="listbox-parts"></a>Parties de ListBox  
 Le <xref:System.Windows.Controls.ListBox> contrôle n’a pas de composants nommés.  
  
 Lorsque vous créez un <xref:System.Windows.Controls.ControlTemplate> pour un <xref:System.Windows.Controls.ListBox>, votre modèle peut contenir un <xref:System.Windows.Controls.ItemsPresenter> au sein d’un <xref:System.Windows.Controls.ScrollViewer>. (Le <xref:System.Windows.Controls.ItemsPresenter> affiche chaque élément dans le <xref:System.Windows.Controls.ListBox>; le <xref:System.Windows.Controls.ScrollViewer> permet le défilement dans le contrôle).  Si le <xref:System.Windows.Controls.ItemsPresenter> n’est pas l’enfant direct de la <xref:System.Windows.Controls.ScrollViewer>, vous devez donner le <xref:System.Windows.Controls.ItemsPresenter> le nom, `ItemsPresenter`.  
  
## <a name="listbox-states"></a>États du contrôle ListBox  
 Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ListBox> contrôle.  
  
|Nom VisualState|Nom VisualStateGroup|Description|  
|-|-|-|  
|Valide|ValidationStates|Le contrôle est valide.|  
|InvalidFocused|ValidationStates|Le contrôle n’est pas valide et a le focus.|  
|InvalidUnfocused|ValidationStates|Le contrôle n’est pas valide et n’a pas le focus.|  
  
## <a name="listboxitem-parts"></a>Parties de ListBoxItem  
 Le <xref:System.Windows.Controls.ListBoxItem> contrôle n’a pas de composants nommés.  
  
## <a name="listboxitem-states"></a>États de ListBoxItem  
 Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ListBox> contrôle.  
  
|Nom VisualState|Nom VisualStateGroup|Description|  
|-|-|-|  
|Normale|CommonStates|État par défaut.|  
|MouseOver|CommonStates|Le pointeur de souris est positionné sur le contrôle.|  
|Désactivé|CommonStates|L’élément est désactivé.|  
|Avec focus|FocusStates|L’élément a le focus.|  
|Sans focus|FocusStates|L’élément n’a pas le focus.|  
|Non sélectionné|SelectionStates|L’élément n’est pas sélectionné.|  
|Selected|SelectionStates|L’élément est actuellement sélectionné.|  
|SelectedUnfocused|SelectionStates|L’élément est sélectionné mais n’a pas le focus.|  
|Valide|ValidationStates|Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.|  
|InvalidFocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.|  
|InvalidUnfocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.|  
  
## <a name="listbox-controltemplate-example"></a>Exemple de ControlTemplate pour les contrôles ListBox  
 L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour le <xref:System.Windows.Controls.ListBox> et <xref:System.Windows.Controls.ListBoxItem> contrôles.  
  
 [!code-xaml[ControlTemplateExamples#ListBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/listbox.xaml#listbox)]  
  
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
