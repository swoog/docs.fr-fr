---
title: 'Procédure : Appeler des fonctions de base de données personnalisées'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 4354e5eb-dd45-469d-97fb-1c495705ee59
ms.openlocfilehash: cc2e25183649f6a95e7862520ccc5719f201277a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774645"
---
# <a name="how-to-call-custom-database-functions"></a><span data-ttu-id="46ac2-102">Procédure : Appeler des fonctions de base de données personnalisées</span><span class="sxs-lookup"><span data-stu-id="46ac2-102">How to: Call Custom Database Functions</span></span>
<span data-ttu-id="46ac2-103">Cette rubrique décrit comment appeler des fonctions personnalisées définies dans la base de données dans des requêtes LINQ to Entities.</span><span class="sxs-lookup"><span data-stu-id="46ac2-103">This topic describes how to call custom functions that are defined in the database from within LINQ to Entities queries.</span></span>  
  
 <span data-ttu-id="46ac2-104">Les fonctions de base de données qui sont appelées à partir de requêtes LINQ to Entities sont exécutées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="46ac2-104">Database functions that are called from LINQ to Entities queries are executed in the database.</span></span> <span data-ttu-id="46ac2-105">L'exécution de fonctions dans la base de données peut améliorer les performances de l'application.</span><span class="sxs-lookup"><span data-stu-id="46ac2-105">Executing functions in the database can improve application performance.</span></span>  
  
 <span data-ttu-id="46ac2-106">La procédure ci-dessous fournit un plan de haut niveau pour l'appel d'une fonction de base de données personnalisée.</span><span class="sxs-lookup"><span data-stu-id="46ac2-106">The procedure below provides a high-level outline for calling a custom database function.</span></span> <span data-ttu-id="46ac2-107">L'exemple qui suit fournit plus de détails sur les étapes de la procédure.</span><span class="sxs-lookup"><span data-stu-id="46ac2-107">The example that follows provides more detail about the steps in the procedure.</span></span>  
  
### <a name="to-call-custom-functions-that-are-defined-in-the-database"></a><span data-ttu-id="46ac2-108">Pour appeler des fonctions personnalisées définies dans la base de données</span><span class="sxs-lookup"><span data-stu-id="46ac2-108">To call custom functions that are defined in the database</span></span>  
  
