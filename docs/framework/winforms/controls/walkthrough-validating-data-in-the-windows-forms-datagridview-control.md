---
title: 'Procédure pas à pas : validation des données dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- validating data [Windows Forms], Windows Forms
- data [Windows Forms], validation
- DataGridView control [Windows Forms], data validation
- data grids [Windows Forms], validating data
- data validation [Windows Forms], Windows Forms
- walkthroughs [Windows Forms], DataGridView control
ms.assetid: a4f1d015-2969-430c-8ea2-b612d179c290
ms.openlocfilehash: a4bf0850b28b7101ba76f1c1fedc6633eccb81a1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59346052"
---
# <a name="walkthrough-validating-data-in-the-windows-forms-datagridview-control"></a>Procédure pas à pas : validation des données dans le contrôle DataGridView Windows Forms
Lorsque vous affichez les fonctionnalités d’entrée de données aux utilisateurs, vous devez fréquemment valider les données entrées dans votre formulaire. Le <xref:System.Windows.Forms.DataGridView> classe offre un moyen pratique pour effectuer la validation avant que les données sont validées dans le magasin de données. Vous pouvez valider les données en gérant la <xref:System.Windows.Forms.DataGridView.CellValidating> événement, qui est déclenché par la <xref:System.Windows.Forms.DataGridView> lorsque la cellule active est modifiée.  
  
 Dans cette procédure pas à pas, vous allez récupérer des lignes à partir de la `Customers` table dans la base de données Northwind et les afficher dans un <xref:System.Windows.Forms.DataGridView> contrôle. Quand un utilisateur modifie une cellule dans le `CompanyName` colonne et essaiera de quitter la cellule, le <xref:System.Windows.Forms.DataGridView.CellValidating> Gestionnaire d’événements examinera la nouvelle chaîne de nom de société pour vous assurer qu’il n’est pas vide ; si la nouvelle valeur est une chaîne vide, le <xref:System.Windows.Forms.DataGridView> empêchera le curseur de l’utilisateur de quitter la cellule jusqu'à ce qu’une chaîne non vide est entrée.  
  
 Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Valider les données dans le contrôle de DataGridView Windows Forms](how-to-validate-data-in-the-windows-forms-datagridview-control.md).  
  
## <a name="prerequisites"></a>Prérequis  
 Pour exécuter cette procédure pas à pas, vous avez besoin des éléments suivants :  
  
-   Accès à un serveur doté de la base de données Northwind SQL Server.  
  
## <a name="creating-the-form"></a>Création du formulaire  
  
#### <a name="to-validate-data-entered-in-a-datagridview"></a>Pour valider les données entrées dans un contrôle DataGridView  
  
