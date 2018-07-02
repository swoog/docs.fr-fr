---
title: À propos de l’autorisation dans les microservices .NET et les applications web
description: Architecture de microservices .NET pour les applications .NET en conteneur | À propos de l’autorisation dans les microservices .NET et les applications web
author: mjrousos
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 7b2981579f28c083a31d7af6ae42f4e3ca8bbd88
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37105499"
---
# <a name="about-authorization-in-net-microservices-and-web-applications"></a><span data-ttu-id="c2a42-103">À propos de l’autorisation dans les microservices .NET et les applications web</span><span class="sxs-lookup"><span data-stu-id="c2a42-103">About authorization in .NET microservices and web applications</span></span>

<span data-ttu-id="c2a42-104">Après l’authentification, les API web ASP.NET Core doivent autoriser l’accès.</span><span class="sxs-lookup"><span data-stu-id="c2a42-104">After authentication, ASP.NET Core Web APIs need to authorize access.</span></span> <span data-ttu-id="c2a42-105">Ce processus permet à un service de mettre les API à la disposition de certains utilisateurs authentifiés, mais pas tous.</span><span class="sxs-lookup"><span data-stu-id="c2a42-105">This process allows a service to make APIs available to some authenticated users, but not to all.</span></span> <span data-ttu-id="c2a42-106">L’[autorisation](https://docs.microsoft.com/aspnet/core/security/authorization/introduction) peut être basée sur les rôles des utilisateurs ou sur une stratégie personnalisée, ce qui peut-être impliquer l’inspection de revendications ou d’autres méthodes heuristiques.</span><span class="sxs-lookup"><span data-stu-id="c2a42-106">[Authorization](https://docs.microsoft.com/aspnet/core/security/authorization/introduction) can be done based on users’ roles or based on custom policy, which might include inspecting claims or other heuristics.</span></span>

<span data-ttu-id="c2a42-107">Il est tout aussi facile de restreindre l’accès à un itinéraire ASP.NET MVC que d’appliquer un attribut Authorize à la méthode d’action (ou à la classe du contrôleur si toutes les actions du contrôleur nécessitent une autorisation), comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c2a42-107">Restricting access to an ASP.NET Core MVC route is as easy as applying an Authorize attribute to the action method (or to the controller’s class if all the controller’s actions require authorization), as shown in following example:</span></span>

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

<span data-ttu-id="c2a42-108">Par défaut, l’ajout d’un attribut Authorize sans paramètres limite l’accès aux utilisateurs authentifiés pour le contrôleur ou l’action en question.</span><span class="sxs-lookup"><span data-stu-id="c2a42-108">By default, adding an Authorize attribute without parameters will limit access to authenticated users for that controller or action.</span></span> <span data-ttu-id="c2a42-109">Pour limiter un peu plus l’accès à un API à certains utilisateurs, l’attribut peut être étendu pour spécifier les rôles ou les stratégies que les utilisateurs doivent obligatoirement satisfaire.</span><span class="sxs-lookup"><span data-stu-id="c2a42-109">To further restrict an API to be available for only specific users, the attribute can be expanded to specify required roles or policies that users must satisfy.</span></span>

## <a name="implementing-role-based-authorization"></a><span data-ttu-id="c2a42-110">Implémentation d’une autorisation basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="c2a42-110">Implementing role-based authorization</span></span>

<span data-ttu-id="c2a42-111">L’identité ASP.NET Core intègre un concept de rôles.</span><span class="sxs-lookup"><span data-stu-id="c2a42-111">ASP.NET Core Identity has a built-in concept of roles.</span></span> <span data-ttu-id="c2a42-112">En plus des utilisateurs, l’identité ASP.NET Core stocke des informations sur les différents rôles utilisés par l’application et assure le suivi des utilisateurs et des rôles qui leur sont attribués.</span><span class="sxs-lookup"><span data-stu-id="c2a42-112">In addition to users, ASP.NET Core Identity stores information about different roles used by the application and keeps track of which users are assigned to which roles.</span></span> <span data-ttu-id="c2a42-113">Ces attributions peuvent être modifiées par programmation avec le type RoleManager (qui met à jour les rôles dans le stockage persistant) et le type UserManager (qui peut attribuer des rôles aux utilisateurs ou les leur supprimer).</span><span class="sxs-lookup"><span data-stu-id="c2a42-113">These assignments can be changed programmatically with the RoleManager type (which updates roles in persisted storage) and UserManager type (which can assign or unassign users from roles).</span></span>

<span data-ttu-id="c2a42-114">Si vous vous authentifiez avec des jetons de porteur JSON, l’intergiciel (middleware) d’authentification du porteur JWT ASP.NET Core remplira les rôles des utilisateurs en fonction des revendications de rôle trouvées dans le jeton.</span><span class="sxs-lookup"><span data-stu-id="c2a42-114">If you are authenticating with JWT bearer tokens, the ASP.NET Core JWT bearer authentication middleware will populate a user’s roles based on role claims found in the token.</span></span> <span data-ttu-id="c2a42-115">Pour limiter l’accès à une action ou à un contrôleur MVC aux seuls utilisateurs ayant un rôle déterminé, vous pouvez inclure un paramètre Roles dans l’en-tête Authorize, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c2a42-115">To limit access to an MVC action or controller to users in specific roles, you can include a Roles parameter in the Authorize header, as shown in the following example:</span></span>

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

<span data-ttu-id="c2a42-116">Dans cet exemple, seuls les utilisateurs appartenant aux rôles Administrator ou PowerUser peuvent accéder aux API dans le contrôleur ControlPanel (comme l’exécution de l’action SetTime).</span><span class="sxs-lookup"><span data-stu-id="c2a42-116">In this example, only users in the Administrator or PowerUser roles can access APIs in the ControlPanel controller (such as executing the SetTime action).</span></span> <span data-ttu-id="c2a42-117">L’API ShutDown est soumise à des restrictions plus contraignantes puisque seuls les utilisateurs appartenant au rôle Administrator peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="c2a42-117">The ShutDown API is further restricted to allow access only to users in the Administrator role.</span></span>

<span data-ttu-id="c2a42-118">Pour exiger qu’un utilisateur appartienne à plusieurs rôles, vous devez utiliser plusieurs attributs Authorize, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c2a42-118">To require a user be in multiple roles, you use multiple Authorize attributes, as shown in the following example:</span></span>

```csharp
[Authorize(Roles = "Administrator, PowerUser")]
[Authorize(Roles = "RemoteEmployee ")]
[Authorize(Policy = "CustomPolicy")]
public ActionResult API1 ()
{
}
```

<span data-ttu-id="c2a42-119">Dans cet exemple, pour appeler API1, un utilisateur doit :</span><span class="sxs-lookup"><span data-stu-id="c2a42-119">In this example, to call API1, a user must:</span></span>

-   <span data-ttu-id="c2a42-120">appartenir au rôle Administrator *ou* PowerUser, *et*</span><span class="sxs-lookup"><span data-stu-id="c2a42-120">Be in the Adminstrator *or* PowerUser role, *and*</span></span>

-   <span data-ttu-id="c2a42-121">appartenir au rôle RemoteEmployee, *et*</span><span class="sxs-lookup"><span data-stu-id="c2a42-121">Be in the RemoteEmployee role, *and*</span></span>

-   <span data-ttu-id="c2a42-122">satisfaire un gestionnaire personnalisé pour l’autorisation CustomPolicy.</span><span class="sxs-lookup"><span data-stu-id="c2a42-122">Satisfy a custom handler for CustomPolicy authorization.</span></span>

## <a name="implementing-policy-based-authorization"></a><span data-ttu-id="c2a42-123">Implémentation d’une autorisation basée sur une stratégie</span><span class="sxs-lookup"><span data-stu-id="c2a42-123">Implementing policy-based authorization</span></span>

<span data-ttu-id="c2a42-124">Des règles d’autorisation personnalisées peuvent aussi être écrites au moyen de [stratégies d’autorisation](https://docs.asp.net/en/latest/security/authorization/policies.html).</span><span class="sxs-lookup"><span data-stu-id="c2a42-124">Custom authorization rules can also be written using [authorization policies](https://docs.asp.net/en/latest/security/authorization/policies.html).</span></span> <span data-ttu-id="c2a42-125">Dans cette section, nous vous fournissons une vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="c2a42-125">In this section we provide an overview.</span></span> <span data-ttu-id="c2a42-126">Vous trouverez davantage de détails à la page [ASP.NET Authorization Workshop](https://github.com/blowdart/AspNetAuthorizationWorkshop).</span><span class="sxs-lookup"><span data-stu-id="c2a42-126">More detail is available in the online [ASP.NET Authorization Workshop](https://github.com/blowdart/AspNetAuthorizationWorkshop).</span></span>

<span data-ttu-id="c2a42-127">Les stratégies d’autorisation personnalisées sont inscrites dans la méthode Startup.ConfigureServices via la méthode service.AddAuthorization.</span><span class="sxs-lookup"><span data-stu-id="c2a42-127">Custom authorization policies are registered in the Startup.ConfigureServices method using the service.AddAuthorization method.</span></span> <span data-ttu-id="c2a42-128">Cette méthode prend un délégué qui configure un argument AuthorizationOptions.</span><span class="sxs-lookup"><span data-stu-id="c2a42-128">This method takes a delegate that configures an AuthorizationOptions argument.</span></span>

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

<span data-ttu-id="c2a42-129">Comme le montre l’exemple, les stratégies peuvent être associées à différents types de conditions.</span><span class="sxs-lookup"><span data-stu-id="c2a42-129">As shown in the example, policies can be associated with different types of requirements.</span></span> <span data-ttu-id="c2a42-130">Une fois inscrites, les stratégies peuvent être appliquées à une action ou un contrôleur en passant le nom de la stratégie en tant qu’argument Policy de l’attribut Authorize (par exemple, \[Authorize(Policy="EmployeesOnly")\]). Les stratégies peuvent être assorties d’un grand nombre de conditions, mais pas qu’une seule (comme le montrent ces exemples).</span><span class="sxs-lookup"><span data-stu-id="c2a42-130">After the policies are registered, they can be applied to an action or controller by passing the policy’s name as the Policy argument of the Authorize attribute (for example, \[Authorize(Policy="EmployeesOnly")\]) Policies can have multiple requirements, not just one (as shown in these examples).</span></span>

<span data-ttu-id="c2a42-131">Dans l’exemple précédent, le premier appel AddPolicy est simplement une autre façon d’autoriser par rôle.</span><span class="sxs-lookup"><span data-stu-id="c2a42-131">In the previous example, the first AddPolicy call is just an alternative way of authorizing by role.</span></span> <span data-ttu-id="c2a42-132">Si \[Authorize(Policy="AdministratorsOnly")\] est appliqué à une API, seuls les utilisateurs du rôle Administrator peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="c2a42-132">If \[Authorize(Policy="AdministratorsOnly")\] is applied to an API, only users in the Administrator role will be able to access it.</span></span>

<span data-ttu-id="c2a42-133">Le deuxième appel AddPolicy présente une façon simple d’exiger la présence d’une revendication précise pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2a42-133">The second AddPolicy call demonstrates an easy way to require that a particular claim should be present for the user.</span></span> <span data-ttu-id="c2a42-134">La méthode RequireClaim peut aussi prendre les valeurs attendues de la revendication.</span><span class="sxs-lookup"><span data-stu-id="c2a42-134">The RequireClaim method also optionally takes expected values for the claim.</span></span> <span data-ttu-id="c2a42-135">Si des valeurs sont spécifiées, la condition n’est remplie que si l’utilisateur dispose d’une revendication du type approprié et de l’une des valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="c2a42-135">If values are specified, the requirement is met only if the user has both a claim of the correct type and one of the specified values.</span></span> <span data-ttu-id="c2a42-136">Si vous utilisez l’intergiciel d’authentification du porteur JSON, toutes les propriétés JWT sont accessibles en tant que revendications d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2a42-136">If you are using the JWT bearer authentication middleware, all JWT properties will be available as user claims.</span></span>

<span data-ttu-id="c2a42-137">Parmi les stratégies présentées ici, la plus intéressante est celle qui se trouve dans la troisième méthode AddPolicy, car elle utilise une condition d’autorisation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c2a42-137">The most interesting policy shown here is in the third AddPolicy method, because it uses a custom authorization requirement.</span></span> <span data-ttu-id="c2a42-138">Le fait d’utiliser des conditions d’autorisation personnalisées vous permet de mieux contrôler la façon dont s’exerce l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="c2a42-138">By using custom authorization requirements, you can have a great deal of control over how authorization is performed.</span></span> <span data-ttu-id="c2a42-139">Pour que cela fonctionne, vous devez implémenter les types suivants :</span><span class="sxs-lookup"><span data-stu-id="c2a42-139">For this to work, you must implement these types:</span></span>

-   <span data-ttu-id="c2a42-140">Un type Requirements qui dérive d’IAuthorizationRequirement et qui contient des champs spécifiant les détails de la condition.</span><span class="sxs-lookup"><span data-stu-id="c2a42-140">A Requirements type that derives from IAuthorizationRequirement and that contains fields specifying the details of the requirement.</span></span> <span data-ttu-id="c2a42-141">Dans l’exemple, il s’agit d’un champ d’âge pour l’exemple de type MinimumAgeRequirement.</span><span class="sxs-lookup"><span data-stu-id="c2a42-141">In the example, this is an age field for the sample MinimumAgeRequirement type.</span></span>

-   <span data-ttu-id="c2a42-142">Un gestionnaire qui implémente AuthorizationHandler&lt;T&gt;, T étant le type d’IAuthorizationRequirement que le gestionnaire peut satisfaire.</span><span class="sxs-lookup"><span data-stu-id="c2a42-142">A handler that implements AuthorizationHandler&lt;T&gt;, where T is the type of IAuthorizationRequirement that the handler can satisfy.</span></span> <span data-ttu-id="c2a42-143">Le gestionnaire doit implémenter la méthode HandleRequirementAsync, qui vérifie si un contexte spécifié contenant des informations sur l’utilisateur satisfait la condition.</span><span class="sxs-lookup"><span data-stu-id="c2a42-143">The handler must implement the HandleRequirementAsync method, which checks whether a specified context that contains information about the user satisfies the requirement.</span></span>

<span data-ttu-id="c2a42-144">Si l’utilisateur remplit la condition, un appel à context.Succeed indique que l’utilisateur est autorisé.</span><span class="sxs-lookup"><span data-stu-id="c2a42-144">If the user meets the requirement, a call to context.Succeed will indicate that the user is authorized.</span></span> <span data-ttu-id="c2a42-145">Si un utilisateur peut satisfaire une condition d’autorisation de différentes manières, plusieurs gestionnaires peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="c2a42-145">If there are multiple ways that a user might satisfy an authorization requirement, multiple handlers can be created.</span></span>

<span data-ttu-id="c2a42-146">En plus de la nécessité d’inscrire des conditions de stratégie personnalisée avec des appels AddPolicy, vous devez aussi inscrire des gestionnaires de conditions personnalisés via l’injection de dépendance (services.AddTransient&lt;IAuthorizationHandler, MinimumAgeHandler&gt;()).</span><span class="sxs-lookup"><span data-stu-id="c2a42-146">In addition to registering custom policy requirements with AddPolicy calls, you also need to register custom requirement handlers via Dependency Injection (services.AddTransient&lt;IAuthorizationHandler, MinimumAgeHandler&gt;()).</span></span>

<span data-ttu-id="c2a42-147">Un exemple de condition d’autorisation personnalisée et de gestionnaire destiné à vérifier l’âge d’un utilisateur (en fonction d’une revendication DateOfBirth) est disponible dans la [documentation traitant de l’autorisation](https://docs.asp.net/en/latest/security/authorization/policies.html) ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="c2a42-147">An example of a custom authorization requirement and handler for checking a user’s age (based on a DateOfBirth claim) is available in the ASP.NET Core [authorization documentation](https://docs.asp.net/en/latest/security/authorization/policies.html).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2a42-148">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c2a42-148">Additional resources</span></span>

-   <span data-ttu-id="c2a42-149">**Authentification dans ASP.NET Core**
    [*https://docs.microsoft.com/aspnet/core/security/authentication/identity*](https://docs.microsoft.com/aspnet/core/security/authentication/identity)</span><span class="sxs-lookup"><span data-stu-id="c2a42-149">**ASP.NET Core Authentication**
[*https://docs.microsoft.com/aspnet/core/security/authentication/identity*](https://docs.microsoft.com/aspnet/core/security/authentication/identity)</span></span>

-   <span data-ttu-id="c2a42-150">**Autorisation dans ASP.NET Core**
    [*https://docs.microsoft.com/aspnet/core/security/authorization/introduction*](https://docs.microsoft.com/aspnet/core/security/authorization/introduction)</span><span class="sxs-lookup"><span data-stu-id="c2a42-150">**ASP.NET Core Authorization**
[*https://docs.microsoft.com/aspnet/core/security/authorization/introduction*](https://docs.microsoft.com/aspnet/core/security/authorization/introduction)</span></span>

-   <span data-ttu-id="c2a42-151">**Autorisation basée sur les rôles**
    [*https://docs.microsoft.com/aspnet/core/security/authorization/roles*](https://docs.microsoft.com/aspnet/core/security/authorization/roles)</span><span class="sxs-lookup"><span data-stu-id="c2a42-151">**Role based Authorization**
[*https://docs.microsoft.com/aspnet/core/security/authorization/roles*](https://docs.microsoft.com/aspnet/core/security/authorization/roles)</span></span>

-   <span data-ttu-id="c2a42-152">**Autorisation basée sur une stratégie personnalisée**
    [*https://docs.microsoft.com/aspnet/core/security/authorization/policies*](https://docs.microsoft.com/aspnet/core/security/authorization/policies)</span><span class="sxs-lookup"><span data-stu-id="c2a42-152">**Custom Policy-Based Authorization**
[*https://docs.microsoft.com/aspnet/core/security/authorization/policies*](https://docs.microsoft.com/aspnet/core/security/authorization/policies)</span></span>




>[!div class="step-by-step"]
<span data-ttu-id="c2a42-153">[Précédent](index.md)
[Suivant](developer-app-secrets-storage.md)</span><span class="sxs-lookup"><span data-stu-id="c2a42-153">[Previous](index.md)
[Next](developer-app-secrets-storage.md)</span></span>
