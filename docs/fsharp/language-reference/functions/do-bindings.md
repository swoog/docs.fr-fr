---
title: Liaisons do (F#)
description: "Découvrir comment une liaison de ' do' F # est utilisé pour exécuter du code sans définir de fonction ou une valeur."
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 4c63da0c5e2f4130d59f9efa6bc54a55e5fe9fd8
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="do-bindings"></a><span data-ttu-id="124e0-103">Liaisons do</span><span class="sxs-lookup"><span data-stu-id="124e0-103">do Bindings</span></span>

<span data-ttu-id="124e0-104">A `do` liaison est utilisée pour exécuter du code sans définir de fonction ou une valeur.</span><span class="sxs-lookup"><span data-stu-id="124e0-104">A `do` binding is used to execute code without defining a function or value.</span></span> <span data-ttu-id="124e0-105">En outre, les liaisons do peuvent être utilisées dans les classes, consultez [ `do` liaisons dans les Classes](../members/do-bindings-in-classes.md).</span><span class="sxs-lookup"><span data-stu-id="124e0-105">Also, do bindings can be used in classes, see [`do` Bindings in Classes](../members/do-bindings-in-classes.md).</span></span>


## <a name="syntax"></a><span data-ttu-id="124e0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="124e0-106">Syntax</span></span>

```fsharp
[ attributes ]
[ do ]expression
```

## <a name="remarks"></a><span data-ttu-id="124e0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="124e0-107">Remarks</span></span>
<span data-ttu-id="124e0-108">Utilisez un `do` liaison lorsque vous souhaitez exécuter du code indépendamment d’une définition de fonction ou de valeur.</span><span class="sxs-lookup"><span data-stu-id="124e0-108">Use a `do` binding when you want to execute code independently of a function or value definition.</span></span> <span data-ttu-id="124e0-109">L’expression dans une `do` liaison doit retourner `unit`.</span><span class="sxs-lookup"><span data-stu-id="124e0-109">The expression in a `do` binding must return `unit`.</span></span> <span data-ttu-id="124e0-110">Le code dans un niveau supérieur `do` liaison est exécutée lorsque le module est initialisé.</span><span class="sxs-lookup"><span data-stu-id="124e0-110">Code in a top-level `do` binding is executed when the module is initialized.</span></span> <span data-ttu-id="124e0-111">Le mot clé `do` est facultatif.</span><span class="sxs-lookup"><span data-stu-id="124e0-111">The keyword `do` is optional.</span></span>

<span data-ttu-id="124e0-112">Attributs peuvent être appliqués à un niveau supérieur `do` liaison.</span><span class="sxs-lookup"><span data-stu-id="124e0-112">Attributes can be applied to a top-level `do` binding.</span></span> <span data-ttu-id="124e0-113">Par exemple, si votre programme utilise COM interop, vous pouvez souhaiter appliquer le `STAThread` d’attribut à votre programme.</span><span class="sxs-lookup"><span data-stu-id="124e0-113">For example, if your program uses COM interop, you might want to apply the `STAThread` attribute to your program.</span></span> <span data-ttu-id="124e0-114">Vous pouvez pour cela à l’aide d’un attribut sur un `do` de liaison, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="124e0-114">You can do this by using an attribute on a `do` binding, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet201.fs)]
    
## <a name="see-also"></a><span data-ttu-id="124e0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="124e0-115">See Also</span></span>
[<span data-ttu-id="124e0-116">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="124e0-116">F# Language Reference</span></span>](../index.md)

[<span data-ttu-id="124e0-117">Fonctions</span><span class="sxs-lookup"><span data-stu-id="124e0-117">Functions</span></span>](index.md)

