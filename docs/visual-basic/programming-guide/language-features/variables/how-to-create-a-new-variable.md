---
title: 'Comment : créer une variable (Visual Basic)'
ms.custom: ''
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Dim statement [Visual Basic]
- variables [Visual Basic], creating
ms.assetid: 35300be3-77b0-4bef-a156-034d3cdedde0
caps.latest.revision: 29
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: aff160584d3d1fe382020d5b8c25ac57dab66d92
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-create-a-new-variable-visual-basic"></a><span data-ttu-id="4048e-102">Comment : créer une variable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4048e-102">How to: Create a New Variable (Visual Basic)</span></span>
<span data-ttu-id="4048e-103">Vous créez une variable avec un [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md).</span><span class="sxs-lookup"><span data-stu-id="4048e-103">You create a variable with a [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md).</span></span>  
  
### <a name="to-create-a-new-variable"></a><span data-ttu-id="4048e-104">Pour créer une variable</span><span class="sxs-lookup"><span data-stu-id="4048e-104">To create a new variable</span></span>  
  
1.  <span data-ttu-id="4048e-105">Déclarez la variable dans un `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="4048e-105">Declare the variable in a `Dim` statement.</span></span>  
  
    ```  
    Dim newCustomer  
    ```  
  
2.  <span data-ttu-id="4048e-106">Inclure les spécifications pour les caractéristiques de la variable, tel que [privé](../../../../visual-basic/language-reference/modifiers/private.md), [statique](../../../../visual-basic/language-reference/modifiers/static.md), [ombres](../../../../visual-basic/language-reference/modifiers/shadows.md), ou [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md).</span><span class="sxs-lookup"><span data-stu-id="4048e-106">Include specifications for the variable's characteristics, such as [Private](../../../../visual-basic/language-reference/modifiers/private.md), [Static](../../../../visual-basic/language-reference/modifiers/static.md), [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md), or [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md).</span></span> <span data-ttu-id="4048e-107">Pour plus d’informations, consultez [caractéristiques de l’élément déclaré](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md).</span><span class="sxs-lookup"><span data-stu-id="4048e-107">For more information, see [Declared Element Characteristics](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md).</span></span>  
  
    ```  
    Public Static newCustomer  
    ```  
  
     <span data-ttu-id="4048e-108">Vous n’avez pas besoin du `Dim` mot clé si vous utilisez d’autres mots clés dans la déclaration.</span><span class="sxs-lookup"><span data-stu-id="4048e-108">You do not need the `Dim` keyword if you use other keywords in the declaration.</span></span>  
  
3.  <span data-ttu-id="4048e-109">Suivez les spécifications de nom de la variable qui doit respecter les conventions et les règles de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4048e-109">Follow the specifications with the variable's name, which must follow Visual Basic rules and conventions.</span></span> <span data-ttu-id="4048e-110">Pour plus d’informations, consultez [noms d’élément déclaré](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="4048e-110">For more information, see [Declared Element Names](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>  
  
    ```  
    Public Static newCustomer  
    ```  
  
4.  <span data-ttu-id="4048e-111">Suivre le nom de la [comme](../../../../visual-basic/language-reference/statements/as-clause.md) clause pour spécifier le type de données de la variable.</span><span class="sxs-lookup"><span data-stu-id="4048e-111">Follow the name with the [As](../../../../visual-basic/language-reference/statements/as-clause.md) clause to specify the variable's data type.</span></span>  
  
    ```  
    Public Static newCustomer As Customer  
    ```  
  
     <span data-ttu-id="4048e-112">Si vous ne spécifiez pas le type de données, il utilise la valeur par défaut : `Object`.</span><span class="sxs-lookup"><span data-stu-id="4048e-112">If you do not specify the data type, it uses the default: `Object`.</span></span>  
  
5.  <span data-ttu-id="4048e-113">Suivez les `As` clause avec un signe égal (`=`) et suivez le signe égal, la valeur de la variable initiale.</span><span class="sxs-lookup"><span data-stu-id="4048e-113">Follow the `As` clause with an equal sign (`=`) and follow the equal sign with the variable's initial value.</span></span>  
  
     <span data-ttu-id="4048e-114">Visual Basic assigne la valeur spécifiée à la variable à chaque fois qu’il exécute la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="4048e-114">Visual Basic assigns the specified value to the variable every time it runs the `Dim` statement.</span></span> <span data-ttu-id="4048e-115">Si vous ne spécifiez pas une valeur initiale, Visual Basic assigne la valeur initiale de la valeur par défaut pour le type de données de la variable lorsqu’il entre d’abord dans le code qui contient la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="4048e-115">If you do not specify an initial value, Visual Basic assigns the default initial value for the variable's data type when it first enters the code that contains the `Dim` statement.</span></span>  
  
     <span data-ttu-id="4048e-116">Si la variable est un type référence, vous pouvez créer une instance de la classe en incluant le [nouvel opérateur](../../../../visual-basic/language-reference/operators/new-operator.md) mot clé dans le `As` clause.</span><span class="sxs-lookup"><span data-stu-id="4048e-116">If the variable is a reference type, you can create an instance of its class by including the [New Operator](../../../../visual-basic/language-reference/operators/new-operator.md) keyword in the `As` clause.</span></span> <span data-ttu-id="4048e-117">Si vous n’utilisez pas `New`, la valeur initiale de la variable est [rien](../../../../visual-basic/language-reference/nothing.md).</span><span class="sxs-lookup"><span data-stu-id="4048e-117">If you do not use `New`, the initial value of the variable is [Nothing](../../../../visual-basic/language-reference/nothing.md).</span></span>  
  
    ```  
    Public Static newCustomer As New Customer  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="4048e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4048e-118">See Also</span></span>  
 [<span data-ttu-id="4048e-119">Variables</span><span class="sxs-lookup"><span data-stu-id="4048e-119">Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/index.md)  
 [<span data-ttu-id="4048e-120">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="4048e-120">Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)  
 [<span data-ttu-id="4048e-121">Noms d’éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="4048e-121">Declared Element Names</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)  
 [<span data-ttu-id="4048e-122">Caractéristiques d’éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="4048e-122">Declared Element Characteristics</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md)  
 [<span data-ttu-id="4048e-123">Types valeur et types référence</span><span class="sxs-lookup"><span data-stu-id="4048e-123">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)  
 [<span data-ttu-id="4048e-124">Instructions</span><span class="sxs-lookup"><span data-stu-id="4048e-124">Statements</span></span>](../../../../visual-basic/language-reference/statements/index.md)  
 [<span data-ttu-id="4048e-125">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="4048e-125">Local Type Inference</span></span>](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)  
 [<span data-ttu-id="4048e-126">Option Infer (instruction)</span><span class="sxs-lookup"><span data-stu-id="4048e-126">Option Infer Statement</span></span>](../../../../visual-basic/language-reference/statements/option-infer-statement.md)
