---
title: "À propos de l’autorisation dans les microservices .NET et les applications web"
description: "Architecture de microservices .NET pour les applications .NET en conteneur | À propos de l’autorisation dans les microservices .NET et les applications web"
keywords: Docker, microservices, ASP.NET, conteneur
author: mjrousos
ms.author: wiwagn
ms.date: 05/26/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 6cd7be9bc8216aecf85f99a76e859b411a8735b0
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="about-authorization-in-net-microservices-and-web-applications"></a>À propos de l’autorisation dans les microservices .NET et les applications web

Après l’authentification, les API web ASP.NET Core doivent autoriser l’accès. Ce processus permet à un service de mettre les API à la disposition de certains utilisateurs authentifiés, mais pas tous. L’[autorisation](https://docs.microsoft.com/aspnet/core/security/authorization/introduction) peut être basée sur les rôles des utilisateurs ou sur une stratégie personnalisée, ce qui peut-être impliquer l’inspection de revendications ou d’autres méthodes heuristiques.

Il est tout aussi facile de restreindre l’accès à un itinéraire ASP.NET MVC que d’appliquer un attribut Authorize à la méthode d’action (ou à la classe du contrôleur si toutes les actions du contrôleur nécessitent une autorisation), comme dans l’exemple suivant :

```csharp
public class AccountController : Controller
{
    public ActionResult Login()
    {
    }

    [Authorize]
    public ActionResult Logout()
    {
    }
}
```

Par défaut, l’ajout d’un attribut Authorize sans paramètres limite l’accès aux utilisateurs authentifiés pour le contrôleur ou l’action en question. Pour limiter un peu plus l’accès à un API à certains utilisateurs, l’attribut peut être étendu pour spécifier les rôles ou les stratégies que les utilisateurs doivent obligatoirement satisfaire.

## <a name="implementing-role-based-authorization"></a>Implémentation d’une autorisation basée sur les rôles

L’identité ASP.NET Core intègre un concept de rôles. En plus des utilisateurs, l’identité ASP.NET Core stocke des informations sur les différents rôles utilisés par l’application et assure le suivi des utilisateurs et des rôles qui leur sont attribués. Ces attributions peuvent être modifiées par programmation avec le type RoleManager (qui met à jour les rôles dans le stockage persistant) et le type UserManager (qui peut attribuer des rôles aux utilisateurs ou les leur supprimer).

Si vous vous authentifiez avec des jetons de porteur JSON, l’intergiciel (middleware) d’authentification du porteur JWT ASP.NET Core remplira les rôles des utilisateurs en fonction des revendications de rôle trouvées dans le jeton. Pour limiter l’accès à une action ou à un contrôleur MVC aux seuls utilisateurs ayant un rôle déterminé, vous pouvez inclure un paramètre Roles dans l’en-tête Authorize, comme dans l’exemple suivant :

```csharp
[Authorize(Roles = "Administrator, PowerUser")]
public class ControlPanelController : Controller
{
    public ActionResult SetTime()
    {
    }

    [Authorize(Roles = "Administrator")]
    public ActionResult ShutDown()
    {
    }
}
```

Dans cet exemple, seuls les utilisateurs appartenant aux rôles Administrator ou PowerUser peuvent accéder aux API dans le contrôleur ControlPanel (comme l’exécution de l’action SetTime). L’API ShutDown est soumise à des restrictions plus contraignantes puisque seuls les utilisateurs appartenant au rôle Administrator peuvent y accéder.

Pour exiger qu’un utilisateur appartienne à plusieurs rôles, vous devez utiliser plusieurs attributs Authorize, comme dans l’exemple suivant :

```csharp
[Authorize(Roles = "Administrator, PowerUser")]
[Authorize(Roles = "RemoteEmployee ")]
[Authorize(Policy = "CustomPolicy")]
public ActionResult API1 ()
{
}
```

Dans cet exemple, pour appeler API1, un utilisateur doit :

-   appartenir au rôle Administrator *ou* PowerUser, *et*

-   appartenir au rôle RemoteEmployee, *et*

-   satisfaire un gestionnaire personnalisé pour l’autorisation CustomPolicy.

## <a name="implementing-policy-based-authorization"></a>Implémentation d’une autorisation basée sur une stratégie

Des règles d’autorisation personnalisées peuvent aussi être écrites au moyen de [stratégies d’autorisation](https://docs.asp.net/en/latest/security/authorization/policies.html). Dans cette section, nous vous fournissons une vue d’ensemble. Vous trouverez davantage de détails à la page [ASP.NET Authorization Workshop](https://github.com/blowdart/AspNetAuthorizationWorkshop).

Les stratégies d’autorisation personnalisées sont inscrites dans la méthode Startup.ConfigureServices via la méthode service.AddAuthorization. Cette méthode prend un délégué qui configure un argument AuthorizationOptions.

```csharp
services.AddAuthorization(options =>
{
    options.AddPolicy("AdministratorsOnly", policy =>
        policy.RequireRole("Administrator"));
    options.AddPolicy("EmployeesOnly", policy =>
        policy.RequireClaim("EmployeeNumber"));
    options.AddPolicy("Over21", policy =>
        policy.Requirements.Add(new MinimumAgeRequirement(21)));
});
```

Comme le montre l’exemple, les stratégies peuvent être associées à différents types de conditions. Une fois inscrites, les stratégies peuvent être appliquées à une action ou un contrôleur en passant le nom de la stratégie en tant qu’argument Policy de l’attribut Authorize (par exemple, \[Authorize(Policy="EmployeesOnly")\]). Les stratégies peuvent être assorties d’un grand nombre de conditions, mais pas qu’une seule (comme le montrent ces exemples).

Dans l’exemple précédent, le premier appel AddPolicy est simplement une autre façon d’autoriser par rôle. Si \[Authorize(Policy="AdministratorsOnly")\] est appliqué à une API, seuls les utilisateurs du rôle Administrator peuvent y accéder.

Le deuxième appel AddPolicy présente une façon simple d’exiger la présence d’une revendication précise pour l’utilisateur. La méthode RequireClaim peut aussi prendre les valeurs attendues de la revendication. Si des valeurs sont spécifiées, la condition n’est remplie que si l’utilisateur dispose d’une revendication du type approprié et de l’une des valeurs spécifiées. Si vous utilisez l’intergiciel d’authentification du porteur JSON, toutes les propriétés JWT sont accessibles en tant que revendications d’utilisateur.

Parmi les stratégies présentées ici, la plus intéressante est celle qui se trouve dans la troisième méthode AddPolicy, car elle utilise une condition d’autorisation personnalisée. Le fait d’utiliser des conditions d’autorisation personnalisées vous permet de mieux contrôler la façon dont s’exerce l’autorisation. Pour que cela fonctionne, vous devez implémenter les types suivants :

-   Un type Requirements qui dérive d’IAuthorizationRequirement et qui contient des champs spécifiant les détails de la condition. Dans l’exemple, il s’agit d’un champ d’âge pour l’exemple de type MinimumAgeRequirement.

-   Un gestionnaire qui implémente AuthorizationHandler&lt;T&gt;, T étant le type d’IAuthorizationRequirement que le gestionnaire peut satisfaire. Le gestionnaire doit implémenter la méthode HandleRequirementAsync, qui vérifie si un contexte spécifié contenant des informations sur l’utilisateur satisfait la condition.

Si l’utilisateur remplit la condition, un appel à context.Succeed indique que l’utilisateur est autorisé. Si un utilisateur peut satisfaire une condition d’autorisation de différentes manières, plusieurs gestionnaires peuvent être créés.

En plus de la nécessité d’inscrire des conditions de stratégie personnalisée avec des appels AddPolicy, vous devez aussi inscrire des gestionnaires de conditions personnalisés via l’injection de dépendance (services.AddTransient&lt;IAuthorizationHandler, MinimumAgeHandler&gt;()).

Un exemple de condition d’autorisation personnalisée et de gestionnaire destiné à vérifier l’âge d’un utilisateur (en fonction d’une revendication DateOfBirth) est disponible dans la [documentation traitant de l’autorisation](https://docs.asp.net/en/latest/security/authorization/policies.html) ASP.NET Core.

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Authentification ASP.NET Core**
    [*https://docs.microsoft.com/aspnet/core/security/authentication/identity*](https://docs.microsoft.com/aspnet/core/security/authentication/identity)

-   **Autorisation ASP.NET Core**
    [*https://docs.microsoft.com/aspnet/core/security/authorization/introduction*](https://docs.microsoft.com/aspnet/core/security/authorization/introduction)

-   **Autorisation basée sur les rôles**
    [*https://docs.microsoft.com/aspnet/core/security/authorization/roles*](https://docs.microsoft.com/aspnet/core/security/authorization/roles)

-   **Autorisation basée sur la stratégie personnalisée**
    [*https://docs.microsoft.com/aspnet/core/security/authorization/policies*](https://docs.microsoft.com/aspnet/core/security/authorization/policies)




>[!div class="step-by-step"]
[Précédent] (index.md) [Suivant] (developer-app-secrets-storage.md)
