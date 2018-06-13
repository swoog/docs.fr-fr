---
title: Implémentation de lectures/requêtes dans un microservice CQRS
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation de lectures/requêtes dans un microservice CQRS
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/02/2017
ms.openlocfilehash: 8eca01acc2308097d1684be8bdb0f07edd86832f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33579104"
---
# <a name="implementing-readsqueries-in-a-cqrs-microservice"></a><span data-ttu-id="200fc-103">Implémentation de lectures/requêtes dans un microservice CQRS</span><span class="sxs-lookup"><span data-stu-id="200fc-103">Implementing reads/queries in a CQRS microservice</span></span>

<span data-ttu-id="200fc-104">Pour les lectures/requêtes, le microservice Ordering (Commandes) de l’application de référence eShopOnContainers implémente les requêtes indépendamment du modèle DDD et de la zone transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="200fc-104">For reads/queries, the ordering microservice from the eShopOnContainers reference application implements the queries independently from the DDD model and transactional area.</span></span> <span data-ttu-id="200fc-105">La raison principale en est que les demandes de requêtes et de transactions sont radicalement différentes.</span><span class="sxs-lookup"><span data-stu-id="200fc-105">This was done primarily because the demands for queries and for transactions are drastically different.</span></span> <span data-ttu-id="200fc-106">Les écritures exécutent des transactions qui doivent être conformes à la logique de domaine.</span><span class="sxs-lookup"><span data-stu-id="200fc-106">Writes execute transactions that must be compliant with the domain logic.</span></span> <span data-ttu-id="200fc-107">En revanche, les requêtes sont idempotentes et peuvent être séparées des règles du domaine.</span><span class="sxs-lookup"><span data-stu-id="200fc-107">Queries, on the other hand, are idempotent and can be segregated from the domain rules.</span></span>

<span data-ttu-id="200fc-108">L’approche est simple, comme le montre la figure 9-3.</span><span class="sxs-lookup"><span data-stu-id="200fc-108">The approach is simple, as shown in Figure 9-3.</span></span> <span data-ttu-id="200fc-109">L’interface API est implémentée par les contrôleurs d’API web à l’aide de n’importe quelle infrastructure, comme un micro-mappeur objet/relationnel (ORM) tel que Dapper, et en retournant des ViewModels dynamiques en fonction des besoins des applications d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="200fc-109">The API interface is implemented by the Web API controllers using any infrastructure, such as a micro Object Relational Mapper (ORM) like Dapper, and returning dynamic ViewModels depending on the needs of the UI applications.</span></span>

![](./media/image3.png)

<span data-ttu-id="200fc-110">**Figure 9-3**.</span><span class="sxs-lookup"><span data-stu-id="200fc-110">**Figure 9-3**.</span></span> <span data-ttu-id="200fc-111">Approche la plus simple pour les requêtes dans un microservice CQRS</span><span class="sxs-lookup"><span data-stu-id="200fc-111">The simplest approach for queries in a CQRS microservice</span></span>

<span data-ttu-id="200fc-112">Il s’agit de l’approche la plus simple possible pour les requêtes.</span><span class="sxs-lookup"><span data-stu-id="200fc-112">This is the simplest possible approach for queries.</span></span> <span data-ttu-id="200fc-113">Les définitions de requête interrogent la base de données et retournent un ViewModel dynamique généré instantanément pour chaque requête.</span><span class="sxs-lookup"><span data-stu-id="200fc-113">The query definitions query the database and return a dynamic ViewModel built on the fly for each query.</span></span> <span data-ttu-id="200fc-114">Étant donné que les requêtes sont idempotentes, elles ne changent pas les données, quel que soit le nombre d’exécutions d’une requête.</span><span class="sxs-lookup"><span data-stu-id="200fc-114">Since the queries are idempotent, they won't change the data no matter how many times you run a query.</span></span> <span data-ttu-id="200fc-115">Par conséquent, vous n’avez pas besoin d’être restreint par un modèle DDD utilisé du côté transactionnel, comme les agrégats et d’autres modèles. C’est pourquoi les requêtes sont séparées de la zone transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="200fc-115">Therefore, you don't need to be restricted by any DDD pattern used in the transactional side, like aggregates and other patterns, and that is why queries are separated from the transactional area.</span></span> <span data-ttu-id="200fc-116">Vous interrogez juste la base de données sur les données dont l’interface utilisateur a besoin et vous retournez un ViewModel dynamique qui n’a pas besoin d’être défini statiquement où que ce soit (aucune classe pour les ViewModels) excepté dans les instructions SQL elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="200fc-116">You simply query the database for the data that the UI needs and return a dynamic ViewModel that does not need to be statically defined anywhere (no classes for the ViewModels) except in the SQL statements themselves.</span></span>

