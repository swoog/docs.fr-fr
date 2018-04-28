---
title: Identificateurs de ligne, de fichier et de chemin d’accès source (F#)
description: 'Découvrez comment utiliser F # identificateur valeurs intégrées qui vous permettent d’accéder à la source de numéro de ligne, un répertoire et un nom de fichier dans votre code.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 18a26f0aa0a0c1f9c0b448ec46eaebd540391324
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="source-line-file-and-path-identifiers"></a><span data-ttu-id="ea86e-103">Identificateurs de ligne, de fichier et de chemin d’accès source</span><span class="sxs-lookup"><span data-stu-id="ea86e-103">Source Line, File, and Path Identifiers</span></span>

<span data-ttu-id="ea86e-104">Les identificateurs `__LINE__`, `__SOURCE_DIRECTORY__` et `__SOURCE_FILE__` sont des valeurs intégrées qui vous permettent d’accéder à la ligne source nombre, les répertoires et les fichiers nom dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ea86e-104">The identifiers `__LINE__`, `__SOURCE_DIRECTORY__` and `__SOURCE_FILE__` are built-in values that enable you to access the source line number, directory and file name in your code.</span></span>


## <a name="syntax"></a><span data-ttu-id="ea86e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea86e-105">Syntax</span></span>

```fsharp
__LINE__
__SOURCE_DIRECTORY__
__SOURCE_FILE__
```

## <a name="remarks"></a><span data-ttu-id="ea86e-106">Notes</span><span class="sxs-lookup"><span data-stu-id="ea86e-106">Remarks</span></span>
<span data-ttu-id="ea86e-107">Chacune de ces valeurs a le type `string`.</span><span class="sxs-lookup"><span data-stu-id="ea86e-107">Each of these values has type `string`.</span></span>

<span data-ttu-id="ea86e-108">Le tableau suivant récapitule la ligne source, fichier et les identificateurs de chemin d’accès qui sont disponibles en F #.</span><span class="sxs-lookup"><span data-stu-id="ea86e-108">The following table summarizes the source line, file, and path identifiers that are available in F#.</span></span> <span data-ttu-id="ea86e-109">Ces identificateurs ne sont pas des macros de préprocesseur ; ils sont des valeurs intégrées qui sont reconnus par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="ea86e-109">These identifiers are not preprocessor macros; they are built-in values that are recognized by the compiler.</span></span>

|<span data-ttu-id="ea86e-110">Identificateur prédéfini</span><span class="sxs-lookup"><span data-stu-id="ea86e-110">Predefined identifier</span></span>|<span data-ttu-id="ea86e-111">Description</span><span class="sxs-lookup"><span data-stu-id="ea86e-111">Description</span></span>|
|---------------------|-----------|
|`__LINE__`|<span data-ttu-id="ea86e-112">Prend la valeur de numéro de ligne active, vous envisagez de `#line` directives.</span><span class="sxs-lookup"><span data-stu-id="ea86e-112">Evaluates to the current line number, considering `#line` directives.</span></span>|
|`__SOURCE_DIRECTORY__`|<span data-ttu-id="ea86e-113">Prend la valeur de chemin d’accès complet en cours du répertoire source, envisagez `#line` directives.</span><span class="sxs-lookup"><span data-stu-id="ea86e-113">Evaluates to the current full path of the source directory, considering `#line` directives.</span></span>|
|`__SOURCE_FILE__`|<span data-ttu-id="ea86e-114">Donne le nom du fichier source et son chemin d’accès, vous envisagez de `#line` directives.</span><span class="sxs-lookup"><span data-stu-id="ea86e-114">Evaluates to the current source file name and its path, considering `#line` directives.</span></span>|
<span data-ttu-id="ea86e-115">Pour plus d’informations sur la `#line` directive, voir [Directives de compilateur](compiler-directives.md).</span><span class="sxs-lookup"><span data-stu-id="ea86e-115">For more information about the `#line` directive, see [Compiler Directives](compiler-directives.md).</span></span>

## <a name="example"></a><span data-ttu-id="ea86e-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="ea86e-116">Example</span></span>

<span data-ttu-id="ea86e-117">L’exemple de code suivant illustre l’utilisation de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="ea86e-117">The following code example demonstrates the use of these values.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7401.fs)]

<span data-ttu-id="ea86e-118">Sortie :</span><span class="sxs-lookup"><span data-stu-id="ea86e-118">Output:</span></span>

```
Line: 4
Source Directory: C:\Users\username\Documents\Visual Studio 2017\Projects\SourceInfo\SourceInfo
Source File: C:\Users\username\Documents\Visual Studio 2017\Projects\SourceInfo\SourceInfo\Program.fs
```

## <a name="see-also"></a><span data-ttu-id="ea86e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea86e-119">See Also</span></span>
[<span data-ttu-id="ea86e-120">Directives de compilateur</span><span class="sxs-lookup"><span data-stu-id="ea86e-120">Compiler Directives</span></span>](compiler-directives.md)

[<span data-ttu-id="ea86e-121">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="ea86e-121">F# Language Reference</span></span>](index.md)
