---
title: 'Procédure : Lier des données pour le contrôle de DataGridView Windows Forms à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, binding to a data source
- data sources [Windows Forms], binding to Windows Forms controls
- DataGridView control [Windows Forms], data binding
ms.assetid: f4f46009-cec2-441b-8668-6b5af057558b
ms.openlocfilehash: 428f558c125bb11e5cbd4f794713440c22c89d7e
ms.sourcegitcommit: 0069cb3de8eed4e92b2195d29e5769a76111acdd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/16/2019
ms.locfileid: "56333363"
---
# <a name="how-to-bind-data-to-the-windows-forms-datagridview-control-using-the-designer"></a>Procédure : Lier des données pour le contrôle de DataGridView Windows Forms à l’aide du Concepteur
Vous pouvez utiliser le concepteur pour connecter un <xref:System.Windows.Forms.DataGridView> contrôle aux sources de données de plusieurs types différents, y compris les bases de données, les objets métier ou les services Web. Lorsque vous liez le contrôle à une source de données à l’aide du concepteur, le contrôle est automatiquement lié à un <xref:System.Windows.Forms.BindingSource> composant qui représente la source de données. En outre, les colonnes sont générées automatiquement dans le contrôle pour faire correspondre les informations de schéma fournies par la source de données.  
  
 Après avoir généré les colonnes, vous pouvez les modifier pour répondre à vos besoins. Par exemple, vous pouvez supprimer ou masquer des colonnes qui ne vous intéressent pas dans l’affichage, vous pouvez réorganiser les colonnes, ou vous pouvez modifier les types de colonnes. Pour plus d’informations sur la modification des colonnes, consultez les rubriques répertoriées dans la section Voir aussi.  
  
 Vous pouvez également lier plusieurs <xref:System.Windows.Forms.DataGridView> contrôles à des tables associées pour créer des relations maître/détail. Dans cette configuration, un contrôle affiche une table parent et un autre contrôle affiche uniquement les lignes d’une table enfant qui sont liées à la ligne actuelle dans la table parent. Pour plus d'informations, voir [Procédure : Affichage liées à des données dans un Windows Forms Application](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/57tx3hhe(v=vs.120)).  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire qui contient un <xref:System.Windows.Forms.DataGridView> ou les deux contrôles pour une relation maître/détail. Pour plus d’informations sur le démarrage d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-bind-the-control-to-a-data-source"></a>Pour lier le contrôle à une source de données  
  
1.  Cliquez sur le glyphe de balise active (![glyphe de balise active](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôle.  
  
2.  Cliquez sur la flèche déroulante correspondant à l’option **Choisir la Source de données**.  
  
3.  Si votre projet ne dispose pas déjà d’une source de données, cliquez **Ajouter la source de données projet** et suivez les étapes indiquées par l’Assistant.  
  
     Pour plus d’informations, consultez la page [Assistant Configuration de source de données](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/w4dd7z6t(v=vs.120)). Votre nouvelle source de données s’affiche dans la liste déroulante **Choisir la source de données**. Si votre nouvelle source de données contient un seul membre, comme une table de base de données unique, le contrôle est automatiquement lié à ce membre. Sinon, passez à l'étape suivante.  
  
4.  Développez les nœuds **Autres sources de données** et **Sources de données du projet** si cela n’est pas déjà fait, puis sélectionnez la source de données à laquelle lier le contrôle.  
  
5.  Si votre source de données contient plusieurs membres, par exemple si vous avez créé un <xref:System.Data.DataSet?displayProperty=nameWithType> qui contient plusieurs tables, développez la source de données, puis sélectionnez le membre spécifique à lier.  
  
6.  Pour créer une relation maître/détail, dans le **choisir la Source de données** fenêtre de liste déroulante pour un deuxième <xref:System.Windows.Forms.DataGridView> contrôler, développez le <xref:System.Windows.Forms.BindingSource> créé pour la table parent, puis sélectionnez la table enfant connexe dans la liste indiqué.  
  
    > [!NOTE]
    >  Si votre projet a déjà une source de données, vous pouvez également utiliser la fenêtre **Sources de données** pour créer un formulaire de données. Pour plus d’informations, consultez la page [Fenêtre Sources de données](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/6ckyxa83(v=vs.120)).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.DataGridView.DataMember%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.DataSource%2A?displayProperty=nameWithType>
- [Guide pratique pour Se connecter aux données dans une base de données](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/fxk9yw1t(v=vs.120))
- [Guide pratique pour Ajouter et supprimer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur](../../../../docs/framework/winforms/controls/add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [Guide pratique pour Modifier l’ordre des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur](../../../../docs/framework/winforms/controls/change-the-order-of-columns-in-the-datagrid-using-the-designer.md)
- [Guide pratique pour Modifier le Type d’une colonne de DataGridView Windows Forms à l’aide du Concepteur](../../../../docs/framework/winforms/controls/change-the-type-of-a-wf-datagridview-column-using-the-designer.md)
- [Guide pratique pour Figer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur](../../../../docs/framework/winforms/controls/freeze-columns-in-the-datagrid-using-the-designer.md)
- [Guide pratique pour Masquer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur](../../../../docs/framework/winforms/controls/hide-columns-in-the-datagrid-using-the-designer.md)
- [Guide pratique pour Rendre les colonnes en lecture seule dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur](../../../../docs/framework/winforms/controls/make-columns-read-only-in-the-datagrid-using-the-designer.md)
- [Guide pratique pour Créer un projet Application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [Guide pratique pour Ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)
- [Fenêtre Sources de données](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/6ckyxa83(v=vs.120))
- [Guide pratique pour Afficher les données associées dans une Application de formulaires Windows](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/57tx3hhe(v=vs.120))
