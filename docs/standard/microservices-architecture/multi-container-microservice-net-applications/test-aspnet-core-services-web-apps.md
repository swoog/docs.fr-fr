---
title: Test d’applications web et de services ASP.NET Core
description: Architecture des microservices .NET pour les applications .NET en conteneur | Test d’applications web et de services ASP.NET Core
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 12/11/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 596f588aae8c0814e5b40d29c4bf5723f944c5ac
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2018
---
# <a name="testing-aspnet-core-services-and-web-apps"></a><span data-ttu-id="1b477-104">Test d’applications web et de services ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="1b477-104">Testing ASP.NET Core services and web apps</span></span>

<span data-ttu-id="1b477-105">Les contrôleurs constituent l’élément central des services d’API ASP.NET Core et des applications web ASP.NET MVC.</span><span class="sxs-lookup"><span data-stu-id="1b477-105">Controllers are a central part of any ASP.NET Core API service and ASP.NET MVC Web application.</span></span> <span data-ttu-id="1b477-106">Par conséquent, vous devez être sûr qu’ils vont se comporter comme prévu avec votre application.</span><span class="sxs-lookup"><span data-stu-id="1b477-106">As such, you should have confidence they behave as intended for your application.</span></span> <span data-ttu-id="1b477-107">Les tests automatisés peuvent vous donner cette confiance et détecter des erreurs avant la mise en production.</span><span class="sxs-lookup"><span data-stu-id="1b477-107">Automated tests can provide you with this confidence and can detect errors before they reach production.</span></span>

<span data-ttu-id="1b477-108">Vous devez tester le comportement du contrôleur avec les entrées valides et non valides, ainsi que les réponses du contrôleur en fonction du résultat de l’opération qu’il effectue.</span><span class="sxs-lookup"><span data-stu-id="1b477-108">You need to test how the controller behaves based on valid or invalid inputs, and test controller responses based on the result of the business operation it performs.</span></span> <span data-ttu-id="1b477-109">Toutefois, vous devez effectuer ces types de tests pour vos microservices :</span><span class="sxs-lookup"><span data-stu-id="1b477-109">However, you should have these types of tests your microservices:</span></span>

-   <span data-ttu-id="1b477-110">Tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="1b477-110">Unit tests.</span></span> <span data-ttu-id="1b477-111">Ces tests permettent de vérifier que les composants de l’application fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="1b477-111">These ensure that individual components of the application work as expected.</span></span> <span data-ttu-id="1b477-112">Les assertions testent l’API des composants.</span><span class="sxs-lookup"><span data-stu-id="1b477-112">Assertions test the component API.</span></span>

-   <span data-ttu-id="1b477-113">Tests d’intégration.</span><span class="sxs-lookup"><span data-stu-id="1b477-113">Integration tests.</span></span> <span data-ttu-id="1b477-114">Ces tests permettent de vérifier que les interactions entre composants fonctionnent comme prévu, en se basant sur des artefacts externes comme les bases de données.</span><span class="sxs-lookup"><span data-stu-id="1b477-114">These ensure that component interactions work as expected against external artifacts like databases.</span></span> <span data-ttu-id="1b477-115">Les assertions peuvent tester l’API des composants, l’interface utilisateur ou les effets secondaires des actions telles que les E/S de base de données, la journalisation, etc.</span><span class="sxs-lookup"><span data-stu-id="1b477-115">Assertions can test component API, UI, or the side effects of actions like database I/O, logging, etc.</span></span>

-   <span data-ttu-id="1b477-116">Tests fonctionnels pour chaque microservice.</span><span class="sxs-lookup"><span data-stu-id="1b477-116">Functional tests for each microservice.</span></span> <span data-ttu-id="1b477-117">Ces tests permettent de vérifier que l’application fonctionne comme prévu du point de vue de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b477-117">These ensure that the application works as expected from the user’s perspective.</span></span>

-   <span data-ttu-id="1b477-118">Tests de service.</span><span class="sxs-lookup"><span data-stu-id="1b477-118">Service tests.</span></span> <span data-ttu-id="1b477-119">Ces tests permettent de garantir que les cas d’usage de service de bout en bout (y compris l’exécution simultanée de plusieurs services) sont testés.</span><span class="sxs-lookup"><span data-stu-id="1b477-119">These ensure that end-to-end service use cases, including testing multiple services at the same time, are tested.</span></span> <span data-ttu-id="1b477-120">Pour ce type de test, vous devez d’abord préparer l’environnement.</span><span class="sxs-lookup"><span data-stu-id="1b477-120">For this type of testing, you need to prepare the environment first.</span></span> <span data-ttu-id="1b477-121">Dans ce cas, cela signifie démarrer les services (à l’aide de docker-composer, par exemple).</span><span class="sxs-lookup"><span data-stu-id="1b477-121">In this case, it means starting the services (for example, by using docker-compose up).</span></span>

