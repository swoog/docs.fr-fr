---
title: "Procédure : Afficher un contenu ListView à l'aide d'un GridView"
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], displaying contents with GridView
- GridView [WPF], displaying ListView contents
ms.assetid: 5bc1e767-ab46-4f14-bd41-3d5d39e1d000
ms.openlocfilehash: 1066869c80bf5bd87d656bcb4994c188ee0e8efc
ms.sourcegitcommit: 462dc41a13942e467984e48f4018d1f79ae67346
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "58185608"
---
# <a name="how-to-display-listview-contents-by-using-a-gridview"></a><span data-ttu-id="80edf-102">Procédure : Afficher un contenu ListView à l'aide d'un GridView</span><span class="sxs-lookup"><span data-stu-id="80edf-102">How to: Display ListView Contents by Using a GridView</span></span>
<span data-ttu-id="80edf-103">Cet exemple montre comment définir un <xref:System.Windows.Controls.GridView> mode d’affichage pour un <xref:System.Windows.Controls.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="80edf-103">This example shows how to define a <xref:System.Windows.Controls.GridView> view mode for a <xref:System.Windows.Controls.ListView> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="80edf-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="80edf-104">Example</span></span>  
 <span data-ttu-id="80edf-105">Vous pouvez définir le mode d’affichage d’un <xref:System.Windows.Controls.GridView> en spécifiant <xref:System.Windows.Controls.GridViewColumn> objets.</span><span class="sxs-lookup"><span data-stu-id="80edf-105">You can define the view mode of a <xref:System.Windows.Controls.GridView> by specifying <xref:System.Windows.Controls.GridViewColumn> objects.</span></span> <span data-ttu-id="80edf-106">L’exemple suivant montre comment définir <xref:System.Windows.Controls.GridViewColumn> objets lier au contenu de données qui est spécifié pour le <xref:System.Windows.Controls.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="80edf-106">The following example shows how to define <xref:System.Windows.Controls.GridViewColumn> objects that bind to the data content that is specified for the <xref:System.Windows.Controls.ListView> control.</span></span> <span data-ttu-id="80edf-107">Cela <xref:System.Windows.Controls.GridView> exemple spécifie trois <xref:System.Windows.Controls.GridViewColumn> objets qui mappent au `FirstName`, `LastName`, et `EmployeeNumber` champs de la `EmployeeInfoDataSource` qui est défini comme le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> de la <xref:System.Windows.Controls.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="80edf-107">This <xref:System.Windows.Controls.GridView> example specifies three <xref:System.Windows.Controls.GridViewColumn> objects that map to the `FirstName`, `LastName`, and `EmployeeNumber` fields of the `EmployeeInfoDataSource` that is set as the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> of the <xref:System.Windows.Controls.ListView> control.</span></span>  
  
 [!code-xaml[ListViewCode#ListViewEmployee](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCode/CSharp/Window1.xaml#listviewemployee)]  
  
 <span data-ttu-id="80edf-108">L’illustration suivante montre comment cet exemple s’affiche.</span><span class="sxs-lookup"><span data-stu-id="80edf-108">The following illustration shows how this example appears.</span></span>  
  
 ![Capture d’écran montrant un ListView avec GridView sortie.](./media/gridview-overview/listview-gridview-output.jpg)  
  
## <a name="see-also"></a><span data-ttu-id="80edf-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80edf-110">See also</span></span>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="80edf-111">Vue d’ensemble de ListView</span><span class="sxs-lookup"><span data-stu-id="80edf-111">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="80edf-112">Vue d’ensemble de GridView</span><span class="sxs-lookup"><span data-stu-id="80edf-112">GridView Overview</span></span>](gridview-overview.md)
- [<span data-ttu-id="80edf-113">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="80edf-113">How-to Topics</span></span>](listview-how-to-topics.md)
