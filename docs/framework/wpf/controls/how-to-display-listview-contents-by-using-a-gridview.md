---
title: "Procédure : Afficher un contenu ListView à l'aide d'un GridView"
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], displaying contents with GridView
- GridView [WPF], displaying ListView contents
ms.assetid: 5bc1e767-ab46-4f14-bd41-3d5d39e1d000
ms.openlocfilehash: 0e2b37cb061cc92b34c3a4f94bcd42e8ffc69ab5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54606005"
---
# <a name="how-to-display-listview-contents-by-using-a-gridview"></a><span data-ttu-id="0d91e-102">Procédure : Afficher un contenu ListView à l'aide d'un GridView</span><span class="sxs-lookup"><span data-stu-id="0d91e-102">How to: Display ListView Contents by Using a GridView</span></span>
<span data-ttu-id="0d91e-103">Cet exemple montre comment définir un <xref:System.Windows.Controls.GridView> mode d’affichage pour un <xref:System.Windows.Controls.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0d91e-103">This example shows how to define a <xref:System.Windows.Controls.GridView> view mode for a <xref:System.Windows.Controls.ListView> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0d91e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0d91e-104">Example</span></span>  
 <span data-ttu-id="0d91e-105">Vous pouvez définir le mode d’affichage d’un <xref:System.Windows.Controls.GridView> en spécifiant <xref:System.Windows.Controls.GridViewColumn> objets.</span><span class="sxs-lookup"><span data-stu-id="0d91e-105">You can define the view mode of a <xref:System.Windows.Controls.GridView> by specifying <xref:System.Windows.Controls.GridViewColumn> objects.</span></span> <span data-ttu-id="0d91e-106">L’exemple suivant montre comment définir <xref:System.Windows.Controls.GridViewColumn> objets lier au contenu de données qui est spécifié pour le <xref:System.Windows.Controls.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0d91e-106">The following example shows how to define <xref:System.Windows.Controls.GridViewColumn> objects that bind to the data content that is specified for the <xref:System.Windows.Controls.ListView> control.</span></span> <span data-ttu-id="0d91e-107">Cela <xref:System.Windows.Controls.GridView> exemple spécifie trois <xref:System.Windows.Controls.GridViewColumn> objets qui mappent au `FirstName`, `LastName`, et `EmployeeNumber` champs de la `EmployeeInfoDataSource` qui est défini comme le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> de la <xref:System.Windows.Controls.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0d91e-107">This <xref:System.Windows.Controls.GridView> example specifies three <xref:System.Windows.Controls.GridViewColumn> objects that map to the `FirstName`, `LastName`, and `EmployeeNumber` fields of the `EmployeeInfoDataSource` that is set as the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> of the <xref:System.Windows.Controls.ListView> control.</span></span>  
  
 [!code-xaml[ListViewCode#ListViewEmployee](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewCode/CSharp/Window1.xaml#listviewemployee)]  
  
 <span data-ttu-id="0d91e-108">L’illustration suivante montre comment cet exemple s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0d91e-108">The following illustration shows how this example appears.</span></span>  
  
 <span data-ttu-id="0d91e-109">![Sortie de ListView avec GridView](../../../../docs/framework/wpf/controls/media/listviewgridview.JPG "ListViewGridView")</span><span class="sxs-lookup"><span data-stu-id="0d91e-109">![ListView with GridView output](../../../../docs/framework/wpf/controls/media/listviewgridview.JPG "ListViewGridView")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d91e-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d91e-110">See also</span></span>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="0d91e-111">Vue d’ensemble de ListView</span><span class="sxs-lookup"><span data-stu-id="0d91e-111">ListView Overview</span></span>](../../../../docs/framework/wpf/controls/listview-overview.md)
- [<span data-ttu-id="0d91e-112">Vue d’ensemble de GridView</span><span class="sxs-lookup"><span data-stu-id="0d91e-112">GridView Overview</span></span>](../../../../docs/framework/wpf/controls/gridview-overview.md)
- [<span data-ttu-id="0d91e-113">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="0d91e-113">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
