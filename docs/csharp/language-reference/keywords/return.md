---
title: return, instruction - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- return_CSharpKeyword
- return
helpviewer_keywords:
- return statement [C#]
- return keyword [C#]
ms.assetid: 6da6e152-5b58-4448-8f3f-470dd0617ecd
ms.openlocfilehash: 058dc1d51099196559bee4ec2b96dc883e813f93
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236555"
---
# <a name="return-c-reference"></a><span data-ttu-id="fdc15-102">return (référence C#)</span><span class="sxs-lookup"><span data-stu-id="fdc15-102">return (C# Reference)</span></span>

<span data-ttu-id="fdc15-103">L’instruction `return` met un terme à l’exécution de la méthode dans laquelle elle apparaît et retourne le contrôle à la méthode d’appel.</span><span class="sxs-lookup"><span data-stu-id="fdc15-103">The `return` statement terminates execution of the method in which it appears and returns control to the calling method.</span></span> <span data-ttu-id="fdc15-104">Elle peut également retourner une valeur facultative.</span><span class="sxs-lookup"><span data-stu-id="fdc15-104">It can also return an optional value.</span></span> <span data-ttu-id="fdc15-105">Si la méthode est un type `void`, l’instruction `return` peut être omise.</span><span class="sxs-lookup"><span data-stu-id="fdc15-105">If the method is a `void` type, the `return` statement can be omitted.</span></span>

 <span data-ttu-id="fdc15-106">Si l’instruction return est à l’intérieur d’un bloc `try`, le bloc `finally`, le cas échéant, est exécuté avant que le contrôle retourne à la méthode d’appel.</span><span class="sxs-lookup"><span data-stu-id="fdc15-106">If the return statement is inside a `try` block, the `finally` block, if one exists, will be executed before control returns to the calling method.</span></span>

## <a name="example"></a><span data-ttu-id="fdc15-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="fdc15-107">Example</span></span>

 <span data-ttu-id="fdc15-108">Dans l’exemple suivant, la méthode `CalculateArea()` retourne la variable locale `area` en tant que valeur [double](double.md).</span><span class="sxs-lookup"><span data-stu-id="fdc15-108">In the following example, the method `CalculateArea()` returns the local variable `area` as a [double](double.md) value.</span></span>

[!code-csharp[csrefKeywordsJump#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#6)]  

## <a name="c-language-specification"></a><span data-ttu-id="fdc15-109">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="fdc15-109">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="fdc15-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdc15-110">See also</span></span>

- [<span data-ttu-id="fdc15-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="fdc15-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="fdc15-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="fdc15-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="fdc15-113">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="fdc15-113">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="fdc15-114">Instruction return</span><span class="sxs-lookup"><span data-stu-id="fdc15-114">return Statement</span></span>](/cpp/cpp/return-statement-cpp)
- [<span data-ttu-id="fdc15-115">Instructions de saut</span><span class="sxs-lookup"><span data-stu-id="fdc15-115">Jump Statements</span></span>](jump-statements.md)
