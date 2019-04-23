---
title: 'Procédure : Stocker plusieurs valeurs dans une Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- classes [Visual Basic], composite data types
- composite types [Visual Basic]
- composite data types [Visual Basic]
- data types [Visual Basic], composite
- arrays [Visual Basic], composite data types
- structures [Visual Basic], composite data types
- arrays [Visual Basic], compilation errors
- types [Visual Basic], composite
ms.assetid: 5fe0e558-aac2-4a40-b7f2-7cfea7336917
ms.openlocfilehash: e2e1648ea508ecdd744adb8d2a4f7fdbc1e586c4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59332259"
---
# <a name="how-to-hold-more-than-one-value-in-a-variable-visual-basic"></a><span data-ttu-id="4faa6-102">Procédure : Stocker plusieurs valeurs dans une Variable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4faa6-102">How to: Hold More Than One Value in a Variable (Visual Basic)</span></span>
<span data-ttu-id="4faa6-103">Une variable contient plusieurs valeurs si vous déclarez comme étant d’un *type de données composite*.</span><span class="sxs-lookup"><span data-stu-id="4faa6-103">A variable holds more than one value if you declare it to be of a *composite data type*.</span></span>  
  
 <span data-ttu-id="4faa6-104">[Les Types de données composites](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md) incluent des structures, des tableaux et des classes.</span><span class="sxs-lookup"><span data-stu-id="4faa6-104">[Composite Data Types](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md) include structures, arrays, and classes.</span></span> <span data-ttu-id="4faa6-105">Une variable de type de données composite peut contenir une combinaison de types de données élémentaires et d’autres types composites.</span><span class="sxs-lookup"><span data-stu-id="4faa6-105">A variable of a composite data type can hold a combination of elementary data types and other composite types.</span></span> <span data-ttu-id="4faa6-106">Structures et classes peuvent contenir du code ainsi que les données.</span><span class="sxs-lookup"><span data-stu-id="4faa6-106">Structures and classes can hold code as well as data.</span></span>  
  
### <a name="to-hold-more-than-one-value-in-a-variable"></a><span data-ttu-id="4faa6-107">Pour stocker plusieurs valeurs dans une variable</span><span class="sxs-lookup"><span data-stu-id="4faa6-107">To hold more than one value in a variable</span></span>  
  
1. <span data-ttu-id="4faa6-108">Déterminer le type de données composites que vous souhaitez utiliser pour votre variable.</span><span class="sxs-lookup"><span data-stu-id="4faa6-108">Determine what composite data type you want to use for your variable.</span></span>  
  
2. <span data-ttu-id="4faa6-109">Si le type de données composite n’est pas déjà défini, définissez-le afin que votre variable puisse l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="4faa6-109">If the composite data type is not already defined, define it so that your variable can use it.</span></span>  
  
    -   <span data-ttu-id="4faa6-110">Définir une structure avec un [instruction Structure](../../../../visual-basic/language-reference/statements/structure-statement.md).</span><span class="sxs-lookup"><span data-stu-id="4faa6-110">Define a structure with a [Structure Statement](../../../../visual-basic/language-reference/statements/structure-statement.md).</span></span>  
  
    -   <span data-ttu-id="4faa6-111">Définir un tableau avec un [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md).</span><span class="sxs-lookup"><span data-stu-id="4faa6-111">Define an array with a [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md).</span></span>  
  
    -   <span data-ttu-id="4faa6-112">Définir une classe avec un [Class, instruction](../../../../visual-basic/language-reference/statements/class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="4faa6-112">Define a class with a [Class Statement](../../../../visual-basic/language-reference/statements/class-statement.md).</span></span>  
  
3. <span data-ttu-id="4faa6-113">Déclarez votre variable avec un `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="4faa6-113">Declare your variable with a `Dim` statement.</span></span>  
  
4. <span data-ttu-id="4faa6-114">Suivez le nom de variable avec une `As` clause.</span><span class="sxs-lookup"><span data-stu-id="4faa6-114">Follow the variable name with an `As` clause.</span></span>  
  
5. <span data-ttu-id="4faa6-115">Suivez le `As` mot clé par le nom du type de données composite approprié.</span><span class="sxs-lookup"><span data-stu-id="4faa6-115">Follow the `As` keyword with the name of the appropriate composite data type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4faa6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4faa6-116">See also</span></span>

- [<span data-ttu-id="4faa6-117">Types de données</span><span class="sxs-lookup"><span data-stu-id="4faa6-117">Data Types</span></span>](../../../../visual-basic/language-reference/data-types/index.md)
- [<span data-ttu-id="4faa6-118">Caractères de type</span><span class="sxs-lookup"><span data-stu-id="4faa6-118">Type Characters</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)
- [<span data-ttu-id="4faa6-119">Types de données composites</span><span class="sxs-lookup"><span data-stu-id="4faa6-119">Composite Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)
- [<span data-ttu-id="4faa6-120">Structures</span><span class="sxs-lookup"><span data-stu-id="4faa6-120">Structures</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="4faa6-121">Tableaux</span><span class="sxs-lookup"><span data-stu-id="4faa6-121">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [<span data-ttu-id="4faa6-122">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="4faa6-122">Objects and Classes</span></span>](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [<span data-ttu-id="4faa6-123">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="4faa6-123">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
