---
title: 'Procédure : lier des objets à des contrôles DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], object binding
- data grids [Windows Forms], object binding
- object binding [Windows Forms], DataGridView control
ms.assetid: cb8f29fa-577e-4e2b-883f-3a01c6189b9c
ms.openlocfilehash: e1fef71de799f9f906c956a0441c92e027173a1c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64612343"
---
# <a name="how-to-bind-objects-to-windows-forms-datagridview-controls"></a>Procédure : lier des objets à des contrôles DataGridView Windows Forms
L'exemple de code suivant montre comment lier une collection d'objets à un contrôle <xref:System.Windows.Forms.DataGridView> pour que chaque objet soit affichée sur une ligne distincte. Cet exemple illustre également comment afficher une propriété avec un type énumération dans un <xref:System.Windows.Forms.DataGridViewComboBoxColumn> pour que la zone de liste déroulante modifiable contienne les valeurs d'énumération.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridView._CollectionBound#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView._CollectionBound/CS/collectionbound.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridView._CollectionBound#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView._CollectionBound/VB/collectionbound.vb#00)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- des références aux assemblys System et System.Windows.Forms ;  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- [Affichage des données dans le contrôle DataGridView Windows Forms](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Accéder aux objets liés à des Windows Forms DataGridView lignes](how-to-access-objects-bound-to-windows-forms-datagridview-rows.md)
