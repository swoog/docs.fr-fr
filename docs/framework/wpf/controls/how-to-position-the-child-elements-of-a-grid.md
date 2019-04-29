---
title: 'Procédure : Positionner les éléments enfants d’une grille'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], positioning child elements
ms.assetid: 27b3ba9b-ad32-44e2-bcab-a79d573a463c
ms.openlocfilehash: c508f45c1ea3d0925503d6fe5600498a0558d5ad
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770800"
---
# <a name="how-to-position-the-child-elements-of-a-grid"></a><span data-ttu-id="55c38-102">Procédure : Positionner les éléments enfants d’une grille</span><span class="sxs-lookup"><span data-stu-id="55c38-102">How to: Position the Child Elements of a Grid</span></span>
<span data-ttu-id="55c38-103">Cet exemple montre comment obtenir et définir des méthodes qui sont définies sur <xref:System.Windows.Controls.Grid> pour positionner des éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="55c38-103">This example shows how to use the get and set methods that are defined on <xref:System.Windows.Controls.Grid> to position child elements.</span></span>  
  
## <a name="example"></a><span data-ttu-id="55c38-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="55c38-104">Example</span></span>  
 <span data-ttu-id="55c38-105">L’exemple suivant définit un parent <xref:System.Windows.Controls.Grid> élément (`grid1`) qui a trois colonnes et trois lignes.</span><span class="sxs-lookup"><span data-stu-id="55c38-105">The following example defines a parent <xref:System.Windows.Controls.Grid> element (`grid1`) that has three columns and three rows.</span></span> <span data-ttu-id="55c38-106">Un enfant <xref:System.Windows.Shapes.Rectangle> élément (`rect1`) est ajouté à la <xref:System.Windows.Controls.Grid> position de colonne zéro, position de ligne zéro.</span><span class="sxs-lookup"><span data-stu-id="55c38-106">A child <xref:System.Windows.Shapes.Rectangle> element (`rect1`) is added to the <xref:System.Windows.Controls.Grid> in column position zero, row position zero.</span></span> <span data-ttu-id="55c38-107"><xref:System.Windows.Controls.Button> les éléments représentent les méthodes qui peuvent être appelées pour repositionner le <xref:System.Windows.Shapes.Rectangle> élément dans le <xref:System.Windows.Controls.Grid>.</span><span class="sxs-lookup"><span data-stu-id="55c38-107"><xref:System.Windows.Controls.Button> elements represent methods that can be called to reposition the <xref:System.Windows.Shapes.Rectangle> element within the <xref:System.Windows.Controls.Grid>.</span></span> <span data-ttu-id="55c38-108">Lorsqu’un utilisateur clique sur un bouton, la méthode associée est activée.</span><span class="sxs-lookup"><span data-stu-id="55c38-108">When a user clicks a button, the related method is activated.</span></span>  
  
 [!code-xaml[gridGetSetMethods](~/samples/snippets/csharp/VS_Snippets_Wpf/gridGetSetMethods/CSharp/Window1.xaml)]  
  
 <span data-ttu-id="55c38-109">L’exemple de code-behind suivant gère les méthodes que le bouton <xref:System.Windows.Controls.Primitives.ButtonBase.Click> déclenchent des événements.</span><span class="sxs-lookup"><span data-stu-id="55c38-109">The following code-behind example handles the methods that the button <xref:System.Windows.Controls.Primitives.ButtonBase.Click> events raise.</span></span> <span data-ttu-id="55c38-110">L’exemple écrit ces appels de méthode <xref:System.Windows.Controls.TextBlock> éléments liée de l’utilisation des méthodes get pour les nouvelles valeurs de propriété sous forme de chaînes de sortie.</span><span class="sxs-lookup"><span data-stu-id="55c38-110">The example writes these method calls to <xref:System.Windows.Controls.TextBlock> elements that use related get methods to output the new property values as strings.</span></span>  
  
 [!code-csharp[gridGetSetMethods#2](~/samples/snippets/csharp/VS_Snippets_Wpf/gridGetSetMethods/CSharp/Window1.xaml.cs#2)]
 [!code-vb[gridGetSetMethods#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gridGetSetMethods/VisualBasic/Window1.xaml.vb#2)]  
 <span data-ttu-id="55c38-111">Voici le résultat final !</span><span class="sxs-lookup"><span data-stu-id="55c38-111">Here is the finished result!</span></span>
 
 ![une capture d’écran illustre une interface utilisateur WPF avec deux colonnes, la partie droite a une grille de 3 x 3 et gauche comprend des boutons pour déplacer un rectangle coloré entre les colonnes et les lignes de la grille](././media/grid-methods-sample.png) 
  
## <a name="see-also"></a><span data-ttu-id="55c38-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55c38-113">See also</span></span>

- <xref:System.Windows.Controls.Grid>
- [<span data-ttu-id="55c38-114">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="55c38-114">Panels Overview</span></span>](panels-overview.md)
