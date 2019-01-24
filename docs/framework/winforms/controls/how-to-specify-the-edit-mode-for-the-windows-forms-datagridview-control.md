---
title: 'Procédure : Spécifier le Mode édition pour le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], edit mode
- data grids [Windows Forms], edit mode
ms.assetid: 93e117e8-94c4-411b-ba31-645e475ed85c
ms.openlocfilehash: fcb2014cc92a8a3e4afe7c3ed0365fd5947c70f3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54628264"
---
# <a name="how-to-specify-the-edit-mode-for-the-windows-forms-datagridview-control"></a>Procédure : Spécifier le Mode édition pour le contrôle de DataGridView Windows Forms
Par défaut, les utilisateurs peuvent modifier le contenu du cours <xref:System.Windows.Forms.DataGridView> cellule de zone de texte en tapant qu’il contient, ou en appuyant sur F2. Cela met la cellule en mode édition si toutes les conditions suivantes sont remplies :  
  
-   La source de données sous-jacente prend en charge la modification.  
  
-   Le <xref:System.Windows.Forms.DataGridView> contrôle est activé.  
  
-   Le <xref:System.Windows.Forms.DataGridView.EditMode%2A> valeur de propriété n’est pas <xref:System.Windows.Forms.DataGridViewEditMode.EditProgrammatically>.  
  
-   Le `ReadOnly` propriétés de la cellule, ligne, colonne et le contrôle sont prêts à `false`.  
  
 En mode édition, l’utilisateur peut modifier la valeur de cellule et appuyez sur ENTRÉE pour valider la modification ou la touche ÉCHAP pour rétablir la cellule à sa valeur d’origine.  
  
 Vous pouvez configurer un <xref:System.Windows.Forms.DataGridView> contrôler afin qu’une cellule passe en mode édition dès qu’elle devient la cellule active. Le comportement des touches entrée et ÉCHAP est inchangé dans ce cas, mais la cellule reste en mode édition après que la valeur est validée ou annulée. Vous pouvez également configurer le contrôle afin que les cellules entrer en mode Édition uniquement lorsque les utilisateurs tapent dans la cellule ou uniquement lorsque les utilisateurs appuient sur F2. Enfin, vous pouvez empêcher des cellules d’entrée en mode édition, sauf lorsque vous appelez le <xref:System.Windows.Forms.DataGridView.BeginEdit%2A> (méthode).  
  
### <a name="to-change-the-edit-mode-of-a-datagridview-control"></a>Pour modifier le mode d’édition d’un contrôle DataGridView  
  
-   Définir le <xref:System.Windows.Forms.DataGridView.EditMode%2A?displayProperty=nameWithType> propriété appropriés <xref:System.Windows.Forms.DataGridViewEditMode> énumération.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#067](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#067)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#067](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#067)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;  
  
-   des références aux assemblys <xref:System> et <xref:System.Windows.Forms>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.EditMode%2A?displayProperty=nameWithType>
- [Saisie de données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/data-entry-in-the-windows-forms-datagridview-control.md)
