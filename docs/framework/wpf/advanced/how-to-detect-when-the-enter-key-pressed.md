---
title: 'Procédure : Détecter quand la touche enfoncée'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Enter key [WPF], detecting
- keys [WPF], Enter
ms.assetid: a66f39d2-ef4a-43a5-b454-a4ea0fe88655
ms.openlocfilehash: fbb9b1b9cbb56a49aba018f122a7e903bd4f677d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54592245"
---
# <a name="how-to-detect-when-the-enter-key-pressed"></a><span data-ttu-id="13474-102">Procédure : Détecter quand la touche enfoncée</span><span class="sxs-lookup"><span data-stu-id="13474-102">How to: Detect When the Enter Key Pressed</span></span>
<span data-ttu-id="13474-103">Cet exemple montre comment détecter lorsque le <xref:System.Windows.Input.Key.Enter> touche du clavier.</span><span class="sxs-lookup"><span data-stu-id="13474-103">This example shows how to detect when the <xref:System.Windows.Input.Key.Enter> key is pressed on the keyboard.</span></span>  
  
 <span data-ttu-id="13474-104">Cet exemple se compose d’un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier et un fichier code-behind.</span><span class="sxs-lookup"><span data-stu-id="13474-104">This example consists of a [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file and a code-behind file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="13474-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="13474-105">Example</span></span>  
 <span data-ttu-id="13474-106">Lorsque l’utilisateur appuie sur la touche <xref:System.Windows.Input.Key.Enter> dans la <xref:System.Windows.Controls.TextBox>, le texte entré s’affiche dans une autre zone de la [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)].  </span><span class="sxs-lookup"><span data-stu-id="13474-106">When the user presses the <xref:System.Windows.Input.Key.Enter> key in the <xref:System.Windows.Controls.TextBox>, the input in the text box appears in another area of the [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)].</span></span>  
  
 <span data-ttu-id="13474-107">Ce qui suit [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] crée l’interface utilisateur, qui se compose d’un <xref:System.Windows.Controls.StackPanel>, un <xref:System.Windows.Controls.TextBlock>et un <xref:System.Windows.Controls.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="13474-107">The following [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] creates the user interface, which consists of a <xref:System.Windows.Controls.StackPanel>, a <xref:System.Windows.Controls.TextBlock>, and a <xref:System.Windows.Controls.TextBox>.</span></span>  
  
 [!code-xaml[keydown#KeyDownUI](../../../../samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml#keydownui)]  
  
 <span data-ttu-id="13474-108">Le code-behind suivant crée le <xref:System.Windows.UIElement.KeyDown> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="13474-108">The following code behind creates the <xref:System.Windows.UIElement.KeyDown> event handler.</span></span>  <span data-ttu-id="13474-109">Si la touche enfoncée est la touche <xref:System.Windows.Input.Key.Enter>, un message s’affiche dans le <xref:System.Windows.Controls.TextBlock>. </span><span class="sxs-lookup"><span data-stu-id="13474-109">If the key that is pressed is the <xref:System.Windows.Input.Key.Enter> key, a message is displayed in the <xref:System.Windows.Controls.TextBlock>.</span></span>  
  
 [!code-csharp[keydown#KeyDownSample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml.cs#keydownsample)]
 [!code-vb[keydown#KeyDownSample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/KeyDown/VisualBasic/Window1.xaml.vb#keydownsample)]  
  
## <a name="see-also"></a><span data-ttu-id="13474-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13474-110">See also</span></span>
- [<span data-ttu-id="13474-111">Vue d’ensemble des entrées</span><span class="sxs-lookup"><span data-stu-id="13474-111">Input Overview</span></span>](../../../../docs/framework/wpf/advanced/input-overview.md)
- [<span data-ttu-id="13474-112">Vue d’ensemble des événements routés</span><span class="sxs-lookup"><span data-stu-id="13474-112">Routed Events Overview</span></span>](../../../../docs/framework/wpf/advanced/routed-events-overview.md)
