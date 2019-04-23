---
title: Méthode Load
ms.date: 03/30/2017
dev_langs:
- vb
ms.assetid: e22e5812-89c6-41f0-9302-bb899a46dbff
ms.openlocfilehash: 82f840ab7dd26a4888ebf024d696f2c70701eb18
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173288"
---
# <a name="the-load-method"></a><span data-ttu-id="0e50a-102">Méthode Load</span><span class="sxs-lookup"><span data-stu-id="0e50a-102">The Load Method</span></span>
<span data-ttu-id="0e50a-103">Vous pouvez utiliser la méthode <xref:System.Data.DataTable.Load%2A> pour charger un objet <xref:System.Data.DataTable> de lignes d'une source de données.</span><span class="sxs-lookup"><span data-stu-id="0e50a-103">You can use the <xref:System.Data.DataTable.Load%2A> method to load a <xref:System.Data.DataTable> with rows from a data source.</span></span> <span data-ttu-id="0e50a-104">Il s’agit d’une méthode surchargée qui, dans sa forme la plus simple, accepte un seul paramètre, un **DataReader**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-104">This is an overloaded method which, in its simplest form, accepts a single parameter, a **DataReader**.</span></span> <span data-ttu-id="0e50a-105">Dans cet écran, elle charge simplement la **DataTable** avec des lignes.</span><span class="sxs-lookup"><span data-stu-id="0e50a-105">In this form, it simply loads the **DataTable** with rows.</span></span> <span data-ttu-id="0e50a-106">Si vous le souhaitez, vous pouvez spécifier le **LoadOption** paramètre pour contrôler la façon dont les données sont ajoutées à la **DataTable**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-106">Optionally, you can specify the **LoadOption** parameter to control how data is added to the **DataTable**.</span></span>  
  
 <span data-ttu-id="0e50a-107">Le **LoadOption** paramètre est particulièrement utile dans les cas où le **DataTable** déjà contient des lignes de données, car il décrit les données entrantes à partir de la source de données seront combinées avec les données dans la table.</span><span class="sxs-lookup"><span data-stu-id="0e50a-107">The **LoadOption** parameter is particularly useful in cases where the **DataTable** already contains rows of data, because it describes how incoming data from the data source will be combined with the data already in the table.</span></span> <span data-ttu-id="0e50a-108">Par exemple, **PreserveCurrentValues** (la valeur par défaut) Spécifie que dans les cas où une ligne est marquée en tant que **Added** dans le **DataTable**, le **Original** valeur ou chaque colonne est définie pour le contenu de la ligne correspondante à partir de la source de données.</span><span class="sxs-lookup"><span data-stu-id="0e50a-108">For example, **PreserveCurrentValues** (the default) specifies that in cases where a row is marked as **Added** in the **DataTable**, the **Original** value or each column is set to the contents of the matching row from the data source.</span></span> <span data-ttu-id="0e50a-109">Le **actuel** valeur conserve les valeurs affectées lors de la ligne a été ajoutée et le **RowState** de la ligne aura la valeur **Changed**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-109">The **Current** value will retain the values assigned when the row was added, and the **RowState** of the row will be set to **Changed**.</span></span>  
  
 <span data-ttu-id="0e50a-110">Le tableau suivant donne une brève description des valeurs d'énumération <xref:System.Data.LoadOption>.</span><span class="sxs-lookup"><span data-stu-id="0e50a-110">The following table gives a short description of the <xref:System.Data.LoadOption> enumeration values.</span></span>  
  
