---
title: Seedwork (interfaces et classes de base réutilisables pour votre modèle de domaine)
description: Architecture des microservices .NET pour les applications .NET en conteneur | Seedwork (interfaces et classes de base réutilisables pour votre modèle de domaine)
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 12/12/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 641439267d7fcb504965487aeed165188b2cf123
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="seedwork-reusable-base-classes-and-interfaces-for-your-domain-model"></a><span data-ttu-id="4db0d-104">Seedwork (interfaces et classes de base réutilisables pour votre modèle de domaine)</span><span class="sxs-lookup"><span data-stu-id="4db0d-104">Seedwork (reusable base classes and interfaces for your domain model)</span></span>

<span data-ttu-id="4db0d-105">Le dossier solution contient un dossier *SeedWork*.</span><span class="sxs-lookup"><span data-stu-id="4db0d-105">The solution folder contains a *SeedWork* folder.</span></span> <span data-ttu-id="4db0d-106">Le dossier *SeedWork* contient des classes de base personnalisées que vous pouvez utiliser comme base pour vos entités de domaine et objets de valeur.</span><span class="sxs-lookup"><span data-stu-id="4db0d-106">The *SeedWork* folder contains custom base classes that you can use as a base for your domain entities and value objects.</span></span> <span data-ttu-id="4db0d-107">Utilisez ces classes de base pour ne pas avoir de code redondant dans la classe d’objets de chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="4db0d-107">Use these base classes so you do not have redundant code in each domain’s object class.</span></span> <span data-ttu-id="4db0d-108">Le dossier de ces types de classes s’appelle *SeedWork* et non pas *Framework*.</span><span class="sxs-lookup"><span data-stu-id="4db0d-108">The folder for these types of classes is called *SeedWork* and not something like *Framework*.</span></span> <span data-ttu-id="4db0d-109">Il s’appelle *SeedWork* car le dossier contient juste un petit sous-ensemble de classes réutilisables qui ne peut pas être vraiment considéré comme un framework.</span><span class="sxs-lookup"><span data-stu-id="4db0d-109">It's called *SeedWork* because the folder contains just a small subset of reusable classes which cannot really be considered a framework.</span></span> <span data-ttu-id="4db0d-110">*Seedwork* est un terme introduit par [Michael Feathers](https://www.artima.com/forums/flat.jsp?forum=106&thread=8826) que [Martin Fowler](https://martinfowler.com/bliki/Seedwork.html) a rendu populaire, mais vous pouvez également donner à ce dossier le nom Common, SharedKernel ou un autre nom similaire.</span><span class="sxs-lookup"><span data-stu-id="4db0d-110">*Seedwork* is a term introduced by [Michael Feathers](https://www.artima.com/forums/flat.jsp?forum=106&thread=8826) and popularized by [Martin Fowler](https://martinfowler.com/bliki/Seedwork.html) but you could also name that folder Common, SharedKernel, or similar.</span></span>

<span data-ttu-id="4db0d-111">La figure 9-12 montre les classes qui constituent le seedwork du modèle de domaine dans le microservice de commande.</span><span class="sxs-lookup"><span data-stu-id="4db0d-111">Figure 9-12 shows the classes that form the seedwork of the domain model in the ordering microservice.</span></span> <span data-ttu-id="4db0d-112">Il comporte quelques classes de base personnalisées comme Entity, ValueObject et Enumeration, ainsi que quelques interfaces.</span><span class="sxs-lookup"><span data-stu-id="4db0d-112">It has a few custom base classes like Entity, ValueObject, and Enumeration, plus a few interfaces.</span></span> <span data-ttu-id="4db0d-113">Ces interfaces (IRepository et IUnitOfWork) informent la couche d’infrastructure sur ce qui doit être implémenté.</span><span class="sxs-lookup"><span data-stu-id="4db0d-113">These interfaces (IRepository and IUnitOfWork) inform the infrastructure layer about what needs to be implemented.</span></span> <span data-ttu-id="4db0d-114">Elles sont également utilisées par injection de dépendances à partir de la couche Application.</span><span class="sxs-lookup"><span data-stu-id="4db0d-114">Those interfaces are also used through Dependency Injection from the application layer.</span></span>

![](./media/image13.PNG)

<span data-ttu-id="4db0d-115">**Figure 9-12**.</span><span class="sxs-lookup"><span data-stu-id="4db0d-115">**Figure 9-12**.</span></span> <span data-ttu-id="4db0d-116">Exemple d’ensemble de classes de base et d’interfaces « seedwork » de modèle de domaine</span><span class="sxs-lookup"><span data-stu-id="4db0d-116">A sample set of domain model “seedwork" base classes and interfaces</span></span>

