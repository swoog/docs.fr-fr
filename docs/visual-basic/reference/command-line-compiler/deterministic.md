---
title: -déterministe
ms.date: 04/11/2018
ms.prod: .net
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- deterministic compiler option [Visual Basic]
- -deterministic compiler option [Visual Basic]
- -deterministic compiler option [Visual Basic]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 273abf8811f04cd7f58599ce3421ca1f17c740d9
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2018
---
# <a name="-deterministic"></a><span data-ttu-id="22408-102">-déterministe</span><span class="sxs-lookup"><span data-stu-id="22408-102">-deterministic</span></span>

<span data-ttu-id="22408-103">Indique au compilateur de produire un assembly dont la sortie octet est identique sur les compilations pour des entrées identiques.</span><span class="sxs-lookup"><span data-stu-id="22408-103">Causes the compiler to produce an assembly whose byte-for-byte output is identical across compilations for identical inputs.</span></span> 

## <a name="syntax"></a><span data-ttu-id="22408-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22408-104">Syntax</span></span>

```
-deterministic
```

## <a name="remarks"></a><span data-ttu-id="22408-105">Notes</span><span class="sxs-lookup"><span data-stu-id="22408-105">Remarks</span></span>

<span data-ttu-id="22408-106">Par défaut, les résultats de la compilation à partir d’un ensemble donné d’entrées est unique, étant donné que le compilateur ajoute un horodateur et un GUID qui est généré à partir de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="22408-106">By default, compiler output from a given set of inputs is unique, since the compiler adds a timestamp and a GUID that is generated from random numbers.</span></span> <span data-ttu-id="22408-107">Vous utilisez la `-deterministic` option pour générer un *assembly déterministe*, dont le contenu binaire est identique entre les compilations tant que l’entrée reste le même.</span><span class="sxs-lookup"><span data-stu-id="22408-107">You use the `-deterministic` option to produce a *deterministic assembly*, one whose binary content is identical across compilations as long as the input remains the same.</span></span>

<span data-ttu-id="22408-108">Le compilateur considère les entrées suivantes à des fins de déterminisme :</span><span class="sxs-lookup"><span data-stu-id="22408-108">The compiler considers the following inputs for the purpose of determinism:</span></span>

- <span data-ttu-id="22408-109">La séquence de paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="22408-109">The sequence of command-line parameters.</span></span>
- <span data-ttu-id="22408-110">Le contenu du fichier de réponse du compilateur .rsp.</span><span class="sxs-lookup"><span data-stu-id="22408-110">The contents of the compiler's .rsp response file.</span></span>
- <span data-ttu-id="22408-111">La version précise du compilateur utilisé et ses assemblys référencés.</span><span class="sxs-lookup"><span data-stu-id="22408-111">The precise version of the compiler used, and its referenced assemblies.</span></span>
- <span data-ttu-id="22408-112">Le chemin du répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="22408-112">The current directory path.</span></span>
- <span data-ttu-id="22408-113">Le contenu binaire de tous les fichiers explicitement passé au compilateur directement ou indirectement, y compris :</span><span class="sxs-lookup"><span data-stu-id="22408-113">The binary contents of all files explicitly passed to the compiler either directly or indirectly, including:</span></span> 
    - <span data-ttu-id="22408-114">Fichiers sources</span><span class="sxs-lookup"><span data-stu-id="22408-114">Source files</span></span>
    - <span data-ttu-id="22408-115">assemblys référencés</span><span class="sxs-lookup"><span data-stu-id="22408-115">Referenced assemblies</span></span>
    - <span data-ttu-id="22408-116">Modules référencés</span><span class="sxs-lookup"><span data-stu-id="22408-116">Referenced modules</span></span>
    - <span data-ttu-id="22408-117">Ressources</span><span class="sxs-lookup"><span data-stu-id="22408-117">Resources</span></span>
    - <span data-ttu-id="22408-118">Le fichier de clé de nom fort</span><span class="sxs-lookup"><span data-stu-id="22408-118">The strong name key file</span></span>
    - <span data-ttu-id="22408-119">@ fichiers réponse</span><span class="sxs-lookup"><span data-stu-id="22408-119">@ response files</span></span>
    - <span data-ttu-id="22408-120">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="22408-120">Analyzers</span></span>
    - <span data-ttu-id="22408-121">Groupes de règles</span><span class="sxs-lookup"><span data-stu-id="22408-121">Rulesets</span></span>
    - <span data-ttu-id="22408-122">Fichiers supplémentaires qui peuvent être utilisées par des analyseurs</span><span class="sxs-lookup"><span data-stu-id="22408-122">Additional files that may be used by analyzers</span></span>
- <span data-ttu-id="22408-123">La culture actuelle (pour le langage dans lequel les tests de diagnostic et exception messages sont produites).</span><span class="sxs-lookup"><span data-stu-id="22408-123">The current culture (for the language in which diagnostics and exception messages are produced).</span></span>
- <span data-ttu-id="22408-124">L’encodage par défaut (ou la page de codes en cours) si l’encodage n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="22408-124">The default encoding (or the current code page) if the encoding is not specified.</span></span>
- <span data-ttu-id="22408-125">L’existence, la non existence et le contenu des fichiers sur les chemins de recherche du compilateur (spécifié, par exemple, en `/lib` ou `/recurse`).</span><span class="sxs-lookup"><span data-stu-id="22408-125">The existence, non-existence, and contents of files on the compiler's search paths (specified, for example, by `/lib` or `/recurse`).</span></span>
- <span data-ttu-id="22408-126">La plateforme CLR sur lequel est exécuté le compilateur.</span><span class="sxs-lookup"><span data-stu-id="22408-126">The CLR platform on which the compiler is run.</span></span>
- <span data-ttu-id="22408-127">La valeur de `%LIBPATH%`, qui peut affecter le chargement de dépendance analyzer.</span><span class="sxs-lookup"><span data-stu-id="22408-127">The value of `%LIBPATH%`, which can affect analyzer dependency loading.</span></span>

<span data-ttu-id="22408-128">Lorsque les sources sont accessibles, compilation déterministe peut servir pour établir si un fichier binaire est compilé à partir d’une source approuvée.</span><span class="sxs-lookup"><span data-stu-id="22408-128">When sources are publicly available, deterministic compilation can be used for establishing whether a binary is compiled from a trusted source.</span></span> <span data-ttu-id="22408-129">Il peut également être utile dans un système de build en continu pour déterminer si les étapes de génération qui sont dépendantes des modifications apportées à un fichier binaire doivent être exécutée.</span><span class="sxs-lookup"><span data-stu-id="22408-129">It can also be useful in a continuous build system for determining whether build steps that are dependent on changes to a binary need to be executed.</span></span> 

## <a name="see-also"></a><span data-ttu-id="22408-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22408-130">See Also</span></span>
[<span data-ttu-id="22408-131">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="22408-131">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
[<span data-ttu-id="22408-132">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="22408-132">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
