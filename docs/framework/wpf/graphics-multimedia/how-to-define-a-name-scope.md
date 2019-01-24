---
title: 'Procédure : Définir une portée de nom'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- name scope [WPF], defining
- Storyboards [WPF], animating in procedural code
- animation [WPF], Storyboards [WPF], in procedural code
ms.assetid: 4f361925-6a08-40dc-8231-a61111c6b28b
ms.openlocfilehash: 656c1e9af11697cd4a1253bdab673887765976a6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674464"
---
# <a name="how-to-define-a-name-scope"></a><span data-ttu-id="062d3-102">Procédure : Définir une portée de nom</span><span class="sxs-lookup"><span data-stu-id="062d3-102">How to: Define a Name Scope</span></span>
<span data-ttu-id="062d3-103">Pour animer avec <xref:System.Windows.Media.Animation.Storyboard> dans le code, vous devez créer un <xref:System.Windows.NameScope> et enregistrer les noms des objets de la cible avec l’élément qui possède cette portée de nom.</span><span class="sxs-lookup"><span data-stu-id="062d3-103">To animate with <xref:System.Windows.Media.Animation.Storyboard> in code, you must create a <xref:System.Windows.NameScope> and register the target objects' names with the element that owns that name scope.</span></span> <span data-ttu-id="062d3-104">Dans l’exemple suivant, un <xref:System.Windows.NameScope> est créé pour `myMainPanel`.</span><span class="sxs-lookup"><span data-stu-id="062d3-104">In the following example, a <xref:System.Windows.NameScope> is created for `myMainPanel`.</span></span> <span data-ttu-id="062d3-105">Deux boutons, `button1` et `button2`, sont ajoutées pour le panneau de configuration et leurs noms enregistrés.</span><span class="sxs-lookup"><span data-stu-id="062d3-105">Two buttons, `button1` and `button2`, are added to the panel, and their names registered.</span></span> <span data-ttu-id="062d3-106">Plusieurs animations et un <xref:System.Windows.Media.Animation.Storyboard> sont créés.</span><span class="sxs-lookup"><span data-stu-id="062d3-106">Several animations and a <xref:System.Windows.Media.Animation.Storyboard> are created.</span></span> <span data-ttu-id="062d3-107">La table de montage séquentiel <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> méthode est utilisée pour démarrer les animations.</span><span class="sxs-lookup"><span data-stu-id="062d3-107">The storyboard's <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> method is used to start the animations.</span></span>  
  
 <span data-ttu-id="062d3-108">Étant donné que `button1`, `button2`, et `myMainPanel` partagent tous la même portée de nom, l’un d’eux peut être utilisé avec le <xref:System.Windows.Media.Animation.Storyboard> <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> méthode pour démarrer les animations.</span><span class="sxs-lookup"><span data-stu-id="062d3-108">Because `button1`, `button2`, and `myMainPanel` all share the same name scope, any one of them can be used with the <xref:System.Windows.Media.Animation.Storyboard> <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> method to start the animations.</span></span>  
  
## <a name="example"></a><span data-ttu-id="062d3-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="062d3-109">Example</span></span>  
 [!code-csharp[StoryboardBeginAnimation_procedural_snip#NameScopeExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/CSharp/ScopeExample.cs#namescopeexample)]
 [!code-vb[StoryboardBeginAnimation_procedural_snip#NameScopeExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/visualbasic/scopeexample.vb#namescopeexample)]  
  
## <a name="see-also"></a><span data-ttu-id="062d3-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="062d3-110">See also</span></span>
- [<span data-ttu-id="062d3-111">Animer une propriété à l’aide d’une table de montage séquentiel</span><span class="sxs-lookup"><span data-stu-id="062d3-111">Animate a Property by Using a Storyboard</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-by-using-a-storyboard.md)
- [<span data-ttu-id="062d3-112">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="062d3-112">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
