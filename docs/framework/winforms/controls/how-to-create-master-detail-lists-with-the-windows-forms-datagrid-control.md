---
title: 'Procédure : Créer les listes maître / détail avec le contrôle DataGrid Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- master-details lists
- DataGrid control [Windows Forms], master-details lists
- related tables [Windows Forms], displaying in DataGrid control
ms.assetid: 20388c6a-94f9-4d96-be18-8c200491247f
ms.openlocfilehash: 92b4a7d9513ce0ec9b7c02f57c23fa4267fb26ad
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052167"
---
# <a name="how-to-create-masterdetail-lists-with-the-windows-forms-datagrid-control"></a>Procédure : créer des listes maître/détails avec le contrôle DataGrid Windows Forms
> [!NOTE]
>  Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix. Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Si votre <xref:System.Data.DataSet> contient une série de tables associées, vous pouvez utiliser deux <xref:System.Windows.Forms.DataGrid> contrôles pour afficher les données dans un format maître/détail. Un <xref:System.Windows.Forms.DataGrid> est désigné comme étant la grille principale, et la seconde peut être désignée comme la grille de détails. Lorsque vous sélectionnez une entrée dans la liste principale, toutes les entrées enfants connexes s’affichent dans la liste des détails. Par exemple, si votre <xref:System.Data.DataSet> contient une table Customers et une table connexe Orders, vous devez spécifier la table Customers pour la grille principale et la table Orders pour la grille de détails. Lorsqu’un client est sélectionné dans la grille principale, toutes les commandes associées à ce client dans la table Orders seraient affiché dans la grille de détails.  
  
### <a name="to-set-a-masterdetail-relationship-programmatically"></a>Pour définir une relation maître/détail par programmation  
  
1. Créez deux nouveaux <xref:System.Windows.Forms.DataGrid> contrôle et définir leurs propriétés.  
  
2. Ajouter des tables au jeu de données.  
  
3. Déclarez une variable de type <xref:System.Data.DataRelation> pour représenter la relation que vous souhaitez créer.  
  
4. Instanciez la relation en spécifiant un nom pour la relation et la table, une colonne et un élément qui lie les deux tables.  
  
5. Ajouter la relation à la <xref:System.Data.DataSet> l’objet <xref:System.Data.DataSet.Relations%2A> collection.  
  
6. Utilisez le <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> méthode de la <xref:System.Windows.Forms.DataGrid> pour chacune des grilles pour lier le <xref:System.Data.DataSet>.  
  
     L’exemple suivant montre comment définir une relation maître/détail entre les tables Customers et Orders dans généré précédemment <xref:System.Data.DataSet> (`ds`).  
  
    ```vb  
    Dim myDataRelation As DataRelation  
    myDataRelation = New DataRelation _  
       ("CustOrd", ds.Tables("Customers").Columns("CustomerID"), _  
       ds.Tables("Orders").Columns("CustomerID"))  
    ' Add the relation to the DataSet.  
    ds.Relations.Add(myDataRelation)  
    GridOrders.SetDataBinding(ds, "Customers")  
    GridDetails.SetDataBinding(ds, "Customers.CustOrd")  
    ```  
  
    ```csharp  
    DataRelation myDataRelation;  
    myDataRelation = new DataRelation("CustOrd", ds.Tables["Customers"].Columns["CustomerID"], ds.Tables["Orders"].Columns["CustomerID"]);  
    // Add the relation to the DataSet.  
    ds.Relations.Add(myDataRelation);  
    GridOrders.SetDataBinding(ds,"Customers");  
    GridDetails.SetDataBinding(ds,"Customers.CustOrd");  
    ```  
  
    ```cpp  
    DataRelation^ myDataRelation;  
    myDataRelation = gcnew DataRelation("CustOrd",  
       ds->Tables["Customers"]->Columns["CustomerID"],  
       ds->Tables["Orders"]->Columns["CustomerID"]);  
    // Add the relation to the DataSet.  
    ds->Relations->Add(myDataRelation);  
    GridOrders->SetDataBinding(ds, "Customers");  
    GridDetails->SetDataBinding(ds, "Customers.CustOrd");  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [DataGrid, contrôle](datagrid-control-windows-forms.md)
- [Vue d’ensemble du contrôle DataGrid](datagrid-control-overview-windows-forms.md)
- [Guide pratique pour Lier le contrôle DataGrid Windows Forms à une Source de données](how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md)
