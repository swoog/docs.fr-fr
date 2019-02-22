---
title: 'Procédure : Lier des données au contrôle Windows Forms DataGridView'
ms.date: 02/08/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [Windows Forms], grids
- data binding [Windows Forms], DataGridView control
- DataGridView control [Windows Forms], data binding
ms.assetid: 1660f69c-5711-45d2-abc1-e25bc6779124
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f98f095f888a8ef3622fabbf4c4745af60e930e3
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56584055"
---
# <a name="how-to-bind-data-to-the-windows-forms-datagridview-control"></a>Procédure : Lier des données au contrôle Windows Forms DataGridView

Le <xref:System.Windows.Forms.DataGridView> contrôle prend en charge le modèle de liaison de données Windows Forms standard, il peut être lié à une variété de sources de données. En règle générale, vous liez à un <xref:System.Windows.Forms.BindingSource> qui gère l’interaction avec la source de données. Le <xref:System.Windows.Forms.BindingSource> peut être toute source de données Windows Forms, qui vous donne une grande souplesse lors du choix ou de modification de l’emplacement de vos données. Pour plus d’informations sur les sources de données le <xref:System.Windows.Forms.DataGridView> contrôle prend en charge, consultez le [vue d’ensemble du contrôle DataGridView](../../../../docs/framework/winforms/controls/datagridview-control-overview-windows-forms.md).  

Visual Studio propose une prise en charge complète de la liaison de données pour le contrôle DataGridView. Pour plus d'informations, voir [Procédure : Lier des données au contrôle DataGridView de Windows Forms à l’aide du concepteur](bind-data-to-the-datagrid-using-the-designer.md).  

Pour vous connecter à un contrôle DataGridView à des données :

1. Implémenter une méthode pour gérer les détails de la récupération des données. Le code suivant exemple implémente un `GetData` méthode qui initialise un <xref:System.Data.SqlClient.SqlDataAdapter>et l’utilise pour remplir un <xref:System.Data.DataTable>. Il lie ensuite le <xref:System.Data.DataTable> à la <xref:System.Windows.Forms.BindingSource>. 

2. Dans le formulaire <xref:System.Windows.Forms.Form.Load> Gestionnaire d’événements, liez le <xref:System.Windows.Forms.DataGridView> le contrôle à la <xref:System.Windows.Forms.BindingSource>et appelez le `GetData` méthode pour récupérer les données.  

## <a name="example"></a>Exemple

Cet exemple de code complet récupère des données à partir d’une base de données pour remplir un contrôle DataGridView dans un formulaire Windows. Le formulaire comporte également des boutons pour recharger les données et soumettre des modifications à la base de données.  

Cet exemple nécessite : 

- Accès à une base de données exemple Northwind SQL Server. Pour plus d’informations sur l’installation de la base de données Northwind, consultez [obtenir les bases de données d’exemple pour obtenir des exemples de code ADO.NET](../../data/adonet/sql/linq/downloading-sample-databases.md). 

- Références aux assemblys System, System.Windows.Forms, System.Data et System.Xml.  

Pour générer et exécuter cet exemple, collez le code dans le *Form1* fichier de code dans un nouveau projet Windows Forms. Pour plus d’informations sur la génération à partir de la C# ou ligne de commande de Visual Basic, consultez [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md) ou [construire à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md).  
  
Remplir le `connectionString` variable dans l’exemple avec les valeurs pour votre connexion de base de données exemple Northwind SQL Server. L’authentification Windows, également appelée sécurité intégrée, est un moyen plus sûr pour vous connecter à la base de données que le stockage d’un mot de passe dans la chaîne de connexion. Pour plus d’informations sur la sécurité de connexion, consultez [protéger les informations de connexion](../../data/adonet/protecting-connection-information.md).  

[!code-csharp[System.Windows.Forms.DataGridViewBoundEditable](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewBoundEditable/CS/datagridviewboundeditable.cs)]
[!code-vb[System.Windows.Forms.DataGridViewBoundEditable](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewBoundEditable/VB/datagridviewboundeditable.vb)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.DataSource%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.BindingSource>
- [Afficher des données dans le contrôle Windows Forms DataGridView](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Protéger les informations de connexion](../../data/adonet/protecting-connection-information.md)
