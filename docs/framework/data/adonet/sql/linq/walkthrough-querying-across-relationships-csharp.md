---
title: 'Procédure pas à pas : Interrogation de relations (C#)'
ms.date: 03/30/2017
ms.assetid: 552abeb1-18f2-4e93-a9c6-ef7b2db30c32
ms.openlocfilehash: a24d96c9d138f0dcd2f162dad474da01f49e45d2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563663"
---
# <a name="walkthrough-querying-across-relationships-c"></a><span data-ttu-id="6dcaf-102">Procédure pas à pas : Interrogation de relations (C#)</span><span class="sxs-lookup"><span data-stu-id="6dcaf-102">Walkthrough: Querying Across Relationships (C#)</span></span>
<span data-ttu-id="6dcaf-103">Cette procédure pas à pas illustre l’utilisation de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] *associations* pour représenter les relations de clé étrangère dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-103">This walkthrough demonstrates the use of [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] *associations* to represent foreign-key relationships in the database.</span></span>  
  
 [!INCLUDE[note_settings_general](../../../../../../includes/note-settings-general-md.md)]  
  
 <span data-ttu-id="6dcaf-104">Cette procédure pas à pas a été écrite à l'aide des paramètres de développement Visual C#.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-104">This walkthrough was written by using Visual C# Development Settings.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="6dcaf-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="6dcaf-105">Prerequisites</span></span>  
 <span data-ttu-id="6dcaf-106">Vous devez avoir terminé [procédure pas à pas : Requête et modèle objet simples (C#)](../../../../../../docs/framework/data/adonet/sql/linq/walkthrough-simple-object-model-and-query-csharp.md).</span><span class="sxs-lookup"><span data-stu-id="6dcaf-106">You must have completed [Walkthrough: Simple Object Model and Query (C#)](../../../../../../docs/framework/data/adonet/sql/linq/walkthrough-simple-object-model-and-query-csharp.md).</span></span> <span data-ttu-id="6dcaf-107">Cette procédure pas à pas est basée sur cette dernière, y compris la présence du fichier northwnd.mdf dans c:\linqtest5.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-107">This walkthrough builds on that one, including the presence of the northwnd.mdf file in c:\linqtest5.</span></span>  
  
## <a name="overview"></a><span data-ttu-id="6dcaf-108">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="6dcaf-108">Overview</span></span>  
 <span data-ttu-id="6dcaf-109">Cette procédure pas à pas se compose de trois tâches principales :</span><span class="sxs-lookup"><span data-stu-id="6dcaf-109">This walkthrough consists of three main tasks:</span></span>  
  
-   <span data-ttu-id="6dcaf-110">Ajout d'une classe d'entité pour représenter la table Orders dans l'exemple de base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-110">Adding an entity class to represent the Orders table in the sample Northwind database.</span></span>  
  
-   <span data-ttu-id="6dcaf-111">Ajout d'annotations à la classe `Customer` pour améliorer la relation entre les classes `Customer` et `Order`.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-111">Supplementing annotations to the `Customer` class to enhance the relationship between the `Customer` and `Order` classes.</span></span>  
  
-   <span data-ttu-id="6dcaf-112">Création et exécution d'une requête pour tenter d'obtenir des informations `Order` en utilisant la classe `Customer`.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-112">Creating and running a query to test obtaining `Order` information by using the `Customer` class.</span></span>  
  
## <a name="mapping-relationships-across-tables"></a><span data-ttu-id="6dcaf-113">Mappage de relations entre des tables</span><span class="sxs-lookup"><span data-stu-id="6dcaf-113">Mapping Relationships Across Tables</span></span>  
 <span data-ttu-id="6dcaf-114">Une fois la définition de classe `Customer` terminée, créez la définition de classe d'entité `Order` qui inclut le code suivant indiquant que `Order.Customer` est une clé étrangère de `Customer.CustomerID`.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-114">After the `Customer` class definition, create the `Order` entity class definition that includes the following code, which indicates that `Order.Customer` relates as a foreign key to `Customer.CustomerID`.</span></span>  
  
#### <a name="to-add-the-order-entity-class"></a><span data-ttu-id="6dcaf-115">Pour ajouter la classe d'entité Order</span><span class="sxs-lookup"><span data-stu-id="6dcaf-115">To add the Order entity class</span></span>  
  
-   <span data-ttu-id="6dcaf-116">Tapez ou collez le code suivant après la classe `Customer` :</span><span class="sxs-lookup"><span data-stu-id="6dcaf-116">Type or paste the following code after the `Customer` class:</span></span>  
  
     [!code-csharp[DLinqWalk2CS#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk2CS/cs/Program.cs#1)]  
  
## <a name="annotating-the-customer-class"></a><span data-ttu-id="6dcaf-117">Annotation de la classe Customer</span><span class="sxs-lookup"><span data-stu-id="6dcaf-117">Annotating the Customer Class</span></span>  
 <span data-ttu-id="6dcaf-118">Dans cette étape, annotez la classe `Customer` pour indiquer sa relation avec la classe `Order`.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-118">In this step, you annotate the `Customer` class to indicate its relationship to the `Order` class.</span></span> <span data-ttu-id="6dcaf-119">Cet ajout n'est pas strictement nécessaire étant donné que la définition de la relation dans chacune des directions est suffisante pour créer le lien.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-119">(This addition is not strictly necessary, because defining the relationship in either direction is sufficient to create the link.</span></span> <span data-ttu-id="6dcaf-120">Cependant, l'ajout de cette annotation vous permet de naviguer facilement parmi les objets dans chacune des directions.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-120">But adding this annotation does enable you to easily navigate objects in either direction.)</span></span>  
  
#### <a name="to-annotate-the-customer-class"></a><span data-ttu-id="6dcaf-121">Pour annoter la classe Customer</span><span class="sxs-lookup"><span data-stu-id="6dcaf-121">To annotate the Customer class</span></span>  
  
-   <span data-ttu-id="6dcaf-122">Tapez ou collez le code suivant dans la classe `Customer` :</span><span class="sxs-lookup"><span data-stu-id="6dcaf-122">Type or paste the following code into the `Customer` class:</span></span>  
  
     [!code-csharp[DLinqWalk2CS#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk2CS/cs/Program.cs#2)]  
  
## <a name="creating-and-running-a-query-across-the-customer-order-relationship"></a><span data-ttu-id="6dcaf-123">Création et exécution d'une requête dans la relation entre les classes Order et Customer</span><span class="sxs-lookup"><span data-stu-id="6dcaf-123">Creating and Running a Query Across the Customer-Order Relationship</span></span>  
 <span data-ttu-id="6dcaf-124">Vous pouvez désormais accéder aux objets `Order` directement à partir des objets `Customer` ou inversement.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-124">You can now access `Order` objects directly from the `Customer` objects, or in the opposite order.</span></span> <span data-ttu-id="6dcaf-125">Vous n’avez pas besoin explicite *jointure* entre customers et orders.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-125">You do not need an explicit *join* between customers and orders.</span></span>  
  
#### <a name="to-access-order-objects-by-using-customer-objects"></a><span data-ttu-id="6dcaf-126">Pour accéder aux objets Order à l'aide d'objets Customer</span><span class="sxs-lookup"><span data-stu-id="6dcaf-126">To access Order objects by using Customer objects</span></span>  
  
1.  <span data-ttu-id="6dcaf-127">Modifiez la méthode `Main` en tapant ou en collant le code suivant dans la méthode :</span><span class="sxs-lookup"><span data-stu-id="6dcaf-127">Modify the `Main` method by typing or pasting the following code into the method:</span></span>  
  
     [!code-csharp[DLinqWalk2CS#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk2CS/cs/Program.cs#3)]  
  
2.  <span data-ttu-id="6dcaf-128">Appuyez sur F5 pour déboguer l'application.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-128">Press F5 to debug your application.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="6dcaf-129">Vous pouvez supprimer le code SQL dans la fenêtre de console en supprimant `db.Log = Console.Out;`.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-129">You can eliminate the SQL code in the Console window by commenting out `db.Log = Console.Out;`.</span></span>  
  
3.  <span data-ttu-id="6dcaf-130">Appuyez sur Entrée dans la fenêtre de console pour arrêter le débogage.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-130">Press Enter in the Console window to stop debugging.</span></span>  
  
## <a name="creating-a-strongly-typed-view-of-your-database"></a><span data-ttu-id="6dcaf-131">Création d'une vue fortement typée de votre base de données</span><span class="sxs-lookup"><span data-stu-id="6dcaf-131">Creating a Strongly Typed View of Your Database</span></span>  
 <span data-ttu-id="6dcaf-132">Il est beaucoup plus facile de démarrer avec une vue fortement typée de votre base de données.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-132">It is much easier to start with a strongly typed view of your database.</span></span> <span data-ttu-id="6dcaf-133">En effectuant un typage fort de l'objet <xref:System.Data.Linq.DataContext>, vous n'avez pas besoin d'effectuer des appels à <xref:System.Data.Linq.DataContext.GetTable%2A>.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-133">By strongly typing the <xref:System.Data.Linq.DataContext> object, you do not need calls to <xref:System.Data.Linq.DataContext.GetTable%2A>.</span></span> <span data-ttu-id="6dcaf-134">Vous pouvez utiliser des tables fortement typées dans toutes vos requêtes lorsque vous utilisez l'objet <xref:System.Data.Linq.DataContext> fortement typé.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-134">You can use strongly typed tables in all your queries when you use the strongly typed <xref:System.Data.Linq.DataContext> object.</span></span>  
  
 <span data-ttu-id="6dcaf-135">Dans les étapes suivantes, vous créerez `Customers` comme table fortement typée qui mappe à la table Customers dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-135">In the following steps, you will create `Customers` as a strongly typed table that maps to the Customers table in the database.</span></span>  
  
#### <a name="to-strongly-type-the-datacontext-object"></a><span data-ttu-id="6dcaf-136">Pour effectuer un typage fort de l'objet DataContext</span><span class="sxs-lookup"><span data-stu-id="6dcaf-136">To strongly type the DataContext object</span></span>  
  
1.  <span data-ttu-id="6dcaf-137">Ajoutez le code suivant au-dessus de la déclaration de classe `Customer`.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-137">Add the following code above the `Customer` class declaration.</span></span>  
  
     [!code-csharp[DLinqWalk2CS#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk2CS/cs/Program.cs#4)]  
  
2.  <span data-ttu-id="6dcaf-138">Modifiez la méthode `Main` pour utiliser le <xref:System.Data.Linq.DataContext> fortement typé comme suit :</span><span class="sxs-lookup"><span data-stu-id="6dcaf-138">Modify the `Main` method to use the strongly typed <xref:System.Data.Linq.DataContext> as follows:</span></span>  
  
     [!code-csharp[DLinqWalk2CS#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk2CS/cs/Program.cs#5)]  
  
3.  <span data-ttu-id="6dcaf-139">Appuyez sur F5 pour déboguer l'application.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-139">Press F5 to debug your application.</span></span>  
  
     <span data-ttu-id="6dcaf-140">La sortie de la fenêtre de console est :</span><span class="sxs-lookup"><span data-stu-id="6dcaf-140">The Console window output is:</span></span>  
  
     `ID=WHITC`  
  
4.  <span data-ttu-id="6dcaf-141">Appuyez sur Entrée dans la fenêtre de console pour arrêter le débogage.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-141">Press Enter in the console window to stop debugging.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="6dcaf-142">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6dcaf-142">Next Steps</span></span>  
 <span data-ttu-id="6dcaf-143">La procédure pas à pas suivante ([procédure pas à pas : Manipulation des données (C#)](../../../../../../docs/framework/data/adonet/sql/linq/walkthrough-manipulating-data-csharp.md)) montre comment manipuler des données.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-143">The next walkthrough ([Walkthrough: Manipulating Data (C#)](../../../../../../docs/framework/data/adonet/sql/linq/walkthrough-manipulating-data-csharp.md)) demonstrates how to manipulate data.</span></span> <span data-ttu-id="6dcaf-144">Cette procédure pas à pas ne requiert pas d'enregistrer les deux procédures pas à pas de cette série que vous avez déjà terminées.</span><span class="sxs-lookup"><span data-stu-id="6dcaf-144">That walkthrough does not require that you save the two walkthroughs in this series that you have already completed.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6dcaf-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dcaf-145">See also</span></span>
- [<span data-ttu-id="6dcaf-146">Apprentissage par les procédures pas à pas</span><span class="sxs-lookup"><span data-stu-id="6dcaf-146">Learning by Walkthroughs</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/learning-by-walkthroughs.md)
