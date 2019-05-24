---
title: Utilisation de classes d’énumération plutôt que de types enum
description: Architecture de microservices .NET pour les applications .NET conteneurisées | Découvrez comment utiliser des classes d’énumération pour contourner certaines limitations des types enum.
ms.date: 10/08/2018
ms.openlocfilehash: 02d5fcef580f71b6f8c4af6d88095e24b0bd3462
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65644479"
---
# <a name="use-enumeration-classes-instead-of-enum-types"></a>Utiliser des classes d’énumération à la place de types enum

Les [énumérations](../../../../docs/csharp/language-reference/keywords/enum.md) (ou *types enum* en abrégé) constituent un wrapper de langage simple autour d’un type intégral. Vous souhaiterez peut-être limiter leur utilisation au stockage d’une valeur d’un ensemble fermé de valeurs. La classification basée sur les tailles (petite, moyenne, grande) est un bon exemple. L’utilisation d’enums pour le flux de contrôle ou d’abstractions plus puissantes peut être un [code smell](https://deviq.com/code-smells/). Ce type d’utilisation a pour effet de fragiliser le code avec de nombreuses instructions de flux de contrôle qui vérifient les valeurs de l’enum.

À la place, vous pouvez créer des classes d’énumération qui activent toutes les fonctionnalités avancées d’un langage orienté objet.

Toutefois, ce n’est pas un sujet très important et, dans de nombreux cas, vous pouvez toujours simplifier en utilisant des [types enum](../../../csharp/language-reference/keywords/enum.md) standard, si vous préférez. En fait, l’utilisation des classes d’énumération est davantage liée à des concepts métier.

## <a name="implement-an-enumeration-base-class"></a>Implémenter une classe d’énumération de base

Le microservice Ordering (Commandes) dans eShopOnContainers fournit un exemple d’implémentation de classe d’énumération de base, comme illustré dans l’exemple suivant :

```csharp
public abstract class Enumeration : IComparable
{
    public string Name { get; private set; }

    public int Id { get; private set; }

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

Vous pouvez utiliser cette classe comme type dans n’importe quel objet entité ou valeur, comme pour la classe `CardType` : `Enumeration` suivante :

```csharp
public class CardType : Enumeration
{
    public static CardType Amex = new CardType(1, "Amex");
    public static CardType Visa = new CardType(2, "Visa");
    public static CardType MasterCard = new CardType(3, "MasterCard");

    public CardType(int id, string name)
        : base(id, name)
    {
    }
}
```

## <a name="additional-resources"></a>Ressources supplémentaires

- **Enum’s are evil—update** \
  <https://www.planetgeek.ch/2009/07/01/enums-are-evil/>

- **Daniel Hardman. How Enums Spread Disease — And How To Cure It** \
  <https://codecraft.co/2012/10/29/how-enums-spread-disease-and-how-to-cure-it/>

- **Jimmy Bogard. Enumeration classes** \
  <https://lostechies.com/jimmybogard/2008/08/12/enumeration-classes/>

- **Steve Smith. Enum Alternatives in C#** \
  <https://ardalis.com/enum-alternatives-in-c>

- **Enumeration.cs.** Classe d’énumération de base dans eShopOnContainers \
  <https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.Domain/SeedWork/Enumeration.cs>

- **CardType.cs**. Exemple de classe d’énumération dans eShopOnContainers. \
  <https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.Domain/AggregatesModel/BuyerAggregate/CardType.cs>
    
- **SmartEnum**. Ardalis - Cours pour apprendre à créer des enums fortement typés plus intelligents dans .NET. \
  <https://www.nuget.org/packages/Ardalis.SmartEnum/>

>[!div class="step-by-step"]
>[Précédent](implement-value-objects.md)
>[Suivant](domain-model-layer-validations.md)