### <a name="implementing-unit-tests-for-aspnet-core-web-apis"></a><span data-ttu-id="1b477-122">Implémentation des tests unitaires pour les API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="1b477-122">Implementing unit tests for ASP.NET Core Web APIs</span></span>

<span data-ttu-id="1b477-123">Les tests unitaires impliquent le test d’une partie d’une application de façon isolée, par rapport à son infrastructure et à ses dépendances.</span><span class="sxs-lookup"><span data-stu-id="1b477-123">Unit testing involves testing a part of an application in isolation from its infrastructure and dependencies.</span></span> <span data-ttu-id="1b477-124">Lors du test de la logique d’un contrôleur, seul le contenu d’une action ou d’une méthode est testé, et non pas le comportement de ses dépendances ou du framework lui-même.</span><span class="sxs-lookup"><span data-stu-id="1b477-124">When you unit test controller logic, only the content of a single action or method is tested, not the behavior of its dependencies or of the framework itself.</span></span> <span data-ttu-id="1b477-125">Les tests unitaires ne détectent pas les problèmes d’interaction entre les composants, qui sont l’objet des tests d’intégration.</span><span class="sxs-lookup"><span data-stu-id="1b477-125">Unit tests do not detect issues in the interaction between components—that is the purpose of integration testing.</span></span>

<span data-ttu-id="1b477-126">Quand vous procédez à des tests unitaires pour les actions de votre contrôleur, concentrez-vous uniquement sur leur comportement.</span><span class="sxs-lookup"><span data-stu-id="1b477-126">As you unit test your controller actions, make sure you focus only on their behavior.</span></span> <span data-ttu-id="1b477-127">Les tests unitaires d’un contrôleur évitent les éléments tels que les filtres, le routage ou la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="1b477-127">A controller unit test avoids things like filters, routing, or model binding.</span></span> <span data-ttu-id="1b477-128">Comme ils ne s’occupent que d’un seul objet à la fois, les tests unitaires sont généralement simples à écrire et rapides à exécuter.</span><span class="sxs-lookup"><span data-stu-id="1b477-128">Because they focus on testing just one thing, unit tests are generally simple to write and quick to run.</span></span> <span data-ttu-id="1b477-129">Un ensemble de tests unitaires bien écrits peut être exécuté fréquemment sans engendrer une surcharge importante.</span><span class="sxs-lookup"><span data-stu-id="1b477-129">A well-written set of unit tests can be run frequently without much overhead.</span></span>

<span data-ttu-id="1b477-130">Les tests unitaires sont implémentés selon les frameworks de tests comme xUnit.net, MSTest, Moq ou NUnit.</span><span class="sxs-lookup"><span data-stu-id="1b477-130">Unit tests are implemented based on test frameworks like xUnit.net, MSTest, Moq, or NUnit.</span></span> <span data-ttu-id="1b477-131">Pour l’exemple d’application eShopOnContainers, nous utilisons XUnit.</span><span class="sxs-lookup"><span data-stu-id="1b477-131">For the eShopOnContainers sample application, we are using XUnit.</span></span>

<span data-ttu-id="1b477-132">Lorsque vous écrivez un test unitaire pour un contrôleur d’API web, vous instanciez la classe de contrôleur directement à l’aide du mot clé new dans du code C\#, pour que le test s’exécute aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="1b477-132">When you write a unit test for a Web API controller, you instantiate the controller class directly using the new keyword in C\#, so that the test will run as fast as possible.</span></span> <span data-ttu-id="1b477-133">L’exemple suivant montre comment effectuer cette opération lorsque vous utilisez [XUnit](https://xunit.github.io/) comme framework de tests.</span><span class="sxs-lookup"><span data-stu-id="1b477-133">The following example shows how to do this when using [XUnit](https://xunit.github.io/) as the Test framework.</span></span>

```csharp
[Fact]
public void Add_new_Order_raises_new_event()
{
    // Arrange
    var street = " FakeStreet ";
    var city = "FakeCity";
    // Other variables omitted for brevity ...
    // Act
    var fakeOrder = new Order(new Address(street, city, state, country, zipcode),
        cardTypeId, cardNumber,
        cardSecurityNumber, cardHolderName,
        cardExpiration);
    // Assert
    Assert.Equal(fakeOrder.DomainEvents.Count, expectedResult);
}
```

