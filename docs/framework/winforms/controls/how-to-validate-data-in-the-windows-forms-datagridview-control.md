---
title: 'Procédure : Valider les données dans le contrôle de DataGridView Windows Forms'
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
ms.openlocfilehash: 10cd8a0bd2bed7c55be9540d5ee68b13dcd5f90d
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "56261724"
---
# <a name="how-to-validate-data-in-the-windows-forms-datagridview-control"></a>Procédure : Valider les données dans le contrôle de DataGridView Windows Forms
L'exemple de code suivant montre comment valider les données entrées par un utilisateur dans un contrôle <xref:System.Windows.Forms.DataGridView>. Dans cet exemple, le <xref:System.Windows.Forms.DataGridView> est rempli avec des lignes de la table `Customers` de la base de données Northwind. Quand l'utilisateur modifie une cellule dans la colonne `CompanyName`, la validité de sa valeur est testée en vérifiant qu'elle n'est pas vide. Si le gestionnaire d'événements de l'événement <xref:System.Windows.Forms.DataGridView.CellValidating> détecte que la valeur est une chaîne vide, le <xref:System.Windows.Forms.DataGridView> empêche l'utilisateur de quitter la cellule tant qu'il n'a pas entré une chaîne non vide.  
  
 Pour obtenir une explication complète de cet exemple de code, consultez [procédure pas à pas : Validation des données dans les Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#00](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewDataValidation#00](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#00)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Data, System.Windows.Forms et System.XML.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application. L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données. Pour plus d’informations, consultez [Protection des informations de connexion](../../../../docs/framework/data/adonet/protecting-connection-information.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [Procédure pas à pas : Validation des données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [Saisie de données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/data-entry-in-the-windows-forms-datagridview-control.md)
- [Procédure pas à pas : Gestion des erreurs qui se produisent lors de la saisie de données dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [Protection des informations de connexion](../../../../docs/framework/data/adonet/protecting-connection-information.md)
