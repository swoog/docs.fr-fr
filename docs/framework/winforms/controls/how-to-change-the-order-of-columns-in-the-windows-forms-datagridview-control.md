---
title: 'Procédure : Modifier l’ordre des colonnes dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- columns [Windows Forms], changing order
- DataGridView control [Windows Forms], column order
- data grids [Windows Forms], changing column order
ms.assetid: 5e9ac3bc-b0f0-48cb-a3d5-b005af905395
ms.openlocfilehash: a8e18080e757ceb4818bb795926a1eb4c27cf067
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56583353"
---
# <a name="how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="62b36-102">Procédure : Modifier l’ordre des colonnes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="62b36-102">How to: Change the Order of Columns in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="62b36-103">Quand vous utilisez un <xref:System.Windows.Forms.DataGridView> pour afficher des données à partir d'une source de données, les colonnes du schéma de la source de données apparaissent parfois dans un ordre différent de celui souhaité.</span><span class="sxs-lookup"><span data-stu-id="62b36-103">When you use a <xref:System.Windows.Forms.DataGridView> to display data from a data source, the columns in the data source's schema sometimes do not appear in the order you would like to display them.</span></span> <span data-ttu-id="62b36-104">Vous pouvez modifier l'ordre des colonnes à l'aide de la propriété <xref:System.Windows.Forms.DataGridViewColumn.DisplayIndex%2A> de la classe <xref:System.Windows.Forms.DataGridViewColumn>.</span><span class="sxs-lookup"><span data-stu-id="62b36-104">You can change the displayed order of the columns by using the <xref:System.Windows.Forms.DataGridViewColumn.DisplayIndex%2A> property of the <xref:System.Windows.Forms.DataGridViewColumn> class.</span></span>  
  
 <span data-ttu-id="62b36-105">L’exemple de code suivant repositionne quelques-unes des colonnes générées automatiquement lors de la liaison à la table Customers dans l’exemple de base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="62b36-105">The following code example repositions some of the columns automatically generated when binding to the Customers table in the Northwind sample database.</span></span> <span data-ttu-id="62b36-106">Pour plus d’informations sur la façon de lier le <xref:System.Windows.Forms.DataGridView> le contrôle à une table de base de données, consultez [Comment : Lier des données pour les Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/how-to-bind-data-to-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="62b36-106">For more information about how to bind the <xref:System.Windows.Forms.DataGridView> control to a database table, see [How to: Bind Data to the Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/how-to-bind-data-to-the-windows-forms-datagridview-control.md).</span></span>  
  
 <span data-ttu-id="62b36-107">Cette tâche est prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="62b36-107">There is support for this task in Visual Studio.</span></span>  <span data-ttu-id="62b36-108">Voir également [Guide pratique pour Modifier l’ordre des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du concepteur](change-the-order-of-columns-in-the-datagrid-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="62b36-108">Also see [How to: Change the Order of Columns in the Windows Forms DataGridView Control Using the Designer](change-the-order-of-columns-in-the-datagrid-using-the-designer.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="62b36-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="62b36-109">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#040](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#040)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#040](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#040)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="62b36-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="62b36-110">Compiling the Code</span></span>  
 <span data-ttu-id="62b36-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="62b36-111">This example requires:</span></span>  
  
-   <span data-ttu-id="62b36-112">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `customersDataGridView` qui est lié à une table avec les noms de colonnes indiqués, comme la table `Customers` dans la base de données Northwind ;</span><span class="sxs-lookup"><span data-stu-id="62b36-112">A <xref:System.Windows.Forms.DataGridView> control named `customersDataGridView` that is bound to a table with the indicated column names, such as the `Customers` table in the Northwind sample database.</span></span>  
  
-   <span data-ttu-id="62b36-113">des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, <xref:System.Data?displayProperty=nameWithType> et <xref:System.Xml?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="62b36-113">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, <xref:System.Data?displayProperty=nameWithType>, and <xref:System.Xml?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62b36-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62b36-114">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn>
- <xref:System.Windows.Forms.DataGridViewColumn.DisplayIndex%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType>
- [<span data-ttu-id="62b36-115">Affichage des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="62b36-115">Displaying Data in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/displaying-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="62b36-116">Guide pratique pour Lier des données au contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="62b36-116">How to: Bind Data to the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-bind-data-to-the-windows-forms-datagridview-control.md)
