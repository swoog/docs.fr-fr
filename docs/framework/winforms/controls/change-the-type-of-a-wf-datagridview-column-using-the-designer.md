---
title: 'Procédure : Modifier le Type d’une colonne de DataGridView Windows Forms à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- columns [Windows Forms], types
- DataGridView control [Windows Forms], changing column type
- data [Windows Forms], displaying
ms.assetid: 7f994d45-600d-4190-a187-35803214b40c
ms.openlocfilehash: 12e6e15dd3b4e7941be198a526e8145ceb126e8d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544612"
---
# <a name="how-to-change-the-type-of-a-windows-forms-datagridview-column-using-the-designer"></a>Procédure : Modifier le Type d’une colonne de DataGridView Windows Forms à l’aide du Concepteur
Parfois vous souhaitez modifier le type d’une colonne qui a déjà été ajouté à un formulaire Windows <xref:System.Windows.Forms.DataGridView> contrôle. Par exemple, vous souhaiterez modifier les types de certaines des colonnes qui sont générés automatiquement lorsque vous liez le contrôle à une source de données. Cela est utile lorsque la table que vous affichez a des colonnes contenant des clés étrangères aux lignes dans une table associée. Dans ce cas, vous souhaiterez remplacer les colonnes de zone de texte qui affichent ces clés étrangères avec des colonnes de zone de liste déroulante qui affichent des valeurs plus significatives à partir de la table associée.  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’Application Windows](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa) et [Comment : Ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-change-the-type-of-a-column-using-the-designer"></a>Pour modifier le type d’une colonne à l’aide du Concepteur  
  
1.  Cliquez sur le glyphe de balise active (![glyphe de balise active](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler, puis sélectionnez **modifier les colonnes**.  
  
2.  Sélectionnez une colonne dans la **colonnes sélectionnées** liste.  
  
3.  Dans le **propriétés de la colonne** grille, définissez la `ColumnType` propriété vers le nouveau type de colonne.  
  
    > [!NOTE]
    >  Le `ColumnType` propriété est une propriété de conception uniquement au moment qui indique la classe qui représente le type de colonne. Il n’est pas une propriété réelle définie dans une classe de la colonne.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn>
- [Guide pratique pour créer un projet d’application Windows](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)
- [Guide pratique pour Ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)
