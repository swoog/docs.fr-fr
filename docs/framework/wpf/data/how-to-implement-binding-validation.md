---
title: 'Procédure : Implémenter la validation de la liaison'
ms.date: 03/30/2017
helpviewer_keywords:
- validation of binding [WPF]
- data binding [WPF], validation of binding
- binding [WPF], validation of
ms.assetid: eb98b33d-9866-49ae-b981-bc5ff20d607a
ms.openlocfilehash: 3950df8b6f4b48a035c6ebf37d8d65c18cb82e1e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59197215"
---
# <a name="how-to-implement-binding-validation"></a>Procédure : Implémenter la validation de la liaison
Cet exemple montre comment utiliser un <xref:System.Windows.Controls.Validation.ErrorTemplate%2A> et un déclencheur de style pour fournir des commentaires visuels afin d’informer l’utilisateur lorsqu’une valeur non valide est entrée, basée sur une règle de validation personnalisée.  
  
## <a name="example"></a>Exemple  
 Le contenu textuel de la <xref:System.Windows.Controls.TextBox> dans l’exemple suivant est lié à la `Age` propriété (de type int) d’un objet de source de liaison nommée `ods`. La liaison est configurée pour utiliser une règle de validation nommée `AgeRangeRule` afin que si l’utilisateur entre des caractères non numériques ou une valeur inférieure à 21 ou supérieure à 130, un point d’exclamation rouge apparaisse en regard de la zone de texte et une info-bulle contenant le message d’erreur s’affiche lorsque l’utilisateur déplace la souris sur la zone de texte.  
  
 [!code-xaml[BindValidation#2](~/samples/snippets/csharp/VS_Snippets_Wpf/BindValidation/CSharp/Window1.xaml#2)]  
  
 L’exemple suivant montre l’implémentation de `AgeRangeRule`, qui hérite de <xref:System.Windows.Controls.ValidationRule> et remplace le <xref:System.Windows.Controls.ValidationRule.Validate%2A> (méthode). La méthode Int32.Parse() est appelée sur la valeur pour s’assurer qu’elle ne contient pas de caractères non valides. Le <xref:System.Windows.Controls.ValidationRule.Validate%2A> méthode retourne un <xref:System.Windows.Controls.ValidationResult> qui indique si la valeur est valide selon si une exception est interceptée lors de l’analyse et indique si la valeur d’âge se trouve en dehors des limites inférieure et supérieure.  
  
 [!code-csharp[BindValidation#3](~/samples/snippets/csharp/VS_Snippets_Wpf/BindValidation/CSharp/AgeRangeRule.cs#3)]  
  
 L’exemple suivant montre le personnalisé <xref:System.Windows.Controls.ControlTemplate> `validationTemplate` qui crée un point d’exclamation rouge pour informer l’utilisateur d’une erreur de validation. Les modèles de contrôle sont utilisés pour redéfinir l’apparence d’un contrôle.  
  
 [!code-xaml[BindValidation#4](~/samples/snippets/csharp/VS_Snippets_Wpf/BindValidation/CSharp/Window1.xaml#4)]  
  
 Comme indiqué dans l’exemple suivant, le <xref:System.Windows.Controls.ToolTip> qui affiche le message d’erreur est créé à l’aide du style nommé `textBoxInError`. Si la valeur de <xref:System.Windows.Controls.Validation.HasError%2A> est `true`, le déclencheur définit l’info-bulle de l’actuel <xref:System.Windows.Controls.TextBox> sa première erreur de validation. Le <xref:System.Windows.Data.Binding.RelativeSource%2A> a la valeur <xref:System.Windows.Data.RelativeSourceMode.Self>, qui fait référence à l’élément actuel.  
  
 [!code-xaml[BindValidation#5](~/samples/snippets/csharp/VS_Snippets_Wpf/BindValidation/CSharp/Window1.xaml#5)]  
  
 Pour obtenir un exemple complet, consultez [Validation de liaison, exemple](https://go.microsoft.com/fwlink/?LinkID=159972).  
  
 Notez que si vous ne fournissez pas un personnalisé <xref:System.Windows.Controls.Validation.ErrorTemplate%2A> le modèle d’erreur par défaut s’affiche pour fournir des commentaires visuels à l’utilisateur lorsqu’il existe une erreur de validation. Pour plus d’informations, consultez la section relative à la validation de données de la rubrique [Vue d’ensemble de la liaison de données](data-binding-overview.md). En outre, [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] fournit une règle de validation intégrée qui capte les exceptions levées pendant la mise à jour de la propriété de source de liaison. Pour plus d'informations, consultez <xref:System.Windows.Controls.ExceptionValidationRule>.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
