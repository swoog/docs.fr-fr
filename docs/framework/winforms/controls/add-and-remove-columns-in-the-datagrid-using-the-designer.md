---
title: 'Procédure : ajouter et supprimer des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
f1_keywords:
- vs.DataGridViewAddColumnDialog
helpviewer_keywords:
- DataGridView control [Windows Forms], adding columns
- DataGridView control [Windows Forms], removing columns
ms.assetid: 9e709f35-0a8c-4e7e-b4c4-bacb7a834077
ms.openlocfilehash: 80ede9b7bc5bf667e03dc0a745fbc0b5f6c2663a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59343283"
---
# <a name="how-to-add-and-remove-columns-in-the-windows-forms-datagridview-control-using-the-designer"></a>Procédure : ajouter et supprimer des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur
Les formulaires Windows <xref:System.Windows.Forms.DataGridView> contrôle doit contenir des colonnes pour afficher des données. Si vous envisagez de remplir le contrôle manuellement, vous devez ajouter les colonnes vous-même. Alternativement, vous pouvez lier le contrôle à une source de données, ce qui génère et remplit automatiquement les colonnes. Si la source de données contient plus de colonnes que vous souhaitez afficher, vous pouvez supprimer les colonnes indésirables.  
  
 Les procédures suivantes nécessitent un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-a-column-using-the-designer"></a>Pour ajouter une colonne à l’aide du Concepteur  
  
1. Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler, puis sélectionnez **ajouter une colonne**.  
  
2. Dans le **ajouter une colonne** boîte de dialogue, sélectionnez le **colonne liée aux données** option et sélectionnez une colonne dans la source de données ou choisissez le **colonne indépendante** option et définissez la colonne à l’aide des champs fournis.  
  
3. Cliquez sur le **ajouter** pour ajouter la colonne, qui n’apparaissent dans le concepteur, si les colonnes existantes ne remplissent pas déjà de la zone d’affichage de contrôle.  
  
    > [!NOTE]
    >  Vous pouvez modifier les propriétés des colonnes dans le **modifier les colonnes** boîte de dialogue, vous pouvez accéder à partir de la balise active du contrôle.  
  
### <a name="to-remove-a-column-using-the-designer"></a>Pour supprimer une colonne à l’aide du Concepteur  
  
1. Choisissez **modifier les colonnes** à partir de la balise active du contrôle.  
  
2. Sélectionnez une colonne dans la **colonnes sélectionnées** liste.  
  
3. Cliquez sur le **supprimer** bouton pour supprimer la colonne, qui n’apparaît plus dans le concepteur.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- [Guide pratique pour Créer un projet Application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [Guide pratique pour Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md)