|<span data-ttu-id="0e50a-111">Valeur LoadOption</span><span class="sxs-lookup"><span data-stu-id="0e50a-111">LoadOption value</span></span>|<span data-ttu-id="0e50a-112">Description</span><span class="sxs-lookup"><span data-stu-id="0e50a-112">Description</span></span>|  
|----------------------|-----------------|  
|<span data-ttu-id="0e50a-113">**OverwriteRow**</span><span class="sxs-lookup"><span data-stu-id="0e50a-113">**OverwriteRow**</span></span>|<span data-ttu-id="0e50a-114">Si des lignes entrantes ont la même **PrimaryKey** valeur sous la forme d’une ligne figurant déjà dans le **DataTable**, le **d’origine** et **actuel** les valeurs de chacun d’eux colonne sont remplacées par les valeurs dans la ligne entrante et la **RowState** propriété est définie sur **Unchanged**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-114">If incoming rows have the same **PrimaryKey** value as a row already in the **DataTable**, the **Original** and **Current** values of each column are replaced with the values in the incoming row, and the **RowState** property is set to **Unchanged**.</span></span><br /><br /> <span data-ttu-id="0e50a-115">Lignes de la source de données qui n’existent pas déjà dans le **DataTable** sont ajoutés avec un **RowState** valeur **Unchanged**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-115">Rows from the data source that do not already exist in the **DataTable** are added with a **RowState** value of **Unchanged**.</span></span><br /><br /> <span data-ttu-id="0e50a-116">Cette option actualise le contenu de la **DataTable** afin qu’il correspond au contenu de la source de données.</span><span class="sxs-lookup"><span data-stu-id="0e50a-116">This option in effect refreshes the contents of the **DataTable** so that it matches the contents of the data source.</span></span>|  
|<span data-ttu-id="0e50a-117">**PreserveCurrentValues (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="0e50a-117">**PreserveCurrentValues (default)**</span></span>|<span data-ttu-id="0e50a-118">Si des lignes entrantes ont la même **PrimaryKey** valeur sous la forme d’une ligne figurant déjà dans le **DataTable**, le **d’origine** a la valeur pour le contenu de la ligne entrante et la **Actuel** valeur n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="0e50a-118">If incoming rows have the same **PrimaryKey** value as a row already in the **DataTable**, the **Original** value is set to the contents of the incoming row, and the **Current** value is not changed.</span></span><br /><br /> <span data-ttu-id="0e50a-119">Si le **RowState** est **Added** ou **Modified**, il est défini sur **Modified**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-119">If the **RowState** is **Added** or **Modified**, it is set to **Modified**.</span></span><br /><br /> <span data-ttu-id="0e50a-120">Si le **RowState** a été **Deleted**, il reste **Deleted**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-120">If the **RowState** was **Deleted**, it remains **Deleted**.</span></span><br /><br /> <span data-ttu-id="0e50a-121">Lignes de la source de données qui n’existent pas déjà dans le **DataTable** sont ajoutés et le **RowState** a la valeur **Unchanged**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-121">Rows from the data source that do not already exist in the **DataTable** are added, and the **RowState** is set to **Unchanged**.</span></span>|  
|<span data-ttu-id="0e50a-122">**UpdateCurrentValues**</span><span class="sxs-lookup"><span data-stu-id="0e50a-122">**UpdateCurrentValues**</span></span>|<span data-ttu-id="0e50a-123">Si des lignes entrantes ont la même **PrimaryKey** valeur en tant que ligne figurant déjà dans le **DataTable**, le **actuel** valeur est copiée dans le **Original**valeur et le **actuel** valeur est ensuite définie sur le contenu de la ligne entrante.</span><span class="sxs-lookup"><span data-stu-id="0e50a-123">If incoming rows have the same **PrimaryKey** value as the row already in the **DataTable**, the **Current** value is copied to the **Original** value, and the **Current** value is then set to the contents of the incoming row.</span></span><br /><br /> <span data-ttu-id="0e50a-124">Si le **RowState** dans le **DataTable** a été **Added**, le **RowState** reste **Added**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-124">If the **RowState** in the **DataTable** was **Added**, the **RowState** remains **Added**.</span></span> <span data-ttu-id="0e50a-125">Pour les lignes marquées comme **Modified** ou **Deleted**, le **RowState** est **Modified**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-125">For rows marked as **Modified** or **Deleted**, the **RowState** is **Modified**.</span></span><br /><br /> <span data-ttu-id="0e50a-126">Lignes de la source de données qui n’existent pas déjà dans le **DataTable** sont ajoutés et le **RowState** a la valeur **Added**.</span><span class="sxs-lookup"><span data-stu-id="0e50a-126">Rows from the data source that do not already exist in the **DataTable** are added, and the **RowState** is set to **Added**.</span></span>|  
  
 <span data-ttu-id="0e50a-127">L’exemple suivant utilise le **charge** méthode pour afficher une liste d’anniversaires des employés dans la **Northwind** base de données.</span><span class="sxs-lookup"><span data-stu-id="0e50a-127">The following sample uses the **Load** method to display a list of birthdays for the employees in the **Northwind** database.</span></span>  
  
```vb  
Private Sub LoadBirthdays(ByVal connectionString As String)  
    ' Assumes that connectionString is a valid connection string  
    ' to the Northwind database on SQL Server.  
    Dim queryString As String = _  
    "SELECT LastName, FirstName, BirthDate " & _  
      " FROM dbo.Employees " & _  
      "ORDER BY BirthDate, LastName, FirstName"  
  
    ' Open and fill a DataSet.   
    Dim adapter As SqlDataAdapter = New SqlDataAdapter( _  
        queryString, connectionString)  
    Dim employees As New DataSet  
    adapter.Fill(employees, "Employees")  
  
    ' Create a SqlDataReader for use with the Load Method.  
    Dim reader As DataTableReader = employees.GetDataReader()  
  
    ' Create an instance of DataTable and assign the first  
    ' DataTable in the DataSet.Tables collection to it.  
    Dim dataTableEmp As DataTable = employees.Tables(0)  
  
    ' Fill the DataTable with data by calling Load and  
    ' passing the SqlDataReader.  
    dataTableEmp.Load(reader, LoadOption.OverwriteRow)  
  
    ' Loop through the rows collection and display the values  
    ' in the console window.  
    Dim employeeRow As DataRow  
    For Each employeeRow In dataTableEmp.Rows  
        Console.WriteLine("{0:MM\\dd\\yyyy}" & ControlChars.Tab & _  
          "{1}, {2}", _  
          employeeRow("BirthDate"), _  
          employeeRow("LastName"), _  
          employeeRow("FirstName"))  
    Next employeeRow  
  
    ' Keep the window opened to view the contents.  
    Console.ReadLine()  
End Sub  
```  
  
## <a name="see-also"></a><span data-ttu-id="0e50a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e50a-128">See also</span></span>

- [<span data-ttu-id="0e50a-129">Manipulation des données dans un DataTable</span><span class="sxs-lookup"><span data-stu-id="0e50a-129">Manipulating Data in a DataTable</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)
- [<span data-ttu-id="0e50a-130">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="0e50a-130">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
