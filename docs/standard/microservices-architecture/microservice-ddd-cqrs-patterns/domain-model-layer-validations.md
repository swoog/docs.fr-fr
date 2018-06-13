---
title: Conception de validations dans la couche de modèle de domaine
description: Architecture des microservices .NET pour les applications .NET en conteneur | Conception de validations dans la couche de modèle de domaine
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: ce3cb0c79cbd492224ce1d4ecb25cd02062f11cd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33578948"
---
# <a name="designing-validations-in-the-domain-model-layer"></a><span data-ttu-id="96188-103">Conception de validations dans la couche de modèle de domaine</span><span class="sxs-lookup"><span data-stu-id="96188-103">Designing validations in the domain model layer</span></span>

<span data-ttu-id="96188-104">Dans la conception DDD, les règles de validation peuvent être considérées comme des invariants.</span><span class="sxs-lookup"><span data-stu-id="96188-104">In DDD, validation rules can be thought as invariants.</span></span> <span data-ttu-id="96188-105">La responsabilité principale d’un agrégat est d’appliquer des invariants aux changements d’état pour toutes les entités de cet agrégat.</span><span class="sxs-lookup"><span data-stu-id="96188-105">The main responsibility of an aggregate is to enforce invariants across state changes for all the entities within that aggregate.</span></span>

<span data-ttu-id="96188-106">Les entités de domaine doivent toujours être des entités valides.</span><span class="sxs-lookup"><span data-stu-id="96188-106">Domain entities should always be valid entities.</span></span> <span data-ttu-id="96188-107">Pour un objet, il existe un certain nombre d’invariants qui doivent toujours avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="96188-107">There are a certain number of invariants for an object that should always be true.</span></span> <span data-ttu-id="96188-108">Par exemple, un objet d’élément de commande doit toujours avoir une quantité qui doit être un entier positif, ainsi qu’un nom d’article et un prix.</span><span class="sxs-lookup"><span data-stu-id="96188-108">For example, an order item object always has to have a quantity that must be a positive integer, plus an article name and price.</span></span> <span data-ttu-id="96188-109">Par conséquent, il incombe aux entités de domaine (en particulier celles de la racine d’agrégat) de mettre en application les invariants, et un objet d’entité ne doit pas pouvoir exister s’il n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="96188-109">Therefore, invariants enforcement is the responsibility of the domain entities (especially of the aggregate root) and an entity object should not be able to exist without being valid.</span></span> <span data-ttu-id="96188-110">Les règles invariantes sont simplement exprimées sous la forme de contrats. Quand elles sont enfreintes, des exceptions ou des notifications sont déclenchées.</span><span class="sxs-lookup"><span data-stu-id="96188-110">Invariant rules are simply expressed as contracts, and exceptions or notifications are raised when they are violated.</span></span>

