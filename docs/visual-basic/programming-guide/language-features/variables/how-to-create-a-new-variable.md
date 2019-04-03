---
title: 'Procédure : Créer une Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Dim statement [Visual Basic]
- variables [Visual Basic], creating
ms.assetid: 35300be3-77b0-4bef-a156-034d3cdedde0
ms.openlocfilehash: 86236f7e6f4821cc45dfab80273d82b6f167fba8
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58823283"
---
# <a name="how-to-create-a-new-variable-visual-basic"></a><span data-ttu-id="c273d-102">Procédure : Créer une Variable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c273d-102">How to: Create a New Variable (Visual Basic)</span></span>
<span data-ttu-id="c273d-103">Vous créez une variable avec un [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md).</span><span class="sxs-lookup"><span data-stu-id="c273d-103">You create a variable with a [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md).</span></span>  
  
### <a name="to-create-a-new-variable"></a><span data-ttu-id="c273d-104">Pour créer une variable</span><span class="sxs-lookup"><span data-stu-id="c273d-104">To create a new variable</span></span>  
  
1.  <span data-ttu-id="c273d-105">Déclarez la variable dans un `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="c273d-105">Declare the variable in a `Dim` statement.</span></span>  
  
    ```  
    Dim newCustomer  
    ```  
  
2.  <span data-ttu-id="c273d-106">Inclure les spécifications des caractéristiques de la variable, tel que [privé](../../../../visual-basic/language-reference/modifiers/private.md), [statique](../../../../visual-basic/language-reference/modifiers/static.md), [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md), ou [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md).</span><span class="sxs-lookup"><span data-stu-id="c273d-106">Include specifications for the variable's characteristics, such as [Private](../../../../visual-basic/language-reference/modifiers/private.md), [Static](../../../../visual-basic/language-reference/modifiers/static.md), [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md), or [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md).</span></span> <span data-ttu-id="c273d-107">Pour plus d’informations, consultez [caractéristiques d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md).</span><span class="sxs-lookup"><span data-stu-id="c273d-107">For more information, see [Declared Element Characteristics](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md).</span></span>  
  
    ```  
    Public Static newCustomer  
    ```  
  
     <span data-ttu-id="c273d-108">Vous n’avez pas besoin du `Dim` mot clé si vous utilisez d’autres mots clés dans la déclaration.</span><span class="sxs-lookup"><span data-stu-id="c273d-108">You do not need the `Dim` keyword if you use other keywords in the declaration.</span></span>  
  
3.  <span data-ttu-id="c273d-109">Suivez les spécifications de nom de la variable, qui doit respecter les conventions et règles de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c273d-109">Follow the specifications with the variable's name, which must follow Visual Basic rules and conventions.</span></span> <span data-ttu-id="c273d-110">Pour plus d’informations, consultez [noms d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="c273d-110">For more information, see [Declared Element Names](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>  
  
    ```  
    Public Static newCustomer  
    ```  
  
4.  <span data-ttu-id="c273d-111">Faites suivre le nom de la [comme](../../../../visual-basic/language-reference/statements/as-clause.md) clause pour spécifier le type de données de la variable.</span><span class="sxs-lookup"><span data-stu-id="c273d-111">Follow the name with the [As](../../../../visual-basic/language-reference/statements/as-clause.md) clause to specify the variable's data type.</span></span>  
  
    ```  
    Public Static newCustomer As Customer  
    ```  
  
     <span data-ttu-id="c273d-112">Si vous ne spécifiez pas le type de données, il utilise la valeur par défaut : `Object`.</span><span class="sxs-lookup"><span data-stu-id="c273d-112">If you do not specify the data type, it uses the default: `Object`.</span></span>  
  
5.  <span data-ttu-id="c273d-113">Suivez le `As` clause avec un signe égal (`=`) et suivez le signe égal avec la valeur initiale de la variable.</span><span class="sxs-lookup"><span data-stu-id="c273d-113">Follow the `As` clause with an equal sign (`=`) and follow the equal sign with the variable's initial value.</span></span>  
  
     <span data-ttu-id="c273d-114">Visual Basic assigne la valeur spécifiée à la variable à chaque fois qu’il exécute la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="c273d-114">Visual Basic assigns the specified value to the variable every time it runs the `Dim` statement.</span></span> <span data-ttu-id="c273d-115">Si vous ne spécifiez pas une valeur initiale, Visual Basic assigne la valeur initiale par défaut pour le type de données de la variable lorsqu’elle tout d’abord entre le code qui contient le `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="c273d-115">If you do not specify an initial value, Visual Basic assigns the default initial value for the variable's data type when it first enters the code that contains the `Dim` statement.</span></span>  
  
     <span data-ttu-id="c273d-116">Si la variable est un type référence, vous pouvez créer une instance de sa classe en incluant le [nouvel opérateur](../../../../visual-basic/language-reference/operators/new-operator.md) mot clé dans le `As` clause.</span><span class="sxs-lookup"><span data-stu-id="c273d-116">If the variable is a reference type, you can create an instance of its class by including the [New Operator](../../../../visual-basic/language-reference/operators/new-operator.md) keyword in the `As` clause.</span></span> <span data-ttu-id="c273d-117">Si vous n’utilisez pas `New`, la valeur initiale de la variable est [rien](../../../../visual-basic/language-reference/nothing.md).</span><span class="sxs-lookup"><span data-stu-id="c273d-117">If you do not use `New`, the initial value of the variable is [Nothing](../../../../visual-basic/language-reference/nothing.md).</span></span>  
  
    ```  
    Public Static newCustomer As New Customer  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="c273d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c273d-118">See also</span></span>

- [<span data-ttu-id="c273d-119">Variables</span><span class="sxs-lookup"><span data-stu-id="c273d-119">Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/index.md)
- [<span data-ttu-id="c273d-120">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="c273d-120">Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="c273d-121">Noms d’éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="c273d-121">Declared Element Names</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="c273d-122">Caractéristiques d’éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="c273d-122">Declared Element Characteristics</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md)
- [<span data-ttu-id="c273d-123">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="c273d-123">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [<span data-ttu-id="c273d-124">Instructions</span><span class="sxs-lookup"><span data-stu-id="c273d-124">Statements</span></span>](../../../../visual-basic/language-reference/statements/index.md)
- [<span data-ttu-id="c273d-125">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="c273d-125">Local Type Inference</span></span>](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="c273d-126">Option Infer (instruction)</span><span class="sxs-lookup"><span data-stu-id="c273d-126">Option Infer Statement</span></span>](../../../../visual-basic/language-reference/statements/option-infer-statement.md)
