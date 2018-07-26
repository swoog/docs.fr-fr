---
title: Test d’applications web et de services ASP.NET Core
description: Architecture des microservices .NET pour les applications .NET en conteneur | Test d’applications web et de services ASP.NET Core
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 12/11/2017
ms.openlocfilehash: f7bd75ecdd85e49524ccdf67f3e59aa4be46bdce
ms.sourcegitcommit: 702d5ffc6e733b6c4ded85bf1c92e2293638ee9a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/04/2018
ms.locfileid: "37792411"
---
# <a name="testing-aspnet-core-services-and-web-apps"></a>Test d’applications web et de services ASP.NET Core

Les contrôleurs constituent l’élément central des services d’API ASP.NET Core et des applications web ASP.NET MVC. Par conséquent, vous devez être sûr qu’ils vont se comporter comme prévu avec votre application. Les tests automatisés peuvent vous donner cette confiance et détecter des erreurs avant la mise en production.

Vous devez tester le comportement du contrôleur avec les entrées valides et non valides, ainsi que les réponses du contrôleur en fonction du résultat de l’opération qu’il effectue. Toutefois, vous devez effectuer ces types de tests pour vos microservices :

-   Tests unitaires. Ces tests permettent de vérifier que les composants de l’application fonctionnent comme prévu. Les assertions testent l’API des composants.

-   Tests d’intégration. Ces tests permettent de vérifier que les interactions entre composants fonctionnent comme prévu, en se basant sur des artefacts externes comme les bases de données. Les assertions peuvent tester l’API des composants, l’interface utilisateur ou les effets secondaires des actions telles que les E/S de base de données, la journalisation, etc.

-   Tests fonctionnels pour chaque microservice. Ces tests permettent de vérifier que l’application fonctionne comme prévu du point de vue de l’utilisateur.

-   Tests de service. Ces tests permettent de garantir que les cas d’usage de service de bout en bout (y compris l’exécution simultanée de plusieurs services) sont testés. Pour ce type de test, vous devez d’abord préparer l’environnement. Dans ce cas, cela signifie démarrer les services (à l’aide de docker-composer, par exemple).

### <a name="implementing-unit-tests-for-aspnet-core-web-apis"></a>Implémentation des tests unitaires pour les API web ASP.NET Core

Les tests unitaires impliquent le test d’une partie d’une application de façon isolée, par rapport à son infrastructure et à ses dépendances. Lors du test de la logique d’un contrôleur, seul le contenu d’une action ou d’une méthode est testé, et non pas le comportement de ses dépendances ou du framework lui-même. Les tests unitaires ne détectent pas les problèmes d’interaction entre les composants, qui sont l’objet des tests d’intégration.

Quand vous procédez à des tests unitaires pour les actions de votre contrôleur, concentrez-vous uniquement sur leur comportement. Les tests unitaires d’un contrôleur évitent les éléments tels que les filtres, le routage ou la liaison de données. Comme ils ne s’occupent que d’un seul objet à la fois, les tests unitaires sont généralement simples à écrire et rapides à exécuter. Un ensemble de tests unitaires bien écrits peut être exécuté fréquemment sans engendrer une surcharge importante.

Les tests unitaires sont implémentés selon les frameworks de tests comme xUnit.net, MSTest, Moq ou NUnit. Pour l’exemple d’application eShopOnContainers, nous utilisons XUnit.

Lorsque vous écrivez un test unitaire pour un contrôleur d’API web, vous instanciez la classe de contrôleur directement à l’aide du mot clé new dans du code C\#, pour que le test s’exécute aussi rapidement que possible. L’exemple suivant montre comment effectuer cette opération lorsque vous utilisez [XUnit](https://xunit.github.io/) comme framework de tests.

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

### <a name="implementing-integration-and-functional-tests-for-each-microservice"></a>Implémentation de tests d’intégration et de tests fonctionnels pour chaque microservice

Comme mentionné précédemment, les tests d’intégration et les tests fonctionnels ont des objectifs différents. Toutefois, leur implémentation est similaire lorsque vous testez les contrôleurs ASP.NET Core. Cette section se concentre donc sur les tests d’intégration.

Les tests d’intégration permettent de vérifier que les composants d’une application fonctionnent correctement une fois assemblés. ASP.NET Core prend en charge les tests d’intégration à l’aide des frameworks de tests unitaires et d’un hôte web de test intégré qui peut être utilisé pour gérer les requêtes, sans surcharger le réseau.