<span data-ttu-id="4db0d-117">Il s’agit du type de réutilisation par copier- coller que de nombreux développeurs partagent entre les projets, et non d’un framework formel.</span><span class="sxs-lookup"><span data-stu-id="4db0d-117">This is the type of copy and paste reuse that many developers share between projects, not a formal framework.</span></span> <span data-ttu-id="4db0d-118">Vous pouvez avoir des seedworks dans n’importe quelle couche ou bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4db0d-118">You can have seedworks in any layer or library.</span></span> <span data-ttu-id="4db0d-119">Toutefois, si l’ensemble des classes et interfaces est suffisamment important, vous pouvez créer une bibliothèque de classes unique.</span><span class="sxs-lookup"><span data-stu-id="4db0d-119">However, if the set of classes and interfaces gets big enough, you might want to create a single class library.</span></span>

## <a name="the-custom-entity-base-class"></a><span data-ttu-id="4db0d-120">Classe de base Entity personnalisée</span><span class="sxs-lookup"><span data-stu-id="4db0d-120">The custom Entity base class</span></span>

<span data-ttu-id="4db0d-121">Le code suivant est un exemple de classe de base Entity dans lequel vous pouvez placer du code utilisable de la même façon par une entité de domaine, comme l’ID d’entité, les [opérateurs d’égalité](/cpp/cpp/equality-operators-equal-equal-and-exclpt-equal), une liste d’événements de domaine par entité, etc.</span><span class="sxs-lookup"><span data-stu-id="4db0d-121">The following code is an example of an Entity base class where you can place code that can be used the same way by any domain entity, such as the entity ID, [equality operators](/cpp/cpp/equality-operators-equal-equal-and-exclpt-equal), a domain event list per entity, etc.</span></span>

```csharp
// COMPATIBLE WITH ENTITY FRAMEWORK CORE (1.1 and later)
public abstract class Entity
{
    int? _requestedHashCode;
    int _Id;    
    private List<INotification> _domainEvents;
    public virtual int Id 
    {
        get
        {
            return _Id;
        }
        protected set
        {
            _Id = value;
        }
    }

    public List<INotification> DomainEvents => _domainEvents;        
    public void AddDomainEvent(INotification eventItem)
    {
        _domainEvents = _domainEvents ?? new List<INotification>();
        _domainEvents.Add(eventItem);
    }
    public void RemoveDomainEvent(INotification eventItem)
    {
        if (_domainEvents is null) return;
        _domainEvents.Remove(eventItem);
    }

    public bool IsTransient()
    {
        return this.Id == default(Int32);
    }

    public override bool Equals(object obj)
    {
        if (obj == null || !(obj is Entity))
            return false;
        if (Object.ReferenceEquals(this, obj))
            return true;
        if (this.GetType() != obj.GetType())
            return false;
        Entity item = (Entity)obj;
        if (item.IsTransient() || this.IsTransient())
            return false;
        else
            return item.Id == this.Id;
    }

    public override int GetHashCode()
    {
        if (!IsTransient())
        {
            if (!_requestedHashCode.HasValue)
                _requestedHashCode = this.Id.GetHashCode() ^ 31; 
            // XOR for random distribution. See:
            // http://blogs.msdn.com/b/ericlippert/archive/2011/02/28/guidelines-and-rules-for-gethashcode.aspx
            return _requestedHashCode.Value;
        }
        else
            return base.GetHashCode();
    }
    public static bool operator ==(Entity left, Entity right)
    {
        if (Object.Equals(left, null))
            return (Object.Equals(right, null)) ? true : false;
        else
            return left.Equals(right);
    }
    public static bool operator !=(Entity left, Entity right)
    {
        return !(left == right);
    }
}
```

<span data-ttu-id="4db0d-122">Le code précédent qui utilise une liste d’événements de domaine par entité est expliqué dans les sections suivantes dédiées aux événements de domaine.</span><span class="sxs-lookup"><span data-stu-id="4db0d-122">The previous code using a domain event list per entity will be explained in the next sections when focusing on domain events.</span></span> 

## <a name="repository-contracts-interfaces-in-the-domain-model-layer"></a><span data-ttu-id="4db0d-123">Contrats (interfaces) de dépôt dans la couche du modèle de domaine</span><span class="sxs-lookup"><span data-stu-id="4db0d-123">Repository contracts (interfaces) in the domain model layer</span></span>

<span data-ttu-id="4db0d-124">Les contrats de dépôt sont simplement des interfaces .NET qui expriment les spécifications contractuelles des dépôts à utiliser pour chaque agrégat.</span><span class="sxs-lookup"><span data-stu-id="4db0d-124">Repository contracts are simply .NET interfaces that express the contract requirements of the repositories to be used for each aggregate.</span></span> 

