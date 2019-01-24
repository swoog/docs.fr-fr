---
title: Détermination du type Object (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- classes [Visual Basic], discovering which an object belongs to
- types [Visual Basic], determining Visual Basic object types
- object variables [Visual Basic], testing values
- TypeOf...Is expression, object type at run time
- TypeName function
- objects [Visual Basic], type determining
ms.assetid: d95e7ad1-cd63-41d6-9a28-d7a1380d49c1
ms.openlocfilehash: 5980549dd063b2c7d5c60ebd4e9762284c072009
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54586616"
---
# <a name="determining-object-type-visual-basic"></a><span data-ttu-id="049e2-102">Détermination du type Object (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="049e2-102">Determining Object Type (Visual Basic)</span></span>
<span data-ttu-id="049e2-103">Variables de l’objet générique (autrement dit, les variables que vous déclarez comme `Object`) peut contenir des objets à partir de n’importe quelle classe.</span><span class="sxs-lookup"><span data-stu-id="049e2-103">Generic object variables (that is, variables you declare as `Object`) can hold objects from any class.</span></span> <span data-ttu-id="049e2-104">Lors de l’utilisation de variables de type `Object`, vous devrez peut-être prendre des mesures différentes selon la classe de l’objet ; par exemple, certains objets ne peuvent pas en charge une propriété ou méthode particulière.</span><span class="sxs-lookup"><span data-stu-id="049e2-104">When using variables of type `Object`, you may need to take different actions based on the class of the object; for example, some objects might not support a particular property or method.</span></span> <span data-ttu-id="049e2-105">Visual Basic fournit deux moyens de déterminer quel type d’objet est stocké dans une variable objet : le `TypeName` (fonction) et le `TypeOf...Is` opérateur.</span><span class="sxs-lookup"><span data-stu-id="049e2-105">Visual Basic provides two means of determining which type of object is stored in an object variable: the `TypeName` function and the `TypeOf...Is` operator.</span></span>  
  
## <a name="typename-and-typeofis"></a><span data-ttu-id="049e2-106">TypeName et TypeOf... Est</span><span class="sxs-lookup"><span data-stu-id="049e2-106">TypeName and TypeOf…Is</span></span>  
 <span data-ttu-id="049e2-107">Le `TypeName` fonction retourne une chaîne et est le meilleur choix lorsque vous devez stocker ou afficher le nom de classe d’un objet, comme illustré dans le fragment de code suivant :</span><span class="sxs-lookup"><span data-stu-id="049e2-107">The `TypeName` function returns a string and is the best choice when you need to store or display the class name of an object, as shown in the following code fragment:</span></span>  
  
 [!code-vb[VbVbalrOOP#92](../../../../visual-basic/misc/codesnippet/VisualBasic/determining-object-type_1.vb)]  
  
 <span data-ttu-id="049e2-108">Le `TypeOf...Is` opérateur est le meilleur choix pour le test d’un type d’objet, car il est beaucoup plus rapide qu’une comparaison de chaîne équivalente à l’aide de `TypeName`.</span><span class="sxs-lookup"><span data-stu-id="049e2-108">The `TypeOf...Is` operator is the best choice for testing an object's type, because it is much faster than an equivalent string comparison using `TypeName`.</span></span> <span data-ttu-id="049e2-109">Le fragment de code suivant utilise `TypeOf...Is` au sein d’un `If...Then...Else` instruction :</span><span class="sxs-lookup"><span data-stu-id="049e2-109">The following code fragment uses `TypeOf...Is` within an `If...Then...Else` statement:</span></span>  
  
 [!code-vb[VbVbalrOOP#93](../../../../visual-basic/misc/codesnippet/VisualBasic/determining-object-type_2.vb)]  
  
 <span data-ttu-id="049e2-110">Un mot de prudence est due ici.</span><span class="sxs-lookup"><span data-stu-id="049e2-110">A word of caution is due here.</span></span> <span data-ttu-id="049e2-111">Le `TypeOf...Is` opérateur retourne `True` si un objet est d’un type spécifique, ou est dérivé d’un type spécifique.</span><span class="sxs-lookup"><span data-stu-id="049e2-111">The `TypeOf...Is` operator returns `True` if an object is of a specific type, or is derived from a specific type.</span></span> <span data-ttu-id="049e2-112">Presque tout ce que vous faites avec Visual Basic implique des objets, qui incluent certains éléments pas normalement considérés comme des objets, tels que des chaînes et les entiers.</span><span class="sxs-lookup"><span data-stu-id="049e2-112">Almost everything you do with Visual Basic involves objects, which include some elements not normally thought of as objects, such as strings and integers.</span></span> <span data-ttu-id="049e2-113">Ces objets sont dérivés et héritent des méthodes de <xref:System.Object>.</span><span class="sxs-lookup"><span data-stu-id="049e2-113">These objects are derived from and inherit methods from <xref:System.Object>.</span></span> <span data-ttu-id="049e2-114">Quand il est passé un `Integer` et évaluée avec `Object`, le `TypeOf...Is` opérateur retourne `True`.</span><span class="sxs-lookup"><span data-stu-id="049e2-114">When passed an `Integer` and evaluated with `Object`, the `TypeOf...Is` operator returns `True`.</span></span> <span data-ttu-id="049e2-115">L’exemple suivant indique que le paramètre `InParam` est à la fois un `Object` et un `Integer`:</span><span class="sxs-lookup"><span data-stu-id="049e2-115">The following example reports that the parameter `InParam` is both an `Object` and an `Integer`:</span></span>  
  
 [!code-vb[VbVbalrOOP#94](../../../../visual-basic/misc/codesnippet/VisualBasic/determining-object-type_3.vb)]  
  
 <span data-ttu-id="049e2-116">L’exemple suivant utilise à la fois `TypeOf...Is` et `TypeName` pour déterminer le type d’objet passé dans le `Ctrl` argument.</span><span class="sxs-lookup"><span data-stu-id="049e2-116">The following example uses both `TypeOf...Is` and `TypeName` to determine the type of object passed to it in the `Ctrl` argument.</span></span> <span data-ttu-id="049e2-117">Le `TestObject` les appels de procédure `ShowType` avec trois différents types de contrôles.</span><span class="sxs-lookup"><span data-stu-id="049e2-117">The `TestObject` procedure calls `ShowType` with three different kinds of controls.</span></span>  
  
#### <a name="to-run-the-example"></a><span data-ttu-id="049e2-118">Pour exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="049e2-118">To run the example</span></span>  
  
1.  <span data-ttu-id="049e2-119">Créez un nouveau projet d’Application de Windows et ajoutez un <xref:System.Windows.Forms.Button> contrôle, un <xref:System.Windows.Forms.CheckBox> contrôle et un <xref:System.Windows.Forms.RadioButton> contrôle au formulaire.</span><span class="sxs-lookup"><span data-stu-id="049e2-119">Create a new Windows Application project and add a <xref:System.Windows.Forms.Button> control, a <xref:System.Windows.Forms.CheckBox> control, and a <xref:System.Windows.Forms.RadioButton> control to the form.</span></span>  
  
2.  <span data-ttu-id="049e2-120">À partir du bouton sur votre formulaire, appelez le `TestObject` procédure.</span><span class="sxs-lookup"><span data-stu-id="049e2-120">From the button on your form, call the `TestObject` procedure.</span></span>  
  
3.  <span data-ttu-id="049e2-121">Ajoutez le code suivant à votre formulaire :</span><span class="sxs-lookup"><span data-stu-id="049e2-121">Add the following code to your form:</span></span>  
  
     [!code-vb[VbVbalrOOP#95](../../../../visual-basic/misc/codesnippet/VisualBasic/determining-object-type_4.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="049e2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="049e2-122">See also</span></span>
- <xref:Microsoft.VisualBasic.Information.TypeName%2A>
- [<span data-ttu-id="049e2-123">Appel d’une propriété ou méthode à l’aide d’un nom de chaîne</span><span class="sxs-lookup"><span data-stu-id="049e2-123">Calling a Property or Method Using a String Name</span></span>](../../../../visual-basic/programming-guide/language-features/early-late-binding/calling-a-property-or-method-using-a-string-name.md)
- [<span data-ttu-id="049e2-124">Object (type de données)</span><span class="sxs-lookup"><span data-stu-id="049e2-124">Object Data Type</span></span>](../../../../visual-basic/language-reference/data-types/object-data-type.md)
- [<span data-ttu-id="049e2-125">If...Then...Else (instruction)</span><span class="sxs-lookup"><span data-stu-id="049e2-125">If...Then...Else Statement</span></span>](../../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [<span data-ttu-id="049e2-126">String (type de données)</span><span class="sxs-lookup"><span data-stu-id="049e2-126">String Data Type</span></span>](../../../../visual-basic/language-reference/data-types/string-data-type.md)
- [<span data-ttu-id="049e2-127">Integer (type de données)</span><span class="sxs-lookup"><span data-stu-id="049e2-127">Integer Data Type</span></span>](../../../../visual-basic/language-reference/data-types/integer-data-type.md)
