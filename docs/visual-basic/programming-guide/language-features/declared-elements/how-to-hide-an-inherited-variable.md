---
title: 'Procédure : Masquer une Variable héritée (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- qualification [Visual Basic], of element names
- element names [Visual Basic], qualification
- references [Visual Basic], declared elements
- declaration statements [Visual Basic], declared elements
- referencing declared elements [Visual Basic]
- declared elements [Visual Basic], referencing
- declared elements [Visual Basic], about declared elements
- variables [Visual Basic], hiding inherited
ms.assetid: 765728d9-7351-4a30-999d-b5f34f024412
ms.openlocfilehash: ee147ecd00b88b538ace32844c42ac9c5022b2ef
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61794691"
---
# <a name="how-to-hide-an-inherited-variable-visual-basic"></a><span data-ttu-id="6416d-102">Procédure : Masquer une Variable héritée (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6416d-102">How to: Hide an Inherited Variable (Visual Basic)</span></span>
<span data-ttu-id="6416d-103">Une classe dérivée hérite de toutes les définitions de sa classe de base.</span><span class="sxs-lookup"><span data-stu-id="6416d-103">A derived class inherits all the definitions of its base class.</span></span> <span data-ttu-id="6416d-104">Si vous souhaitez définir une variable en utilisant le même nom qu’un élément de la classe de base, vous pouvez masquer, ou *ombre*, cet élément de classe de base lorsque vous définissez votre variable dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="6416d-104">If you want to define a variable using the same name as an element of the base class, you can hide, or *shadow*, that base class element when you define your variable in the derived class.</span></span> <span data-ttu-id="6416d-105">Si vous procédez ainsi, le code dans la classe dérivée accède à votre variable, sauf si elle ignore explicitement le mécanisme d’occultation.</span><span class="sxs-lookup"><span data-stu-id="6416d-105">If you do this, code in the derived class accesses your variable unless it explicitly bypasses the shadowing mechanism.</span></span>  
  
 <span data-ttu-id="6416d-106">Une autre raison, que vous souhaiterez peut-être masquer une variable héritée est pour vous protéger contre la révision de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="6416d-106">Another reason you might want to hide an inherited variable is to protect against base class revision.</span></span> <span data-ttu-id="6416d-107">La classe de base peut subir un changement qui modifie l’élément que vous héritez.</span><span class="sxs-lookup"><span data-stu-id="6416d-107">The base class might undergo a change that alters the element you are inheriting.</span></span> <span data-ttu-id="6416d-108">Si cela se produit, le `Shadows` modificateur force les références de la classe dérivée pour être résolu à votre variable, au lieu de l’élément de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="6416d-108">If this happens, the `Shadows` modifier forces references from the derived class to be resolved to your variable, instead of to the base class element.</span></span>  
  
### <a name="to-hide-an-inherited-variable"></a><span data-ttu-id="6416d-109">Pour masquer une variable héritée</span><span class="sxs-lookup"><span data-stu-id="6416d-109">To hide an inherited variable</span></span>  
  
1. <span data-ttu-id="6416d-110">Assurez-vous que la variable que vous souhaitez masquer est déclarée au niveau de la classe (en dehors de toute procédure).</span><span class="sxs-lookup"><span data-stu-id="6416d-110">Be sure the variable you want to hide is declared at class level (outside any procedure).</span></span> <span data-ttu-id="6416d-111">Sinon, vous n’avez pas besoin pour le masquer.</span><span class="sxs-lookup"><span data-stu-id="6416d-111">Otherwise you do not need to hide it.</span></span>  
  
2. <span data-ttu-id="6416d-112">À l’intérieur de votre classe dérivée, écrivez une [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) déclarer votre variable.</span><span class="sxs-lookup"><span data-stu-id="6416d-112">Inside your derived class, write a [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md) declaring your variable.</span></span> <span data-ttu-id="6416d-113">Utiliser le même nom que celui de la variable héritée.</span><span class="sxs-lookup"><span data-stu-id="6416d-113">Use the same name as that of the inherited variable.</span></span>  
  