### <a name="implementing-integration-and-functional-tests-for-each-microservice"></a><span data-ttu-id="1b477-134">Implémentation de tests d’intégration et de tests fonctionnels pour chaque microservice</span><span class="sxs-lookup"><span data-stu-id="1b477-134">Implementing integration and functional tests for each microservice</span></span>

<span data-ttu-id="1b477-135">Comme mentionné précédemment, les tests d’intégration et les tests fonctionnels ont des objectifs différents.</span><span class="sxs-lookup"><span data-stu-id="1b477-135">As noted, integration tests and functional tests have different purposes and goals.</span></span> <span data-ttu-id="1b477-136">Toutefois, leur implémentation est similaire lorsque vous testez les contrôleurs ASP.NET Core. Cette section se concentre donc sur les tests d’intégration.</span><span class="sxs-lookup"><span data-stu-id="1b477-136">However, the way you implement both when testing ASP.NET Core controllers is similar, so in this section we concentrate on integration tests.</span></span>

<span data-ttu-id="1b477-137">Les tests d’intégration permettent de vérifier que les composants d’une application fonctionnent correctement une fois assemblés.</span><span class="sxs-lookup"><span data-stu-id="1b477-137">Integration testing ensures that an application's components function correctly when assembled.</span></span> <span data-ttu-id="1b477-138">ASP.NET Core prend en charge les tests d’intégration à l’aide des frameworks de tests unitaires et d’un hôte web de test intégré qui peut être utilisé pour gérer les requêtes, sans surcharger le réseau.</span><span class="sxs-lookup"><span data-stu-id="1b477-138">ASP.NET Core supports integration testing using unit test frameworks and a built-in test web host that can be used to handle requests without network overhead.</span></span>

<span data-ttu-id="1b477-139">Contrairement aux tests unitaires, les tests d’intégration rencontrent souvent des problèmes d’infrastructure d’application, liés par exemple, aux bases de données, aux systèmes de fichiers, aux ressources réseau ou aux requêtes et réponses web.</span><span class="sxs-lookup"><span data-stu-id="1b477-139">Unlike unit testing, integration tests frequently involve application infrastructure concerns, such as a database, file system, network resources, or web requests and responses.</span></span> <span data-ttu-id="1b477-140">Les tests unitaires utilisent des fakes ou objets fictifs pour éviter de tels problèmes.</span><span class="sxs-lookup"><span data-stu-id="1b477-140">Unit tests use fakes or mock objects in place of these concerns.</span></span> <span data-ttu-id="1b477-141">Toutefois, l’objectif des tests d’intégration est de vérifier que le système fonctionne comme prévu avec ces systèmes. Par conséquent, pour les tests d’intégration, vous ne devez pas utiliser de fakes ou d’objets fictifs.</span><span class="sxs-lookup"><span data-stu-id="1b477-141">But the purpose of integration tests is to confirm that the system works as expected with these systems, so for integration testing you do not use fakes or mock objects.</span></span> <span data-ttu-id="1b477-142">Vous devez inclure l’infrastructure, comme l’accès de base de données ou l’appel de service, des autres services.</span><span class="sxs-lookup"><span data-stu-id="1b477-142">Instead, you include the infrastructure, like database access or service invocation from other services.</span></span>

<span data-ttu-id="1b477-143">Étant donné que les tests d’intégration utilisent de plus grands segments de code que les tests unitaires, et comme les tests d’intégration reposent sur des éléments d’infrastructure, ils ont tendance à être beaucoup plus lents que les tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="1b477-143">Because integration tests exercise larger segments of code than unit tests, and because integration tests rely on infrastructure elements, they tend to be orders of magnitude slower than unit tests.</span></span> <span data-ttu-id="1b477-144">Par conséquent, il est conseillé de limiter le nombre de tests d’intégration que vous écrivez et exécutez.</span><span class="sxs-lookup"><span data-stu-id="1b477-144">Thus, it is a good idea to limit how many integration tests you write and run.</span></span>

<span data-ttu-id="1b477-145">ASP.NET Core inclut un web hôte de test intégré qui peut être utilisé pour gérer les requêtes HTTP sans surcharger le réseau. Vous pouvez donc exécuter ces tests plus rapidement lorsque vous utilisez un hôte web réel.</span><span class="sxs-lookup"><span data-stu-id="1b477-145">ASP.NET Core includes a built-in test web host that can be used to handle HTTP requests without network overhead, meaning that you can run those tests faster when using a real web host.</span></span> <span data-ttu-id="1b477-146">L’hôte web de test est disponible dans un composant NuGet, sous le nom de Microsoft.AspNetCore.TestHost.</span><span class="sxs-lookup"><span data-stu-id="1b477-146">The test web host is available in a NuGet component as Microsoft.AspNetCore.TestHost.</span></span> <span data-ttu-id="1b477-147">Il peut être ajouté aux projets de test d’intégration et utilisé pour héberger les applications ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="1b477-147">It can be added to integration test projects and used to host ASP.NET Core applications.</span></span>

