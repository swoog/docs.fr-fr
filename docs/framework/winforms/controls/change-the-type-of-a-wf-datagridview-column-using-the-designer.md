---
title: 'Procédure : Modifier le Type d’une colonne de DataGridView Windows Forms à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- columns [Windows Forms], types
- DataGridView control [Windows Forms], changing column type
- data [Windows Forms], displaying
ms.assetid: 7f994d45-600d-4190-a187-35803214b40c
ms.openlocfilehash: 99728e473223f3393cc9d09f38728cf873a95c99
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57718816"
---
# <a name="how-to-change-the-type-of-a-windows-forms-datagridview-column-using-the-designer"></a>Procédure : Modifier le Type d’une colonne de DataGridView Windows Forms à l’aide du Concepteur
Parfois vous souhaitez modifier le type d’une colonne qui a déjà été ajouté à un formulaire Windows <xref:System.Windows.Forms.DataGridView> contrôle. Par exemple, vous souhaiterez modifier les types de certaines des colonnes qui sont générés automatiquement lorsque vous liez le contrôle à une source de données. Cela est utile lorsque la table que vous affichez a des colonnes contenant des clés étrangères aux lignes dans une table associée. Dans ce cas, vous souhaiterez remplacer les colonnes de zone de texte qui affichent ces clés étrangères avec des colonnes de zone de liste déroulante qui affichent des valeurs plus significatives à partir de la table associée.  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-change-the-type-of-a-column-using-the-designer"></a>Pour modifier le type d’une colonne à l’aide du Concepteur  
  
1.  Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler, puis sélectionnez **modifier les colonnes**.  
  
2.  Sélectionnez une colonne dans la **colonnes sélectionnées** liste.  
  
3.  Dans le **propriétés de la colonne** grille, définissez la `ColumnType` propriété vers le nouveau type de colonne.  
  
    > [!NOTE]
    >  Le `ColumnType` propriété est une propriété de conception uniquement au moment qui indique la classe qui représente le type de colonne. Il n’est pas une propriété réelle définie dans une classe de la colonne.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn>
- [Guide pratique pour Créer un projet Application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [Guide pratique pour Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md)
