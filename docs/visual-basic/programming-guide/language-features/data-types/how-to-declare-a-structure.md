---
title: 'Procédure : Déclarer une Structure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- declarations [Visual Basic], structures
- structure statements [Visual Basic]
- statements [Visual Basic], structure
- structures [Visual Basic], declaring
ms.assetid: d5e98381-eb81-47d4-af83-48cc534a2572
ms.openlocfilehash: 7fc4aed4d405729b64a2f7ba772cdd794df40f2a
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58825091"
---
# <a name="how-to-declare-a-structure-visual-basic"></a><span data-ttu-id="58c7b-102">Procédure : Déclarer une Structure (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="58c7b-102">How to: Declare a Structure (Visual Basic)</span></span>
<span data-ttu-id="58c7b-103">Vous commencez une déclaration de structure par le [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md), vous vous retrouvez avec la `End Structure` instruction.</span><span class="sxs-lookup"><span data-stu-id="58c7b-103">You begin a structure declaration with the [Structure Statement](../../../../visual-basic/language-reference/statements/structure-statement.md), and you end it with the `End Structure` statement.</span></span> <span data-ttu-id="58c7b-104">Entre ces deux instructions, vous devez déclarer au moins un *élément*.</span><span class="sxs-lookup"><span data-stu-id="58c7b-104">Between these two statements you must declare at least one *element*.</span></span> <span data-ttu-id="58c7b-105">Les éléments peuvent être de n’importe quel type de données, mais au moins un doit être une variable non partagée ou un événement non partagé.</span><span class="sxs-lookup"><span data-stu-id="58c7b-105">The elements can be of any data type, but at least one must be either a nonshared variable or a nonshared, noncustom event.</span></span>  
  
 <span data-ttu-id="58c7b-106">Vous ne peut pas initialiser un des éléments de structure dans la déclaration de structure.</span><span class="sxs-lookup"><span data-stu-id="58c7b-106">You cannot initialize any of the structure elements in the structure declaration.</span></span> <span data-ttu-id="58c7b-107">Lorsque vous déclarez une variable comme étant d’un type structure, vous attribuez des valeurs aux éléments en y accédant via la variable.</span><span class="sxs-lookup"><span data-stu-id="58c7b-107">When you declare a variable to be of a structure type, you assign values to the elements by accessing them through the variable.</span></span>  
  
 <span data-ttu-id="58c7b-108">Pour une explication des différences entre les classes et structures, consultez [Structures et Classes](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="58c7b-108">For a discussion of the differences between structures and classes, see [Structures and Classes](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md).</span></span>  
  
 <span data-ttu-id="58c7b-109">À des fins de démonstration, considérez une situation où vous souhaitez effectuer le suivi de nom d’un employé, numéro de poste et salaire.</span><span class="sxs-lookup"><span data-stu-id="58c7b-109">For demonstration purposes, consider a situation where you want to keep track of an employee's name, telephone extension, and salary.</span></span> <span data-ttu-id="58c7b-110">Une structure vous permet de procéder dans une variable unique.</span><span class="sxs-lookup"><span data-stu-id="58c7b-110">A structure allows you to do this in a single variable.</span></span>  
  
### <a name="to-declare-a-structure"></a><span data-ttu-id="58c7b-111">Pour déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="58c7b-111">To declare a structure</span></span>  
  
1.  <span data-ttu-id="58c7b-112">Créer le début et fin des instructions pour la structure.</span><span class="sxs-lookup"><span data-stu-id="58c7b-112">Create the beginning and ending statements for the structure.</span></span>  
  
     <span data-ttu-id="58c7b-113">Vous pouvez spécifier le niveau d’accès d’une structure en utilisant le [Public](../../../../visual-basic/language-reference/modifiers/public.md), [protégé](../../../../visual-basic/language-reference/modifiers/protected.md), [Friend](../../../../visual-basic/language-reference/modifiers/friend.md), ou [privé](../../../../visual-basic/language-reference/modifiers/private.md) mot clé, ou vous pouvez la laisser la valeur par défaut `Public`.</span><span class="sxs-lookup"><span data-stu-id="58c7b-113">You can specify the access level of a structure using the [Public](../../../../visual-basic/language-reference/modifiers/public.md), [Protected](../../../../visual-basic/language-reference/modifiers/protected.md), [Friend](../../../../visual-basic/language-reference/modifiers/friend.md), or [Private](../../../../visual-basic/language-reference/modifiers/private.md) keyword, or you can let it default to `Public`.</span></span>  
  
    ```  
    Private Structure employee  
    End Structure  
    ```  
  
2.  <span data-ttu-id="58c7b-114">Ajouter des éléments au corps de la structure.</span><span class="sxs-lookup"><span data-stu-id="58c7b-114">Add elements to the body of the structure.</span></span>  
  
     <span data-ttu-id="58c7b-115">Une structure doit avoir au moins un élément.</span><span class="sxs-lookup"><span data-stu-id="58c7b-115">A structure must have at least one element.</span></span> <span data-ttu-id="58c7b-116">Vous devez déclarer chaque élément et lui attribuer un niveau d’accès.</span><span class="sxs-lookup"><span data-stu-id="58c7b-116">You must declare every element and specify an access level for it.</span></span> <span data-ttu-id="58c7b-117">Si vous utilisez le [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) sans les mots clés, l’accessibilité par défaut est `Public`.</span><span class="sxs-lookup"><span data-stu-id="58c7b-117">If you use the [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md) without any keywords, the accessibility defaults to `Public`.</span></span>  
  
    ```  
    Private Structure employee  
        Public givenName As String  
        Public familyName As String  
        Public phoneExtension As Long  
        Private salary As Decimal  
        Public Sub giveRaise(raise As Double)  
            salary *= raise  
        End Sub  
        Public Event salaryReviewTime()  
    End Structure  
    ```  
  
     <span data-ttu-id="58c7b-118">Le `salary` champ dans l’exemple précédent est `Private`, ce qui signifie qu’il n’est pas accessible en dehors de la structure, même à partir de la classe conteneur.</span><span class="sxs-lookup"><span data-stu-id="58c7b-118">The `salary` field in the preceding example is `Private`, which means it is inaccessible outside the structure, even from the containing class.</span></span> <span data-ttu-id="58c7b-119">Toutefois, le `giveRaise` procédure est `Public`, donc elle peut être appelée à partir de l’extérieur de la structure.</span><span class="sxs-lookup"><span data-stu-id="58c7b-119">However, the `giveRaise` procedure is `Public`, so it can be called from outside the structure.</span></span> <span data-ttu-id="58c7b-120">De même, vous pouvez déclencher la `salaryReviewTime` événement en dehors de la structure de.</span><span class="sxs-lookup"><span data-stu-id="58c7b-120">Similarly, you can raise the `salaryReviewTime` event from outside the structure.</span></span>  
  
     <span data-ttu-id="58c7b-121">En plus des variables, `Sub` procédures et événements, vous pouvez également définir des constantes, `Function` procédures et des propriétés dans une structure.</span><span class="sxs-lookup"><span data-stu-id="58c7b-121">In addition to variables, `Sub` procedures, and events, you can also define constants, `Function` procedures, and properties in a structure.</span></span> <span data-ttu-id="58c7b-122">Vous pouvez désigner au plus une propriété comme le *propriété par défaut*, à condition qu’elle accepte au moins un argument.</span><span class="sxs-lookup"><span data-stu-id="58c7b-122">You can designate at most one property as the *default property*, provided it takes at least one argument.</span></span> <span data-ttu-id="58c7b-123">Vous pouvez gérer un événement avec un [partagé](../../../../visual-basic/language-reference/modifiers/shared.md) `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="58c7b-123">You can handle an event with a [Shared](../../../../visual-basic/language-reference/modifiers/shared.md)`Sub` procedure.</span></span> <span data-ttu-id="58c7b-124">Pour plus d'informations, voir [Procédure : Déclarer et appeler une propriété par défaut en Visual Basic](../../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-and-call-a-default-property.md).</span><span class="sxs-lookup"><span data-stu-id="58c7b-124">For more information, see [How to: Declare and Call a Default Property in Visual Basic](../../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-and-call-a-default-property.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58c7b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58c7b-125">See also</span></span>

- [<span data-ttu-id="58c7b-126">Types de données</span><span class="sxs-lookup"><span data-stu-id="58c7b-126">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [<span data-ttu-id="58c7b-127">Types de données élémentaires</span><span class="sxs-lookup"><span data-stu-id="58c7b-127">Elementary Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)
- [<span data-ttu-id="58c7b-128">Types de données composites</span><span class="sxs-lookup"><span data-stu-id="58c7b-128">Composite Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)
- [<span data-ttu-id="58c7b-129">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="58c7b-129">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [<span data-ttu-id="58c7b-130">Structures</span><span class="sxs-lookup"><span data-stu-id="58c7b-130">Structures</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="58c7b-131">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="58c7b-131">Troubleshooting Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="58c7b-132">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="58c7b-132">Structure Variables</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structure-variables.md)
- [<span data-ttu-id="58c7b-133">Structures et autres éléments de programmation</span><span class="sxs-lookup"><span data-stu-id="58c7b-133">Structures and Other Programming Elements</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-other-programming-elements.md)
- [<span data-ttu-id="58c7b-134">Structures et classes</span><span class="sxs-lookup"><span data-stu-id="58c7b-134">Structures and Classes</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md)
- [<span data-ttu-id="58c7b-135">Type de données défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="58c7b-135">User-Defined Data Type</span></span>](../../../../visual-basic/language-reference/data-types/user-defined-data-type.md)