<span data-ttu-id="200fc-117">Dans la mesure où il s’agit d’une approche simple, le code nécessaire côté requêtes (comme le code utilisant un micro-ORM tel que [Dapper](https://github.com/StackExchange/Dapper)) peut être implémenté [dans le même projet d’API web](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/src/Services/Ordering/Ordering.API/Application/Queries/OrderQueries.cs).</span><span class="sxs-lookup"><span data-stu-id="200fc-117">Since this is a simple approach, the code required for the queries side (such as code using a micro ORM like [Dapper](https://github.com/StackExchange/Dapper)) can be implemented [within the same Web API project](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/src/Services/Ordering/Ordering.API/Application/Queries/OrderQueries.cs).</span></span> <span data-ttu-id="200fc-118">La figure 9-4 illustre ce point.</span><span class="sxs-lookup"><span data-stu-id="200fc-118">Figure 9-4 shows this.</span></span> <span data-ttu-id="200fc-119">Les requêtes sont définies dans le projet de microservice **Ordering.API** dans la solution eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="200fc-119">The queries are defined in the **Ordering.API** microservice project within the eShopOnContainers solution.</span></span>

![](./media/image4.png)

<span data-ttu-id="200fc-120">**Figure 9-4**.</span><span class="sxs-lookup"><span data-stu-id="200fc-120">**Figure 9-4**.</span></span> <span data-ttu-id="200fc-121">Requêtes dans le microservice de commandes dans eShopOnContainers</span><span class="sxs-lookup"><span data-stu-id="200fc-121">Queries in the Ordering microservice in eShopOnContainers</span></span>

## <a name="using-viewmodels-specifically-made-for-client-apps-independent-from-domain-model-constraints"></a><span data-ttu-id="200fc-122">Utilisation de ViewModels spécifiquement conçus pour les applications clientes, soumis à aucune contrainte de modèle de domaine</span><span class="sxs-lookup"><span data-stu-id="200fc-122">Using ViewModels specifically made for client apps, independent from domain model constraints</span></span>

<span data-ttu-id="200fc-123">Étant donné que les requêtes sont exécutées pour obtenir les données exigées par les applications clientes, le type retourné peut être spécifiquement conçu pour les clients, en fonction des données retournées par les requêtes.</span><span class="sxs-lookup"><span data-stu-id="200fc-123">Since the queries are performed to obtain the data needed by the client applications, the returned type can be specifically made for the clients, based on the data returned by the queries.</span></span> <span data-ttu-id="200fc-124">Ces modèles, ou objets de transfert de données (DTO), sont appelés ViewModels.</span><span class="sxs-lookup"><span data-stu-id="200fc-124">These models, or Data Transfer Objects (DTOs), are called ViewModels.</span></span>

<span data-ttu-id="200fc-125">Les données retournées (ViewModel) peuvent être le résultat de données de plusieurs entités ou tables jointes à la base de données, ou même de plusieurs agrégats définis dans le modèle de domaine de la zone transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="200fc-125">The returned data (ViewModel) can be the result of joining data from multiple entities or tables in the database, or even across multiple aggregates defined in the domain model for the transactional area.</span></span> <span data-ttu-id="200fc-126">Dans ce cas, étant donné que vous créez des requêtes indépendantes du modèle de domaine, les limites et contraintes des agrégats sont totalement ignorées et vous êtes libre d’interroger toute table et colonne dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="200fc-126">In this case, because you are creating queries independent of the domain model, the aggregates boundaries and constraints are completely ignored and you're free to query any table and column you might need.</span></span> <span data-ttu-id="200fc-127">Cette approche offre une grande souplesse et une grande productivité pour les développeurs qui créent ou mettent à jour les requêtes.</span><span class="sxs-lookup"><span data-stu-id="200fc-127">This approach provides great flexibility and productivity for the developers creating or updating the queries.</span></span>

<span data-ttu-id="200fc-128">Les ViewModels peuvent être des types statiques définis dans des classes.</span><span class="sxs-lookup"><span data-stu-id="200fc-128">The ViewModels can be static types defined in classes.</span></span> <span data-ttu-id="200fc-129">Ils peuvent également être créés de manière dynamique en fonction des requêtes exécutées (tel qu’implémenté dans le microservice de commandes), ce qui représente une méthode très agile pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="200fc-129">Or they can be created dynamically based on the queries performed (as is implemented in the ordering microservice), which is very agile for developers.</span></span>

## <a name="using-dapper-as-a-micro-orm-to-perform-queries"></a><span data-ttu-id="200fc-130">Utilisation de Dapper comme micro-ORM pour exécuter des requêtes</span><span class="sxs-lookup"><span data-stu-id="200fc-130">Using Dapper as a micro ORM to perform queries</span></span>

<span data-ttu-id="200fc-131">Vous pouvez utiliser n’importe quel micro-ORM, Entity Framework Core ou même ADO.NET standard pour exécuter des requêtes.</span><span class="sxs-lookup"><span data-stu-id="200fc-131">You can use any micro ORM, Entity Framework Core, or even plain ADO.NET for querying.</span></span> <span data-ttu-id="200fc-132">Dans l’exemple d’application, Dapper a été sélectionné pour le microservice de commandes dans eShopOnContainers comme un bon exemple de micro-ORM courant.</span><span class="sxs-lookup"><span data-stu-id="200fc-132">In the sample application, Dapper was selected for the ordering microservice in eShopOnContainers as a good example of a popular micro ORM.</span></span> <span data-ttu-id="200fc-133">Vous pouvez exécuter des requêtes SQL standard avec de hautes performances, car il s’agit d’un framework très léger.</span><span class="sxs-lookup"><span data-stu-id="200fc-133">It can run plain SQL queries with great performance, because it's a very light framework.</span></span> <span data-ttu-id="200fc-134">Dapper vous permet d’écrire une requête SQL qui peut accéder à plusieurs tables et les joindre.</span><span class="sxs-lookup"><span data-stu-id="200fc-134">Using Dapper, you can write a SQL query that can access and join multiple tables.</span></span>

<span data-ttu-id="200fc-135">Dapper est un projet Open Source (initialement créé par Sam Saffron). Il fait partie des éléments essentiels utilisés dans [Stack Overflow](https://stackoverflow.com/).</span><span class="sxs-lookup"><span data-stu-id="200fc-135">Dapper is an open-source project (original created by Sam Saffron), and is part of the building blocks used in [Stack Overflow](https://stackoverflow.com/).</span></span> <span data-ttu-id="200fc-136">Pour utiliser Dapper, il vous suffit de l’installer par le biais du [package NuGet Dapper](https://www.nuget.org/packages/Dapper), comme illustré dans la figure suivante :</span><span class="sxs-lookup"><span data-stu-id="200fc-136">To use Dapper, you just need to install it through the [Dapper NuGet package](https://www.nuget.org/packages/Dapper), as shown in the following figure:</span></span>

![](./media/image4.1.png)

<span data-ttu-id="200fc-137">Vous devez également ajouter une instruction using afin que votre code ait accès aux méthodes d’extension Dapper.</span><span class="sxs-lookup"><span data-stu-id="200fc-137">You also need to add a using statement so your code has access to the Dapper extension methods.</span></span>

<span data-ttu-id="200fc-138">Quand vous utilisez Dapper dans votre code, vous utilisez directement la classe <xref:System.Data.SqlClient.SqlConnection> disponible dans l’espace de noms <xref:System.Data.SqlClient>.</span><span class="sxs-lookup"><span data-stu-id="200fc-138">When you use Dapper in your code, you directly use the <xref:System.Data.SqlClient.SqlConnection> class available in the <xref:System.Data.SqlClient> namespace.</span></span> <span data-ttu-id="200fc-139">Avec la méthode QueryAsync et d’autres méthodes d’extension qui étendent la classe <xref:System.Data.SqlClient.SqlConnection>, vous pouvez simplement exécuter des requêtes de façon directe et performante.</span><span class="sxs-lookup"><span data-stu-id="200fc-139">Through the QueryAsync method and other extension methods that extend the <xref:System.Data.SqlClient.SqlConnection> class, you can simply run queries in a straightforward and performant way.</span></span>

## <a name="dynamic-versus-static-viewmodels"></a><span data-ttu-id="200fc-140">ViewModels dynamiques et statiques</span><span class="sxs-lookup"><span data-stu-id="200fc-140">Dynamic versus static ViewModels</span></span>

<span data-ttu-id="200fc-141">Quand des ViewModels sont retournés à partir du côté serveur à des applications clientes, vous pouvez considérer ces ViewModels comme des objets de transfert de données (DTO) qui peuvent être différents pour les entités de domaine internes de votre modèle d’entité, car les ViewModels contiennent les données comme l’application cliente le souhaite.</span><span class="sxs-lookup"><span data-stu-id="200fc-141">When returning ViewModels from the server-side to client apps, you can think about those ViewModels as DTOs that can be different to the internal domain entities of your entity model because the ViewModels hold the data the way the client app needs.</span></span> <span data-ttu-id="200fc-142">Par conséquent, dans de nombreux cas, vous pouvez agréger des données provenant de plusieurs entités de domaine et composer les ViewModels précisément selon la façon dont l’application cliente a besoin de ces données.</span><span class="sxs-lookup"><span data-stu-id="200fc-142">Therefore, in many cases, you can aggregate data coming from multiple domain entities and compose the ViewModels precisely according to how the client app needs that data.</span></span>

<span data-ttu-id="200fc-143">Ces ViewModels ou DTO peuvent être définis explicitement (sous la forme de classes de conteneurs de données), comme la classe [OrderSummary](https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.API/Application/Queries/OrderViewModel.cs) présentée ultérieurement dans un extrait de code. Vous pouvez également retourner simplement des ViewModels dynamiques ou des DTO dynamiques en fonction des attributs retournés par vos requêtes, sous la forme d’un type `dynamic`.</span><span class="sxs-lookup"><span data-stu-id="200fc-143">Those ViewModels or DTOs can be defined explicitly (as data holder classes) like the [OrderSummary](https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.API/Application/Queries/OrderViewModel.cs) class shown in a later code snippet, or you could just return dynamic ViewModels or dynamic DTOs simply based on the attributes returned by your queries, as a `dynamic` type.</span></span>

### <a name="viewmodel-as-dynamic-type"></a><span data-ttu-id="200fc-144">ViewModel sous la forme d’un type dynamique</span><span class="sxs-lookup"><span data-stu-id="200fc-144">ViewModel as dynamic type</span></span>

<span data-ttu-id="200fc-145">Comme illustré dans le code suivant, un ViewModel peut être retourné directement par les requêtes en retournant un type dynamique qui, en interne, est basé sur les attributs retournés par une requête.</span><span class="sxs-lookup"><span data-stu-id="200fc-145">As shown in the following code, a ViewModel can be directly returned by the queries by returning a dynamic type that internally is based on the attributes returned by a query.</span></span> <span data-ttu-id="200fc-146">Cela signifie que le sous-ensemble d’attributs à retourner est basé sur la requête elle-même.</span><span class="sxs-lookup"><span data-stu-id="200fc-146">That means that the subset of attributes to be returned is based on the query itself.</span></span> <span data-ttu-id="200fc-147">Par conséquent, si vous ajoutez une nouvelle colonne à la requête ou à la jointure, ces données sont dynamiquement ajoutées au ViewModel retourné.</span><span class="sxs-lookup"><span data-stu-id="200fc-147">Therefore, if you add a new column to the query or join, that data is dynamically added to the returned ViewModel.</span></span>

```csharp
using Dapper;
using Microsoft.Extensions.Configuration;
using System.Data.SqlClient;
using System.Threading.Tasks;
using System.Dynamic;
using System.Collections.Generic;

public class OrderQueries : IOrderQueries
{
    public async Task<IEnumerable<dynamic>> GetOrdersAsync()
    {
        using (var connection = new SqlConnection(_connectionString))
        {
            connection.Open();
            return await connection.QueryAsync<dynamic>(
@"SELECT o.[Id] as ordernumber,
o.[OrderDate] as [date],os.[Name] as [status],
SUM(oi.units*oi.unitprice) as total
FROM [ordering].[Orders] o
LEFT JOIN[ordering].[orderitems] oi ON o.Id = oi.orderid
LEFT JOIN[ordering].[orderstatus] os on o.OrderStatusId = os.Id
GROUP BY o.[Id], o.[OrderDate], os.[Name]");
        }
    }
}
```

<span data-ttu-id="200fc-148">Le point important à retenir est qu’en utilisant un type dynamique, la collection de données retournée est assemblée de manière dynamique sous la forme du ViewModel.</span><span class="sxs-lookup"><span data-stu-id="200fc-148">The important point is that by using a dynamic type, the returned collection of data is dynamically assembled as the ViewModel.</span></span>

<span data-ttu-id="200fc-149">*Avantages :* Cette approche réduit la nécessité de modifier les classes ViewModel statiques quand vous mettez à jour la phrase SQL d’une requête. De ce fait, cette approche de conception est assez souple lors du codage, simple et peut évoluer rapidement en cas de changements futurs.</span><span class="sxs-lookup"><span data-stu-id="200fc-149">*Pros:* This approach reduces the need to modify static ViewModel classes whenever you update the SQL sentence of a query, making this design approach pretty agile when coding, straightforward, and quick to evolve in regard to future changes.</span></span>

<span data-ttu-id="200fc-150">*Inconvénients :* À long terme, les types dynamiques peuvent nuire à la clarté et avoir un impact sur la compatibilité d’un service avec les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="200fc-150">*Cons:* In the long term, dynamic types can impact negatively the clarity and impact the compatibility of a service with client apps.</span></span> <span data-ttu-id="200fc-151">De plus, les intergiciels (middleware) comme Swagger ne peuvent pas fournir le même niveau de documentation sur les types retournés si vous utilisez des types dynamiques.</span><span class="sxs-lookup"><span data-stu-id="200fc-151">In addition, middleware software like Swagger cannot provide the same level of documentation on returned types if using dynamic types.</span></span>

### <a name="viewmodel-as-predefined-dto-classes"></a><span data-ttu-id="200fc-152">ViewModel sous la forme de classes DTO prédéfinies</span><span class="sxs-lookup"><span data-stu-id="200fc-152">ViewModel as predefined DTO classes</span></span>

<span data-ttu-id="200fc-153">*Avantages :* Avoir des classes ViewModel prédéfinies statiques, comme des « contrats » basés sur des classes DTO explicites, est définitivement mieux pour les API publiques, mais également pour les microservices à long terme, même s’ils sont utilisés uniquement par la même application.</span><span class="sxs-lookup"><span data-stu-id="200fc-153">*Pros:* Having static predefined ViewModel classes, like "contracts" based on explicit DTO classes, is definitely better for public APIs but also for long term microservices, even if they are only used by the same application.</span></span>

<span data-ttu-id="200fc-154">Si vous voulez spécifier des types de réponse pour Swagger, vous devez utiliser des classes DTO explicites comme type de retour.</span><span class="sxs-lookup"><span data-stu-id="200fc-154">If you want to specify response types for swagger, you need to use explicit DTO classes as the return type.</span></span> <span data-ttu-id="200fc-155">Par conséquent, les classes DTO prédéfinies vous permettent de fournir des informations plus détaillées à partir de Swagger.</span><span class="sxs-lookup"><span data-stu-id="200fc-155">Therefore, predefined DTO classes allow you to offer richer information from Swagger.</span></span> <span data-ttu-id="200fc-156">Cela améliore la documentation et la compatibilité d’une API lors de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="200fc-156">That improves the API documentation and compatibility when consuming an API.</span></span>

<span data-ttu-id="200fc-157">*Inconvénient :* Comme indiqué précédemment, lors de la mise à jour du code, certaines étapes supplémentaires sont nécessaires pour mettre à jour les classes DTO.</span><span class="sxs-lookup"><span data-stu-id="200fc-157">*Cons:* As mentioned earlier, when updating the code, it takes some more steps to update the DTO classes.</span></span>

<span data-ttu-id="200fc-158">*Conseil basés sur notre expérience :* Dans les requêtes implémentées au niveau du microservice de commandes dans eShopOnContainers, nous avons commencé le développement en utilisant des ViewModels, car c’était très simple et agile pour les premières étapes du développement.</span><span class="sxs-lookup"><span data-stu-id="200fc-158">*Tip based on our experience:* In the queries implemented at the Ordering microservice in eShopOnContainers, we started developing by using dynamic ViewModels as it was very straightforward and agile on the early development stages.</span></span> <span data-ttu-id="200fc-159">Toutefois, une fois le développement stabilisé, nous avons choisi de refactoriser les API et d’utiliser des DTO statiques ou prédéfinis pour les ViewModels, car il est plus clair pour les consommateurs du microservice de connaître les types de DTO explicites, utilisés comme « contrats ».</span><span class="sxs-lookup"><span data-stu-id="200fc-159">But, once the development was stabilized, we chose to refactor the APIs and use static or pre-defined DTOs for the ViewModels, because it is clearer for the microservice’s consumers to know explicit DTO types, used as "contracts".</span></span>

<span data-ttu-id="200fc-160">Dans l’exemple suivant, vous pouvez voir comment la requête retourne des données en utilisant une classe DTO de ViewModel explicite : la classe OrderSummary.</span><span class="sxs-lookup"><span data-stu-id="200fc-160">In the following example, you can see how the query is returning data by using an explicit ViewModel DTO class: the OrderSummary class.</span></span>

```csharp
using Dapper;
using Microsoft.Extensions.Configuration;
using System.Data.SqlClient;
using System.Threading.Tasks;
using System.Dynamic;
using System.Collections.Generic;

public class OrderQueries : IOrderQueries
{
  public async Task<IEnumerable<OrderSummary>> GetOrdersAsync()
    {
        using (var connection = new SqlConnection(_connectionString))
        {
            connection.Open();
            var result = await connection.QueryAsync<dynamic>(
                  @"SELECT o.[Id] as ordernumber, 
                  o.[OrderDate] as [date],os.[Name] as [status], 
                  SUM(oi.units*oi.unitprice) as total
                  FROM [ordering].[Orders] o
                  LEFT JOIN[ordering].[orderitems] oi ON  o.Id = oi.orderid 
                  LEFT JOIN[ordering].[orderstatus] os on o.OrderStatusId = os.Id
                  GROUP BY o.[Id], o.[OrderDate], os.[Name]
                  ORDER BY o.[Id]");
        }
    } 
}
```

#### <a name="describing-response-types-of-web-apis"></a><span data-ttu-id="200fc-161">Description des types de réponse d’API web</span><span class="sxs-lookup"><span data-stu-id="200fc-161">Describing response types of Web APIs</span></span>

<span data-ttu-id="200fc-162">Les développeurs qui consomment des API web et des microservices se soucient davantage de ce qui est retourné, plus spécifiquement par les types de réponse et les codes d’erreur (s’ils ne sont pas standard).</span><span class="sxs-lookup"><span data-stu-id="200fc-162">Developers consuming web APIs and microservices are most concerned with what is returned — specifically response types and error codes (if not standard).</span></span> <span data-ttu-id="200fc-163">Ceux-ci sont gérés dans les annotations de données et les commentaires XML.</span><span class="sxs-lookup"><span data-stu-id="200fc-163">These are handled in the XML comments and data annotations.</span></span>

<span data-ttu-id="200fc-164">Sans documentation appropriée dans l’interface utilisateur de Swagger, le consommateur n’a pas connaissance des types retournés ou des codes HTTP pouvant être retournés.</span><span class="sxs-lookup"><span data-stu-id="200fc-164">Without proper documentation in the Swagger UI, the consumer lacks knowledge of what types are being returned or what HTTP codes can be returned.</span></span> <span data-ttu-id="200fc-165">Ce problème est résolu en ajoutant le <xref:Microsoft.AspNetCore.Mvc.ProducesResponseTypeAttribute?displayProperty=nameWithType>, afin que Swagger puisse générer des informations plus détaillées concernant les valeurs et le modèle de retour d’API, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="200fc-165">That problem is fixed by adding the <xref:Microsoft.AspNetCore.Mvc.ProducesResponseTypeAttribute?displayProperty=nameWithType>, so Swagger can generate richer information about the API return model and values, as shown in the following code:</span></span>

```csharp
namespace Microsoft.eShopOnContainers.Services.Ordering.API.Controllers
{
    [Route("api/v1/[controller]")]
    [Authorize]
    public class OrdersController : Controller
    {
       //Additional code...
       [Route("")]
       [HttpGet]
       [ProducesResponseType(typeof(IEnumerable<OrderSummary>),
                             (int)HttpStatusCode.OK)]
       public async Task<IActionResult> GetOrders()
       {
           var orderTask = _orderQueries.GetOrdersAsync();
           var orders = await orderTask;
           return Ok(orders);
        }
    }
}
```

<span data-ttu-id="200fc-166">Toutefois, l’attribut `ProducesResponseType` ne peut pas utiliser dynamic comme type, mais exige d’utiliser des types explicites, comme le DTO de ViewModel `OrderSummary`, illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="200fc-166">However, the `ProducesResponseType` attribute cannot use dynamic as a type but requires to use explicit types, like the `OrderSummary` ViewModel DTO, shown in the following example:</span></span>

```csharp
public class OrderSummary
{
    public int ordernumber { get; set; }
    public DateTime date { get; set; }
    public string status { get; set; }
    public double total { get; set; }
}
```

<span data-ttu-id="200fc-167">C’est une autre raison pour laquelle les types retournés explicites sont, à long terme, préférables aux types dynamiques.</span><span class="sxs-lookup"><span data-stu-id="200fc-167">This is another reason why explicit returned types are better than dynamic types, in the long term.</span></span>
<span data-ttu-id="200fc-168">Quand vous utilisez l’attribut `ProducesResponseType`, vous pouvez également spécifier le résultat attendu en ce qui concerne les erreurs/codes HTTP possibles, comme 200, 400, etc.</span><span class="sxs-lookup"><span data-stu-id="200fc-168">When using the `ProducesResponseType` attribute, you can also specify what is the expected outcome in regards possible HTTP errors/codes, like 200,400, etc.</span></span>

<span data-ttu-id="200fc-169">Dans l’image suivante, vous pouvez voir comment l’interface utilisateur de Swagger affiche les informations ResponseType.</span><span class="sxs-lookup"><span data-stu-id="200fc-169">In the following image, you can see how Swagger UI shows the ResponseType information.</span></span>

![](./media/image5.png)

<span data-ttu-id="200fc-170">**Figure 9-5**.</span><span class="sxs-lookup"><span data-stu-id="200fc-170">**Figure 9-5**.</span></span> <span data-ttu-id="200fc-171">Interface utilisateur de Swagger affichant les types de réponse et les codes d’état HTTP possibles à partir d’une API web</span><span class="sxs-lookup"><span data-stu-id="200fc-171">Swagger UI showing response types and possible HTTP status codes from a Web API</span></span>

<span data-ttu-id="200fc-172">L’image ci-dessus présente des exemples de valeurs basés sur les types ViewModel, ainsi que les codes d’état HTTP qui peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="200fc-172">You can see in the image above some example values based on the ViewModel types plus the possible HTTP status codes that can be returned.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="200fc-173">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="200fc-173">Additional resources</span></span>

-   <span data-ttu-id="200fc-174">**Dapper**
    [*https://github.com/StackExchange/dapper-dot-net*](https://github.com/StackExchange/dapper-dot-net)</span><span class="sxs-lookup"><span data-stu-id="200fc-174">**Dapper**
[*https://github.com/StackExchange/dapper-dot-net*](https://github.com/StackExchange/dapper-dot-net)</span></span>

-   <span data-ttu-id="200fc-175">**Julie Lerman. Points de données : Dapper, Entity Framework et les applications hybrides (article du magazine MSDN)**</span><span class="sxs-lookup"><span data-stu-id="200fc-175">**Julie Lerman. Data Points - Dapper, Entity Framework and Hybrid Apps (MSDN Mag. article)**</span></span>

    *https://msdn.microsoft.com/magazine/mt703432.aspx*

-   <span data-ttu-id="200fc-176">**Pages d’aide sur l’API web ASP.NET Core avec Swagger**</span><span class="sxs-lookup"><span data-stu-id="200fc-176">**ASP.NET Core Web API Help Pages using Swagger**</span></span>

    *https://docs.microsoft.com/aspnet/core/tutorials/web-api-help-pages-using-swagger?tabs=visual-studio*

>[!div class="step-by-step"]
<span data-ttu-id="200fc-177">[Précédent] (eshoponcontainers-cqrs-ddd-microservice.md) [Suivant] (ddd-oriented-microservice.md)</span><span class="sxs-lookup"><span data-stu-id="200fc-177">[Previous] (eshoponcontainers-cqrs-ddd-microservice.md) [Next] (ddd-oriented-microservice.md)</span></span>
