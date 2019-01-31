---
title: "Procédure : Dessiner du texte sur l'arrière-plan d'un contrôle"
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], drawing text to backgrounds
- text [WPF], drawing to control backgrounds
- drawing [WPF], text to control backgrounds
- backgrounds [WPF], drawing text to
- typography [WPF], drawing text to control backgrounds
ms.assetid: 686d8fba-f61c-4974-a871-c635d67a7f69
ms.openlocfilehash: 9be4eb92021a62baaf6b43198587616d00cc265e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259252"
---
# <a name="how-to-draw-text-to-a-controls-background"></a><span data-ttu-id="3a8fe-102">Procédure : Dessiner du texte sur l'arrière-plan d'un contrôle</span><span class="sxs-lookup"><span data-stu-id="3a8fe-102">How to: Draw Text to a Control's Background</span></span>
<span data-ttu-id="3a8fe-103">Vous pouvez dessiner du texte directement sur l’arrière-plan d’un contrôle en convertissant une chaîne de texte à un <xref:System.Windows.Media.FormattedText> de l’objet, puis en dessinant l’objet du contrôle <xref:System.Windows.Media.DrawingContext>.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-103">You can draw text directly to the background of a control by converting a text string to a <xref:System.Windows.Media.FormattedText> object, and then drawing the object to the control's <xref:System.Windows.Media.DrawingContext>.</span></span> <span data-ttu-id="3a8fe-104">Vous pouvez également utiliser cette technique pour le dessin de l’arrière-plan des objets dérivés de <xref:System.Windows.Controls.Panel>, tel que <xref:System.Windows.Controls.Canvas> et <xref:System.Windows.Controls.StackPanel>.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-104">You can also use this technique for drawing to the background of objects derived from <xref:System.Windows.Controls.Panel>, such as <xref:System.Windows.Controls.Canvas> and <xref:System.Windows.Controls.StackPanel>.</span></span>  
  
 <span data-ttu-id="3a8fe-105">![Contrôles affichant le texte en arrière-plan](../../../../docs/framework/wpf/advanced/media/drawtext2background01.png "DrawText2Background01")</span><span class="sxs-lookup"><span data-stu-id="3a8fe-105">![Controls displaying text as background](../../../../docs/framework/wpf/advanced/media/drawtext2background01.png "DrawText2Background01")</span></span>  
<span data-ttu-id="3a8fe-106">Exemple de contrôles avec des arrière-plans de texte personnalisés</span><span class="sxs-lookup"><span data-stu-id="3a8fe-106">Example of controls with custom text backgrounds</span></span>  
  
## <a name="example"></a><span data-ttu-id="3a8fe-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a8fe-107">Example</span></span>  
 <span data-ttu-id="3a8fe-108">Pour dessiner à l’arrière-plan d’un contrôle, créez un nouveau <xref:System.Windows.Media.DrawingBrush> de l’objet et de dessiner le texte converti à l’objet <xref:System.Windows.Media.DrawingContext>.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-108">To draw to the background of a control, create a new <xref:System.Windows.Media.DrawingBrush> object and draw the converted text to the object's <xref:System.Windows.Media.DrawingContext>.</span></span> <span data-ttu-id="3a8fe-109">Ensuite, assignez le nouveau <xref:System.Windows.Media.DrawingBrush> à la propriété du contrôle d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-109">Then, assign the new <xref:System.Windows.Media.DrawingBrush> to the control's background property.</span></span>  
  
 <span data-ttu-id="3a8fe-110">L’exemple de code suivant montre comment créer un <xref:System.Windows.Media.FormattedText> de l’objet et dessiner sur l’arrière-plan d’un <xref:System.Windows.Controls.Label> et <xref:System.Windows.Controls.Button> objet.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-110">The following code example shows how to create a <xref:System.Windows.Media.FormattedText> object and draw to the background of a <xref:System.Windows.Controls.Label> and <xref:System.Windows.Controls.Button> object.</span></span>  
  
 [!code-csharp[DrawTextToControlBackground#DrawTextToControlBackground1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawTextToControlBackground/CSHARP/Window1.xaml.cs#drawtexttocontrolbackground1)]  
  
## <a name="see-also"></a><span data-ttu-id="3a8fe-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a8fe-111">See also</span></span>
- <xref:System.Windows.Media.FormattedText>
- [<span data-ttu-id="3a8fe-112">Dessin du texte mis en forme</span><span class="sxs-lookup"><span data-stu-id="3a8fe-112">Drawing Formatted Text</span></span>](../../../../docs/framework/wpf/advanced/drawing-formatted-text.md)
