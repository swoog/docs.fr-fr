---
title: 'Procédure : Déterminer le Type désigné par une Variable d’objet (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- TypeOf operator [Visual Basic], determining object variable type
- variables [Visual Basic], object
- object variables [Visual Basic], determining type
ms.assetid: 6f6a138d-58a4-40d1-9f4e-0a3c598eaf81
ms.openlocfilehash: 6499dfce880cc9ce16e5d77887afc0598692f48e
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59342867"
---
# <a name="how-to-determine-what-type-an-object-variable-refers-to-visual-basic"></a><span data-ttu-id="071af-102">Procédure : Déterminer le Type désigné par une Variable d’objet (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="071af-102">How to: Determine What Type an Object Variable Refers To (Visual Basic)</span></span>
<span data-ttu-id="071af-103">Une variable objet contient un pointeur vers les données stockées ailleurs.</span><span class="sxs-lookup"><span data-stu-id="071af-103">An object variable contains a pointer to data that is stored elsewhere.</span></span> <span data-ttu-id="071af-104">Le type de ces données peut changer pendant l’exécution.</span><span class="sxs-lookup"><span data-stu-id="071af-104">The type of that data can change during run time.</span></span> <span data-ttu-id="071af-105">À tout moment, vous pouvez utiliser la <xref:System.Type.GetTypeCode%2A> méthode pour déterminer le type d’exécution actuel, ou le [TypeOf, opérateur](../../../../visual-basic/language-reference/operators/typeof-operator.md) pour déterminer si l’actuel type au moment de l’exécution est compatible avec un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="071af-105">At any moment, you can use the <xref:System.Type.GetTypeCode%2A> method to determine the current run-time type, or the [TypeOf Operator](../../../../visual-basic/language-reference/operators/typeof-operator.md) to find out if the current run-time type is compatible with a specified type.</span></span>  
  
### <a name="to-determine-the-exact-type-an-object-variable-currently-refers-to"></a><span data-ttu-id="071af-106">Pour déterminer que le type exact auquel une variable objet actuellement fait référence à</span><span class="sxs-lookup"><span data-stu-id="071af-106">To determine the exact type an object variable currently refers to</span></span>  
  
1. <span data-ttu-id="071af-107">Sur la variable objet, appelez le <xref:System.Object.GetType%2A> méthode pour récupérer un <xref:System.Type?displayProperty=nameWithType> objet.</span><span class="sxs-lookup"><span data-stu-id="071af-107">On the object variable, call the <xref:System.Object.GetType%2A> method to retrieve a <xref:System.Type?displayProperty=nameWithType> object.</span></span>  
  
    ```  
    Dim myObject As Object  
    myObject.GetType()  
    ```  
  
2. <span data-ttu-id="071af-108">Sur le <xref:System.Type?displayProperty=nameWithType> de classe, appelez la méthode partagée <xref:System.Type.GetTypeCode%2A> pour récupérer le <xref:System.TypeCode> valeur d’énumération pour le type d’objet.</span><span class="sxs-lookup"><span data-stu-id="071af-108">On the <xref:System.Type?displayProperty=nameWithType> class, call the shared method <xref:System.Type.GetTypeCode%2A> to retrieve the <xref:System.TypeCode> enumeration value for the object's type.</span></span>  
  
    ```  
    Dim myObject As Object  
    Dim datTyp As Integer = Type.GetTypeCode(myObject.GetType())  
    MsgBox("myObject currently has type code " & CStr(datTyp))  
    ```  
  
     <span data-ttu-id="071af-109">Vous pouvez tester le <xref:System.TypeCode> valeur d’énumération par rapport à tout membre d’énumération est dignes d’intérêt, telles que `Double`.</span><span class="sxs-lookup"><span data-stu-id="071af-109">You can test the <xref:System.TypeCode> enumeration value against whichever enumeration members are of interest, such as `Double`.</span></span>  
  
### <a name="to-determine-whether-an-object-variables-type-is-compatible-with-a-specified-type"></a><span data-ttu-id="071af-110">Pour déterminer si un objet type de variable est compatible avec un type spécifié</span><span class="sxs-lookup"><span data-stu-id="071af-110">To determine whether an object variable's type is compatible with a specified type</span></span>  
  
-   <span data-ttu-id="071af-111">Utilisez le `TypeOf` opérateur en association avec le [opérateur Is](../../../../visual-basic/language-reference/operators/is-operator.md) pour tester l’objet avec un `TypeOf`... `Is` expression.</span><span class="sxs-lookup"><span data-stu-id="071af-111">Use the `TypeOf` operator in combination with the [Is Operator](../../../../visual-basic/language-reference/operators/is-operator.md) to test the object with a `TypeOf`...`Is` expression.</span></span>  
  
    ```  
    If TypeOf objA Is System.Windows.Forms.Control Then  
        MsgBox("objA is compatible with the Control class")  
    End If  
    ```  
  
     <span data-ttu-id="071af-112">Le `TypeOf`... `Is` expression retourne `True` si l’objet de l’exécution type est compatible avec le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="071af-112">The `TypeOf`...`Is` expression returns `True` if the object's run-time type is compatible with the specified type.</span></span>  
  
     <span data-ttu-id="071af-113">Le critère de compatibilité varie selon que le type spécifié est une classe, une structure ou une interface.</span><span class="sxs-lookup"><span data-stu-id="071af-113">The criterion for compatibility depends on whether the specified type is a class, structure, or interface.</span></span> <span data-ttu-id="071af-114">En règle générale, les types sont compatibles si l’objet est du même type que, hérite ou implémente le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="071af-114">In general, the types are compatible if the object is of the same type as, inherits from, or implements the specified type.</span></span> <span data-ttu-id="071af-115">Pour plus d’informations, consultez [TypeOf, opérateur](../../../../visual-basic/language-reference/operators/typeof-operator.md).</span><span class="sxs-lookup"><span data-stu-id="071af-115">For more information, see [TypeOf Operator](../../../../visual-basic/language-reference/operators/typeof-operator.md).</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="071af-116">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="071af-116">Compiling the Code</span></span>  
 <span data-ttu-id="071af-117">Notez que le type spécifié ne peut pas être une variable ou une expression.</span><span class="sxs-lookup"><span data-stu-id="071af-117">Note that the specified type cannot be a variable or expression.</span></span> <span data-ttu-id="071af-118">Il doit être le nom d’un type défini, comme une classe, une structure ou une interface.</span><span class="sxs-lookup"><span data-stu-id="071af-118">It must be the name of a defined type, such as a class, structure, or interface.</span></span> <span data-ttu-id="071af-119">Cela inclut les types intrinsèques tels que `Integer` et `String`.</span><span class="sxs-lookup"><span data-stu-id="071af-119">This includes intrinsic types such as `Integer` and `String`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="071af-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="071af-120">See also</span></span>

- <xref:System.Object.GetType%2A>
- <xref:System.Type?displayProperty=nameWithType>
- <xref:System.Type.GetTypeCode%2A>
- <xref:System.TypeCode>
- [<span data-ttu-id="071af-121">Variables objets</span><span class="sxs-lookup"><span data-stu-id="071af-121">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [<span data-ttu-id="071af-122">Valeurs des variables objets</span><span class="sxs-lookup"><span data-stu-id="071af-122">Object Variable Values</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-values.md)
- [<span data-ttu-id="071af-123">Object Data Type</span><span class="sxs-lookup"><span data-stu-id="071af-123">Object Data Type</span></span>](../../../../visual-basic/language-reference/data-types/object-data-type.md)
