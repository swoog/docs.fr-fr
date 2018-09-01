---
title: 'Comment : déclarer une constante (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.constant
helpviewer_keywords:
- Integer data type [Visual Basic], declaring constants
- Single data type [Visual Basic], declaring constants
- Const statement [Visual Basic], declaring constants
- procedures [Visual Basic], declaration
- data types [Visual Basic], constants
- Long data type [Visual Basic], declaring constants
- Visual Basic code, declaring variables and constants
- Double data type [Visual Basic], declaring constants
- Boolean data type [Visual Basic], declaring constants
- modules, declaring constants
- Byte data type [Visual Basic], declaring constants
- constants [Visual Basic], declaring
- Date data type [Visual Basic], declaring constants
- String data type [Visual Basic], declaring constants
- declaring constants [Visual Basic], const keyword
- Currency data type [Visual Basic], declaring constants and variants
- module-level constants and variables
- Object data type [Visual Basic], declaring constants
ms.assetid: f901b4fa-481f-4621-822e-427060577ad1
ms.openlocfilehash: ce45e4df7f74cd68bde0fb2adba10197a11edb1b
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43394312"
---
# <a name="how-to-declare-a-constant-visual-basic"></a><span data-ttu-id="b1554-102">Comment : déclarer une constante (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b1554-102">How to: Declare A Constant (Visual Basic)</span></span>
<span data-ttu-id="b1554-103">Vous utilisez la `Const` instruction pour déclarer une constante et définir sa valeur.</span><span class="sxs-lookup"><span data-stu-id="b1554-103">You use the `Const` statement to declare a constant and set its value.</span></span> <span data-ttu-id="b1554-104">En déclarant une constante, vous affectez un nom explicite à une valeur.</span><span class="sxs-lookup"><span data-stu-id="b1554-104">By declaring a constant, you assign a meaningful name to a value.</span></span> <span data-ttu-id="b1554-105">Une fois qu’une constante est déclarée, il ne peut pas être modifié ou attribuer une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="b1554-105">Once a constant is declared, it cannot be modified or assigned a new value.</span></span>  
  
 <span data-ttu-id="b1554-106">Vous déclarez une constante dans une procédure ou dans la section Déclarations d’un module, une classe ou une structure.</span><span class="sxs-lookup"><span data-stu-id="b1554-106">You declare a constant within a procedure or in the declarations section of a module, class, or structure.</span></span> <span data-ttu-id="b1554-107">Classe ou des constantes au niveau de la structure sont `Private` par défaut, mais peuvent également être déclarées comme `Public`, `Friend`, `Protected`, ou `Protected Friend` pour le niveau d’accès au code approprié.</span><span class="sxs-lookup"><span data-stu-id="b1554-107">Class or structure-level constants are `Private` by default, but may also be declared as `Public`, `Friend`, `Protected`, or `Protected Friend` for the appropriate level of code access.</span></span>  
  
 <span data-ttu-id="b1554-108">La constante doit avoir un nom symbolique valide (les règles sont les mêmes que celles permettant de créer des noms de variables) et une expression composée de numérique ou chaîne constantes et opérateurs (mais aucun appel de fonction).</span><span class="sxs-lookup"><span data-stu-id="b1554-108">The constant must have a valid symbolic name (the rules are the same as those for creating variable names) and an expression composed of numeric or string constants and operators (but no function calls).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-declare-a-constant"></a><span data-ttu-id="b1554-109">Pour déclarer une constante</span><span class="sxs-lookup"><span data-stu-id="b1554-109">To declare a constant</span></span>  
  
