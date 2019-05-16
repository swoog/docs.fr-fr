---
title: Liaisons do
description: Découvrez comment un F# 'do' liaison est utilisé pour exécuter du code sans définir une fonction ou une valeur.
ms.date: 05/16/2016
ms.openlocfilehash: 0755e36912fc4e5a645e55eb4bee5c730a56cadf
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641915"
---
# <a name="do-bindings"></a><span data-ttu-id="47bcf-103">Liaisons do</span><span class="sxs-lookup"><span data-stu-id="47bcf-103">do Bindings</span></span>

<span data-ttu-id="47bcf-104">Un `do` liaison est utilisée pour exécuter du code sans définir une fonction ou une valeur.</span><span class="sxs-lookup"><span data-stu-id="47bcf-104">A `do` binding is used to execute code without defining a function or value.</span></span> <span data-ttu-id="47bcf-105">En outre, les liaisons do peuvent être utilisées dans les classes, consultez [ `do` liaisons dans les Classes](../members/do-bindings-in-classes.md).</span><span class="sxs-lookup"><span data-stu-id="47bcf-105">Also, do bindings can be used in classes, see [`do` Bindings in Classes](../members/do-bindings-in-classes.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="47bcf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47bcf-106">Syntax</span></span>

```fsharp
[ attributes ]
[ do ]expression
```

## <a name="remarks"></a><span data-ttu-id="47bcf-107">Notes</span><span class="sxs-lookup"><span data-stu-id="47bcf-107">Remarks</span></span>

<span data-ttu-id="47bcf-108">Utilisez un `do` liaison lorsque vous souhaitez exécuter du code indépendamment d’une définition de fonction ou de valeur.</span><span class="sxs-lookup"><span data-stu-id="47bcf-108">Use a `do` binding when you want to execute code independently of a function or value definition.</span></span> <span data-ttu-id="47bcf-109">L’expression dans une `do` liaison doit retourner `unit`.</span><span class="sxs-lookup"><span data-stu-id="47bcf-109">The expression in a `do` binding must return `unit`.</span></span> <span data-ttu-id="47bcf-110">Le code dans un niveau supérieur `do` liaison est exécutée lorsque le module est initialisé.</span><span class="sxs-lookup"><span data-stu-id="47bcf-110">Code in a top-level `do` binding is executed when the module is initialized.</span></span> <span data-ttu-id="47bcf-111">Le mot clé `do` est facultatif.</span><span class="sxs-lookup"><span data-stu-id="47bcf-111">The keyword `do` is optional.</span></span>

<span data-ttu-id="47bcf-112">Attributs peuvent être appliqués à un niveau supérieur `do` liaison.</span><span class="sxs-lookup"><span data-stu-id="47bcf-112">Attributes can be applied to a top-level `do` binding.</span></span> <span data-ttu-id="47bcf-113">Par exemple, si votre programme utilise COM interop, vous souhaiterez appliquer la `STAThread` attribut à votre programme.</span><span class="sxs-lookup"><span data-stu-id="47bcf-113">For example, if your program uses COM interop, you might want to apply the `STAThread` attribute to your program.</span></span> <span data-ttu-id="47bcf-114">Vous pouvez le faire à l’aide d’un attribut sur un `do` de liaison, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="47bcf-114">You can do this by using an attribute on a `do` binding, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet201.fs)]

## <a name="see-also"></a><span data-ttu-id="47bcf-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47bcf-115">See also</span></span>

- [<span data-ttu-id="47bcf-116">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="47bcf-116">F# Language Reference</span></span>](../index.md)
- [<span data-ttu-id="47bcf-117">Fonctions</span><span class="sxs-lookup"><span data-stu-id="47bcf-117">Functions</span></span>](index.md)
