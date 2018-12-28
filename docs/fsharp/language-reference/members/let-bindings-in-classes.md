---
title: Liaisons let dans des classes
description: Découvrez comment définir des champs privés et des fonctions privées pour F# classes à l’aide de 'let' liaisons dans la définition de classe.
ms.date: 05/16/2016
ms.openlocfilehash: 03dd583a141971284e6a8ddaad02272236cd1e4c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53611124"
---
# <a name="let-bindings-in-classes"></a><span data-ttu-id="b0e6e-103">Liaisons let dans des classes</span><span class="sxs-lookup"><span data-stu-id="b0e6e-103">let Bindings in Classes</span></span>

<span data-ttu-id="b0e6e-104">Vous pouvez définir des champs privés et des fonctions privées pour F# classes à l’aide de `let` liaisons dans la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-104">You can define private fields and private functions for F# classes by using `let` bindings in the class definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e6e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0e6e-105">Syntax</span></span>

```fsharp
// Field.
[static] let [ mutable ] binding1 [ and ... binding-n ]

// Function.
[static] let [ rec ] binding1 [ and ... binding-n ]
```

## <a name="remarks"></a><span data-ttu-id="b0e6e-106">Notes</span><span class="sxs-lookup"><span data-stu-id="b0e6e-106">Remarks</span></span>

<span data-ttu-id="b0e6e-107">La syntaxe précédente apparaît après les déclarations de titre et l’héritage de classe, mais avant les définitions de membre.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-107">The previous syntax appears after the class heading and inheritance declarations but before any member definitions.</span></span> <span data-ttu-id="b0e6e-108">La syntaxe est similaire à celle de `let` liaisons en dehors des classes, mais les noms définis dans une classe ont une portée est limitée à la classe.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-108">The syntax is like that of `let` bindings outside of classes, but the names defined in a class have a scope that is limited to the class.</span></span> <span data-ttu-id="b0e6e-109">Un `let` liaison crée un champ privé ou une fonction ; pour exposer des données ou les fonctions déclarer publiquement, une propriété ou une méthode membre.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-109">A `let` binding creates a private field or function; to expose data or functions publicly, declare a property or a member method.</span></span>

<span data-ttu-id="b0e6e-110">Un `let` liaison qui n’est pas statique est appelée une instance `let` liaison.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-110">A `let` binding that is not static is called an instance `let` binding.</span></span> <span data-ttu-id="b0e6e-111">Instance `let` liaisons exécutent lorsque des objets sont créés.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-111">Instance `let` bindings execute when objects are created.</span></span> <span data-ttu-id="b0e6e-112">Statique `let` liaisons font partie de l’initialiseur statique pour la classe, qui est toujours exécuté avant que le type est utilisé tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-112">Static `let` bindings are part of the static initializer for the class, which is guaranteed to execute before the type is first used.</span></span>

<span data-ttu-id="b0e6e-113">Le code au sein de l’instance `let` liaisons peuvent utiliser les paramètres du constructeur principal.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-113">The code within instance `let` bindings can use the primary constructor's parameters.</span></span>

<span data-ttu-id="b0e6e-114">Attributs et les modificateurs d’accessibilité ne sont pas autorisés sur `let` liaisons dans les classes.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-114">Attributes and accessibility modifiers are not permitted on `let` bindings in classes.</span></span>

<span data-ttu-id="b0e6e-115">Les exemples de code suivants illustrent plusieurs types de `let` liaisons dans les classes.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-115">The following code examples illustrate several types of `let` bindings in classes.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3001.fs)]

<span data-ttu-id="b0e6e-116">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-116">The output is as follows.</span></span>

```
10 52 1 204
```

## <a name="alternative-ways-to-create-fields"></a><span data-ttu-id="b0e6e-117">Autres manières de créer des champs</span><span class="sxs-lookup"><span data-stu-id="b0e6e-117">Alternative Ways to Create Fields</span></span>

<span data-ttu-id="b0e6e-118">Vous pouvez également utiliser le `val` mot clé pour créer un champ privé.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-118">You can also use the `val` keyword to create a private field.</span></span> <span data-ttu-id="b0e6e-119">Lorsque vous utilisez le `val` mot clé, le champ n'est pas une valeur donné lorsque l’objet est créé, mais est initialisé avec une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-119">When using the `val` keyword, the field is not given a value when the object is created, but instead is initialized with a default value.</span></span> <span data-ttu-id="b0e6e-120">Pour plus d’informations, consultez [champs explicites : Val mot clé](explicit-fields-the-val-keyword.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6e-120">For more information, see [Explicit Fields: The val Keyword](explicit-fields-the-val-keyword.md).</span></span>

<span data-ttu-id="b0e6e-121">Vous pouvez également définir des champs privés dans une classe en utilisant une définition de membre et en ajoutant le mot clé `private` à la définition.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-121">You can also define private fields in a class by using a member definition and adding the keyword `private` to the definition.</span></span> <span data-ttu-id="b0e6e-122">Cela peut être utile si vous envisagez de modifier l’accessibilité d’un membre sans réécrire votre code.</span><span class="sxs-lookup"><span data-stu-id="b0e6e-122">This can be useful if you expect to change the accessibility of a member without rewriting your code.</span></span> <span data-ttu-id="b0e6e-123">Pour plus d’informations, consultez [Contrôle d’accès](../access-control.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6e-123">For more information, see [Access Control](../access-control.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b0e6e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0e6e-124">See also</span></span>

- [<span data-ttu-id="b0e6e-125">Membres</span><span class="sxs-lookup"><span data-stu-id="b0e6e-125">Members</span></span>](index.md)
- [<span data-ttu-id="b0e6e-126">Liaisons `do` dans des classes</span><span class="sxs-lookup"><span data-stu-id="b0e6e-126">`do` Bindings in Classes</span></span>](do-bindings-in-classes.md)
- [<span data-ttu-id="b0e6e-127">`let` liaisons</span><span class="sxs-lookup"><span data-stu-id="b0e6e-127">`let` Bindings</span></span>](../functions/let-bindings.md)