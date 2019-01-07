---
title: virtual - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- virtual_CSharpKeyword
- virtual
helpviewer_keywords:
- virtual keyword [C#]
ms.assetid: 5da9abae-bc1e-434f-8bea-3601b8dcb3b2
ms.openlocfilehash: eede3359b195661ff89a387e9b226bc970c27942
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612568"
---
# <a name="virtual-c-reference"></a><span data-ttu-id="08957-102">virtual (référence C#)</span><span class="sxs-lookup"><span data-stu-id="08957-102">virtual (C# Reference)</span></span>

<span data-ttu-id="08957-103">Le mot clé `virtual` sert à modifier une méthode, une propriété, un indexeur ou une déclaration event et leur permet d’être substitués dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="08957-103">The `virtual` keyword is used to modify a method, property, indexer, or event declaration and allow for it to be overridden in a derived class.</span></span> <span data-ttu-id="08957-104">Par exemple, cette méthode peut être substituée par toute classe qui en hérite :</span><span class="sxs-lookup"><span data-stu-id="08957-104">For example, this method can be overridden by any class that inherits it:</span></span>

```csharp
public virtual double Area() 
{
    return x * y;
}
```

<span data-ttu-id="08957-105">L’implémentation d’un membre virtuel peut être modifiée par un [membre de substitution](override.md) dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="08957-105">The implementation of a virtual member can be changed by an [overriding member](override.md) in a derived class.</span></span> <span data-ttu-id="08957-106">Pour plus d’informations sur l’utilisation du mot clé `virtual`, consultez [Gestion de version avec les mots clés override et new](../../programming-guide/classes-and-structs/versioning-with-the-override-and-new-keywords.md) et [Savoir quand utiliser les mots clés override et new](../../programming-guide/classes-and-structs/knowing-when-to-use-override-and-new-keywords.md).</span><span class="sxs-lookup"><span data-stu-id="08957-106">For more information about how to use the `virtual` keyword, see [Versioning with the Override and New Keywords](../../programming-guide/classes-and-structs/versioning-with-the-override-and-new-keywords.md) and [Knowing When to Use Override and New Keywords](../../programming-guide/classes-and-structs/knowing-when-to-use-override-and-new-keywords.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="08957-107">Notes</span><span class="sxs-lookup"><span data-stu-id="08957-107">Remarks</span></span>

<span data-ttu-id="08957-108">Quand une méthode virtuelle est appelée, un membre de substitution est recherché dans le type d’objet au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="08957-108">When a virtual method is invoked, the run-time type of the object is checked for an overriding member.</span></span> <span data-ttu-id="08957-109">Le membre de substitution de la classe la plus dérivée est appelé (cela peut être le membre d’origine), si aucune classe dérivée n’a substitué le membre.</span><span class="sxs-lookup"><span data-stu-id="08957-109">The overriding member in the most derived class is called, which might be the original member, if no derived class has overridden the member.</span></span>

<span data-ttu-id="08957-110">Par défaut, les méthodes ne sont pas virtuelles.</span><span class="sxs-lookup"><span data-stu-id="08957-110">By default, methods are non-virtual.</span></span> <span data-ttu-id="08957-111">Vous ne pouvez pas substituer une méthode non virtuelle.</span><span class="sxs-lookup"><span data-stu-id="08957-111">You cannot override a non-virtual method.</span></span>

<span data-ttu-id="08957-112">Vous ne pouvez pas utiliser le modificateur `virtual` avec les modificateurs `static`, `abstract`, `private` ou `override`.</span><span class="sxs-lookup"><span data-stu-id="08957-112">You cannot use the `virtual` modifier with the `static`, `abstract`, `private`, or `override` modifiers.</span></span> <span data-ttu-id="08957-113">L’exemple suivant illustre une propriété virtuelle :</span><span class="sxs-lookup"><span data-stu-id="08957-113">The following example shows a virtual property:</span></span>

[!code-csharp[csrefKeywordsModifiers#26](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#26)]

<span data-ttu-id="08957-114">Les propriétés virtuelles se comportent comme les méthodes abstraites, à l’exception des différences dans la syntaxe de déclaration et d’appel.</span><span class="sxs-lookup"><span data-stu-id="08957-114">Virtual properties behave like abstract methods, except for the differences in declaration and invocation syntax.</span></span>

- <span data-ttu-id="08957-115">L’utilisation du modificateur `virtual` sur une propriété statique est une erreur.</span><span class="sxs-lookup"><span data-stu-id="08957-115">It is an error to use the `virtual` modifier on a static property.</span></span>

- <span data-ttu-id="08957-116">Une propriété virtuelle héritée peut être substituée dans une classe dérivée en incluant une déclaration de propriété qui utilise le modificateur `override`.</span><span class="sxs-lookup"><span data-stu-id="08957-116">A virtual inherited property can be overridden in a derived class by including a property declaration that uses the `override` modifier.</span></span>

## <a name="example"></a><span data-ttu-id="08957-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="08957-117">Example</span></span>

<span data-ttu-id="08957-118">Dans cet exemple, la classe `Shape` contient les deux coordonnées `x` et `y`, ainsi que la méthode virtuelle `Area()`.</span><span class="sxs-lookup"><span data-stu-id="08957-118">In this example, the `Shape` class contains the two coordinates `x`, `y`, and the `Area()` virtual method.</span></span> <span data-ttu-id="08957-119">Différentes classes de formes, telles que `Circle`, `Cylinder` et `Sphere`, héritent de la classe `Shape`, et la surface est calculée pour chaque figure.</span><span class="sxs-lookup"><span data-stu-id="08957-119">Different shape classes such as `Circle`, `Cylinder`, and `Sphere` inherit the `Shape` class, and the surface area is calculated for each figure.</span></span> <span data-ttu-id="08957-120">Chaque classe dérivée a sa propre implémentation de substitution de `Area()`.</span><span class="sxs-lookup"><span data-stu-id="08957-120">Each derived class has its own override implementation of `Area()`.</span></span>

<span data-ttu-id="08957-121">Notez que les classes héritées `Circle`, `Sphere` et `Cylinder` utilisent toutes des constructeurs qui initialisent la classe de base, comme indiqué dans la déclaration suivante.</span><span class="sxs-lookup"><span data-stu-id="08957-121">Notice that the inherited classes `Circle`, `Sphere`, and `Cylinder` all use constructors that initialize the base class, as shown in the following declaration.</span></span>

```csharp
public Cylinder(double r, double h): base(r, h) {}
```

<span data-ttu-id="08957-122">Le programme suivant calcule et affiche la zone appropriée pour chaque figure en appelant l’implémentation appropriée de la méthode `Area()`, selon l’objet associé à la méthode.</span><span class="sxs-lookup"><span data-stu-id="08957-122">The following program calculates and displays the appropriate area for each figure by invoking the appropriate implementation of the `Area()` method, according to the object that is associated with the method.</span></span>

[!code-csharp[csrefKeywordsModifiers#23](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#23)]

## <a name="c-language-specification"></a><span data-ttu-id="08957-123">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="08957-123">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="08957-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08957-124">See also</span></span>

- [<span data-ttu-id="08957-125">Référence C#</span><span class="sxs-lookup"><span data-stu-id="08957-125">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="08957-126">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="08957-126">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="08957-127">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="08957-127">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="08957-128">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="08957-128">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="08957-129">Polymorphisme</span><span class="sxs-lookup"><span data-stu-id="08957-129">Polymorphism</span></span>](../../programming-guide/classes-and-structs/polymorphism.md)
- [<span data-ttu-id="08957-130">abstract</span><span class="sxs-lookup"><span data-stu-id="08957-130">abstract</span></span>](abstract.md)
- [<span data-ttu-id="08957-131">override</span><span class="sxs-lookup"><span data-stu-id="08957-131">override</span></span>](override.md)
- [<span data-ttu-id="08957-132">new</span><span class="sxs-lookup"><span data-stu-id="08957-132">new</span></span>](new.md)