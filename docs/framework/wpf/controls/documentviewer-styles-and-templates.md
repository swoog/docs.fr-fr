---
title: Styles et modèles DocumentViewer
ms.date: 03/30/2017
helpviewer_keywords:
- templates [WPF], DocumentViewer
- DocumentViewer [WPF], styles and templates
- states [WPF], DocumentViewer
- ControlTemplate [WPF], DocumentViewer
- parts [WPF], DocumentViewer
- styles [WPF], DocumentViewer
ms.assetid: 6bd4ff8f-ea6a-4084-ac58-e7a67446ce1c
ms.openlocfilehash: 4e91a640b36e4793567c9e728fd71ec8ce596743
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61911766"
---
# <a name="documentviewer-styles-and-templates"></a>Styles et modèles DocumentViewer
Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.DocumentViewer> contrôle. Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique. Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).  
  
## <a name="documentviewer-parts"></a>Composants de DocumentViewer  
 Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.DocumentViewer> contrôle.  
  
|Élément|Type|Description|  
|-|-|-|  
|PART_ContentHost|<xref:System.Windows.Controls.ScrollViewer>|Le contenu et la zone de défilement.|  
|PART_FindToolBarHost|<xref:System.Windows.Controls.ContentControl>|La zone de recherche, en bas par défaut.|  
  
## <a name="documentviewer-states"></a>États de DocumentViewer  
 Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.DocumentViewer> contrôle.  
  
|Nom VisualState|Nom VisualStateGroup|Description|  
|-|-|-|  
|Valide|ValidationStates|Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.|  
|InvalidFocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.|  
|InvalidUnfocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.|  
  
## <a name="documentviewer-controltemplate-example"></a>Exemple de ControlTemplate DocumentViewer  
 L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.DocumentViewer> contrôle.  
  
 [!code-xaml[ControlTemplateExamples#DocumentViewer](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/documentviewer.xaml#documentviewer)]  
  
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