1. <span data-ttu-id="46ac2-109">Créez une fonction personnalisée dans votre base de données.</span><span class="sxs-lookup"><span data-stu-id="46ac2-109">Create a custom function in your database.</span></span>  
  
     <span data-ttu-id="46ac2-110">Pour plus d’informations sur la création de fonctions personnalisées dans SQL Server, consultez [CREATE FUNCTION (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkID=139871).</span><span class="sxs-lookup"><span data-stu-id="46ac2-110">For more information about creating custom functions in SQL Server, see [CREATE FUNCTION (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkID=139871).</span></span>  
  
2. <span data-ttu-id="46ac2-111">Déclarez une fonction dans la partie SSDL (Store Schema Definition Language) de votre fichier .edmx.</span><span class="sxs-lookup"><span data-stu-id="46ac2-111">Declare a function in the store schema definition language (SSDL) of your .edmx file.</span></span> <span data-ttu-id="46ac2-112">Le nom de la fonction doit être le même que le nom de la fonction déclarée dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="46ac2-112">The name of the function must be the same as the name of the function declared in the database.</span></span>  
  
     <span data-ttu-id="46ac2-113">Pour plus d’informations, consultez [élément (fonction) (SSDL)](/ef/ef6/modeling/designer/advanced/edmx/ssdl-spec#function-element-ssdl).</span><span class="sxs-lookup"><span data-stu-id="46ac2-113">For more information, see [Function Element (SSDL)](/ef/ef6/modeling/designer/advanced/edmx/ssdl-spec#function-element-ssdl).</span></span>  
  
3. <span data-ttu-id="46ac2-114">Ajoutez une méthode correspondante à une classe dans votre code d'application et appliquez un attribut <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute> à la méthode. Notez que les paramètres <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute.NamespaceName%2A> et <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute.FunctionName%2A> de l'attribut sont respectivement le nom de l'espace de noms du modèle conceptuel et le nom de la fonction dans le modèle conceptuel.</span><span class="sxs-lookup"><span data-stu-id="46ac2-114">Add a corresponding method to a class in your application code and apply a <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute> to the method Note that the <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute.NamespaceName%2A> and <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute.FunctionName%2A> parameters of the attribute are the namespace name of the conceptual model and the function name in the conceptual model respectively.</span></span> <span data-ttu-id="46ac2-115">La résolution des noms de fonctions pour LINQ respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="46ac2-115">Function name resolution for LINQ is case sensitive.</span></span>  
  
4. <span data-ttu-id="46ac2-116">Appelez la méthode dans une requête LINQ to Entities.</span><span class="sxs-lookup"><span data-stu-id="46ac2-116">Call the method in a LINQ to Entities query.</span></span>  
  
## <a name="example"></a><span data-ttu-id="46ac2-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="46ac2-117">Example</span></span>  
 <span data-ttu-id="46ac2-118">L'exemple suivant montre comment appeler une fonction de base de données personnalisée dans une requête LINQ to Entities.</span><span class="sxs-lookup"><span data-stu-id="46ac2-118">The following example demonstrates how to call a custom database function from within a LINQ to Entities query.</span></span> <span data-ttu-id="46ac2-119">L'exemple utilise le modèle School.</span><span class="sxs-lookup"><span data-stu-id="46ac2-119">The example uses the School model.</span></span> <span data-ttu-id="46ac2-120">Pour plus d’informations sur le modèle School, consultez [création de la base de données School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)) et [générant le fichier de School .edmx](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399739(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="46ac2-120">For information about the School model, see [Creating the School Sample Database](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)) and [Generating the School .edmx File](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399739(v=vs.100)).</span></span>  
  
 <span data-ttu-id="46ac2-121">Le code suivant ajoute la fonction `AvgStudentGrade` à l'exemple de base de données School.</span><span class="sxs-lookup"><span data-stu-id="46ac2-121">The following code adds the `AvgStudentGrade` function to the School sample database.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="46ac2-122">La procédure d'appel d'une fonction de base de données personnalisée est la même indépendamment du serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="46ac2-122">The steps for calling a custom database function are the same regardless of the database server.</span></span> <span data-ttu-id="46ac2-123">Toutefois, le code ci-dessous est spécifique à la création d'une fonction dans une base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="46ac2-123">However, the code below is specific to creating a function in a SQL Server database.</span></span> <span data-ttu-id="46ac2-124">Le code pour la création d'une fonction personnalisée sur d'autres serveurs de bases de données peut différer.</span><span class="sxs-lookup"><span data-stu-id="46ac2-124">The code for creating a custom function in other database servers might differ.</span></span>  
  
 [!code-sql[DP L2E MapToDBFunction#1](../../../../../../samples/snippets/tsql/VS_Snippets_Data/dp l2e maptodbfunction/tsql/create_avgstudentgrade.sql#1)]  
  
## <a name="example"></a><span data-ttu-id="46ac2-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="46ac2-125">Example</span></span>  
 <span data-ttu-id="46ac2-126">Ensuite, déclarez une fonction dans la partie SSDL (Store Schema Definition Language) de votre fichier .edmx.</span><span class="sxs-lookup"><span data-stu-id="46ac2-126">Next, declare a function in the store schema definition language (SSDL) of your .edmx file.</span></span> <span data-ttu-id="46ac2-127">Le code suivant déclare la fonction `AvgStudentGrade` en langage SSDL :</span><span class="sxs-lookup"><span data-stu-id="46ac2-127">the following code declares the `AvgStudentGrade` function in SSDL:</span></span>  
  
 [!code-xml[DP L2E MapToDBFunction#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp l2e maptodbfunction/cs/school.edmx#2)]  
  
## <a name="example"></a><span data-ttu-id="46ac2-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="46ac2-128">Example</span></span>  
 <span data-ttu-id="46ac2-129">À présent, créez une méthode et mappez-la à la fonction déclarée dans le langage SSDL.</span><span class="sxs-lookup"><span data-stu-id="46ac2-129">Now create a method and map it to the function declared in the SSDL.</span></span> <span data-ttu-id="46ac2-130">La méthode dans la classe suivante est mappée à la fonction définie dans le langage SSDL (ci-dessus) à l'aide d'un attribut <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute>.</span><span class="sxs-lookup"><span data-stu-id="46ac2-130">The method in the following class is mapped to the function defined in the SSDL (above) by using an <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute>.</span></span> <span data-ttu-id="46ac2-131">Lorsque cette méthode est appelée, la fonction correspondante dans la base de données est exécutée.</span><span class="sxs-lookup"><span data-stu-id="46ac2-131">When this method is called, the corresponding function in the database is executed.</span></span>  
  
 [!code-csharp[DP L2E MapToDBFunction#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp l2e maptodbfunction/cs/program.cs#3)]
 [!code-vb[DP L2E MapToDBFunction#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp l2e maptodbfunction/vb/module1.vb#3)]  
  
## <a name="example"></a><span data-ttu-id="46ac2-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="46ac2-132">Example</span></span>  
 <span data-ttu-id="46ac2-133">Enfin, appelez la méthode dans une requête LINQ to Entities.</span><span class="sxs-lookup"><span data-stu-id="46ac2-133">Finally, call the method in a LINQ to Entities query.</span></span> <span data-ttu-id="46ac2-134">Le code suivant affiche le nom des étudiants et la moyenne des notes sur la console :</span><span class="sxs-lookup"><span data-stu-id="46ac2-134">The following code displays students' last names and average grades to the console:</span></span>  
  
 [!code-csharp[DP L2E MapToDBFunction#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp l2e maptodbfunction/cs/program.cs#4)]
 [!code-vb[DP L2E MapToDBFunction#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp l2e maptodbfunction/vb/module1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="46ac2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46ac2-135">See also</span></span>

- <span data-ttu-id="46ac2-136">[vue d’ensemble du fichier .edmx](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="46ac2-136">[.edmx File Overview](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100))</span></span>
- [<span data-ttu-id="46ac2-137">Requêtes dans LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="46ac2-137">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
