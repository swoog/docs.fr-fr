---
title: "Procédure : Créer un contrôle avec touche d'accès rapide et habillage du texte"
ms.date: 03/30/2017
helpviewer_keywords:
- access keys [WPF], control for
- controls [WPF], text wrapping
- wrapping text [WPF]
- keys [WPF], control for
- controls [WPF], access keys
- text wrapping [WPF]
ms.assetid: 205099d9-2551-4302-a25e-a15af9f67e04
ms.openlocfilehash: bb8379776066802277886b54c60c502ad58768e0
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "56748165"
---
# <a name="how-to-create-a-control-that-has-an-access-key-and-text-wrapping"></a>Procédure : Créer un contrôle avec touche d'accès rapide et habillage du texte
Cet exemple montre comment créer un contrôle avec touche d’accès rapide, prenant en charge l’habillage du texte. L’exemple utilise un <xref:System.Windows.Controls.Label> contrôle pour illustrer ces concepts.  
  
## <a name="example"></a>Exemple  
 **Ajouter l’habillage du texte à votre étiquette**  
  
 Le <xref:System.Windows.Controls.Label> contrôle ne prend pas en charge l’habillage du texte. Si vous avez besoin d’une étiquette couvrant plusieurs lignes, vous pouvez imbriquer un autre élément qui prend en charge l’habillage du texte d’habillage et le placer dans l’étiquette. L’exemple suivant montre comment utiliser un <xref:System.Windows.Controls.TextBlock> pour créer une étiquette couvrant plusieurs lignes de texte.  
  
 [!code-xaml[LabelSnippet#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LabelSnippet/CS/Pane1.xaml#5)]  
  
 **Ajouter une touche d’accès rapide et l’habillage du texte à votre étiquette**  
  
 Si vous avez besoin d’un <xref:System.Windows.Controls.Label> qui a une clé d’accès (mnémonique), utilisez le <xref:System.Windows.Controls.AccessText> élément qui se trouve dans le <xref:System.Windows.Controls.Label>.  
  
 Les contrôles tels que <xref:System.Windows.Controls.Label>, <xref:System.Windows.Controls.Button>, <xref:System.Windows.Controls.RadioButton>, <xref:System.Windows.Controls.CheckBox>, <xref:System.Windows.Controls.MenuItem>, <xref:System.Windows.Controls.TabItem>, <xref:System.Windows.Controls.Expander>, et <xref:System.Windows.Controls.GroupBox> ont des modèles de contrôle par défaut. Ces modèles contiennent un <xref:System.Windows.Controls.ContentPresenter>. Une des propriétés que vous pouvez définir sur le <xref:System.Windows.Controls.ContentPresenter> est <xref:System.Windows.Controls.ContentPresenter.RecognizesAccessKey%2A>= « true », qui vous permet de spécifier une clé d’accès pour le contrôle.  
  
 L’exemple suivant montre comment créer un <xref:System.Windows.Controls.Label> qui a une clé d’accès et prend en charge l’habillage du texte. Pour activer l’habillage du texte, l’exemple définit le <xref:System.Windows.Controls.AccessText.TextWrapping%2A> propriété et utilise un caractère de soulignement pour spécifier la clé d’accès. (Le caractère qui suit immédiatement le caractère de soulignement est la touche d’accès rapide.)  
  
 [!code-xaml[LabelSnippet#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LabelSnippet/CS/Pane1.xaml#4)]  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Définissez la propriété de cible d’une étiquette](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms752101(v=vs.90))