<span data-ttu-id="96188-111">Le raisonnement derrière cette règle est que de nombreux bogues se produisent car les objets sont dans un état dans lequel ils n’auraient jamais dû se trouver.</span><span class="sxs-lookup"><span data-stu-id="96188-111">The reasoning behind this is that many bugs occur because objects are in a state they should never have been in.</span></span> <span data-ttu-id="96188-112">Ce qui suit en est une bonne explication de Greg Young dans une [discussion en ligne](http://jeffreypalermo.com/blog/the-fallacy-of-the-always-valid-entity/) :</span><span class="sxs-lookup"><span data-stu-id="96188-112">The following is a good explanation from Greg Young in an [online discussion](http://jeffreypalermo.com/blog/the-fallacy-of-the-always-valid-entity/):</span></span>

<span data-ttu-id="96188-113">Supposons que nous disposons désormais d’un service SendUserCreationEmailService qui prend un UserProfile... Comment pouvons-nous justifier, dans ce service, que le nom ne soit pas null ?</span><span class="sxs-lookup"><span data-stu-id="96188-113">Let's propose we now have a SendUserCreationEmailService that takes a UserProfile ... how can we rationalize in that service that Name is not null?</span></span> <span data-ttu-id="96188-114">Le vérifions-nous à nouveau ?</span><span class="sxs-lookup"><span data-stu-id="96188-114">Do we check it again?</span></span> <span data-ttu-id="96188-115">Ou plus probablement... vous ne vous souciez simplement pas de la vérification et « espérez que tout se passera au mieux » : vous espérez que quelqu’un a pris la peine de le valider avant de vous l’envoyer.</span><span class="sxs-lookup"><span data-stu-id="96188-115">Or more likely ... you just don't bother to check and "hope for the best"—you hope that someone bothered to validate it before sending it to you.</span></span> <span data-ttu-id="96188-116">Bien entendu, en utilisant TDD, l’un des premiers tests que nous devons écrire est que si j’envoie un client avec un nom null, une erreur doit être déclenchée.</span><span class="sxs-lookup"><span data-stu-id="96188-116">Of course, using TDD one of the first tests we should be writing is that if I send a customer with a null name that it should raise an error.</span></span> <span data-ttu-id="96188-117">Mais une fois que nous commençons à écrire ce genre de tests encore et encore, nous réalisons ceci : « Si nous n’avions pas autorisé qu’un nom devienne null, nous n’aurions pas tous ces tests ».</span><span class="sxs-lookup"><span data-stu-id="96188-117">But once we start writing these kinds of tests over and over again we realize ... "wait if we never allowed name to become null we wouldn't have all of these tests"</span></span>

## <a name="implementing-validations-in-the-domain-model-layer"></a><span data-ttu-id="96188-118">Implémentation de validations dans la couche du modèle de domaine</span><span class="sxs-lookup"><span data-stu-id="96188-118">Implementing validations in the domain model layer</span></span>

<span data-ttu-id="96188-119">Les validations sont généralement implémentées dans des constructeurs d’entité de domaine ou dans des méthodes qui peuvent mettre à jour l’entité.</span><span class="sxs-lookup"><span data-stu-id="96188-119">Validations are usually implemented in domain entity constructors or in methods that can update the entity.</span></span> <span data-ttu-id="96188-120">Il existe plusieurs façons d’implémenter des validations, comme la vérification des données et la levée d’exceptions si la validation échoue.</span><span class="sxs-lookup"><span data-stu-id="96188-120">There are multiple ways to implement validations, such as verifying data and raising exceptions if the validation fails.</span></span> <span data-ttu-id="96188-121">Il existe également des modèles plus avancés comme l’utilisation du modèle Spécification pour les validations, et le modèle Notification pour retourner une collection d’erreurs au lieu de retourner une exception pour chaque validation quand elle se produit.</span><span class="sxs-lookup"><span data-stu-id="96188-121">There are also more advanced patterns such as using the Specification pattern for validations, and the Notification pattern to return a collection of errors instead of returning an exception for each validation as it occurs.</span></span>

### <a name="validating-conditions-and-throwing-exceptions"></a><span data-ttu-id="96188-122">Validation de conditions et levée d’exceptions</span><span class="sxs-lookup"><span data-stu-id="96188-122">Validating conditions and throwing exceptions</span></span>

<span data-ttu-id="96188-123">L’exemple de code suivant illustre l’approche de validation la plus simple dans une entité de domaine en levant une exception.</span><span class="sxs-lookup"><span data-stu-id="96188-123">The following code example shows the simplest approach to validation in a domain entity by raising an exception.</span></span> <span data-ttu-id="96188-124">La table de références figurant à la fin de cette section indique des liens vers des implémentations plus avancées basées sur les modèles abordés précédemment.</span><span class="sxs-lookup"><span data-stu-id="96188-124">In the references table at the end of this section you can see links to more advanced implementations based on the patterns we have discussed previously.</span></span>

```csharp
public void SetAddress(Address address)
{
    _shippingAddress = address?? throw new ArgumentNullException(nameof(address));
}
```

<span data-ttu-id="96188-125">La nécessité de garantir que l’état interne n’a pas changé ou que toutes les mutations pour une méthode se sont produites constituerait un meilleur exemple.</span><span class="sxs-lookup"><span data-stu-id="96188-125">A better example would demonstrate the need to ensure that either the internal state did not change, or that all the mutations for a method occurred.</span></span> <span data-ttu-id="96188-126">Ainsi, l’implémentation suivante laisse l’objet dans un état non valide :</span><span class="sxs-lookup"><span data-stu-id="96188-126">For example, the following implementation would leave the object in an invalid state:</span></span>

```csharp
public void SetAddress(string line1, string line2,
    string city, string state, int zip)
{
    _shipingAddress.line1 = line1 ?? throw new ...
    _shippingAddress.line2 = line2;
    _shippingAddress.city = city ?? throw new ...
    _shippingAddress.state = (IsValid(state) ? state : throw new …);
}
```

<span data-ttu-id="96188-127">Si la valeur de l’état n’est pas valide, la première ligne d’adresse et la ville ont déjà été modifiées.</span><span class="sxs-lookup"><span data-stu-id="96188-127">If the value of the state is invalid, the first address line and the city have already been changed.</span></span> <span data-ttu-id="96188-128">Cela peut rendre l’adresse non valide.</span><span class="sxs-lookup"><span data-stu-id="96188-128">That might make the address invalid.</span></span>

<span data-ttu-id="96188-129">Une approche similaire peut être utilisée dans le constructeur de l’entité, levant une exception pour vérifier que l’entité est valide une fois créée.</span><span class="sxs-lookup"><span data-stu-id="96188-129">A similar approach can be used in the entity’s constructor, raising an exception to make sure that the entity is valid once it is created.</span></span>

### <a name="using-validation-attributes-in-the-model-based-on-data-annotations"></a><span data-ttu-id="96188-130">Utilisation d’attributs de validation dans le modèle basé sur des annotations de données</span><span class="sxs-lookup"><span data-stu-id="96188-130">Using validation attributes in the model based on data annotations</span></span>

<span data-ttu-id="96188-131">Une autre approche consiste à utiliser des attributs de validation basés sur des annotations de données.</span><span class="sxs-lookup"><span data-stu-id="96188-131">Another approach is to use validation attributes based on data annotations.</span></span> <span data-ttu-id="96188-132">Les attributs de validation offrent un moyen de configurer la validation de modèle, qui est, d’un point de vue conceptuel, semblable à la validation des champs dans des tables de base de données.</span><span class="sxs-lookup"><span data-stu-id="96188-132">Validation attributes provide a way to configure model validation, which is similar conceptually to validation on fields in database tables.</span></span> <span data-ttu-id="96188-133">Cela inclut des contraintes comme l’affectation de types de données ou des champs obligatoires.</span><span class="sxs-lookup"><span data-stu-id="96188-133">This includes constraints such as assigning data types or required fields.</span></span> <span data-ttu-id="96188-134">L’application de modèles à des données pour forcer le respect de règles métier, comme un numéro de carte de crédit, un numéro de téléphone ou une adresse e-mail, est un autre type de validation.</span><span class="sxs-lookup"><span data-stu-id="96188-134">Other types of validation include applying patterns to data to enforce business rules, such as a credit card number, phone number, or email address.</span></span> <span data-ttu-id="96188-135">Les attributs de validation facilitent l’application d’une configuration requise.</span><span class="sxs-lookup"><span data-stu-id="96188-135">Validation attributes make it easy to enforce requirements.</span></span>

<span data-ttu-id="96188-136">Toutefois, comme indiqué dans le code suivant, cette approche peut être trop intrusive dans un modèle DDD, car elle a une dépendance sur ModelState.IsValid à partir de Microsoft.AspNetCore.Mvc.ModelState, que vous devez appeler à partir de vos contrôleurs MVC.</span><span class="sxs-lookup"><span data-stu-id="96188-136">However, as shown in the following code, this approach might be too intrusive in a DDD model, because it takes a dependency on ModelState.IsValid from Microsoft.AspNetCore.Mvc.ModelState, which you must call from your MVC controllers.</span></span> <span data-ttu-id="96188-137">La validation de modèle se produit avant l’appel de chaque action du contrôleur ; il incombe à la méthode de contrôleur d’inspecter le résultat de l’appel à ModelState.IsValid et de réagir de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="96188-137">The model validation occurs prior to each controller action being invoked, and it is the controller method’s responsibility to inspect the result of calling ModelState.IsValid and react appropriately.</span></span> <span data-ttu-id="96188-138">La décision de l’utiliser dépend du degré de couplage fort souhaité pour le modèle avec cette infrastructure.</span><span class="sxs-lookup"><span data-stu-id="96188-138">The decision to use it depends on how tightly coupled you want the model to be with that infrastructure.</span></span>

```csharp
using System.ComponentModel.DataAnnotations;
// Other using statements ...
// Entity is a custom base class which has the ID
public class Product : Entity
{
    [Required]
    [StringLength(100)]
    public string Title { get; private set; }

    [Required]
    [Range(0, 999.99)]
    public decimal Price { get; private set; }

    [Required]
    [VintageProduct(1970)]
    [DataType(DataType.Date)]
    public DateTime ReleaseDate { get; private set; }

    [Required]
    [StringLength(1000)]
    public string Description { get; private set; }

    // Constructor...
    // Additional methods for entity logic and constructor...
}
```

<span data-ttu-id="96188-139">Toutefois, du point de vue DDD, il est préférable de conserver le modèle de domaine épuré en utilisant des exceptions dans les méthodes de comportement de votre entité, ou en implémentant les modèles Spécification et Notification pour appliquer des règles de validation.</span><span class="sxs-lookup"><span data-stu-id="96188-139">However, from a DDD point of view, the domain model is best kept lean with the use of exceptions in your entity’s behavior methods, or by implementing the Specification and Notification patterns to enforce validation rules.</span></span> <span data-ttu-id="96188-140">Les frameworks de validation comme les annotations de données dans ASP.NET Core ou tout autre framework de validation comme FluentValidation comportent l’obligation d’appeler le framework d’application.</span><span class="sxs-lookup"><span data-stu-id="96188-140">Validation frameworks like data annotations in ASP.NET Core or any other validation frameworks like FluentValidation carry a requirement to invoke the application framework.</span></span> <span data-ttu-id="96188-141">Par exemple, quand vous appelez la méthode ModelState.IsValid dans des annotations de données, vous devez appeler des contrôleurs ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="96188-141">For example, when calling the ModelState.IsValid method in data annotations, you need to invoke ASP.NET controllers.</span></span>

<span data-ttu-id="96188-142">Il peut être judicieux d’utiliser des annotations de données au niveau de la couche Application dans les classes ViewModel (plutôt que des entités de domaine) qui accepteront des entrées, pour permettre la validation de modèle dans la couche d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96188-142">It can make sense to use data annotations at the application layer in ViewModel classes (instead of domain entities) that will accept input, to allow for model validation within the UI layer.</span></span> <span data-ttu-id="96188-143">Toutefois, cela ne doit pas être effectué à l’exclusion de la validation dans le modèle de domaine.</span><span class="sxs-lookup"><span data-stu-id="96188-143">However, this should not be done at the exclusion of validation within the domain model.</span></span>

### <a name="validating-entities-by-implementing-the-specification-pattern-and-the-notification-pattern"></a><span data-ttu-id="96188-144">Validation d’entités en implémentant le modèle Spécification et le modèle Notification</span><span class="sxs-lookup"><span data-stu-id="96188-144">Validating entities by implementing the Specification pattern and the Notification pattern</span></span>

<span data-ttu-id="96188-145">Enfin, une approche plus élaborée pour implémenter des validations dans le modèle de domaine consiste à implémenter le modèle Spécification conjointement avec le modèle Notification, comme expliqué dans certaines des ressources supplémentaires répertoriées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="96188-145">Finally, a more elaborate approach to implementing validations in the domain model is by implementing the Specification pattern in conjunction with the Notification pattern, as explained in some of the additional resources listed later.</span></span>

<span data-ttu-id="96188-146">Il convient de mentionner que vous pouvez également utiliser un seul de ces modèles, par exemple en effectuant la validation manuellement avec des instructions de contrôle, mais en utilisant le modèle Notification pour empiler des erreurs de validation et en retourner la liste.</span><span class="sxs-lookup"><span data-stu-id="96188-146">It is worth mentioning that you can also use just one of those patterns—for example, validating manually with control statements, but using the Notification pattern to stack and return a list of validation errors.</span></span>

### <a name="using-deferred-validation-in-the-domain"></a><span data-ttu-id="96188-147">Utilisation de la validation différée dans le domaine</span><span class="sxs-lookup"><span data-stu-id="96188-147">Using deferred validation in the domain</span></span>

<span data-ttu-id="96188-148">Il existe différentes approches pour traiter les validations différées dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="96188-148">There are various approaches to deal with deferred validations in the domain.</span></span> <span data-ttu-id="96188-149">Dans son livre [Implementing Domain-Driven Design](https://www.amazon.com/Implementing-Domain-Driven-Design-Vaughn-Vernon/dp/0321834577), Vaughn Vernon les décrit dans la section relative à la validation.</span><span class="sxs-lookup"><span data-stu-id="96188-149">In his book [Implementing Domain-Driven Design](https://www.amazon.com/Implementing-Domain-Driven-Design-Vaughn-Vernon/dp/0321834577), Vaughn Vernon discusses these in the section on validation.</span></span>

### <a name="two-step-validation"></a><span data-ttu-id="96188-150">Validation en deux étapes</span><span class="sxs-lookup"><span data-stu-id="96188-150">Two-step validation</span></span>

<span data-ttu-id="96188-151">Considérons également la validation en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="96188-151">Also consider two-step validation.</span></span> <span data-ttu-id="96188-152">Utilisez la validation au niveau des champs sur vos objets de transfert de données (DTO) de commande et la validation au niveau du domaine à l’intérieur de vos entités.</span><span class="sxs-lookup"><span data-stu-id="96188-152">Use field-level validation on your command Data Transfer Objects (DTOs) and domain-level validation inside your entities.</span></span> <span data-ttu-id="96188-153">Pour cela, retournez un objet de résultat plutôt que des exceptions afin de faciliter la gestion des erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="96188-153">You can do this by returning a result object instead exceptions in order to make it easier to deal with the validation errors.</span></span>

<span data-ttu-id="96188-154">En utilisant la validation de champ avec des annotations de données, par exemple, vous ne dupliquez pas la définition de la validation.</span><span class="sxs-lookup"><span data-stu-id="96188-154">Using field validation with data annotations, for example, you do not duplicate the validation definition.</span></span> <span data-ttu-id="96188-155">L’exécution peut toutefois être à la fois côté serveur et côté client dans le cas d’objets DTO (commandes et ViewModels, par exemple).</span><span class="sxs-lookup"><span data-stu-id="96188-155">The execution, though, can be both server-side and client-side in the case of DTOs (commands and ViewModels, for instance).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96188-156">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="96188-156">Additional resources</span></span>

-   <span data-ttu-id="96188-157">**Rachel Appel. Présentation de la validation de modèle dans ASP.NET Core MVC**
    [*https://docs.microsoft.com/aspnet/core/mvc/models/validation*](https://docs.microsoft.com/aspnet/core/mvc/models/validation)</span><span class="sxs-lookup"><span data-stu-id="96188-157">**Rachel Appel. Introduction to model validation in ASP.NET Core MVC**
[*https://docs.microsoft.com/aspnet/core/mvc/models/validation*](https://docs.microsoft.com/aspnet/core/mvc/models/validation)</span></span>

-   <span data-ttu-id="96188-158">**Rick Anderson. Ajout de la validation**
    [*https://docs.microsoft.com/aspnet/core/tutorials/first-mvc-app/validation*](https://docs.microsoft.com/aspnet/core/tutorials/first-mvc-app/validation)</span><span class="sxs-lookup"><span data-stu-id="96188-158">**Rick Anderson. Adding validation**
[*https://docs.microsoft.com/aspnet/core/tutorials/first-mvc-app/validation*](https://docs.microsoft.com/aspnet/core/tutorials/first-mvc-app/validation)</span></span>

-   <span data-ttu-id="96188-159">**Martin Fowler. Replacing Throwing Exceptions with Notification in Validations**
    [*https://martinfowler.com/articles/replaceThrowWithNotification.html*](https://martinfowler.com/articles/replaceThrowWithNotification.html)</span><span class="sxs-lookup"><span data-stu-id="96188-159">**Martin Fowler. Replacing Throwing Exceptions with Notification in Validations**
[*https://martinfowler.com/articles/replaceThrowWithNotification.html*](https://martinfowler.com/articles/replaceThrowWithNotification.html)</span></span>

-   <span data-ttu-id="96188-160">**Specification and Notification Patterns**
    [*https://www.codeproject.com/Tips/790758/Specification-and-Notification-Patterns*](https://www.codeproject.com/Tips/790758/Specification-and-Notification-Patterns)</span><span class="sxs-lookup"><span data-stu-id="96188-160">**Specification and Notification Patterns**
[*https://www.codeproject.com/Tips/790758/Specification-and-Notification-Patterns*](https://www.codeproject.com/Tips/790758/Specification-and-Notification-Patterns)</span></span>

-   <span data-ttu-id="96188-161">**Lev Gorodinski. Validation in Domain-Driven Design (DDD)**
    [*http://gorodinski.com/blog/2012/05/19/validation-in-domain-driven-design-ddd/*](http://gorodinski.com/blog/2012/05/19/validation-in-domain-driven-design-ddd/)</span><span class="sxs-lookup"><span data-stu-id="96188-161">**Lev Gorodinski. Validation in Domain-Driven Design (DDD)**
[*http://gorodinski.com/blog/2012/05/19/validation-in-domain-driven-design-ddd/*](http://gorodinski.com/blog/2012/05/19/validation-in-domain-driven-design-ddd/)</span></span>

-   <span data-ttu-id="96188-162">**Colin Jack. Domain Model Validation**
    [*http://colinjack.blogspot.com/2008/03/domain-model-validation.html*](http://colinjack.blogspot.com/2008/03/domain-model-validation.html)</span><span class="sxs-lookup"><span data-stu-id="96188-162">**Colin Jack. Domain Model Validation**
[*http://colinjack.blogspot.com/2008/03/domain-model-validation.html*](http://colinjack.blogspot.com/2008/03/domain-model-validation.html)</span></span>

-   <span data-ttu-id="96188-163">**Jimmy Bogard. Validation in a DDD world**
    [*https://lostechies.com/jimmybogard/2009/02/15/validation-in-a-ddd-world/*](https://lostechies.com/jimmybogard/2009/02/15/validation-in-a-ddd-world/)</span><span class="sxs-lookup"><span data-stu-id="96188-163">**Jimmy Bogard. Validation in a DDD world**
[*https://lostechies.com/jimmybogard/2009/02/15/validation-in-a-ddd-world/*](https://lostechies.com/jimmybogard/2009/02/15/validation-in-a-ddd-world/)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="96188-164">[Précédent] (enumeration-classes-over-enum-types.md) [Suivant] (client-side-validation.md)</span><span class="sxs-lookup"><span data-stu-id="96188-164">[Previous] (enumeration-classes-over-enum-types.md) [Next] (client-side-validation.md)</span></span>
