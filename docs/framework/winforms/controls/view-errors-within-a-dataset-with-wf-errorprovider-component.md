---
title: 'Procédure : afficher les erreurs au sein d’un jeu de données avec le composant ErrorProvider Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- errors [Windows Forms], dataset errors
- error messages [Windows Forms], viewing in datasets
- ErrorProvider component [Windows Forms], dataset errors
ms.assetid: cbae023f-d651-4210-bdea-bcc5f037e321
ms.openlocfilehash: 15fbf4a3cebef1485f0c54ace36ab88f3d4289e7
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59310445"
---
# <a name="how-to-view-errors-within-a-dataset-with-the-windows-forms-errorprovider-component"></a>Procédure : afficher les erreurs au sein d’un jeu de données avec le composant ErrorProvider Windows Forms
Vous pouvez utiliser les formulaires Windows <xref:System.Windows.Forms.ErrorProvider> composant pour afficher les erreurs de colonne au sein d’un jeu de données ou autre source de données. Pour un <xref:System.Windows.Forms.ErrorProvider> composant pour afficher les erreurs de données sur un formulaire, il ne devra pas être directement associée à un contrôle. Une fois qu’elle est liée à une source de données, il peut afficher une icône d’erreur en regard de n’importe quel contrôle qui est lié à la même source de données.  
  
> [!NOTE]
>  Si vous modifiez le fournisseur d’erreur <xref:System.Windows.Forms.ErrorProvider.DataSource%2A> et <xref:System.Windows.Forms.ErrorProvider.DataMember%2A> propriétés au moment de l’exécution, vous devez utiliser le <xref:System.Windows.Forms.ErrorProvider.BindToDataAndErrors%2A> méthode pour éviter les conflits.  
  
### <a name="to-display-data-errors"></a>Pour afficher les erreurs de données  
  
1. Lier le composant à une colonne dans une table de données.  
  
    ```vb  
    ' Assumes existence of DataSet1, DataTable1  
    TextBox1.DataBindings.Add("Text", DataSet1, "Customers.Name")  
    ErrorProvider1.DataSource = DataSet1  
    ErrorProvider1.DataMember = "Customers"  
    ```  
  
    ```csharp  
    // Assumes existence of DataSet1, DataTable1  
    textBox1.DataBindings.Add("Text", DataSet1, "Customers.Name");  
    errorProvider1.DataSource = DataSet1;  
    errorProvider1.DataMember = "Customers";  
    ```  
  
2. Définir le <xref:System.Windows.Forms.ErrorProvider.ContainerControl%2A> propriété au formulaire.  
  
    ```vb  
    ErrorProvider1.ContainerControl = Me  
    ```  
  
    ```csharp  
    errorProvider1.ContainerControl = this;  
    ```  
  
3. Définir la position de l’enregistrement en cours sur une ligne qui contient une erreur de colonne.  
  
    ```vb  
    DataTable1.Rows(5).SetColumnError("Name", "Bad data in this row.")  
    Me.BindingContext(DataTable1).Position = 5  
    ```  
  
    ```csharp  
    DataTable1.Rows[5].SetColumnError("Name", "Bad data in this row.");  
    this.BindingContext [DataTable1].Position = 5;  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du composant ErrorProvider](errorprovider-component-overview-windows-forms.md)
- [Procédure : afficher des icônes d’erreur pour la validation de formulaire à l’aide du composant ErrorProvider Windows Forms](display-error-icons-for-form-validation-with-wf-errorprovider.md)
