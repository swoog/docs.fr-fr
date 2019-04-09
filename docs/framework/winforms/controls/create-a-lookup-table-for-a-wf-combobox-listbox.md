---
title: 'Procédure : créer une table de choix pour un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- CheckedListBox control [Windows Forms], creating lookup tables
- lookup tables
- list boxes [Windows Forms], lookup tables
- ListBox control [Windows Forms], lookup tables
- ComboBox control [Windows Forms], lookup table
- lookup tables [Windows Forms], creating for controls
- combo boxes [Windows Forms], lookup tables
- ListBox control [Windows Forms], creating lookup tables
ms.assetid: 4ce35f12-1f4e-4317-92d1-af8686a8cfaa
ms.openlocfilehash: 95b1962b83a44a99ebc466e27c732917d63dc3c2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59125968"
---
# <a name="how-to-create-a-lookup-table-for-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="5d577-102">Procédure : créer une table de choix pour un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5d577-102">How to: Create a Lookup Table for a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>
<span data-ttu-id="5d577-103">Il est parfois utile d'afficher les données dans un format convivial dans un Windows Form, mais de les stocker dans un format plus pertinent pour votre programme.</span><span class="sxs-lookup"><span data-stu-id="5d577-103">Sometimes it is useful to display data in a user-friendly format on a Windows Form, but store the data in a format that is more meaningful to your program.</span></span> <span data-ttu-id="5d577-104">Par exemple, un formulaire de commande de produits alimentaires peut présenter les éléments de menu par leur nom dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="5d577-104">For example, an order form for food might display the menu items by name in a list box.</span></span> <span data-ttu-id="5d577-105">Toutefois, la table de données dans laquelle la commande est enregistrée contient alors les numéros d'ID uniques représentant les produits alimentaires.</span><span class="sxs-lookup"><span data-stu-id="5d577-105">However, the data table recording the order would contain the unique ID numbers representing the food.</span></span> <span data-ttu-id="5d577-106">Les tableaux ci-dessous montrent un exemple de stockage et d’affichage des données du formulaire de commande des produits alimentaires.</span><span class="sxs-lookup"><span data-stu-id="5d577-106">The following tables show an example of how to store and display order-form data for food.</span></span>  
  
### <a name="orderdetailstable"></a><span data-ttu-id="5d577-107">OrderDetailsTable</span><span class="sxs-lookup"><span data-stu-id="5d577-107">OrderDetailsTable</span></span>  
  
|<span data-ttu-id="5d577-108">OrderID</span><span class="sxs-lookup"><span data-stu-id="5d577-108">OrderID</span></span>|<span data-ttu-id="5d577-109">ItemID</span><span class="sxs-lookup"><span data-stu-id="5d577-109">ItemID</span></span>|<span data-ttu-id="5d577-110">Quantité</span><span class="sxs-lookup"><span data-stu-id="5d577-110">Quantity</span></span>|  
|-------------|------------|--------------|  
|<span data-ttu-id="5d577-111">4085</span><span class="sxs-lookup"><span data-stu-id="5d577-111">4085</span></span>|<span data-ttu-id="5d577-112">12</span><span class="sxs-lookup"><span data-stu-id="5d577-112">12</span></span>|<span data-ttu-id="5d577-113">1</span><span class="sxs-lookup"><span data-stu-id="5d577-113">1</span></span>|  
|<span data-ttu-id="5d577-114">4086</span><span class="sxs-lookup"><span data-stu-id="5d577-114">4086</span></span>|<span data-ttu-id="5d577-115">13</span><span class="sxs-lookup"><span data-stu-id="5d577-115">13</span></span>|<span data-ttu-id="5d577-116">3</span><span class="sxs-lookup"><span data-stu-id="5d577-116">3</span></span>|  
  
### <a name="itemtable"></a><span data-ttu-id="5d577-117">ItemTable</span><span class="sxs-lookup"><span data-stu-id="5d577-117">ItemTable</span></span>  
  
