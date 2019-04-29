---
title: 'Procédure : Créer du texte avec une ombre'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], shadow effects
- shadow effects in text [WPF]
- text [WPF], shadowed
ms.assetid: 6ab9c754-6001-4708-b479-5367f2fd1a35
ms.openlocfilehash: a2225e297dbc0b5f9d49799cb34eb5539746e62e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776820"
---
# <a name="how-to-create-text-with-a-shadow"></a>Procédure : Créer du texte avec une ombre
Les exemples de cette section indiquent comment créer un effet d’ombre pour du texte affiché.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Media.Effects.DropShadowEffect> objet permet de créer des effets d’ombre pour une variété de dépôt [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] objets. L’exemple suivant présente un effet d’ombre portée appliqué au texte. Dans ce cas, l’ombre est une ombre légère, ce qui signifie que sa couleur devient floue.  
  
 ![Ombre du texte avec adoucissement &#61; 0,25](./media/how-to-create-text-with-a-shadow/drop-shadow-text-effect.jpg) 
  
 Vous pouvez contrôler la largeur d’une ombre en définissant le <xref:System.Windows.Media.Effects.DropShadowEffect.ShadowDepth%2A> propriété. La valeur `4.0` indique une largeur d’ombre de 4 pixels. Vous pouvez contrôler la douceur, ou flou d’une ombre en modifiant le <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> propriété. La valeur `0.0` indique aucun flou. L’exemple de code suivant montre comment créer une ombre légère.  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet1)]  
  
> [!NOTE]
>  Ces effets d’ombre ne traversent pas le [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] pipeline de rendu de texte. En conséquence, ClearType est désactivé lors de l’utilisation de ces effets.  
  
 L’exemple suivant présente un effet d’ombre portée marquée appliqué au texte. Dans ce cas, l’ombre n’est pas floue.  
  
 ![Ombre du texte avec adoucissement &#61; 0](./media/how-to-create-text-with-a-shadow/text-shadow-softness.jpg) 
  
 Vous pouvez créer une ombre en définissant le <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> propriété `0.0`, qui indique qu’aucun flou n’est utilisé. Vous pouvez contrôler la direction de l’ombre en modifiant le <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> propriété. Définissez la valeur directionnelle de cette propriété à un degré entre `0` et `360`. L’illustration suivante montre les valeurs directionnelles du <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> paramètre de propriété.  
  
 ![Paramètre de degré DropShadow de l’ombre](./media/how-to-create-text-with-a-shadow/drop-shadow-degree-setting.png)
  
 L’exemple de code suivant montre comment créer une ombre marquée.  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet2)]  
  
## <a name="using-a-blur-effect"></a>Utilisation d’un effet de flou  
 Un <xref:System.Windows.Media.Effects.BlurBitmapEffect> peut être utilisé pour créer un effet de clichés instantanés pouvant être placé derrière un objet texte. Un effet bitmap flou appliqué au texte rend le texte flou uniformément dans toutes les directions.  
  
 L’exemple suivant présente un effet de flou appliqué au texte.  
  
 ![Ombre du texte utilisant BlurBitmapEffect](./media/how-to-create-text-with-a-shadow/text-shadow-blur-effect.jpg)  
  
 L’exemple de code suivant montre comment créer un effet de flou.  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet6](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/BlurShadows.xaml#textshadowsnippet6)]  
  
## <a name="using-a-translate-transform"></a>Utilisation d’une transformation de traduction  
 Un <xref:System.Windows.Media.TranslateTransform> peut être utilisé pour créer un effet de clichés instantanés pouvant être placé derrière un objet texte.  
  
 Le code suivant exemple utilise un <xref:System.Windows.Media.TranslateTransform> pour décaler le texte. Dans cet exemple, une copie légèrement décalée de texte en dessous du texte principal crée un effet d’ombre.  
  
 ![Ombre du texte utilisant TranslateTransform](./media/how-to-create-text-with-a-shadow/text-transform-shadow-effect.jpg)    
  
 L’exemple de code suivant indique comment créer une transformation pour un effet d’ombre.  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet7](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/TransformShadows.xaml#textshadowsnippet7)]