-   <span data-ttu-id="b1554-110">Écrivez une déclaration qui inclut un spécificateur d’accès, le `Const` mot clé et une expression, comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="b1554-110">Write a declaration that includes an access specifier, the `Const` keyword, and an expression, as in the following examples:</span></span>  
  
     [!code-vb[VbEnumsTask#8](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-a-constant_1.vb)]  
  
     <span data-ttu-id="b1554-111">Lorsque [Option Infer](../../../../visual-basic/language-reference/statements/option-infer-statement.md) est `Off` et [Option Strict](../../../../visual-basic/language-reference/statements/option-strict-statement.md) est `On`, vous devez déclarer explicitement une constante en spécifiant un type de données (`Boolean`, `Byte`, `Char`, `DateTime`, `Decimal`, `Double`, `Integer`, `Long`, `Short`, `Single`, ou `String`).</span><span class="sxs-lookup"><span data-stu-id="b1554-111">When [Option Infer](../../../../visual-basic/language-reference/statements/option-infer-statement.md) is `Off` and [Option Strict](../../../../visual-basic/language-reference/statements/option-strict-statement.md) is `On`, you must declare a constant explicitly by specifying a data type (`Boolean`, `Byte`, `Char`, `DateTime`, `Decimal`, `Double`, `Integer`, `Long`, `Short`, `Single`, or `String`).</span></span>  
  
     <span data-ttu-id="b1554-112">Lorsque `Option Infer` est `On` ou `Option Strict` est `Off`, vous pouvez déclarer une constante sans spécifier un type de données avec un `As` clause.</span><span class="sxs-lookup"><span data-stu-id="b1554-112">When `Option Infer` is `On` or `Option Strict` is `Off`, you can declare a constant without specifying a data type with an `As` clause.</span></span> <span data-ttu-id="b1554-113">Le compilateur détermine le type de la constante à partir du type de l’expression.</span><span class="sxs-lookup"><span data-stu-id="b1554-113">The compiler determines the type of the constant from the type of the expression.</span></span> <span data-ttu-id="b1554-114">Pour plus d’informations, consultez [constante et les Types de données littérales](constant-and-literal-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="b1554-114">For more information, see [Constant and Literal Data Types](constant-and-literal-data-types.md).</span></span>  
  
### <a name="to-declare-a-constant-that-has-an-explicitly-stated-data-type"></a><span data-ttu-id="b1554-115">Pour déclarer une constante qui a un type de données indiqué explicitement</span><span class="sxs-lookup"><span data-stu-id="b1554-115">To declare a constant that has an explicitly stated data type</span></span>  
  
-   <span data-ttu-id="b1554-116">Écrivez une déclaration qui inclut le `As` mot clé et une explicites type de données, comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="b1554-116">Write a declaration that includes the `As` keyword and an explicit data type, as in the following examples:</span></span>  
  
     [!code-vb[VbEnumsTask#9](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-a-constant_2.vb)]  
  
     <span data-ttu-id="b1554-117">Vous pouvez déclarer plusieurs constantes sur une seule ligne, bien que votre code est plus lisible si vous ne déclarez qu’une seule constante par ligne.</span><span class="sxs-lookup"><span data-stu-id="b1554-117">You can declare multiple constants on a single line, although your code is more readable if you declare only a single constant per line.</span></span> <span data-ttu-id="b1554-118">Si vous déclarez plusieurs constantes sur une seule ligne, ils doivent tous avoir le même niveau d’accès (`Public`, `Private`, `Friend`, `Protected`, ou `Protected Friend`).</span><span class="sxs-lookup"><span data-stu-id="b1554-118">If you declare multiple constants on a single line, they must all have the same access level (`Public`, `Private`, `Friend`, `Protected`, or `Protected Friend`).</span></span>  
  
### <a name="to-declare-multiple-constants-on-a-single-line"></a><span data-ttu-id="b1554-119">Pour déclarer plusieurs constantes sur une seule ligne</span><span class="sxs-lookup"><span data-stu-id="b1554-119">To declare multiple constants on a single line</span></span>  
  
-   <span data-ttu-id="b1554-120">Séparez les déclarations par une virgule et un espace, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b1554-120">Separate the declarations with a comma and a space, as in the following example:</span></span>  
  
    ```  
    Public Const Four As Integer = 4, Five As Integer = 5, Six As Integer = 44  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="b1554-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1554-121">See Also</span></span>  
 [<span data-ttu-id="b1554-122">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="b1554-122">Const Statement</span></span>](../../../../visual-basic/language-reference/statements/const-statement.md)  
 [<span data-ttu-id="b1554-123">Constantes et types de données littérales</span><span class="sxs-lookup"><span data-stu-id="b1554-123">Constant and Literal Data Types</span></span>](constant-and-literal-data-types.md)  
 <span data-ttu-id="b1554-124">[Vue d’ensemble des constantes](constants-overview.md) [Comment : déclarer une constante](how-to-declare-a-constant.md) [constantes définies par l’utilisateur](user-defined-constants.md) [Types de données littéraux et constantes](constant-and-literal-data-types.md) [Comment : groupe Les valeurs de constante connexes](how-to-group-related-constant-values-together.md) [vue d’ensemble des énumérations](enumerations-overview.md) [Comment : déclarer des énumérations](how-to-declare-enumerations.md) [Comment : faire référence à un membre d’énumération](how-to-refer-to-an-enumeration-member.md) [Énumérations et Qualification de noms](enumerations-and-name-qualification.md) [Comment : parcourir une énumération](how-to-iterate-through-an-enumeration.md) [Comment : déterminer la chaîne associée à une valeur d’énumération](how-to-determine-the-string-associated-with-an-enumeration-value.md) [Quand utiliser une énumération](when-to-use-an-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b1554-124">[Constants Overview](constants-overview.md) [How to: Declare A Constant](how-to-declare-a-constant.md) [User-Defined Constants](user-defined-constants.md) [Constant and Literal Data Types](constant-and-literal-data-types.md) [How to: Group Related Constant Values Together](how-to-group-related-constant-values-together.md) [Enumerations Overview](enumerations-overview.md) [How to: Declare Enumerations](how-to-declare-enumerations.md) [How to: Refer to an Enumeration Member](how-to-refer-to-an-enumeration-member.md) [Enumerations and Name Qualification](enumerations-and-name-qualification.md) [How to: Iterate Through An Enumeration](how-to-iterate-through-an-enumeration.md) [How to: Determine the String Associated with an Enumeration Value](how-to-determine-the-string-associated-with-an-enumeration-value.md) [When to Use an Enumeration](when-to-use-an-enumeration.md)</span></span>

 [<span data-ttu-id="b1554-125">Vue d’ensemble des énumérations</span><span class="sxs-lookup"><span data-stu-id="b1554-125">Enumerations Overview</span></span>](enumerations-overview.md)  
 [<span data-ttu-id="b1554-126">Vue d’ensemble des constantes</span><span class="sxs-lookup"><span data-stu-id="b1554-126">Constants Overview</span></span>](constants-overview.md)  
 [<span data-ttu-id="b1554-127">Comment : déclarer une énumération</span><span class="sxs-lookup"><span data-stu-id="b1554-127">How to: Declare an Enumeration</span></span>](how-to-declare-enumerations.md)  
 [<span data-ttu-id="b1554-128">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="b1554-128">Enumerations and Name Qualification</span></span>](enumerations-and-name-qualification.md)  
 [<span data-ttu-id="b1554-129">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="b1554-129">Option Strict Statement</span></span>](../../../../visual-basic/language-reference/statements/option-strict-statement.md)  
 [<span data-ttu-id="b1554-130">Constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="b1554-130">Constants and Enumerations</span></span>](../../../../visual-basic/language-reference/constants-and-enumerations.md)
