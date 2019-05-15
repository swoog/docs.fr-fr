---
title: 'Procédure : Créer un formulaire maître / détail utilisant deux contrôles de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], master/detail form
- parent-child tables [Windows Forms], displaying on Windows Forms
- master-details lists [Windows Forms], creating
ms.assetid: 99f6e876-3f7f-4139-9063-e36587c95b02
ms.openlocfilehash: 16f23fac53cee5f6c007df6046e73cb7d9e1fbca
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65589201"
---
# <a name="how-to-create-a-masterdetail-form-using-two-windows-forms-datagridview-controls"></a><span data-ttu-id="9a19c-102">Procédure : créer un formulaire maître/détails qui utilise deux contrôles DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9a19c-102">How to: Create a Master/Detail Form Using Two Windows Forms DataGridView Controls</span></span>
<span data-ttu-id="9a19c-103">L'exemple de code suivant crée un formulaire maître/détail avec deux contrôles <xref:System.Windows.Forms.DataGridView> liés à deux composants <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="9a19c-103">The following code example creates a master/detail form using two <xref:System.Windows.Forms.DataGridView> controls bound to two <xref:System.Windows.Forms.BindingSource> components.</span></span> <span data-ttu-id="9a19c-104">La source de données est un <xref:System.Data.DataSet> qui contient les tables `Customers` et `Orders` de l'exemple de base de données Northwind SQL Server, ainsi qu'un <xref:System.Data.DataRelation> qui associe les deux par l'intermédiaire de la colonne `CustomerID`.</span><span class="sxs-lookup"><span data-stu-id="9a19c-104">The data source is a <xref:System.Data.DataSet> that contains the `Customers` and `Orders` tables from the Northwind SQL Server sample database along with a <xref:System.Data.DataRelation> that relates the two through the `CustomerID` column.</span></span>  
  
 <span data-ttu-id="9a19c-105">Un <xref:System.Windows.Forms.BindingSource> est lié à la table `Customers` parente dans le jeu de données.</span><span class="sxs-lookup"><span data-stu-id="9a19c-105">One <xref:System.Windows.Forms.BindingSource> is bound to the parent `Customers` table in the data set.</span></span> <span data-ttu-id="9a19c-106">Ces données sont affichées dans le contrôle <xref:System.Windows.Forms.DataGridView> maître.</span><span class="sxs-lookup"><span data-stu-id="9a19c-106">This data is displayed in the master <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="9a19c-107">L'autre <xref:System.Windows.Forms.BindingSource> est lié au premier connecteur de données.</span><span class="sxs-lookup"><span data-stu-id="9a19c-107">The other <xref:System.Windows.Forms.BindingSource> is bound to the first data connector.</span></span> <span data-ttu-id="9a19c-108">La propriété <xref:System.Windows.Forms.BindingSource.DataMember%2A> du deuxième <xref:System.Windows.Forms.BindingSource> a comme valeur le nom de <xref:System.Data.DataRelation>.</span><span class="sxs-lookup"><span data-stu-id="9a19c-108">The <xref:System.Windows.Forms.BindingSource.DataMember%2A> property of the second <xref:System.Windows.Forms.BindingSource> is set to the <xref:System.Data.DataRelation> name.</span></span> <span data-ttu-id="9a19c-109">Cela a pour conséquence l'affichage, par le contrôle <xref:System.Windows.Forms.DataGridView> détail, des lignes de la table `Orders` enfant qui correspondent à la ligne actuelle dans le contrôle <xref:System.Windows.Forms.DataGridView> maître.</span><span class="sxs-lookup"><span data-stu-id="9a19c-109">This causes the associated detail <xref:System.Windows.Forms.DataGridView> control to display the rows of the child `Orders` table that correspond to the current row in the master <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <span data-ttu-id="9a19c-110">Pour obtenir une explication complète de cet exemple de code, consultez [procédure pas à pas : Création d’un formulaire maître/détail à l’aide de deux Windows Forms contrôles DataGridView](creating-a-master-detail-form-using-two-datagridviews.md).</span><span class="sxs-lookup"><span data-stu-id="9a19c-110">For a complete explanation of this code example, see [Walkthrough: Creating a Master/Detail Form Using Two Windows Forms DataGridView Controls](creating-a-master-detail-form-using-two-datagridviews.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a19c-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="9a19c-111">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMasterDetails#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMasterDetails/CS/masterdetails.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewMasterDetails#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMasterDetails/VB/masterdetails.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9a19c-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="9a19c-112">Compiling the Code</span></span>  
 <span data-ttu-id="9a19c-113">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="9a19c-113">This example requires:</span></span>  
  
 <span data-ttu-id="9a19c-114">des références aux assemblys System, System.Data, System.Windows.Forms et System.XML.</span><span class="sxs-lookup"><span data-stu-id="9a19c-114">References to the System, System.Data, System.Windows.Forms, and System.XML assemblies.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="9a19c-115">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="9a19c-115">.NET Framework Security</span></span>  
 <span data-ttu-id="9a19c-116">Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="9a19c-116">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="9a19c-117">L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données.</span><span class="sxs-lookup"><span data-stu-id="9a19c-117">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="9a19c-118">Pour plus d’informations, consultez [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md).</span><span class="sxs-lookup"><span data-stu-id="9a19c-118">For more information, see [Protecting Connection Information](../../data/adonet/protecting-connection-information.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a19c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a19c-119">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="9a19c-120">Procédure pas à pas : Création d’un formulaire maître/détail utilisant deux contrôles de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9a19c-120">Walkthrough: Creating a Master/Detail Form Using Two Windows Forms DataGridView Controls</span></span>](creating-a-master-detail-form-using-two-datagridviews.md)
- [<span data-ttu-id="9a19c-121">Affichage des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9a19c-121">Displaying Data in the Windows Forms DataGridView Control</span></span>](displaying-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="9a19c-122">Protection des informations de connexion</span><span class="sxs-lookup"><span data-stu-id="9a19c-122">Protecting Connection Information</span></span>](../../data/adonet/protecting-connection-information.md)
