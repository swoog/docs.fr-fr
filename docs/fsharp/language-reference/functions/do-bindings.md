---
title: Liaisons do (F#)
description: "Découvrez comment une liaison ' do' F # est utilisé pour exécuter du code sans définir une fonction ou une valeur."
ms.date: 05/16/2016
ms.openlocfilehash: 78dbf8da0fe40b5af566ad98693df1109eede7e4
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44700321"
---
# <a name="do-bindings"></a><span data-ttu-id="7a049-103">Liaisons do</span><span class="sxs-lookup"><span data-stu-id="7a049-103">do Bindings</span></span>

<span data-ttu-id="7a049-104">Un `do` liaison est utilisée pour exécuter du code sans définir une fonction ou une valeur.</span><span class="sxs-lookup"><span data-stu-id="7a049-104">A `do` binding is used to execute code without defining a function or value.</span></span> <span data-ttu-id="7a049-105">En outre, les liaisons do peuvent être utilisées dans les classes, consultez [ `do` liaisons dans les Classes](../members/do-bindings-in-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7a049-105">Also, do bindings can be used in classes, see [`do` Bindings in Classes](../members/do-bindings-in-classes.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a049-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a049-106">Syntax</span></span>

```fsharp
[ attributes ]
[ do ]expression
```

## <a name="remarks"></a><span data-ttu-id="7a049-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7a049-107">Remarks</span></span>

<span data-ttu-id="7a049-108">Utilisez un `do` liaison lorsque vous souhaitez exécuter du code indépendamment d’une définition de fonction ou de valeur.</span><span class="sxs-lookup"><span data-stu-id="7a049-108">Use a `do` binding when you want to execute code independently of a function or value definition.</span></span> <span data-ttu-id="7a049-109">L’expression dans une `do` liaison doit retourner `unit`.</span><span class="sxs-lookup"><span data-stu-id="7a049-109">The expression in a `do` binding must return `unit`.</span></span> <span data-ttu-id="7a049-110">Le code dans un niveau supérieur `do` liaison est exécutée lorsque le module est initialisé.</span><span class="sxs-lookup"><span data-stu-id="7a049-110">Code in a top-level `do` binding is executed when the module is initialized.</span></span> <span data-ttu-id="7a049-111">Le mot clé `do` est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7a049-111">The keyword `do` is optional.</span></span>

<span data-ttu-id="7a049-112">Attributs peuvent être appliqués à un niveau supérieur `do` liaison.</span><span class="sxs-lookup"><span data-stu-id="7a049-112">Attributes can be applied to a top-level `do` binding.</span></span> <span data-ttu-id="7a049-113">Par exemple, si votre programme utilise COM interop, vous souhaiterez appliquer la `STAThread` attribut à votre programme.</span><span class="sxs-lookup"><span data-stu-id="7a049-113">For example, if your program uses COM interop, you might want to apply the `STAThread` attribute to your program.</span></span> <span data-ttu-id="7a049-114">Vous pouvez le faire à l’aide d’un attribut sur un `do` de liaison, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="7a049-114">You can do this by using an attribute on a `do` binding, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet201.fs)]

## <a name="see-also"></a><span data-ttu-id="7a049-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a049-115">See also</span></span>

- [<span data-ttu-id="7a049-116">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="7a049-116">F# Language Reference</span></span>](../index.md)
- [<span data-ttu-id="7a049-117">Fonctions</span><span class="sxs-lookup"><span data-stu-id="7a049-117">Functions</span></span>](index.md)
