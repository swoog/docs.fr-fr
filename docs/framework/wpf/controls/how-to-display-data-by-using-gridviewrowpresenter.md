---
title: "Comment : afficher des données à l'aide de GridViewRowPresenter"
ms.date: 03/30/2017
helpviewer_keywords:
- displaying data with GridViewRowPresenter [WPF]
- GridViewRowPresenter [WPF]
ms.assetid: bdb785a5-a262-44d5-a517-ea14383e5f70
ms.openlocfilehash: f68bc3a4ffff268138721a6750a0eb50c825377e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33550788"
---
# <a name="how-to-display-data-by-using-gridviewrowpresenter"></a><span data-ttu-id="2a1a8-102">Comment : afficher des données à l'aide de GridViewRowPresenter</span><span class="sxs-lookup"><span data-stu-id="2a1a8-102">How to: Display Data by Using GridViewRowPresenter</span></span>
<span data-ttu-id="2a1a8-103">Cet exemple montre comment utiliser le <xref:System.Windows.Controls.GridViewRowPresenter> et <xref:System.Windows.Controls.GridViewHeaderRowPresenter> objets pour afficher des données dans les colonnes.</span><span class="sxs-lookup"><span data-stu-id="2a1a8-103">This example shows how to use the <xref:System.Windows.Controls.GridViewRowPresenter> and <xref:System.Windows.Controls.GridViewHeaderRowPresenter> objects to display data in columns.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2a1a8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2a1a8-104">Example</span></span>  
 <span data-ttu-id="2a1a8-105">L’exemple suivant montre comment spécifier un <xref:System.Windows.Controls.GridViewColumnCollection> qui affiche le <xref:System.DateTime.DayOfWeek%2A> et <xref:System.DateTime.Year%2A> d’un <xref:System.DateTime> à l’aide de l’objet <xref:System.Windows.Controls.GridViewRowPresenter> et <xref:System.Windows.Controls.GridViewHeaderRowPresenter> objets.</span><span class="sxs-lookup"><span data-stu-id="2a1a8-105">The following example shows how to specify a <xref:System.Windows.Controls.GridViewColumnCollection> that displays the <xref:System.DateTime.DayOfWeek%2A> and <xref:System.DateTime.Year%2A> of a <xref:System.DateTime> object by using <xref:System.Windows.Controls.GridViewRowPresenter> and <xref:System.Windows.Controls.GridViewHeaderRowPresenter> objects.</span></span> <span data-ttu-id="2a1a8-106">L’exemple définit également un <xref:System.Windows.Style> pour le <xref:System.Windows.Controls.GridViewColumn.Header%2A> d’un <xref:System.Windows.Controls.GridViewColumn>.</span><span class="sxs-lookup"><span data-stu-id="2a1a8-106">The example also defines a <xref:System.Windows.Style> for the <xref:System.Windows.Controls.GridViewColumn.Header%2A> of a <xref:System.Windows.Controls.GridViewColumn>.</span></span>  
  
 [!code-xaml[GridViewRowPresenterSample#GridViewRowPresenter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridViewRowPresenterSample/CS/Window1.xaml#gridviewrowpresenter)]  
  
## <a name="see-also"></a><span data-ttu-id="2a1a8-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a1a8-107">See Also</span></span>  
 <xref:System.Windows.Controls.GridViewHeaderRowPresenter>  
 <xref:System.Windows.Controls.GridViewRowPresenter>  
 <xref:System.Windows.Controls.GridViewColumnCollection>  
 [<span data-ttu-id="2a1a8-108">Vue d’ensemble de GridView</span><span class="sxs-lookup"><span data-stu-id="2a1a8-108">GridView Overview</span></span>](../../../../docs/framework/wpf/controls/gridview-overview.md)