<span data-ttu-id="1b477-148">Comme vous pouvez le voir dans le code suivant, lorsque vous créez des tests d’intégration pour des contrôleurs ASP.NET Core, vous instanciez les contrôleurs via l’hôte de test.</span><span class="sxs-lookup"><span data-stu-id="1b477-148">As you can see in the following code, when you create integration tests for ASP.NET Core controllers, you instantiate the controllers through the test host.</span></span> <span data-ttu-id="1b477-149">Ceci est comparable à une requête HTTP, avec toutefois, une exécution plus rapide.</span><span class="sxs-lookup"><span data-stu-id="1b477-149">This is comparable to an HTTP request, but it runs faster.</span></span>

```csharp
public class PrimeWebDefaultRequestShould
{
    private readonly TestServer _server;
    private readonly HttpClient _client;

    public PrimeWebDefaultRequestShould()
    {
        // Arrange
        _server = new TestServer(new WebHostBuilder()
           .UseStartup<Startup>());
           _client = _server.CreateClient();
    }

    [Fact]
    public async Task ReturnHelloWorld()
    {
        // Act
        var response = await _client.GetAsync("/");
        response.EnsureSuccessStatusCode();
        var responseString = await response.Content.ReadAsStringAsync();
        // Assert
        Assert.Equal("Hello World!", responseString);
    }
}
```

#### <a name="additional-resources"></a><span data-ttu-id="1b477-150">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="1b477-150">Additional resources</span></span>