1. Créez une classe qui dérive de <xref:System.Windows.Forms.Form> et contient un <xref:System.Windows.Forms.DataGridView> contrôle et un <xref:System.Windows.Forms.BindingSource> composant.  
  
     L’exemple de code suivant fournit l’initialisation de base et inclut un `Main` (méthode).  
  
     [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#01](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#01)]
     [!code-vb[System.Windows.Forms.DataGridViewDataValidation#01](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#01)]  
    [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#02](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#02)]
    [!code-vb[System.Windows.Forms.DataGridViewDataValidation#02](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#02)]  
  
2. Implémenter une méthode dans la définition de classe de votre formulaire pour gérer les détails de la connexion à la base de données.  
  
     Cet exemple de code utilise un `GetData` méthode qui retourne un remplis <xref:System.Data.DataTable> objet. N’oubliez pas que vous avez défini le `connectionString` variable une valeur qui est appropriée pour votre base de données.  
  
    > [!IMPORTANT]
    >  Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application. À l’aide de l’authentification Windows, également appelée sécurité intégrée, est un moyen plus sûr de contrôler l’accès à une base de données. Pour plus d’informations, consultez [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md).  
  
     [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#30)]
     [!code-vb[System.Windows.Forms.DataGridViewDataValidation#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#30)]  
  
3. Implémenter un gestionnaire pour votre formulaire <xref:System.Windows.Forms.Form.Load> événement qui initialise le <xref:System.Windows.Forms.DataGridView> et <xref:System.Windows.Forms.BindingSource> et configure la liaison de données.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#10)]
     [!code-vb[System.Windows.Forms.DataGridViewDataValidation#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#10)]  
  
4. Implémenter des gestionnaires pour les <xref:System.Windows.Forms.DataGridView> du contrôle <xref:System.Windows.Forms.DataGridView.CellValidating> et <xref:System.Windows.Forms.DataGridView.CellEndEdit> événements.  
  
     Le <xref:System.Windows.Forms.DataGridView.CellValidating> Gestionnaire d’événements est l’endroit où vous déterminez si la valeur d’une cellule dans la `CompanyName` colonne est vide. Si la valeur de cellule de validation échoue, définissez le <xref:System.ComponentModel.CancelEventArgs.Cancel%2A> propriété de la <xref:System.Windows.Forms.DataGridViewCellValidatingEventArgs?displayProperty=nameWithType> classe `true`. Cela entraîne le <xref:System.Windows.Forms.DataGridView> contrôle pour empêcher le curseur de quitter la cellule. Définir le <xref:System.Windows.Forms.DataGridViewRow.ErrorText%2A> propriété sur la ligne à une chaîne explicative. Cela affiche une icône d’erreur avec une info-bulle qui contient le texte d’erreur. Dans le <xref:System.Windows.Forms.DataGridView.CellEndEdit> Gestionnaire d’événements, définissez le <xref:System.Windows.Forms.DataGridViewRow.ErrorText%2A> propriété sur la ligne à la chaîne vide. Le <xref:System.Windows.Forms.DataGridView.CellEndEdit> événement produit uniquement lorsque la cellule quitte le mode d’édition, il ne peut faire en cas d’échec de validation.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#20)]
     [!code-vb[System.Windows.Forms.DataGridViewDataValidation#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#20)]  
  
## <a name="testing-the-application"></a>Test de l'application  
 Vous pouvez maintenant tester le formulaire pour vous assurer qu’il se comporte comme prévu.  
  
#### <a name="to-test-the-form"></a>Pour tester le formulaire  
  
-   Compilez et exécutez l'application.  
  
     Vous verrez un <xref:System.Windows.Forms.DataGridView> rempli avec des données à partir de la `Customers` table. Lorsque vous double-cliquez sur une cellule dans la `CompanyName` colonne, vous pouvez modifier la valeur. Si vous supprimez tous les caractères et que vous appuyez sur la touche TAB pour quitter la cellule, le <xref:System.Windows.Forms.DataGridView> vous empêche de le faire. Lorsque vous tapez une chaîne non vide dans la cellule, le <xref:System.Windows.Forms.DataGridView> contrôle vous permet de quitter la cellule.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Cette application vous donne une connaissance élémentaire de la <xref:System.Windows.Forms.DataGridView> fonctionnalités du contrôle. Vous pouvez personnaliser l’apparence et le comportement de la <xref:System.Windows.Forms.DataGridView> contrôle de plusieurs manières :  
  
-   Modifier les styles de bordure et en-tête. Pour plus d'informations, voir [Procédure : Modifier la bordure et de Styles de quadrillage dans les Windows Forms DataGridView Control](change-the-border-and-gridline-styles-in-the-datagrid.md).  
  
-   Activer ou restreindre l’entrée utilisateur et le <xref:System.Windows.Forms.DataGridView> contrôle. Pour plus d'informations, voir [Procédure : Empêcher l’ajout de ligne et de suppression dans les Windows Forms DataGridView Control](prevent-row-addition-and-deletion-datagridview.md), et [Comment : Définir une colonne en lecture seule dans les Windows Forms DataGridView Control](how-to-make-columns-read-only-in-the-windows-forms-datagridview-control.md).  
  
-   Vérifiez l’entrée d’utilisateur pour les erreurs relatives à la base de données. Pour plus d’informations, consultez [Procédure pas à pas : Gestion des erreurs qui se produisent lors de la saisie de données dans les Windows Forms DataGridView Control](handling-errors-that-occur-during-data-entry-in-the-datagrid.md).  
  
-   Gérer des jeux de données très volumineux à l’aide du mode virtuel. Pour plus d’informations, consultez [Procédure pas à pas : Implémentation du Mode virtuel dans les Windows Forms DataGridView Control](implementing-virtual-mode-wf-datagridview-control.md).  
  
-   Personnaliser l’apparence des cellules. Pour plus d'informations, voir [Procédure : Personnaliser l’apparence des cellules dans le contrôle de DataGridView Windows Forms](customize-the-appearance-of-cells-in-the-datagrid.md) et [Comment : Définir des Styles de police et couleur dans le contrôle DataGridView Windows Forms](how-to-set-font-and-color-styles-in-the-windows-forms-datagridview-control.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [Saisie de données dans le contrôle DataGridView Windows Forms](data-entry-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Valider les données dans le contrôle de DataGridView Windows Forms](how-to-validate-data-in-the-windows-forms-datagridview-control.md)
- [Procédure pas à pas : Gestion des erreurs qui se produisent lors de la saisie de données dans le contrôle de DataGridView Windows Forms](handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md)
