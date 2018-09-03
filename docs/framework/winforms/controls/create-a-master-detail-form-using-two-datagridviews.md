---
title: 'Comment : créer un formulaire maître / détail utilisant deux contrôles de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], master/detail form
- parent-child tables [Windows Forms], displaying on Windows Forms
- master-details lists [Windows Forms], creating
ms.assetid: 99f6e876-3f7f-4139-9063-e36587c95b02
ms.openlocfilehash: 328970c5cc14669770793070942dd32f0144c159
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43487102"
---
# <a name="how-to-create-a-masterdetail-form-using-two-windows-forms-datagridview-controls"></a>Comment : créer un formulaire maître/détail utilisant deux contrôles DataGridView Windows Form
L'exemple de code suivant crée un formulaire maître/détail avec deux contrôles <xref:System.Windows.Forms.DataGridView> liés à deux composants <xref:System.Windows.Forms.BindingSource>. La source de données est un <xref:System.Data.DataSet> qui contient les tables `Customers` et `Orders` de l'exemple de base de données Northwind SQL Server, ainsi qu'un <xref:System.Data.DataRelation> qui associe les deux par l'intermédiaire de la colonne `CustomerID`.  
  
 Un <xref:System.Windows.Forms.BindingSource> est lié à la table `Customers` parente dans le jeu de données. Ces données sont affichées dans le contrôle <xref:System.Windows.Forms.DataGridView> maître. L'autre <xref:System.Windows.Forms.BindingSource> est lié au premier connecteur de données. La propriété <xref:System.Windows.Forms.BindingSource.DataMember%2A> du deuxième <xref:System.Windows.Forms.BindingSource> a comme valeur le nom de <xref:System.Data.DataRelation>. Cela a pour conséquence l'affichage, par le contrôle <xref:System.Windows.Forms.DataGridView> détail, des lignes de la table `Orders` enfant qui correspondent à la ligne actuelle dans le contrôle <xref:System.Windows.Forms.DataGridView> maître.  
  
 Pour obtenir une explication complète de cet exemple de code, consultez [procédure pas à pas : création d’un maître/détail utilisant deux Windows Forms DataGridView contrôles de formulaire](../../../../docs/framework/winforms/controls/creating-a-master-detail-form-using-two-datagridviews.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewMasterDetails#00](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMasterDetails/CS/masterdetails.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewMasterDetails#00](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMasterDetails/VB/masterdetails.vb#00)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
 des références aux assemblys System, System.Data, System.Windows.Forms et System.XML.  
  
-   Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application. L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données. Pour plus d’informations, consultez [Protection des informations de connexion](../../../../docs/framework/data/adonet/protecting-connection-information.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.BindingSource>  
 [Procédure pas à pas : création d'un formulaire maître/détail qui utilise deux contrôles DataGridView Windows Forms](../../../../docs/framework/winforms/controls/creating-a-master-detail-form-using-two-datagridviews.md)  
 [Affichage des données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/displaying-data-in-the-windows-forms-datagridview-control.md)  
 [Protection des informations de connexion](../../../../docs/framework/data/adonet/protecting-connection-information.md)