Contrairement aux tests unitaires, les tests d’intégration rencontrent souvent des problèmes d’infrastructure d’application, liés par exemple, aux bases de données, aux systèmes de fichiers, aux ressources réseau ou aux requêtes et réponses web. Les tests unitaires utilisent des fakes ou objets fictifs pour éviter de tels problèmes. Toutefois, l’objectif des tests d’intégration est de vérifier que le système fonctionne comme prévu avec ces systèmes. Par conséquent, pour les tests d’intégration, vous ne devez pas utiliser de fakes ou d’objets fictifs. Vous devez inclure l’infrastructure, comme l’accès de base de données ou l’appel de service, des autres services.

Étant donné que les tests d’intégration utilisent de plus grands segments de code que les tests unitaires, et comme les tests d’intégration reposent sur des éléments d’infrastructure, ils ont tendance à être beaucoup plus lents que les tests unitaires. Par conséquent, il est conseillé de limiter le nombre de tests d’intégration que vous écrivez et exécutez.

ASP.NET Core inclut un web hôte de test intégré qui peut être utilisé pour gérer les requêtes HTTP sans surcharger le réseau. Vous pouvez donc exécuter ces tests plus rapidement lorsque vous utilisez un hôte web réel. L’hôte web de test est disponible dans un composant NuGet, sous le nom de Microsoft.AspNetCore.TestHost. Il peut être ajouté aux projets de test d’intégration et utilisé pour héberger les applications ASP.NET Core.

Comme vous pouvez le voir dans le code suivant, lorsque vous créez des tests d’intégration pour des contrôleurs ASP.NET Core, vous instanciez les contrôleurs via l’hôte de test. Ceci est comparable à une requête HTTP, avec toutefois, une exécution plus rapide.

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

#### <a name="additional-resources"></a>Ressources supplémentaires

-   **Steve Smith. Test des contrôleurs** (ASP.NET Core) [*https://docs.microsoft.com/aspnet/core/mvc/controllers/testing*](/aspnet/core/mvc/controllers/testing)

-   **Steve Smith. Tests d’intégration**  (ASP.NET Core) [*https://docs.microsoft.com/aspnet/core/test/integration-tests*](/aspnet/core/test/integration-tests)

-   **Effectuer des tests unitaires dans .NET Core à l’aide de dotnet test**
    [*https://docs.microsoft.com/dotnet/core/testing/unit-testing-with-dotnet-test*](../../../core/testing/unit-testing-with-dotnet-test.md)

-   **xUnit.net**. Site officiel.
    [*https://xunit.github.io/*](https://xunit.github.io/)

-   **Concepts de base des tests unitaires**
    [*https://msdn.microsoft.com/library/hh694602.aspx*](https://msdn.microsoft.com/library/hh694602.aspx)

-   **Moq**. Dépôt GitHub
    [*https://github.com/moq/moq*](https://github.com/moq/moq)

-   **NUnit**. Site officiel.
    [*https://www.nunit.org/*](https://www.nunit.org/)

### <a name="implementing-service-tests-on-a-multi-container-application"></a>Implémentation de tests de service dans une application à plusieurs conteneurs 

Comme mentionné précédemment, lorsque vous testez des applications à plusieurs conteneurs, tous les microservices doivent être exécutés au sein de l’hôte Docker ou du cluster de conteneurs. Les tests de service de bout en bout qui incluent plusieurs opérations impliquant plusieurs microservices nécessitent le déploiement et le démarrage de l’application entière dans l’hôte Docker, par l’exécution de docker-compose (ou d’un mécanisme comparable si vous utilisez un orchestrateur). Une fois que l’application entière et tous ses services sont exécutés, vous pouvez exécuter des tests d’intégration et des tests fonctionnels de bout en bout.

Il existe pour cela plusieurs méthodes. Dans le fichier docker-compose.yml que vous utilisez pour déployer l’application (ou un fichier similaire tel que docker-compose.ci.build.yml), au niveau de la solution, vous pouvez développer le point d’entrée pour utiliser la commande [dotnet test](../../../core/tools/dotnet-test.md). Vous pouvez également utiliser un autre fichier Compose pour exécuter vos tests dans l’image que vous ciblez. En utilisant un autre fichier Compose pour les tests d’intégration comprenant vos microservices et vos bases de données dans des conteneurs, vous pouvez être sûr que les données associées sont toujours réinitialisées à leur état d’origine avant d’exécuter les tests.

Une fois que l’application Compose est fonctionnelle, vous pouvez tirer parti des points d’arrêt et des exceptions si vous exécutez Visual Studio. Vous pouvez également exécuter les tests d’intégration automatiquement dans votre pipeline d’intégration continue dans Visual Studio Team Services, ou dans un autre système d’intégration ou de livraison continue prenant en charge les conteneurs Docker.

>[!div class="step-by-step"]
[Précédent](subscribe-events.md)
[Suivant](../microservice-ddd-cqrs-patterns/index.md)
