---
title: 'Procédure : Effectuer une liaison à une énumération'
ms.date: 03/30/2017
helpviewer_keywords:
- binding data [WPF], enumeration
- data binding [WPF], enumeration
- enumeration [WPF]
ms.assetid: b9091eba-1119-424e-868b-d1a4168b3732
ms.openlocfilehash: db7b02a961c148bbdc31b05e7c71ea5b5d301c54
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54586564"
---
# <a name="how-to-bind-to-an-enumeration"></a><span data-ttu-id="b589c-102">Procédure : Effectuer une liaison à une énumération</span><span class="sxs-lookup"><span data-stu-id="b589c-102">How to: Bind to an Enumeration</span></span>
<span data-ttu-id="b589c-103">Cet exemple montre comment effectuer une liaison à une énumération en le liant à une méthode de GetValues de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="b589c-103">This example shows how to bind to an enumeration by binding to the enumeration's GetValues method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b589c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b589c-104">Example</span></span>  
 <span data-ttu-id="b589c-105">Dans l’exemple suivant, le <xref:System.Windows.Controls.ListBox> affiche la liste des <xref:System.Windows.HorizontalAlignment> des valeurs d’énumération via la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="b589c-105">In the following example, the <xref:System.Windows.Controls.ListBox> displays the list of <xref:System.Windows.HorizontalAlignment> enumeration values through data binding.</span></span> <span data-ttu-id="b589c-106">Le <xref:System.Windows.Controls.ListBox> et le <xref:System.Windows.Controls.Button> sont liés de telle sorte que vous pouvez modifier le <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> valeur de propriété de la <xref:System.Windows.Controls.Button> en sélectionnant une valeur dans la <xref:System.Windows.Controls.ListBox>.</span><span class="sxs-lookup"><span data-stu-id="b589c-106">The <xref:System.Windows.Controls.ListBox> and the <xref:System.Windows.Controls.Button> are bound such that you can change the <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> property value of the <xref:System.Windows.Controls.Button> by selecting a value in the <xref:System.Windows.Controls.ListBox>.</span></span>  
  
 [!code-xaml[BindToEnum#BindToEnum](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BindToEnum/CS/Window1.xaml#bindtoenum)]  
  
## <a name="see-also"></a><span data-ttu-id="b589c-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b589c-107">See also</span></span>
- [<span data-ttu-id="b589c-108">Effectuer une liaison à une méthode</span><span class="sxs-lookup"><span data-stu-id="b589c-108">Bind to a Method</span></span>](../../../../docs/framework/wpf/data/how-to-bind-to-a-method.md)
- [<span data-ttu-id="b589c-109">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="b589c-109">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [<span data-ttu-id="b589c-110">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="b589c-110">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
