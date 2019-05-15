---
title: 'Procédure : valider les données dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [Windows Forms], validation
- DataGridView control [Windows Forms], data validation
- data grids [Windows Forms], validating data
- data validation [Windows Forms], Windows Forms
ms.assetid: d10aef35-701e-4a3c-a684-2a2ed1aeaca6
ms.openlocfilehash: 12fd668e22703271f8c629baf56487dd084cfd8b
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591036"
---
# <a name="how-to-validate-data-in-the-windows-forms-datagridview-control"></a>Procédure : valider les données dans le contrôle DataGridView Windows Forms
L'exemple de code suivant montre comment valider les données entrées par un utilisateur dans un contrôle <xref:System.Windows.Forms.DataGridView>. Dans cet exemple, le <xref:System.Windows.Forms.DataGridView> est rempli avec des lignes de la table `Customers` de la base de données Northwind. Quand l'utilisateur modifie une cellule dans la colonne `CompanyName`, la validité de sa valeur est testée en vérifiant qu'elle n'est pas vide. Si le gestionnaire d'événements de l'événement <xref:System.Windows.Forms.DataGridView.CellValidating> détecte que la valeur est une chaîne vide, le <xref:System.Windows.Forms.DataGridView> empêche l'utilisateur de quitter la cellule tant qu'il n'a pas entré une chaîne non vide.  
  
 Pour obtenir une explication complète de cet exemple de code, consultez [procédure pas à pas : Validation des données dans les Windows Forms DataGridView Control](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewDataValidation#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#00)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- Références aux assemblys System, System.Data, System.Windows.Forms et System.XML.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application. L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données. Pour plus d’informations, consultez [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [Procédure pas à pas : Validation des données dans le contrôle DataGridView Windows Forms](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [Saisie de données dans le contrôle DataGridView Windows Forms](data-entry-in-the-windows-forms-datagridview-control.md)
- [Procédure pas à pas : Gestion des erreurs qui se produisent lors de la saisie de données dans le contrôle de DataGridView Windows Forms](handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md)
