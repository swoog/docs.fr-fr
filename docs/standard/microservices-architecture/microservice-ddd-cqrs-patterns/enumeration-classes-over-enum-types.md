---
title: Utilisation de classes d’énumération plutôt que de types enum
description: Architecture de microservices .NET pour les applications .NET conteneurisées | Découvrez comment utiliser des classes d’énumération pour contourner certaines limitations des types enum.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/08/2018
ms.openlocfilehash: 31f4807c956a8b4fb9381145f8e9b5eaffafe698
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149495"
---
# <a name="use-enumeration-classes-instead-of-enum-types"></a><span data-ttu-id="12f45-103">Utiliser des classes d’énumération à la place de types enum</span><span class="sxs-lookup"><span data-stu-id="12f45-103">Use enumeration classes instead of enum types</span></span>

<span data-ttu-id="12f45-104">Les [énumérations](../../../../docs/csharp/language-reference/keywords/enum.md) (ou *types enum* en abrégé) constituent un wrapper de langage simple autour d’un type intégral.</span><span class="sxs-lookup"><span data-stu-id="12f45-104">[Enumerations](../../../../docs/csharp/language-reference/keywords/enum.md) (or *enum types* for short) are a thin language wrapper around an integral type.</span></span> <span data-ttu-id="12f45-105">Vous souhaiterez peut-être limiter leur utilisation au stockage d’une valeur d’un ensemble fermé de valeurs.</span><span class="sxs-lookup"><span data-stu-id="12f45-105">You might want to limit their use to when you are storing one value from a closed set of values.</span></span> <span data-ttu-id="12f45-106">La classification basée sur les tailles (petite, moyenne, grande) est un bon exemple.</span><span class="sxs-lookup"><span data-stu-id="12f45-106">Classification based on sizes (small, medium, large) is a good example.</span></span> <span data-ttu-id="12f45-107">L’utilisation d’enums pour le flux de contrôle ou d’abstractions plus puissantes peut être un [code smell](http://deviq.com/code-smells/).</span><span class="sxs-lookup"><span data-stu-id="12f45-107">Using enums for control flow or more robust abstractions can be a [code smell](http://deviq.com/code-smells/).</span></span> <span data-ttu-id="12f45-108">Ce type d’utilisation a pour effet de fragiliser le code avec de nombreuses instructions de flux de contrôle qui vérifient les valeurs de l’enum.</span><span class="sxs-lookup"><span data-stu-id="12f45-108">This type of usage leads to fragile code with many control flow statements checking values of the enum.</span></span>

<span data-ttu-id="12f45-109">À la place, vous pouvez créer des classes d’énumération qui activent toutes les fonctionnalités avancées d’un langage orienté objet.</span><span class="sxs-lookup"><span data-stu-id="12f45-109">Instead, you can create Enumeration classes that enable all the rich features of an object-oriented language.</span></span>

<span data-ttu-id="12f45-110">Toutefois, ce n’est pas un sujet très important et, dans de nombreux cas, vous pouvez toujours simplifier en utilisant des [types enum](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/enum) standard, si vous préférez.</span><span class="sxs-lookup"><span data-stu-id="12f45-110">However, this isn't a critical topic and in many cases, for simplicity, you can still use regular [enum types](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/enum) if that's your preference.</span></span> <span data-ttu-id="12f45-111">En fait, l’utilisation des classes d’énumération est davantage liée à des concepts métier.</span><span class="sxs-lookup"><span data-stu-id="12f45-111">Anyway, the use of enumeration classes is more related to business-related concepts.</span></span>

## <a name="implement-an-enumeration-base-class"></a><span data-ttu-id="12f45-112">Implémenter une classe d’énumération de base</span><span class="sxs-lookup"><span data-stu-id="12f45-112">Implement an Enumeration base class</span></span>

<span data-ttu-id="12f45-113">Le microservice Ordering (Commandes) dans eShopOnContainers fournit un exemple d’implémentation de classe d’énumération de base, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="12f45-113">The ordering microservice in eShopOnContainers provides a sample Enumeration base class implementation, as shown in the following example:</span></span>

```csharp
public abstract class Enumeration : IComparable
{
    public string Name { get; private set; }

    public int Id { get; private set; }

    protected Enumeration()
    { }

    protected Enumeration(int id, string name) 
    {
        Id = id; 
        Name = name; 
    }

    public override string ToString() => Name;

    public static IEnumerable<T> GetAll<T>() where T : Enumeration
    {
        var fields = typeof(T).GetFields(BindingFlags.Public | 
                                         BindingFlags.Static | 
                                         BindingFlags.DeclaredOnly); 

        return fields.Select(f => f.GetValue(null)).Cast<T>();
    }

    public override bool Equals(object obj) 
    {
        var otherValue = obj as Enumeration; 

        if (otherValue == null) 
            return false;

        var typeMatches = GetType().Equals(obj.GetType());
        var valueMatches = Id.Equals(otherValue.Id);

        return typeMatches && valueMatches;
    }

    public int CompareTo(object other) => Id.CompareTo(((Enumeration)other).Id); 

    // Other utility methods ... 
}
```

<span data-ttu-id="12f45-114">Vous pouvez utiliser cette classe comme type dans n’importe quel objet entité ou valeur, comme pour la classe `CardType` : `Enumeration` suivante :</span><span class="sxs-lookup"><span data-stu-id="12f45-114">You can use this class as a type in any entity or value object, as for the following `CardType` : `Enumeration` class:</span></span>

```csharp
public abstract class CardType : Enumeration
{
    public static CardType Amex = new AmexCardType();
    public static CardType Visa = new VisaCardType();
    public static CardType MasterCard = new MasterCardType();

    protected CardType(int id, string name)
        : base(id, name)
    { }

    private class AmexCardType : CardType
    {
        public AmexCardType(): base(1, "Amex")
        { }
    }
    
    private class VisaCardType : CardType
    {
        public VisaCardType(): base(2, "Visa")
        { }
    }
    
    private class MasterCardType : CardType
    {
        public MasterCardType(): base(3, "MasterCard")
        { }
    }
}
```

## <a name="additional-resources"></a><span data-ttu-id="12f45-115">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="12f45-115">Additional resources</span></span>

- <span data-ttu-id="12f45-116">**Enum’s are evil—update** \\</span><span class="sxs-lookup"><span data-stu-id="12f45-116">**Enum’s are evil—update** \\</span></span>
  [*https://www.planetgeek.ch/2009/07/01/enums-are-evil/*](https://www.planetgeek.ch/2009/07/01/enums-are-evil/)

- <span data-ttu-id="12f45-117">**Daniel Hardman. How Enums Spread Disease — And How To Cure It** \\</span><span class="sxs-lookup"><span data-stu-id="12f45-117">**Daniel Hardman. How Enums Spread Disease — And How To Cure It** \\</span></span>
  [*https://codecraft.co/2012/10/29/how-enums-spread-disease-and-how-to-cure-it/*](https://codecraft.co/2012/10/29/how-enums-spread-disease-and-how-to-cure-it/)

- <span data-ttu-id="12f45-118">**Jimmy Bogard. Enumeration classes** \\</span><span class="sxs-lookup"><span data-stu-id="12f45-118">**Jimmy Bogard. Enumeration classes** \\</span></span>
  [*https://lostechies.com/jimmybogard/2008/08/12/enumeration-classes/*](https://lostechies.com/jimmybogard/2008/08/12/enumeration-classes/)

- <span data-ttu-id="12f45-119">**Steve Smith. Enum Alternatives in C#** \\</span><span class="sxs-lookup"><span data-stu-id="12f45-119">**Steve Smith. Enum Alternatives in C#** \\</span></span>
  [*https://ardalis.com/enum-alternatives-in-c*](https://ardalis.com/enum-alternatives-in-c)

- <span data-ttu-id="12f45-120">**Enumeration.cs.**</span><span class="sxs-lookup"><span data-stu-id="12f45-120">**Enumeration.cs.**</span></span> <span data-ttu-id="12f45-121">Classe d’énumération de base dans eShopOnContainers \\</span><span class="sxs-lookup"><span data-stu-id="12f45-121">Base Enumeration class in eShopOnContainers \\</span></span>
  [*https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.Domain/SeedWork/Enumeration.cs*](https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.Domain/SeedWork/Enumeration.cs)

- <span data-ttu-id="12f45-122">**CardType.cs**.</span><span class="sxs-lookup"><span data-stu-id="12f45-122">**CardType.cs**.</span></span> <span data-ttu-id="12f45-123">Exemple de classe d’énumération dans eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="12f45-123">Sample Enumeration class in eShopOnContainers.</span></span> \
  [*https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.Domain/AggregatesModel/BuyerAggregate/CardType.cs*](https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.Domain/AggregatesModel/BuyerAggregate/CardType.cs)
    
- <span data-ttu-id="12f45-124">**SmartEnum**.</span><span class="sxs-lookup"><span data-stu-id="12f45-124">**SmartEnum**.</span></span> <span data-ttu-id="12f45-125">Ardalis - Cours pour apprendre à créer des enums fortement typés plus intelligents dans .NET.</span><span class="sxs-lookup"><span data-stu-id="12f45-125">Ardalis - Classes to help produce strongly typed smarter enums in .NET.</span></span> \
  [*https://www.nuget.org/packages/Ardalis.SmartEnum/*](https://www.nuget.org/packages/Ardalis.SmartEnum/)

>[!div class="step-by-step"]
><span data-ttu-id="12f45-126">[Précédent](implement-value-objects.md)
>[Suivant](domain-model-layer-validations.md)</span><span class="sxs-lookup"><span data-stu-id="12f45-126">[Previous](implement-value-objects.md)
[Next](domain-model-layer-validations.md)</span></span>