|<span data-ttu-id="5d577-118">Id</span><span class="sxs-lookup"><span data-stu-id="5d577-118">ID</span></span>|<span data-ttu-id="5d577-119">Nom</span><span class="sxs-lookup"><span data-stu-id="5d577-119">Name</span></span>|  
|--------|----------|  
|<span data-ttu-id="5d577-120">12</span><span class="sxs-lookup"><span data-stu-id="5d577-120">12</span></span>|<span data-ttu-id="5d577-121">Pomme de terre</span><span class="sxs-lookup"><span data-stu-id="5d577-121">Potato</span></span>|  
|<span data-ttu-id="5d577-122">13</span><span class="sxs-lookup"><span data-stu-id="5d577-122">13</span></span>|<span data-ttu-id="5d577-123">Poulet</span><span class="sxs-lookup"><span data-stu-id="5d577-123">Chicken</span></span>|  
  
 <span data-ttu-id="5d577-124">Dans ce scénario, une seule table, **OrderDetailsTable**, stocke les informations d’affichage et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5d577-124">In this scenario, one table, **OrderDetailsTable**, stores the actual information you are concerned with displaying and saving.</span></span> <span data-ttu-id="5d577-125">Cependant, pour économiser de l'espace, elle procède d’une façon plutôt insolite.</span><span class="sxs-lookup"><span data-stu-id="5d577-125">But to save space, it does so in a fairly cryptic fashion.</span></span> <span data-ttu-id="5d577-126">L’autre table, **ItemTable**, contient uniquement des informations relatives à l’apparence sur quel ID de nombre équivaut au nom de produit alimentaire et rien sur les commandes de produits alimentaires réelle.</span><span class="sxs-lookup"><span data-stu-id="5d577-126">The other table, **ItemTable**, contains only appearance-related information about which ID number is equivalent to which food name, and nothing about the actual food orders.</span></span>  
  
 <span data-ttu-id="5d577-127">Le **ItemTable** est connecté à la <xref:System.Windows.Forms.ComboBox>, <xref:System.Windows.Forms.ListBox>, ou <xref:System.Windows.Forms.CheckedListBox> via trois propriétés.</span><span class="sxs-lookup"><span data-stu-id="5d577-127">The **ItemTable** is connected to the <xref:System.Windows.Forms.ComboBox>, <xref:System.Windows.Forms.ListBox>, or <xref:System.Windows.Forms.CheckedListBox> control through three properties.</span></span> <span data-ttu-id="5d577-128">Le `DataSource` propriété comporte le nom de cette table.</span><span class="sxs-lookup"><span data-stu-id="5d577-128">The `DataSource` property contains the name of this table.</span></span> <span data-ttu-id="5d577-129">Le `DisplayMember` propriété contient la colonne de données de la table que vous souhaitez afficher dans le contrôle (nom du produit alimentaire).</span><span class="sxs-lookup"><span data-stu-id="5d577-129">The `DisplayMember` property contains the data column of that table that you want to display in the control (the food name).</span></span> <span data-ttu-id="5d577-130">Le `ValueMember` propriété contient la colonne de données de la table avec les informations stockées (numéro d’identification).</span><span class="sxs-lookup"><span data-stu-id="5d577-130">The `ValueMember` property contains the data column of that table with the stored information (the ID number).</span></span>  
  
 <span data-ttu-id="5d577-131">Le **OrderDetailsTable** est connecté au contrôle par sa collection de liaisons, accédée via la <xref:System.Windows.Forms.Control.DataBindings%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="5d577-131">The **OrderDetailsTable** is connected to the control by its bindings collection, accessed through the <xref:System.Windows.Forms.Control.DataBindings%2A> property.</span></span> <span data-ttu-id="5d577-132">Lorsque vous ajoutez un objet de liaison à la collection, vous vous connectez une propriété du contrôle à une donnée membre spécifique (la colonne des numéros d’ID) dans une source de données (le **OrderDetailsTable**).</span><span class="sxs-lookup"><span data-stu-id="5d577-132">When you add a binding object to the collection, you connect a control property to a specific data member (the column of ID numbers) in a data source (the **OrderDetailsTable**).</span></span> <span data-ttu-id="5d577-133">Quand une sélection est effectuée dans le contrôle, c’est dans cette table que l'entrée du formulaire est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="5d577-133">When a selection is made in the control, this table is where the form input is saved.</span></span>  
  
### <a name="to-create-a-lookup-table"></a><span data-ttu-id="5d577-134">Pour créer une table de choix</span><span class="sxs-lookup"><span data-stu-id="5d577-134">To create a lookup table</span></span>  
  
1.  <span data-ttu-id="5d577-135">Ajoutez un contrôle <xref:System.Windows.Forms.ComboBox>, <xref:System.Windows.Forms.ListBox> ou <xref:System.Windows.Forms.CheckedListBox> au formulaire.</span><span class="sxs-lookup"><span data-stu-id="5d577-135">Add a <xref:System.Windows.Forms.ComboBox>, <xref:System.Windows.Forms.ListBox>, or <xref:System.Windows.Forms.CheckedListBox> control to the form.</span></span>  
  
2.  <span data-ttu-id="5d577-136">Connectez-vous à la source de données.</span><span class="sxs-lookup"><span data-stu-id="5d577-136">Connect to your data source.</span></span>  
  