3. <span data-ttu-id="6416d-114">Inclure le [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md) mot clé dans la déclaration.</span><span class="sxs-lookup"><span data-stu-id="6416d-114">Include the [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md) keyword in the declaration.</span></span>  
  
     <span data-ttu-id="6416d-115">En cas de code dans la classe dérivée fait référence au nom de variable, le compilateur résout la référence à votre variable.</span><span class="sxs-lookup"><span data-stu-id="6416d-115">When code in the derived class refers to the variable name, the compiler resolves the reference to your variable.</span></span>  
  
     <span data-ttu-id="6416d-116">L’exemple suivant illustre l’occultation d’une variable héritée.</span><span class="sxs-lookup"><span data-stu-id="6416d-116">The following example illustrates shadowing of an inherited variable.</span></span>  
  
    ```  
    Public Class shadowBaseClass  
        Public shadowString As String = "This is the base class string."  
    End Class  
    Public Class shadowDerivedClass  
        Inherits shadowBaseClass  
        Public Shadows shadowString As String = "This is the derived class string."  
        Public Sub showStrings()  
            Dim s As String = "Unqualified shadowString: " & shadowString &  
                vbCrLf & "MyBase.shadowString: " & MyBase.shadowString  
            MsgBox(s)  
        End Sub  
    End Class  
    ```  
  
     <span data-ttu-id="6416d-117">L’exemple précédent déclare la variable `shadowString` dans la classe de base et la masque dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="6416d-117">The preceding example declares the variable `shadowString` in the base class and shadows it in the derived class.</span></span> <span data-ttu-id="6416d-118">La procédure `showStrings` dans la classe dérivée, affiche la version de masquage de la chaîne lorsque le nom `shadowString` n’est pas qualifié.</span><span class="sxs-lookup"><span data-stu-id="6416d-118">The procedure `showStrings` in the derived class displays the shadowing version of the string when the name `shadowString` is not qualified.</span></span> <span data-ttu-id="6416d-119">Il affiche ensuite la version ombrée lorsque `shadowString` est qualifié avec le `MyBase` mot clé.</span><span class="sxs-lookup"><span data-stu-id="6416d-119">It then displays the shadowed version when `shadowString` is qualified with the `MyBase` keyword.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="6416d-120">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="6416d-120">Robust Programming</span></span>  
 <span data-ttu-id="6416d-121">L’occultation introduit plusieurs versions d’une variable portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="6416d-121">Shadowing introduces more than one version of a variable with the same name.</span></span> <span data-ttu-id="6416d-122">Lorsqu’une instruction de code fait référence au nom de variable, la version à laquelle le compilateur résout la référence dépend de facteurs tels que l’emplacement de l’instruction de code et la présence d’une chaîne qualifiante.</span><span class="sxs-lookup"><span data-stu-id="6416d-122">When a code statement refers to the variable name, the version to which the compiler resolves the reference depends on factors such as the location of the code statement and the presence of a qualifying string.</span></span> <span data-ttu-id="6416d-123">Cela peut augmenter le risque de faire référence à une version non souhaitée d’une variable occultée.</span><span class="sxs-lookup"><span data-stu-id="6416d-123">This can increase the risk of referring to an unintended version of a shadowed variable.</span></span> <span data-ttu-id="6416d-124">Vous pouvez réduire ce risque en qualifiant complètement toutes les références à une variable occultée.</span><span class="sxs-lookup"><span data-stu-id="6416d-124">You can lower that risk by fully qualifying all references to a shadowed variable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6416d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6416d-125">See also</span></span>

- [<span data-ttu-id="6416d-126">Références aux éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="6416d-126">References to Declared Elements</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [<span data-ttu-id="6416d-127">Occultation dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6416d-127">Shadowing in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
- [<span data-ttu-id="6416d-128">Différences entre l'occultation et la substitution</span><span class="sxs-lookup"><span data-stu-id="6416d-128">Differences Between Shadowing and Overriding</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/differences-between-shadowing-and-overriding.md)
- [<span data-ttu-id="6416d-129">Guide pratique pour Masquer une Variable portant le même nom que votre Variable</span><span class="sxs-lookup"><span data-stu-id="6416d-129">How to: Hide a Variable with the Same Name as Your Variable</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-a-variable-with-the-same-name-as-your-variable.md)
- [<span data-ttu-id="6416d-130">Guide pratique pour Accéder à une Variable masquée par une classe dérivée</span><span class="sxs-lookup"><span data-stu-id="6416d-130">How to: Access a Variable Hidden by a Derived Class</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-access-a-variable-hidden-by-a-derived-class.md)
- [<span data-ttu-id="6416d-131">Overrides</span><span class="sxs-lookup"><span data-stu-id="6416d-131">Overrides</span></span>](../../../../visual-basic/language-reference/modifiers/overrides.md)
- [<span data-ttu-id="6416d-132">Me, My, MyBase et MyClass</span><span class="sxs-lookup"><span data-stu-id="6416d-132">Me, My, MyBase, and MyClass</span></span>](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="6416d-133">Éléments fondamentaux de l’héritage</span><span class="sxs-lookup"><span data-stu-id="6416d-133">Inheritance Basics</span></span>](../../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
