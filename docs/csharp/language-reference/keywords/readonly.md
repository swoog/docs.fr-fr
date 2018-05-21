---
title: readonly (référence C#)
ms.date: 07/20/2015
f1_keywords:
- readonly_CSharpKeyword
- readonly
helpviewer_keywords:
- readonly keyword [C#]
ms.assetid: 2f8081f6-0de2-4903-898d-99696c48d2f4
ms.openlocfilehash: d2f8a2f192dc319ad806aeef4bfbaeecc44b07a3
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="readonly-c-reference"></a><span data-ttu-id="8a970-102">readonly (référence C#)</span><span class="sxs-lookup"><span data-stu-id="8a970-102">readonly (C# Reference)</span></span>
<span data-ttu-id="8a970-103">Le mot clé `readonly` est un modificateur que vous pouvez utiliser sur des champs.</span><span class="sxs-lookup"><span data-stu-id="8a970-103">The `readonly` keyword is a modifier that you can use on fields.</span></span> <span data-ttu-id="8a970-104">Lorsqu’une déclaration de champ inclut un modificateur `readonly`, les assignations aux champs introduites par la déclaration peuvent se produire uniquement dans le cadre de la déclaration ou dans un constructeur de la même classe.</span><span class="sxs-lookup"><span data-stu-id="8a970-104">When a field declaration includes a `readonly` modifier, assignments to the fields introduced by the declaration can only occur as part of the declaration or in a constructor in the same class.</span></span>  
  
## <a name="readonly-field-example"></a><span data-ttu-id="8a970-105">Exemple de champ en lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a970-105">Readonly field example</span></span>  
 <span data-ttu-id="8a970-106">Dans cet exemple, la valeur du champ `year` ne peut pas être modifiée dans la méthode `ChangeYear`, même si une valeur lui est affectée dans le constructeur de classe :</span><span class="sxs-lookup"><span data-stu-id="8a970-106">In this example, the value of the field `year` cannot be changed in the method `ChangeYear`, even though it is assigned a value in the class constructor:</span></span>  
  
 [!code-csharp[csrefKeywordsModifiers#14](../../../csharp/language-reference/keywords/codesnippet/CSharp/readonly_1.cs)]  
  
 <span data-ttu-id="8a970-107">Vous pouvez affecter une valeur à un champ `readonly` uniquement dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="8a970-107">You can assign a value to a `readonly` field only in the following contexts:</span></span>  
  
-   <span data-ttu-id="8a970-108">Lorsque la variable est initialisée dans la déclaration, par exemple :</span><span class="sxs-lookup"><span data-stu-id="8a970-108">When the variable is initialized in the declaration, for example:</span></span>  
  
    ```csharp  
    public readonly int y = 5;  
    ```  
  
-   <span data-ttu-id="8a970-109">Pour un champ d’instance, dans les constructeurs d’instance de la classe qui contient la déclaration de champ, ou pour un champ statique, dans le constructeur statique de la classe qui contient la déclaration de champ.</span><span class="sxs-lookup"><span data-stu-id="8a970-109">For an instance field, in the instance constructors of the class that contains the field declaration, or for a static field, in the static constructor of the class that contains the field declaration.</span></span> <span data-ttu-id="8a970-110">Ce sont également les seuls contextes dans lesquels il est valide de passer un champ `readonly` comme paramètre [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) ou [ref](../../../csharp/language-reference/keywords/ref.md).</span><span class="sxs-lookup"><span data-stu-id="8a970-110">These are also the only contexts in which it is valid to pass a `readonly` field as an [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) or [ref](../../../csharp/language-reference/keywords/ref.md) parameter.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8a970-111">Le mot clé `readonly` est différent du mot clé [const](../../../csharp/language-reference/keywords/const.md).</span><span class="sxs-lookup"><span data-stu-id="8a970-111">The `readonly` keyword is different from the [const](../../../csharp/language-reference/keywords/const.md) keyword.</span></span> <span data-ttu-id="8a970-112">Un champ `const` ne peut être initialisé qu'au moment de la déclaration du champ.</span><span class="sxs-lookup"><span data-stu-id="8a970-112">A `const` field can only be initialized at the declaration of the field.</span></span> <span data-ttu-id="8a970-113">Un champ `readonly` peut être initialisé dans la déclaration ou dans un constructeur.</span><span class="sxs-lookup"><span data-stu-id="8a970-113">A `readonly` field can be initialized either at the declaration or in a constructor.</span></span> <span data-ttu-id="8a970-114">C'est pourquoi, les champs `readonly` peuvent avoir des valeurs différentes en fonction du constructeur utilisé.</span><span class="sxs-lookup"><span data-stu-id="8a970-114">Therefore, `readonly` fields can have different values depending on the constructor used.</span></span> <span data-ttu-id="8a970-115">De même, alors qu’un champ `const` est une constante au moment de la compilation, le champ `readonly` peut être utilisé pour des constantes au moment de l’exécution, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="8a970-115">Also, while a `const` field is a compile-time constant, the `readonly` field can be used for runtime constants as in the following example:</span></span>  
  
```csharp  
public static readonly uint timeStamp = (uint)DateTime.Now.Ticks;  
```  
  
## <a name="comparing-readonly-and-non-readonly-instance-fields"></a><span data-ttu-id="8a970-116">Comparaison de champs d’instance en lecture seule et non en lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a970-116">Comparing readonly and non-readonly instance fields</span></span>  
 [!code-csharp[csrefKeywordsModifiers#15](../../../csharp/language-reference/keywords/codesnippet/CSharp/readonly_2.cs)]  
  
 <span data-ttu-id="8a970-117">Dans l’exemple précédent, si vous utilisez une instruction telle que :</span><span class="sxs-lookup"><span data-stu-id="8a970-117">In the preceding example, if you use a statement like this:</span></span>  
  
 `p2.y = 66;        // Error`  
  
 <span data-ttu-id="8a970-118">vous obtenez le message d’erreur du compilateur :</span><span class="sxs-lookup"><span data-stu-id="8a970-118">you will get the compiler error message:</span></span>  
  
 `The left-hand side of an assignment must be an l-value`  
  
 <span data-ttu-id="8a970-119">qui est la même erreur que vous obtenez lorsque vous tentez d’assigner une valeur à une constante.</span><span class="sxs-lookup"><span data-stu-id="8a970-119">which is the same error you get when you attempt to assign a value to a constant.</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="8a970-120">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="8a970-120">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8a970-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a970-121">See Also</span></span>  
 [<span data-ttu-id="8a970-122">Référence C#</span><span class="sxs-lookup"><span data-stu-id="8a970-122">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="8a970-123">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="8a970-123">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="8a970-124">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="8a970-124">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="8a970-125">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="8a970-125">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)  
 [<span data-ttu-id="8a970-126">const</span><span class="sxs-lookup"><span data-stu-id="8a970-126">const</span></span>](../../../csharp/language-reference/keywords/const.md)  
 [<span data-ttu-id="8a970-127">Champs</span><span class="sxs-lookup"><span data-stu-id="8a970-127">Fields</span></span>](../../../csharp/programming-guide/classes-and-structs/fields.md)
