---
title: Opérations de requête de base (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- data sources [LINQ in Visual Basic]
- Join clause [LINQ in Visual Basic]
- ordering data [LINQ in Visual Basic]
- projections [LINQ in Visual Basic]
- LINQ [Visual Basic], query operations
- Order By clause [LINQ in Visual Basic]
- joining data [LINQ in Visual Basic]
- queries [LINQ in Visual Basic], basic operations
- selecting data [LINQ in Visual Basic]
- Group By clause [LINQ in Visual Basic]
- grouping data [LINQ in Visual Basic]
- Select clause [LINQ in Visual Basic]
ms.assetid: 1146f6d0-fcb8-4f4d-8223-c9db52620d21
ms.openlocfilehash: ed5ed56366911c3676c4413711207ac0a8f85765
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61925646"
---
# <a name="basic-query-operations-visual-basic"></a><span data-ttu-id="d8a55-102">Opérations de requête de base (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8a55-102">Basic Query Operations (Visual Basic)</span></span>
<span data-ttu-id="d8a55-103">Cette rubrique fournit une brève introduction aux [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] expressions en Visual Basic et certains types d’opérations que vous effectuez dans une requête classiques.</span><span class="sxs-lookup"><span data-stu-id="d8a55-103">This topic provides a brief introduction to [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] expressions in Visual Basic, and to some of the typical kinds of operations that you perform in a query.</span></span> <span data-ttu-id="d8a55-104">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8a55-104">For more information, see the following topics:</span></span>  
  
 [<span data-ttu-id="d8a55-105">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d8a55-105">Introduction to LINQ in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
  
 [<span data-ttu-id="d8a55-106">Requêtes</span><span class="sxs-lookup"><span data-stu-id="d8a55-106">Queries</span></span>](../../../../visual-basic/language-reference/queries/index.md)  
  
 [<span data-ttu-id="d8a55-107">Procédure pas à pas : Écriture de requêtes dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d8a55-107">Walkthrough: Writing Queries in Visual Basic</span></span>](../../../../visual-basic/programming-guide/concepts/linq/walkthrough-writing-queries.md)  
  
## <a name="specifying-the-data-source-from"></a><span data-ttu-id="d8a55-108">Spécification de la Source de données (à partir de)</span><span class="sxs-lookup"><span data-stu-id="d8a55-108">Specifying the Data Source (From)</span></span>  
 <span data-ttu-id="d8a55-109">Dans un [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] requête, la première étape consiste à spécifier la source de données que vous souhaitez interroger.</span><span class="sxs-lookup"><span data-stu-id="d8a55-109">In a [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] query, the first step is to specify the data source that you want to query.</span></span> <span data-ttu-id="d8a55-110">Par conséquent, le `From` clause dans une requête toujours en premier.</span><span class="sxs-lookup"><span data-stu-id="d8a55-110">Therefore, the `From` clause in a query always comes first.</span></span> <span data-ttu-id="d8a55-111">Opérateurs de requête sélectionnent et mettre en forme le résultat en fonction du type de la source.</span><span class="sxs-lookup"><span data-stu-id="d8a55-111">Query operators select and shape the result based on the type of the source.</span></span>  
  
 [!code-vb[VbLINQBasicOps#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#1)]  
  
 <span data-ttu-id="d8a55-112">Le `From` clause spécifie la source de données `customers`et un *variable de portée*, `cust`.</span><span class="sxs-lookup"><span data-stu-id="d8a55-112">The `From` clause specifies the data source, `customers`, and a *range variable*, `cust`.</span></span> <span data-ttu-id="d8a55-113">La variable de portée est comme une variable d’itération de boucle, à ceci près que dans une expression de requête, aucune itération réelle ne se produit.</span><span class="sxs-lookup"><span data-stu-id="d8a55-113">The range variable is like a loop iteration variable, except that in a query expression, no actual iteration occurs.</span></span> <span data-ttu-id="d8a55-114">Lorsque la requête est exécutée, souvent à l’aide un `For Each` boucle, la variable de portée sert de référence pour chaque élément consécutif dans `customers`.</span><span class="sxs-lookup"><span data-stu-id="d8a55-114">When the query is executed, often by using a `For Each` loop, the range variable serves as a reference to each successive element in `customers`.</span></span> <span data-ttu-id="d8a55-115">Comme le compilateur déduit le type de `cust`, vous n’avez pas à le spécifier explicitement.</span><span class="sxs-lookup"><span data-stu-id="d8a55-115">Because the compiler can infer the type of `cust`, you do not have to specify it explicitly.</span></span> <span data-ttu-id="d8a55-116">Pour obtenir des exemples de requêtes écrites avec et sans type explicite, consultez [relations des types dans les opérations de requête (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/type-relationships-in-query-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-116">For examples of queries written with and without explicit typing, see [Type Relationships in Query Operations (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/type-relationships-in-query-operations.md).</span></span>  
  
 <span data-ttu-id="d8a55-117">Pour plus d’informations sur l’utilisation de la `From` clause en Visual Basic, consultez [Clause From](../../../../visual-basic/language-reference/queries/from-clause.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-117">For more information about how to use the `From` clause in Visual Basic, see [From Clause](../../../../visual-basic/language-reference/queries/from-clause.md).</span></span>  
  
## <a name="filtering-data-where"></a><span data-ttu-id="d8a55-118">Filtrage des données (où)</span><span class="sxs-lookup"><span data-stu-id="d8a55-118">Filtering Data (Where)</span></span>  
 <span data-ttu-id="d8a55-119">Probablement l’opération de requête plus courante consiste à appliquer un filtre sous la forme d’une expression booléenne.</span><span class="sxs-lookup"><span data-stu-id="d8a55-119">Probably the most common query operation is applying a filter in the form of a Boolean expression.</span></span> <span data-ttu-id="d8a55-120">Puis, la requête retourne uniquement les éléments pour lesquels l’expression est vraie.</span><span class="sxs-lookup"><span data-stu-id="d8a55-120">The query then returns only those elements for which the expression is true.</span></span> <span data-ttu-id="d8a55-121">Un `Where` clause est utilisée pour effectuer le filtrage.</span><span class="sxs-lookup"><span data-stu-id="d8a55-121">A `Where` clause is used to perform the filtering.</span></span> <span data-ttu-id="d8a55-122">Le filtre spécifie les éléments de la source de données à inclure dans la séquence résultante.</span><span class="sxs-lookup"><span data-stu-id="d8a55-122">The filter specifies which elements in the data source to include in the resulting sequence.</span></span> <span data-ttu-id="d8a55-123">Dans l’exemple suivant, que les clients qui ont une adresse à Londres sont inclus.</span><span class="sxs-lookup"><span data-stu-id="d8a55-123">In the following example, only those customers who have an address in London are included.</span></span>  
  
 [!code-vb[VbLINQBasicOps#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#2)]  
  
 <span data-ttu-id="d8a55-124">Vous pouvez utiliser des opérateurs logiques tels que `And` et `Or` pour combiner des expressions de filtre dans un `Where` clause.</span><span class="sxs-lookup"><span data-stu-id="d8a55-124">You can use logical operators such as `And` and `Or` to combine filter expressions in a `Where` clause.</span></span> <span data-ttu-id="d8a55-125">Par exemple, pour retourner uniquement les clients de Londres et dont le nom est Devon, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8a55-125">For example, to return only those customers who are from London and whose name is Devon, use the following code:</span></span>  
  
```vb  
Where cust.City = "London" And cust.Name = "Devon"   
```  
  
 <span data-ttu-id="d8a55-126">Pour retourner les clients de Londres ou Paris, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8a55-126">To return customers from London or Paris, use the following code:</span></span>  
  
```vb  
Where cust.City = "London" Or cust.City = "Paris"   
```  
  
 <span data-ttu-id="d8a55-127">Pour plus d’informations sur l’utilisation de la `Where` clause en Visual Basic, consultez [une Clause Where](../../../../visual-basic/language-reference/queries/where-clause.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-127">For more information about how to use the `Where` clause in Visual Basic, see [Where Clause](../../../../visual-basic/language-reference/queries/where-clause.md).</span></span>  
  
## <a name="ordering-data-order-by"></a><span data-ttu-id="d8a55-128">Classer des données (Order By)</span><span class="sxs-lookup"><span data-stu-id="d8a55-128">Ordering Data (Order By)</span></span>  
 <span data-ttu-id="d8a55-129">Il est souvent utile de trier les données retournées dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="d8a55-129">It often is convenient to sort returned data into a particular order.</span></span> <span data-ttu-id="d8a55-130">Le `Order By` clause triera les éléments de la séquence retournée à trier sur un ou plusieurs champs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d8a55-130">The `Order By` clause will cause the elements in the returned sequence to be sorted on a specified field or fields.</span></span> <span data-ttu-id="d8a55-131">Par exemple, la requête suivante trie les résultats selon la `Name` propriété.</span><span class="sxs-lookup"><span data-stu-id="d8a55-131">For example, the following query sorts the results based on the `Name` property.</span></span> <span data-ttu-id="d8a55-132">Étant donné que `Name` est une chaîne, les données retournées seront triées par ordre alphabétique, de A à Z.</span><span class="sxs-lookup"><span data-stu-id="d8a55-132">Because `Name` is a string, the returned data will be sorted alphabetically, from A to Z.</span></span>  
  
 [!code-vb[VbLINQBasicOps#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#3)]  
  
 <span data-ttu-id="d8a55-133">Pour trier les résultats dans l’ordre inverse, de Z à A, utilisez la clause `Order By...Descending`.</span><span class="sxs-lookup"><span data-stu-id="d8a55-133">To order the results in reverse order, from Z to A, use the `Order By...Descending` clause.</span></span> <span data-ttu-id="d8a55-134">La valeur par défaut est `Ascending` lorsque ni `Ascending` ni `Descending` est spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8a55-134">The default is `Ascending` when neither `Ascending` nor `Descending` is specified.</span></span>  
  
 <span data-ttu-id="d8a55-135">Pour plus d’informations sur l’utilisation de la `Order By` clause en Visual Basic, consultez [Clause Order By](../../../../visual-basic/language-reference/queries/order-by-clause.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-135">For more information about how to use the `Order By` clause in Visual Basic, see [Order By Clause](../../../../visual-basic/language-reference/queries/order-by-clause.md).</span></span>  
  
## <a name="selecting-data-select"></a><span data-ttu-id="d8a55-136">Sélection de données (Select)</span><span class="sxs-lookup"><span data-stu-id="d8a55-136">Selecting Data (Select)</span></span>  
 <span data-ttu-id="d8a55-137">Le `Select` clause spécifie la forme et le contenu des éléments retournés.</span><span class="sxs-lookup"><span data-stu-id="d8a55-137">The `Select` clause specifies the form and content of returned elements.</span></span> <span data-ttu-id="d8a55-138">Par exemple, vous pouvez spécifier si vos résultats comprendra complète `Customer` d’objets, seul `Customer` propriété, un sous-ensemble de propriétés, une combinaison de propriétés à partir de diverses sources de données ou un nouveau type de résultat basé sur un calcul.</span><span class="sxs-lookup"><span data-stu-id="d8a55-138">For example, you can specify whether your results will consist of complete `Customer` objects, just one `Customer` property, a subset of properties, a combination of properties from various data sources, or some new result type based on a computation.</span></span> <span data-ttu-id="d8a55-139">Quand la clause `Select` produit autre chose qu’une copie de l’élément source, l’opération est appelée *projection*.</span><span class="sxs-lookup"><span data-stu-id="d8a55-139">When the `Select` clause produces something other than a copy of the source element, the operation is called a *projection*.</span></span>  
  
 <span data-ttu-id="d8a55-140">Pour récupérer une collection qui se compose de complet `Customer` objets, sélectionnez la variable de portée elle-même :</span><span class="sxs-lookup"><span data-stu-id="d8a55-140">To retrieve a collection that consists of complete `Customer` objects, select the range variable itself:</span></span>  
  
 [!code-vb[VbLINQBasicOps#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#4)]  
  
 <span data-ttu-id="d8a55-141">Si un `Customer` instance est un objet qui compte de nombreux champs, et tout ce que vous souhaitez récupérer est le nom, vous pouvez sélectionner `cust.Name`, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="d8a55-141">If a `Customer` instance is a large object that has many fields, and all that you want to retrieve is the name, you can select `cust.Name`, as shown in the following example.</span></span> <span data-ttu-id="d8a55-142">Inférence de type local reconnaît que cela modifie le type de résultat d’une collection de `Customer` objets à une collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="d8a55-142">Local type inference recognizes that this changes the result type from a collection of `Customer` objects to a collection of strings.</span></span>  
  
 [!code-vb[VbLINQBasicOps#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#5)]  
  
 <span data-ttu-id="d8a55-143">Pour sélectionner plusieurs champs à partir de la source de données, vous avez deux possibilités :</span><span class="sxs-lookup"><span data-stu-id="d8a55-143">To select multiple fields from the data source, you have two choices:</span></span>  
  
- <span data-ttu-id="d8a55-144">Dans le `Select` clause, spécifiez les champs que vous souhaitez inclure dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="d8a55-144">In the `Select` clause, specify the fields you want to include in the result.</span></span> <span data-ttu-id="d8a55-145">Le compilateur définira un type anonyme qui a ces champs en tant que ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="d8a55-145">The compiler will define an anonymous type that has those fields as its properties.</span></span> <span data-ttu-id="d8a55-146">Pour plus d’informations, consultez [Types anonymes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-146">For more information, see [Anonymous Types](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).</span></span>  
  
     <span data-ttu-id="d8a55-147">Étant donné que les éléments retournés dans l’exemple suivant sont des instances d’un type anonyme, vous ne pouvez pas faire référence au type par nom ailleurs dans votre code.</span><span class="sxs-lookup"><span data-stu-id="d8a55-147">Because the returned elements in the following example are instances of an anonymous type, you cannot refer to the type by name elsewhere in your code.</span></span> <span data-ttu-id="d8a55-148">Le nom désigné par le compilateur pour le type contient des caractères qui ne sont pas valides dans du code Visual Basic normal.</span><span class="sxs-lookup"><span data-stu-id="d8a55-148">The compiler-designated name for the type contains characters that are not valid in normal Visual Basic code.</span></span> <span data-ttu-id="d8a55-149">Dans l’exemple suivant, les éléments dans la collection retournée par la requête dans `londonCusts4` sont des instances d’un type anonyme</span><span class="sxs-lookup"><span data-stu-id="d8a55-149">In the following example, the elements in the collection that is returned by the query in `londonCusts4` are instances of an anonymous type</span></span>  
  
     [!code-vb[VbLINQBasicOps#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#6)]  
  
     <span data-ttu-id="d8a55-150">- ou -</span><span class="sxs-lookup"><span data-stu-id="d8a55-150">-or-</span></span>  
  
- <span data-ttu-id="d8a55-151">Définir un type nommé qui contient les champs spécifiques que vous souhaitez inclure dans le résultat et créer et initialiser les instances du type dans le `Select` clause.</span><span class="sxs-lookup"><span data-stu-id="d8a55-151">Define a named type that contains the particular fields that you want to include in the result, and create and initialize instances of the type in the `Select` clause.</span></span> <span data-ttu-id="d8a55-152">Utilisez cette option uniquement si vous devez utiliser des résultats individuels en dehors de la collection dans laquelle ils sont retournés, ou si vous devez les passer en tant que paramètres dans les appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="d8a55-152">Use this option only if you have to use individual results outside the collection in which they are returned, or if you have to pass them as parameters in method calls.</span></span> <span data-ttu-id="d8a55-153">Le type de `londonCusts5` dans l’exemple suivant est IEnumerable (Of NamePhone).</span><span class="sxs-lookup"><span data-stu-id="d8a55-153">The type of `londonCusts5` in the following example is IEnumerable(Of NamePhone).</span></span>  
  
     [!code-vb[VbLINQBasicOps#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#7)]  
  
     [!code-vb[VbLINQBasicOps#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#8)]  
  
 <span data-ttu-id="d8a55-154">Pour plus d’informations sur l’utilisation de la `Select` clause en Visual Basic, consultez [Clause Select](../../../../visual-basic/language-reference/queries/select-clause.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-154">For more information about how to use the `Select` clause in Visual Basic, see [Select Clause](../../../../visual-basic/language-reference/queries/select-clause.md).</span></span>  
  
## <a name="joining-data-join-and-group-join"></a><span data-ttu-id="d8a55-155">Jointure de données (jointure et jointure groupée)</span><span class="sxs-lookup"><span data-stu-id="d8a55-155">Joining Data (Join and Group Join)</span></span>  
 <span data-ttu-id="d8a55-156">Vous pouvez combiner plusieurs sources de données dans le `From` clause de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="d8a55-156">You can combine more than one data source in the `From` clause in several ways.</span></span> <span data-ttu-id="d8a55-157">Par exemple, le code suivant utilise deux sources de données et associe implicitement les propriétés des deux dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="d8a55-157">For example, the following code uses two data sources and implicitly combines properties from both of them in the result.</span></span> <span data-ttu-id="d8a55-158">La requête sélectionne les étudiants dont le nom commence par une voyelle.</span><span class="sxs-lookup"><span data-stu-id="d8a55-158">The query selects students whose last names start with a vowel.</span></span>  
  
 [!code-vb[VbLINQBasicOps#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#9)]  
  
> [!NOTE]
>  <span data-ttu-id="d8a55-159">Vous pouvez exécuter ce code avec la liste d’étudiants créée dans [Comment : Créer une liste d’éléments](../../../../visual-basic/programming-guide/concepts/linq/how-to-create-a-list-of-items.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-159">You can run this code with the list of students created in [How to: Create a List of Items](../../../../visual-basic/programming-guide/concepts/linq/how-to-create-a-list-of-items.md).</span></span>  
  
 <span data-ttu-id="d8a55-160">Le `Join` mot clé est équivalente à une `INNER JOIN` dans SQL.</span><span class="sxs-lookup"><span data-stu-id="d8a55-160">The `Join` keyword is equivalent to an `INNER JOIN` in SQL.</span></span> <span data-ttu-id="d8a55-161">Il combine deux collections en fonction des valeurs de clés correspondantes entre les éléments dans les deux collections.</span><span class="sxs-lookup"><span data-stu-id="d8a55-161">It combines two collections based on matching key values between elements in the two collections.</span></span> <span data-ttu-id="d8a55-162">La requête retourne tout ou partie des éléments de collection qui ont des valeurs de clés correspondantes.</span><span class="sxs-lookup"><span data-stu-id="d8a55-162">The query returns all or part of the collection elements that have matching key values.</span></span> <span data-ttu-id="d8a55-163">Par exemple, le code suivant reproduit l’action de la jointure implicite précédente.</span><span class="sxs-lookup"><span data-stu-id="d8a55-163">For example, the following code duplicates the action of the previous implicit join.</span></span>  
  
 [!code-vb[VbLINQBasicOps#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#10)]  
  
 <span data-ttu-id="d8a55-164">`Group Join` combine des collections en une collection hiérarchique unique, comme un `LEFT JOIN` dans SQL.</span><span class="sxs-lookup"><span data-stu-id="d8a55-164">`Group Join` combines collections into a single hierarchical collection, just like a `LEFT JOIN` in SQL.</span></span> <span data-ttu-id="d8a55-165">Pour plus d’informations, consultez [Clause Join](../../../../visual-basic/language-reference/queries/join-clause.md) et [Group Join, Clause](../../../../visual-basic/language-reference/queries/group-join-clause.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-165">For more information, see [Join Clause](../../../../visual-basic/language-reference/queries/join-clause.md) and [Group Join Clause](../../../../visual-basic/language-reference/queries/group-join-clause.md).</span></span>  
  
## <a name="grouping-data-group-by"></a><span data-ttu-id="d8a55-166">Regroupement de données (Group By)</span><span class="sxs-lookup"><span data-stu-id="d8a55-166">Grouping Data (Group By)</span></span>  
 <span data-ttu-id="d8a55-167">Vous pouvez ajouter un `Group By` clause pour regrouper les éléments dans un résultat de requête en fonction d’un ou plusieurs champs des éléments.</span><span class="sxs-lookup"><span data-stu-id="d8a55-167">You can add a `Group By` clause to group the elements in a query result according to one or more fields of the elements.</span></span> <span data-ttu-id="d8a55-168">Par exemple, le code suivant regroupe les étudiants par année de la classe.</span><span class="sxs-lookup"><span data-stu-id="d8a55-168">For example, the following code groups students by class year.</span></span>  
  
 [!code-vb[VbLINQBasicOps#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#11)]  
  
 <span data-ttu-id="d8a55-169">Si vous exécutez ce code à l’aide de la liste d’étudiants créée dans [Comment : Créer une liste d’éléments](../../../../visual-basic/programming-guide/concepts/linq/how-to-create-a-list-of-items.md), la sortie de la `For Each` instruction est :</span><span class="sxs-lookup"><span data-stu-id="d8a55-169">If you run this code using the list of students created in [How to: Create a List of Items](../../../../visual-basic/programming-guide/concepts/linq/how-to-create-a-list-of-items.md), the output from the `For Each` statement is:</span></span>  
  
 <span data-ttu-id="d8a55-170">Année : « Junior »</span><span class="sxs-lookup"><span data-stu-id="d8a55-170">Year: Junior</span></span>  
  
 <span data-ttu-id="d8a55-171">Tucker, Michael</span><span class="sxs-lookup"><span data-stu-id="d8a55-171">Tucker, Michael</span></span>  
  
 <span data-ttu-id="d8a55-172">Garcia, Hugo</span><span class="sxs-lookup"><span data-stu-id="d8a55-172">Garcia, Hugo</span></span>  
  
 <span data-ttu-id="d8a55-173">Garcia, Marie</span><span class="sxs-lookup"><span data-stu-id="d8a55-173">Garcia, Debra</span></span>  
  
 <span data-ttu-id="d8a55-174">Tucker, Lance</span><span class="sxs-lookup"><span data-stu-id="d8a55-174">Tucker, Lance</span></span>  
  
 <span data-ttu-id="d8a55-175">Année : Senior</span><span class="sxs-lookup"><span data-stu-id="d8a55-175">Year: Senior</span></span>  
  
 <span data-ttu-id="d8a55-176">Omelchenko, Svetlana remarque</span><span class="sxs-lookup"><span data-stu-id="d8a55-176">Omelchenko, Svetlana</span></span>  
  
 <span data-ttu-id="d8a55-177">Osada, Michiko</span><span class="sxs-lookup"><span data-stu-id="d8a55-177">Osada, Michiko</span></span>  
  
 <span data-ttu-id="d8a55-178">Fakhouri, Fadi</span><span class="sxs-lookup"><span data-stu-id="d8a55-178">Fakhouri, Fadi</span></span>  
  
 <span data-ttu-id="d8a55-179">Feng, Hanying</span><span class="sxs-lookup"><span data-stu-id="d8a55-179">Feng, Hanying</span></span>  
  
 <span data-ttu-id="d8a55-180">Adams, Terry</span><span class="sxs-lookup"><span data-stu-id="d8a55-180">Adams, Terry</span></span>  
  
 <span data-ttu-id="d8a55-181">Année : Freshman</span><span class="sxs-lookup"><span data-stu-id="d8a55-181">Year: Freshman</span></span>  
  
 <span data-ttu-id="d8a55-182">Mortensen, Sven</span><span class="sxs-lookup"><span data-stu-id="d8a55-182">Mortensen, Sven</span></span>  
  
 <span data-ttu-id="d8a55-183">Garcia, Cesar</span><span class="sxs-lookup"><span data-stu-id="d8a55-183">Garcia, Cesar</span></span>  
  
 <span data-ttu-id="d8a55-184">La variante indiquée dans le code suivant trie les années de classe, puis trie les étudiants de chaque année par nom de famille.</span><span class="sxs-lookup"><span data-stu-id="d8a55-184">The variation shown in the following code orders the class years, and then orders the students within each year by last name.</span></span>  
  
 [!code-vb[VbLINQBasicOps#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#12)]  
  
 <span data-ttu-id="d8a55-185">Pour plus d’informations sur `Group By`, consultez [Group By Clause](../../../../visual-basic/language-reference/queries/group-by-clause.md).</span><span class="sxs-lookup"><span data-stu-id="d8a55-185">For more information about `Group By`, see [Group By Clause](../../../../visual-basic/language-reference/queries/group-by-clause.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8a55-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8a55-186">See also</span></span>

- <xref:System.Collections.Generic.IEnumerable%601>
- [<span data-ttu-id="d8a55-187">Bien démarrer avec LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d8a55-187">Getting Started with LINQ in Visual Basic</span></span>](../../../../visual-basic/programming-guide/concepts/linq/getting-started-with-linq.md)
- [<span data-ttu-id="d8a55-188">Requêtes</span><span class="sxs-lookup"><span data-stu-id="d8a55-188">Queries</span></span>](../../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="d8a55-189">Vue d’ensemble des opérateurs de requête standard (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8a55-189">Standard Query Operators Overview (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="d8a55-190">LINQ</span><span class="sxs-lookup"><span data-stu-id="d8a55-190">LINQ</span></span>](../../../../visual-basic/programming-guide/language-features/linq/index.md)