<span data-ttu-id="4db0d-125">Les dépôts eux-mêmes, avec le code EF Core ou d’autres dépendances d’infrastructure et code (Linq, SQL, etc.), ne doivent pas être implémentés au sein du modèle de domaine ; ils doivent uniquement implémenter les interfaces que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="4db0d-125">The repositories themselves, with EF Core code or any other infrastructure dependencies and code (Linq, SQL, etc.), must not be implemented within the domain model; the repositories should only implement the interfaces you define.</span></span> 

<span data-ttu-id="4db0d-126">Le modèle lié à cette pratique (placer les interfaces de dépôt dans la couche du modèle de domaine) est le modèle Interface séparée.</span><span class="sxs-lookup"><span data-stu-id="4db0d-126">A pattern related to this practice (placing the repository interfaces in the domain model layer) is the Separated Interface pattern.</span></span> <span data-ttu-id="4db0d-127">Comme l’[explique](https://www.martinfowler.com/eaaCatalog/separatedInterface.html) Martin Fowler, « utilisez une interface séparée pour définir une interface dans un premier paquet mais l’implémenter dans un autre.</span><span class="sxs-lookup"><span data-stu-id="4db0d-127">As [explained](https://www.martinfowler.com/eaaCatalog/separatedInterface.html) by Martin Fowler, “Use Separated Interface to define an interface in one package but implement it in another.</span></span> <span data-ttu-id="4db0d-128">De cette manière, un client qui a besoin de la dépendance vis-à-vis de l’interface peut ne pas en connaître du tout l’implémentation ».</span><span class="sxs-lookup"><span data-stu-id="4db0d-128">This way a client that needs the dependency to the interface can be completely unaware of the implementation.”</span></span>

<span data-ttu-id="4db0d-129">Avec le modèle Interface séparée, la couche Application (dans ce cas, le projet d’API web pour le microservice) comporte une dépendance vis-à-vis des spécifications définies dans le modèle de domaine, mais pas une dépendance directe vis-à-vis de la couche d’infrastructure/de persistance.</span><span class="sxs-lookup"><span data-stu-id="4db0d-129">Following the Separated Interface pattern enables the application layer (in this case, the Web API project for the microservice) to have a dependency on the requirements defined in the domain model, but not a direct dependency to the infrastructure/persistence layer.</span></span> <span data-ttu-id="4db0d-130">De plus, vous pouvez utiliser l’injection de dépendances pour isoler l’implémentation, qui est implémentée dans la couche d’infrastructure/de persistance à l’aide de dépôts.</span><span class="sxs-lookup"><span data-stu-id="4db0d-130">In addition, you can use Dependency Injection to isolate the implementation, which is implemented in the infrastructure/ persistence layer using repositories.</span></span>

<span data-ttu-id="4db0d-131">L’exemple suivant avec l’interface IOrderRepository définit les opérations que la classe OrderRepository a besoin d’implémenter au niveau de la couche d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="4db0d-131">For example, the following example with the IOrderRepository interface defines what operations the OrderRepository class will need to implement at the infrastructure layer.</span></span> <span data-ttu-id="4db0d-132">Dans l’implémentation actuelle de l’application, le code doit simplement ajouter ou mettre à jour des commandes dans la base de données, étant donné que les requêtes sont fractionnées selon l’approche CQRS simplifiée.</span><span class="sxs-lookup"><span data-stu-id="4db0d-132">In the current implementation of the application, the code just needs to add or update orders to the database, since queries are split following the simplified CQRS approach.</span></span>

```csharp
// Defined at IOrderRepository.cs
public interface IOrderRepository : IRepository<Order>
{
    Order Add(Order order);
        
    void Update(Order order);

    Task<Order> GetAsync(int orderId);
}

// Defined at IRepository.cs (Part of the Domain Seedwork)
public interface IRepository<T> where T : IAggregateRoot
{
    IUnitOfWork UnitOfWork { get; }
}
```

## <a name="additional-resources"></a><span data-ttu-id="4db0d-133">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4db0d-133">Additional resources</span></span>

-   <span data-ttu-id="4db0d-134">**Martin Fowler. Separated Interface.**
    [*https://www.martinfowler.com/eaaCatalog/separatedInterface.html*](https://www.martinfowler.com/eaaCatalog/separatedInterface.html)</span><span class="sxs-lookup"><span data-stu-id="4db0d-134">**Martin Fowler. Separated Interface.**
[*https://www.martinfowler.com/eaaCatalog/separatedInterface.html*](https://www.martinfowler.com/eaaCatalog/separatedInterface.html)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="4db0d-135">[Précédent] (net-core-microservice-domain-model.md) [Suivant] (implement-value-objects.md)</span><span class="sxs-lookup"><span data-stu-id="4db0d-135">[Previous] (net-core-microservice-domain-model.md) [Next] (implement-value-objects.md)</span></span>
