---
title: 'Procédure : Obtenir ou définir des propriétés de positionnement du canevas'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Canvas control [WPF], setting positioning properties
ms.assetid: 1636b950-2b5a-4507-8a10-c5034cc58b1c
ms.openlocfilehash: 06508e1198736ccb1cbda41641dff4bc634ef82b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59194407"
---
# <a name="how-to-get-or-set-canvas-positioning-properties"></a><span data-ttu-id="ff43d-102">Procédure : Obtenir ou définir des propriétés de positionnement du canevas</span><span class="sxs-lookup"><span data-stu-id="ff43d-102">How to: Get or Set Canvas Positioning Properties</span></span>
<span data-ttu-id="ff43d-103">Cet exemple montre comment utiliser les méthodes de positionnement de la <xref:System.Windows.Controls.Canvas> élément pour positionner le contenu enfant.</span><span class="sxs-lookup"><span data-stu-id="ff43d-103">This example shows how to use the positioning methods of the <xref:System.Windows.Controls.Canvas> element to position child content.</span></span> <span data-ttu-id="ff43d-104">Cet exemple utilise le contenu d’un <xref:System.Windows.Controls.ListBoxItem> pour représenter les valeurs de positionnement et convertit les valeurs en instances de <xref:System.Double>, qui est un argument obligatoire de positionnement.</span><span class="sxs-lookup"><span data-stu-id="ff43d-104">This example uses content in a <xref:System.Windows.Controls.ListBoxItem> to represent positioning values and converts the values into instances of <xref:System.Double>, which is a required argument for positioning.</span></span> <span data-ttu-id="ff43d-105">Les valeurs sont converties en chaînes, puis affichées sous forme de texte dans un <xref:System.Windows.Controls.TextBlock> élément à l’aide de la <xref:System.Windows.Controls.Canvas.GetLeft%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="ff43d-105">The values are then converted back into strings and displayed as text in a <xref:System.Windows.Controls.TextBlock> element by using the <xref:System.Windows.Controls.Canvas.GetLeft%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff43d-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff43d-106">Example</span></span>  
 <span data-ttu-id="ff43d-107">L’exemple suivant crée un <xref:System.Windows.Controls.ListBox> élément qui possède onze sélectionnable <xref:System.Windows.Controls.ListBoxItem> éléments.</span><span class="sxs-lookup"><span data-stu-id="ff43d-107">The following example creates a <xref:System.Windows.Controls.ListBox> element that has eleven selectable <xref:System.Windows.Controls.ListBoxItem> elements.</span></span> <span data-ttu-id="ff43d-108">Le <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> déclencheurs d’événements le `ChangeLeft` méthode personnalisée, qui définit le bloc de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ff43d-108">The <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> event triggers the `ChangeLeft` custom method, which the subsequent code block defines.</span></span>  
  
 <span data-ttu-id="ff43d-109">Chaque <xref:System.Windows.Controls.ListBoxItem> représente un <xref:System.Double> valeur, qui est un des arguments qui la <xref:System.Windows.Controls.Canvas.SetLeft%2A> méthode <xref:System.Windows.Controls.Canvas> accepte.</span><span class="sxs-lookup"><span data-stu-id="ff43d-109">Each <xref:System.Windows.Controls.ListBoxItem> represents a <xref:System.Double> value, which is one of the arguments that the <xref:System.Windows.Controls.Canvas.SetLeft%2A> method of <xref:System.Windows.Controls.Canvas> accepts.</span></span> <span data-ttu-id="ff43d-110">Pour pouvoir utiliser un <xref:System.Windows.Controls.ListBoxItem> pour représenter une instance de <xref:System.Double>, vous devez d’abord convertir le <xref:System.Windows.Controls.ListBoxItem> au type de données correct.</span><span class="sxs-lookup"><span data-stu-id="ff43d-110">In order to use a <xref:System.Windows.Controls.ListBoxItem> to represent an instance of <xref:System.Double>, you must first convert the <xref:System.Windows.Controls.ListBoxItem> to the correct data type.</span></span>  
  
 [!code-xaml[CanvasPositioningProperties#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml#1)]  
  
 <span data-ttu-id="ff43d-111">Lorsqu’un utilisateur modifie le <xref:System.Windows.Controls.ListBox> sélection, elle appelle le `ChangeLeft` méthode personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ff43d-111">When a user changes the <xref:System.Windows.Controls.ListBox> selection, it invokes the `ChangeLeft` custom method.</span></span> <span data-ttu-id="ff43d-112">Cette méthode passe le <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.Windows.LengthConverter> objet, qui convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> d’un <xref:System.Windows.Controls.ListBoxItem> à une instance de <xref:System.Double> (Notez que cette valeur a déjà été convertie en un <xref:System.String> à l’aide de la <xref:System.Windows.Controls.Control.ToString%2A> méthode).</span><span class="sxs-lookup"><span data-stu-id="ff43d-112">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.LengthConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Double> (notice that this value has already been converted to a <xref:System.String> by using the <xref:System.Windows.Controls.Control.ToString%2A> method).</span></span> <span data-ttu-id="ff43d-113">Cette valeur est ensuite transmise vers le <xref:System.Windows.Controls.Canvas.SetLeft%2A> et <xref:System.Windows.Controls.Canvas.GetLeft%2A> méthodes de <xref:System.Windows.Controls.Canvas> afin de modifier la position de la `text1` objet.</span><span class="sxs-lookup"><span data-stu-id="ff43d-113">This value is then passed back to the <xref:System.Windows.Controls.Canvas.SetLeft%2A> and <xref:System.Windows.Controls.Canvas.GetLeft%2A> methods of <xref:System.Windows.Controls.Canvas> in order to change the position of the `text1` object.</span></span>  
  
 [!code-csharp[CanvasPositioningProperties#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml.cs#2)]
 [!code-vb[CanvasPositioningProperties#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasPositioningProperties/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="ff43d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff43d-114">See also</span></span>

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.ListBoxItem>
- <xref:System.Windows.LengthConverter>
- [<span data-ttu-id="ff43d-115">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="ff43d-115">Panels Overview</span></span>](panels-overview.md)
