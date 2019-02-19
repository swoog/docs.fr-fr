---
title: Guide pratique pour utiliser le bloc try/catch pour intercepter des exceptions
ms.date: 02/06/2019
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- exceptions, try/catch blocks
- try blocks
- try/catch blocks
- catch blocks
ms.assetid: a3ce6dfd-1f64-471b-8ad8-8cfaf406275d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5183a854ee2b7462ecc27786a5fc0697565194c0
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56092746"
---
# <a name="how-to-use-the-trycatch-block-to-catch-exceptions"></a><span data-ttu-id="8efbb-102">Guide pratique pour utiliser le bloc try/catch pour intercepter des exceptions</span><span class="sxs-lookup"><span data-stu-id="8efbb-102">How to use the try/catch block to catch exceptions</span></span>

<span data-ttu-id="8efbb-103">Placez les instructions de code qui peuvent déclencher ou lever une exception dans un bloc `try` et placez les instructions utilisées pour gérer l’exception ou les exceptions dans un ou plusieurs blocs `catch` sous le bloc `try`.</span><span class="sxs-lookup"><span data-stu-id="8efbb-103">Place any code statements that might raise or throw an exception in a `try` block, and place statements used to handle the exception or exceptions in one or more `catch` blocks below the `try` block.</span></span> <span data-ttu-id="8efbb-104">Chaque bloc `catch` inclut le type d’exception et peut contenir des instructions supplémentaires nécessaires pour gérer ce type d’exception.</span><span class="sxs-lookup"><span data-stu-id="8efbb-104">Each `catch` block includes the exception type and can contain additional statements needed to handle that exception type.</span></span>

<span data-ttu-id="8efbb-105">Dans l’exemple suivant, un <xref:System.IO.StreamReader> ouvre un fichier appelé *data.txt* et récupère une ligne de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="8efbb-105">In the following example, a <xref:System.IO.StreamReader> opens a file called *data.txt* and retrieves a line from the file.</span></span> <span data-ttu-id="8efbb-106">Étant donné que le code peut lever une des trois exceptions, il est placé dans un bloc `try`.</span><span class="sxs-lookup"><span data-stu-id="8efbb-106">Since the code might throw any of three exceptions, it's placed in a `try` block.</span></span> <span data-ttu-id="8efbb-107">Trois blocs `catch` interceptent les exceptions et les gèrent en affichant les résultats dans la console.</span><span class="sxs-lookup"><span data-stu-id="8efbb-107">Three `catch` blocks catch the exceptions and handle them by displaying the results to the console.</span></span>

[!code-csharp[CatchException#3](~/samples/snippets/csharp/VS_Snippets_CLR/CatchException/CS/catchexception2.cs#3)]
[!code-vb[CatchException#3](~/samples/snippets/visualbasic/VS_Snippets_CLR/CatchException/VB/catchexception2.vb#3)]  

<span data-ttu-id="8efbb-108">Le Common Language Runtime (CLR) intercepte les exceptions non gérées par les blocs `catch`.</span><span class="sxs-lookup"><span data-stu-id="8efbb-108">The Common Language Runtime (CLR) catches exceptions not handled by `catch` blocks.</span></span> <span data-ttu-id="8efbb-109">Si une exception est interceptée par le CLR, il peut se produire l’un des résultats suivants selon la configuration du CLR :</span><span class="sxs-lookup"><span data-stu-id="8efbb-109">If an exception is caught by the CLR, one of the following results may occur depending on your CLR configuration:</span></span>

- <span data-ttu-id="8efbb-110">Une boîte de dialogue **Débogage** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8efbb-110">A **Debug** dialog box appears.</span></span>
- <span data-ttu-id="8efbb-111">Le programme s’arrête et une boîte de dialogue d’information sur l’exception s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8efbb-111">The program stops execution and a dialog box with exception information appears.</span></span>
- <span data-ttu-id="8efbb-112">Une erreur s’affiche dans le [flux de sortie d’erreur standard](xref:System.Console.Error).</span><span class="sxs-lookup"><span data-stu-id="8efbb-112">An error prints out to the [standard error output stream](xref:System.Console.Error).</span></span>

> [!NOTE]
> <span data-ttu-id="8efbb-113">La plupart du code peut lever une exception, et quelques exceptions comme <xref:System.OutOfMemoryException> peuvent être levées par le CLR lui-même à tout moment.</span><span class="sxs-lookup"><span data-stu-id="8efbb-113">Most code can throw an exception, and some exceptions, like <xref:System.OutOfMemoryException>, can be thrown by the CLR itself at any time.</span></span> <span data-ttu-id="8efbb-114">L’utilisation d’applications n’est pas obligatoire pour traiter ces exceptions, mais envisagez cette possibilité quand vous écrivez des bibliothèques destinées à l’usage d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8efbb-114">While applications aren't required to deal with these exceptions, be aware of the possibility when writing libraries to be used by others.</span></span> <span data-ttu-id="8efbb-115">Si vous souhaitez des conseils sur la définition de code dans un bloc `try`, consultez [Bonnes pratiques pour les exceptions](best-practices-for-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="8efbb-115">For suggestions on when to set code in a `try` block, see [Best Practices for Exceptions](best-practices-for-exceptions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8efbb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8efbb-116">See also</span></span>

[<span data-ttu-id="8efbb-117">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8efbb-117">Exceptions</span></span>](index.md)  
[<span data-ttu-id="8efbb-118">Gestion des erreurs E/S dans .NET</span><span class="sxs-lookup"><span data-stu-id="8efbb-118">Handling I/O errors in .NET</span></span>](../io/handling-io-errors.md)
