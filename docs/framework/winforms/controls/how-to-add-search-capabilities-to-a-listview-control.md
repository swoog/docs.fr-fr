---
title: 'Procédure : ajouter des fonctionnalités de recherche à un contrôle ListView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- lists [Windows Forms], enabling searching
- list views [Windows Forms], enabling searching
- ListView control [Windows Forms], adding search capabilities
- searching [Windows Forms], adding search capabilities to ListView control
ms.assetid: 557782d9-b705-4bab-b496-9938afddac82
ms.openlocfilehash: d5d4dae55fc9f0613ab6535b2fe57e262d0ef141
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62011020"
---
# <a name="how-to-add-search-capabilities-to-a-listview-control"></a>Procédure : ajouter des fonctionnalités de recherche à un contrôle ListView
Souvent, lorsque vous travaillez avec une longue liste d’éléments dans un <xref:System.Windows.Forms.ListView> contrôle, que vous souhaitez proposer des fonctionnalités de recherche à l’utilisateur. Le <xref:System.Windows.Forms.ListView> contrôle offre cette fonctionnalité de deux manières différentes : correspondance de texte et la recherche d’emplacement.  
  
 Le <xref:System.Windows.Forms.ListView.FindItemWithText%2A> méthode vous permet d’effectuer une recherche de texte sur un <xref:System.Windows.Forms.ListView> dans la vue liste ou détails, donné une chaîne de recherche et d’un début facultatif et d’index de fin. En revanche, le <xref:System.Windows.Forms.ListView.FindNearestItem%2A> méthode permet de rechercher un élément dans un <xref:System.Windows.Forms.ListView> en mode icône ou une vignette, étant donné un ensemble de coordonnées x et y et une direction à rechercher.  
  
### <a name="to-find-an-item-using-text"></a>Pour rechercher un élément à l’aide de texte  
  
1. Créer un <xref:System.Windows.Forms.ListView> avec la <xref:System.Windows.Forms.ListView.View%2A> propriété définie sur <xref:System.Windows.Forms.View.Details> ou <xref:System.Windows.Forms.View.List>, puis remplissez le <xref:System.Windows.Forms.ListView> avec des éléments.  
  
2. Appelez le <xref:System.Windows.Forms.ListView.FindItemWithText%2A> méthode, en passant le texte de l’élément que vous souhaitez obtenir.  
  
3. L’exemple de code suivant montre comment créer un base <xref:System.Windows.Forms.ListView>, remplir avec des éléments et utiliser la saisie de texte à partir de l’utilisateur pour rechercher un élément dans la liste.  
  
 [!code-cpp[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/cpp/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/VB/form1.vb#1)]  
  
### <a name="to-find-an-item-using-x--and-y-coordinates"></a>Pour rechercher un élément à l’aide des coordonnées x et y  
  
1. Créer un <xref:System.Windows.Forms.ListView> avec la <xref:System.Windows.Forms.View> propriété définie sur <xref:System.Windows.Forms.View.SmallIcon> ou <xref:System.Windows.Forms.View.LargeIcon>, puis remplissez le <xref:System.Windows.Forms.ListView> avec des éléments.  
  
2. Appelez le <xref:System.Windows.Forms.ListView.FindNearestItem%2A> méthode, en passant les coordonnées x - et y-souhaitée et la direction que vous souhaitez rechercher.  
  
3. L’exemple de code suivant montre comment créer une icône de base <xref:System.Windows.Forms.ListView>, remplir avec des éléments, puis capturez la <xref:System.Windows.Forms.Control.MouseDown> événements pour rechercher l’élément le plus proche dans la direction verticale.  
  
 [!code-cpp[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/cpp/form1.cpp#2)]
 [!code-csharp[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/CS/form1.cs#2)]
 [!code-vb[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/VB/form1.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.FindItemWithText%2A>
- <xref:System.Windows.Forms.ListView.FindNearestItem%2A>
- [Contrôle ListView](listview-control-windows-forms.md)
- [Vue d’ensemble du contrôle ListView](listview-control-overview-windows-forms.md)
- [Guide pratique pour Ajouter et supprimer des éléments avec le contrôle ListView Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