3.  <span data-ttu-id="5d577-137">Établissez une relation de données entre les deux tables.</span><span class="sxs-lookup"><span data-stu-id="5d577-137">Establish a data relation between the two tables.</span></span> <span data-ttu-id="5d577-138">Consultez [Introduction aux objets DataRelation](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/0k21zcyx(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="5d577-138">See [Introduction to DataRelation Objects](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/0k21zcyx(v=vs.120)).</span></span>  
  
4.  <span data-ttu-id="5d577-139">Définissez les propriétés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5d577-139">Set the following properties.</span></span> <span data-ttu-id="5d577-140">Elles peuvent être définies dans le code ou dans le concepteur.</span><span class="sxs-lookup"><span data-stu-id="5d577-140">They can be set in code or in the designer.</span></span>  
  
    |<span data-ttu-id="5d577-141">Propriété</span><span class="sxs-lookup"><span data-stu-id="5d577-141">Property</span></span>|<span data-ttu-id="5d577-142">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5d577-142">Setting</span></span>|  
    |--------------|-------------|  
    |<xref:System.Windows.Forms.ListControl.DataSource%2A>|<span data-ttu-id="5d577-143">Table qui contient des informations sur les équivalences entre les numéros d’ID et les articles.</span><span class="sxs-lookup"><span data-stu-id="5d577-143">The table that contains information about which ID number is equivalent to which item.</span></span> <span data-ttu-id="5d577-144">Dans le scénario précédent, il s’agit de `ItemTable`.</span><span class="sxs-lookup"><span data-stu-id="5d577-144">In the previous scenario, this is `ItemTable`.</span></span>|  
    |<xref:System.Windows.Forms.ListControl.DisplayMember%2A>|<span data-ttu-id="5d577-145">Colonne de la table de source de données que vous souhaitez afficher dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="5d577-145">The column of the data source table that you want to display in the control.</span></span> <span data-ttu-id="5d577-146">Dans le scénario précédent, il s’agit de `"Name"` (pour la définir dans le code, utilisez des guillemets).</span><span class="sxs-lookup"><span data-stu-id="5d577-146">In the previous scenario, this is `"Name"` (to set in code, use quotation marks).</span></span>|  
    |<xref:System.Windows.Forms.ListControl.ValueMember%2A>|<span data-ttu-id="5d577-147">Colonne de la table de source de données qui contient les informations stockées.</span><span class="sxs-lookup"><span data-stu-id="5d577-147">The column of the data source table that contains the stored information.</span></span> <span data-ttu-id="5d577-148">Dans le scénario précédent, il s’agit de `"ID"` (pour la définir dans le code, utilisez des guillemets).</span><span class="sxs-lookup"><span data-stu-id="5d577-148">In the previous scenario, this is `"ID"` (to set in code, use quotation marks).</span></span>|  
  
5.  <span data-ttu-id="5d577-149">Dans une procédure, appelez la méthode <xref:System.Windows.Forms.ControlBindingsCollection.Add%2A> de la classe <xref:System.Windows.Forms.ControlBindingsCollection> pour lier la ppropriété <xref:System.Windows.Forms.ListControl.SelectedValue%2A> du contrôle à la table d'enregistrement de l'entrée du formulaire.</span><span class="sxs-lookup"><span data-stu-id="5d577-149">In a procedure, call the <xref:System.Windows.Forms.ControlBindingsCollection.Add%2A> method of the <xref:System.Windows.Forms.ControlBindingsCollection> class to bind the control's <xref:System.Windows.Forms.ListControl.SelectedValue%2A> property to the table recording the form input.</span></span> <span data-ttu-id="5d577-150">Vous pouvez également effectuer cela dans le concepteur plutôt que dans le code, en accédant à du contrôle <xref:System.Windows.Forms.Control.DataBindings%2A> propriété dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5d577-150">You can also do this in the Designer instead of in code, by accessing the control's <xref:System.Windows.Forms.Control.DataBindings%2A> property in the **Properties** window.</span></span> <span data-ttu-id="5d577-151">Dans le scénario précédent, il s’agit de `OrderDetailsTable`, et la colonne est `"ItemID"`.</span><span class="sxs-lookup"><span data-stu-id="5d577-151">In the previous scenario, this is `OrderDetailsTable`, and the column is `"ItemID"`.</span></span>  
  
    ```vb  
    ListBox1.DataBindings.Add("SelectedValue", OrderDetailsTable, "ItemID")  
    ```  
  
    ```csharp  
    listBox1.DataBindings.Add("SelectedValue", OrderDetailsTable, "ItemID");  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="5d577-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d577-152">See also</span></span>

- [<span data-ttu-id="5d577-153">Liaison de données et Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5d577-153">Data Binding and Windows Forms</span></span>](../data-binding-and-windows-forms.md)
- [<span data-ttu-id="5d577-154">Vue d’ensemble du contrôle ListBox</span><span class="sxs-lookup"><span data-stu-id="5d577-154">ListBox Control Overview</span></span>](listbox-control-overview-windows-forms.md)
- [<span data-ttu-id="5d577-155">Vue d’ensemble du contrôle ComboBox</span><span class="sxs-lookup"><span data-stu-id="5d577-155">ComboBox Control Overview</span></span>](combobox-control-overview-windows-forms.md)
- [<span data-ttu-id="5d577-156">Vue d’ensemble du contrôle CheckedListBox</span><span class="sxs-lookup"><span data-stu-id="5d577-156">CheckedListBox Control Overview</span></span>](checkedlistbox-control-overview-windows-forms.md)
- [<span data-ttu-id="5d577-157">Contrôles Windows Forms utilisés pour l'affichage de listes d'options</span><span class="sxs-lookup"><span data-stu-id="5d577-157">Windows Forms Controls Used to List Options</span></span>](windows-forms-controls-used-to-list-options.md)