-   <span data-ttu-id="1b477-151">**Steve Smith. Test d’un contrôleur** (ASP.NET Core) [*https://docs.microsoft.com/aspnet/core/mvc/controllers/testing*](/aspnet/core/mvc/controllers/testing)</span><span class="sxs-lookup"><span data-stu-id="1b477-151">**Steve Smith. Testing controllers** (ASP.NET Core) [*https://docs.microsoft.com/aspnet/core/mvc/controllers/testing*](/aspnet/core/mvc/controllers/testing)</span></span>

-   <span data-ttu-id="1b477-152">**Steve Smith. Tests d’intégration** (ASP.NET Core) [*https://docs.microsoft.com/aspnet/core/testing/integration-testing*](/aspnet/core/testing/integration-testing)</span><span class="sxs-lookup"><span data-stu-id="1b477-152">**Steve Smith. Integration testing** (ASP.NET Core) [*https://docs.microsoft.com/aspnet/core/testing/integration-testing*](/aspnet/core/testing/integration-testing)</span></span>

-   <span data-ttu-id="1b477-153">**Test unitaire dans .NET Core, à l’aide de test de dotnet**
    [*https://docs.microsoft.com/dotnet/core/testing/unit-testing-with-dotnet-test*](../../../core/testing/unit-testing-with-dotnet-test.md)</span><span class="sxs-lookup"><span data-stu-id="1b477-153">**Unit testing in .NET Core using dotnet test**
[*https://docs.microsoft.com/dotnet/core/testing/unit-testing-with-dotnet-test*](../../../core/testing/unit-testing-with-dotnet-test.md)</span></span>

-   <span data-ttu-id="1b477-154">**xUnit.net**.</span><span class="sxs-lookup"><span data-stu-id="1b477-154">**xUnit.net**.</span></span> <span data-ttu-id="1b477-155">Site officiel.</span><span class="sxs-lookup"><span data-stu-id="1b477-155">Official site.</span></span>
    [*https://xunit.github.io/*](https://xunit.github.io/)

-   <span data-ttu-id="1b477-156">**Concepts de base du Test unitaire.**
    [*https://msdn.microsoft.com/library/hh694602.aspx*](https://msdn.microsoft.com/library/hh694602.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b477-156">**Unit Test Basics.**
[*https://msdn.microsoft.com/library/hh694602.aspx*](https://msdn.microsoft.com/library/hh694602.aspx)</span></span>

-   <span data-ttu-id="1b477-157">**Moq**.</span><span class="sxs-lookup"><span data-stu-id="1b477-157">**Moq**.</span></span> <span data-ttu-id="1b477-158">Dépôt GitHub</span><span class="sxs-lookup"><span data-stu-id="1b477-158">GitHub repo.</span></span>
    [*https://github.com/moq/moq*](https://github.com/moq/moq)

-   <span data-ttu-id="1b477-159">**NUnit**.</span><span class="sxs-lookup"><span data-stu-id="1b477-159">**NUnit**.</span></span> <span data-ttu-id="1b477-160">Site officiel.</span><span class="sxs-lookup"><span data-stu-id="1b477-160">Official site.</span></span>
    [*https://www.nunit.org/*](https://www.nunit.org/)

### <a name="implementing-service-tests-on-a-multi-container-application"></a><span data-ttu-id="1b477-161">Implémentation de tests de service dans une application à plusieurs conteneurs</span><span class="sxs-lookup"><span data-stu-id="1b477-161">Implementing service tests on a multi-container application</span></span> 

<span data-ttu-id="1b477-162">Comme mentionné précédemment, lorsque vous testez des applications à plusieurs conteneurs, tous les microservices doivent être exécutés au sein de l’hôte Docker ou du cluster de conteneurs.</span><span class="sxs-lookup"><span data-stu-id="1b477-162">As noted earlier, when you test multi-container applications, all the microservices need to be running within the Docker host or container cluster.</span></span> <span data-ttu-id="1b477-163">Les tests de service de bout en bout qui incluent plusieurs opérations impliquant plusieurs microservices nécessitent le déploiement et le démarrage de l’application entière dans l’hôte Docker, par l’exécution de docker-compose (ou d’un mécanisme comparable si vous utilisez un orchestrateur).</span><span class="sxs-lookup"><span data-stu-id="1b477-163">End-to-end service tests that include multiple operations involving several microservices require you to deploy and start the whole application in the Docker host by running docker-compose up (or a comparable mechanism if you are using an orchestrator).</span></span> <span data-ttu-id="1b477-164">Une fois que l’application entière et tous ses services sont exécutés, vous pouvez exécuter des tests d’intégration et des tests fonctionnels de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="1b477-164">Once the whole application and all its services is running, you can execute end-to-end integration and functional tests.</span></span>

<span data-ttu-id="1b477-165">Il existe pour cela plusieurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="1b477-165">There are a few approaches you can use.</span></span> <span data-ttu-id="1b477-166">Dans le fichier docker-compose.yml que vous utilisez pour déployer l’application (ou un fichier similaire tel que docker-compose.ci.build.yml), au niveau de la solution, vous pouvez développer le point d’entrée pour utiliser la commande [dotnet test](../../../core/tools/dotnet-test.md).</span><span class="sxs-lookup"><span data-stu-id="1b477-166">In the docker-compose.yml file that you use to deploy the application (or similar ones, like docker-compose.ci.build.yml), at the solution level you can expand the entry point to use [dotnet test](../../../core/tools/dotnet-test.md).</span></span> <span data-ttu-id="1b477-167">Vous pouvez également utiliser un autre fichier Compose pour exécuter vos tests dans l’image que vous ciblez.</span><span class="sxs-lookup"><span data-stu-id="1b477-167">You can also use another compose file that would run your tests in the image you are targeting.</span></span> <span data-ttu-id="1b477-168">En utilisant un autre fichier Compose pour les tests d’intégration comprenant vos microservices et vos bases de données dans des conteneurs, vous pouvez être sûr que les données associées sont toujours réinitialisées à leur état d’origine avant d’exécuter les tests.</span><span class="sxs-lookup"><span data-stu-id="1b477-168">By using another compose file for integration tests that includes your microservices and databases on containers, you can make sure that the related data is always reset to its original state before running the tests.</span></span>

<span data-ttu-id="1b477-169">Une fois que l’application Compose est fonctionnelle, vous pouvez tirer parti des points d’arrêt et des exceptions si vous exécutez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1b477-169">Once the compose application is up and running, you can take advantage of breakpoints and exceptions if you are running Visual Studio.</span></span> <span data-ttu-id="1b477-170">Vous pouvez également exécuter les tests d’intégration automatiquement dans votre pipeline d’intégration continue dans Visual Studio Team Services, ou dans un autre système d’intégration ou de livraison continue prenant en charge les conteneurs Docker.</span><span class="sxs-lookup"><span data-stu-id="1b477-170">Or you can run the integration tests automatically in your CI pipeline in Visual Studio Team Services or any other CI/CD system that supports Docker containers.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="1b477-171">[précédent] (subscribe-events.md) [suivant] (../microservice-ddd-cqrs-patterns/index.md)</span><span class="sxs-lookup"><span data-stu-id="1b477-171">[Previous] (subscribe-events.md) [Next] (../microservice-ddd-cqrs-patterns/index.md)</span></span>
