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
# <a name="how-to-display-data-by-using-gridviewrowpresenter"></a>Comment : afficher des données à l'aide de GridViewRowPresenter
Cet exemple montre comment utiliser le <xref:System.Windows.Controls.GridViewRowPresenter> et <xref:System.Windows.Controls.GridViewHeaderRowPresenter> objets pour afficher des données dans les colonnes.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment spécifier un <xref:System.Windows.Controls.GridViewColumnCollection> qui affiche le <xref:System.DateTime.DayOfWeek%2A> et <xref:System.DateTime.Year%2A> d’un <xref:System.DateTime> à l’aide de l’objet <xref:System.Windows.Controls.GridViewRowPresenter> et <xref:System.Windows.Controls.GridViewHeaderRowPresenter> objets. L’exemple définit également un <xref:System.Windows.Style> pour le <xref:System.Windows.Controls.GridViewColumn.Header%2A> d’un <xref:System.Windows.Controls.GridViewColumn>.  
  
 [!code-xaml[GridViewRowPresenterSample#GridViewRowPresenter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridViewRowPresenterSample/CS/Window1.xaml#gridviewrowpresenter)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.GridViewHeaderRowPresenter>  
 <xref:System.Windows.Controls.GridViewRowPresenter>  
 <xref:System.Windows.Controls.GridViewColumnCollection>  
 [Vue d’ensemble de GridView](../../../../docs/framework/wpf/controls/gridview-overview.md)
