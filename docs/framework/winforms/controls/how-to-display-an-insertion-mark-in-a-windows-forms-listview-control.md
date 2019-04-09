---
title: 'Procédure : afficher une marque d’insertion dans un contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ListView control [Windows Forms], drag operations
- graphics [Windows Forms], insertion marks
- drop and drag [Windows Forms], insertion marks
- insertion marks
ms.assetid: 88d0a15b-25fd-4dc3-a685-297351311940
ms.openlocfilehash: 60b775408f5c43ff08fc5c7de72a8302b20b2264
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59145611"
---
# <a name="how-to-display-an-insertion-mark-in-a-windows-forms-listview-control"></a>Procédure : afficher une marque d’insertion dans un contrôle ListView Windows Forms
La marque d'insertion dans le contrôle <xref:System.Windows.Forms.ListView> indique aux utilisateurs l'emplacement où les éléments déplacés seront insérés. Quand un utilisateur fait glisser un élément vers un point entre deux autres éléments, la marque d'insertion indique le nouvel emplacement prévu de l'élément.  
  
> [!NOTE]
>  La fonctionnalité de marque d’insertion est disponible uniquement sur [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] quand votre application appelle la méthode <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>. Sur les systèmes d'exploitation antérieurs, tout code relatif à la marque d'insertion n'a aucun effet et la marque d'insertion n'apparaît pas. Pour plus d'informations, consultez <xref:System.Windows.Forms.ListViewInsertionMark>.  
  
 L'illustration suivante montre une marque d'insertion :  
  
 ![Capture d’écran montre une marque d’insertion ListView. ](./media/how-to-display-an-insertion-mark-in-a-windows-forms-listview-control/listview-insertion-mark.gif "ListViewInsertion")  
  
 L’exemple de code suivant montre comment utiliser cette fonctionnalité.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/CPP/listviewinsertionmarkexample.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/CS/listviewinsertionmarkexample.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/VB/listviewinsertionmarkexample.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   des références aux assemblys System et System.Windows.Forms ;  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.InsertionMark%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ListViewInsertionMark>
- [Contrôle ListView](listview-control-windows-forms.md)
- [Vue d’ensemble du contrôle ListView](listview-control-overview-windows-forms.md)
- [Procédure pas à pas : exécution d’une opération glisser-déplacer dans Windows Forms](../advanced/walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md)
