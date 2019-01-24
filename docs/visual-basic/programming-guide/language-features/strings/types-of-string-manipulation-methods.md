---
title: Types de méthodes de manipulation de chaînes en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], manipulating [Visual Basic]
- string manipulation
ms.assetid: 905055cd-7f50-48fb-9eed-b0995af1dc1f
ms.openlocfilehash: fa579303ad268a88269f360bdf626f9590c5d6a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648493"
---
# <a name="types-of-string-manipulation-methods-in-visual-basic"></a><span data-ttu-id="9ca84-102">Types de méthodes de manipulation de chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9ca84-102">Types of String Manipulation Methods in Visual Basic</span></span>
<span data-ttu-id="9ca84-103">Il existe différentes façons de les analyser et manipuler des chaînes.</span><span class="sxs-lookup"><span data-stu-id="9ca84-103">There are several different ways to analyze and manipulate your strings.</span></span> <span data-ttu-id="9ca84-104">Certaines des méthodes font partie du langage Visual Basic, et d’autres sont inhérentes à la `String` classe.</span><span class="sxs-lookup"><span data-stu-id="9ca84-104">Some of the methods are a part of the Visual Basic language, and others are inherent in the `String` class.</span></span>  
  
## <a name="visual-basic-language-and-the-net-framework"></a><span data-ttu-id="9ca84-105">Langage Visual Basic et .NET Framework</span><span class="sxs-lookup"><span data-stu-id="9ca84-105">Visual Basic Language and the .NET Framework</span></span>  
 <span data-ttu-id="9ca84-106">Méthodes de Visual Basic sont utilisées en tant que fonctions inhérentes du langage.</span><span class="sxs-lookup"><span data-stu-id="9ca84-106">Visual Basic methods are used as inherent functions of the language.</span></span> <span data-ttu-id="9ca84-107">Ils peuvent être utilisés sans qualification dans votre code.</span><span class="sxs-lookup"><span data-stu-id="9ca84-107">They may be used without qualification in your code.</span></span> <span data-ttu-id="9ca84-108">L’exemple suivant illustre une utilisation classique d’une commande de manipulation de chaînes Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="9ca84-108">The following example shows typical use of a Visual Basic string-manipulation command:</span></span>  
  
 [!code-vb[VbVbalrStrings#44](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/types-of-string-manipulation-methods_1.vb)]  
  
 <span data-ttu-id="9ca84-109">Dans cet exemple, le `Mid` fonction effectue une opération directe sur `aString` et affecte la valeur à `bString`.</span><span class="sxs-lookup"><span data-stu-id="9ca84-109">In this example, the `Mid` function performs a direct operation on `aString` and assigns the value to `bString`.</span></span>  
  
 <span data-ttu-id="9ca84-110">Pour obtenir la liste des méthodes de manipulation de chaîne Visual Basic, consultez [liste des manipulations de chaîne](../../../../visual-basic/language-reference/keywords/string-manipulation-summary.md).</span><span class="sxs-lookup"><span data-stu-id="9ca84-110">For a list of Visual Basic string manipulation methods, see [String Manipulation Summary](../../../../visual-basic/language-reference/keywords/string-manipulation-summary.md).</span></span>  
  
### <a name="shared-methods-and-instance-methods"></a><span data-ttu-id="9ca84-111">Méthodes partagées et des méthodes d’Instance</span><span class="sxs-lookup"><span data-stu-id="9ca84-111">Shared Methods and Instance Methods</span></span>  
 <span data-ttu-id="9ca84-112">Vous pouvez également manipuler des chaînes avec les méthodes de la `String` classe.</span><span class="sxs-lookup"><span data-stu-id="9ca84-112">You can also manipulate strings with the methods of the `String` class.</span></span> <span data-ttu-id="9ca84-113">Il existe deux types de méthodes de `String`: *partagé* méthodes et *instance* méthodes.</span><span class="sxs-lookup"><span data-stu-id="9ca84-113">There are two types of methods in `String`: *shared* methods and *instance* methods.</span></span>  
  
#### <a name="shared-methods"></a><span data-ttu-id="9ca84-114">Méthodes partagées</span><span class="sxs-lookup"><span data-stu-id="9ca84-114">Shared Methods</span></span>  
 <span data-ttu-id="9ca84-115">Une méthode partagée est une méthode qui provient de la `String` classe lui-même et ne nécessite pas une instance de cette classe fonctionne.</span><span class="sxs-lookup"><span data-stu-id="9ca84-115">A shared method is a method that stems from the `String` class itself and does not require an instance of that class to work.</span></span> <span data-ttu-id="9ca84-116">Ces méthodes peuvent être qualifiés avec le nom de la classe (`String`) plutôt qu’avec une instance de la `String` classe.</span><span class="sxs-lookup"><span data-stu-id="9ca84-116">These methods can be qualified with the name of the class (`String`) rather than with an instance of the `String` class.</span></span> <span data-ttu-id="9ca84-117">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9ca84-117">For example:</span></span>  
  
 [!code-vb[VbVbalrStrings#45](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/types-of-string-manipulation-methods_2.vb)]  
  
 <span data-ttu-id="9ca84-118">Dans l’exemple précédent, le <xref:System.String.Copy%2A?displayProperty=nameWithType> méthode est une méthode statique, qui agit sur une expression qui lui est attribuée et affecte la valeur obtenue vers `bString`.</span><span class="sxs-lookup"><span data-stu-id="9ca84-118">In the preceding example, the <xref:System.String.Copy%2A?displayProperty=nameWithType> method is a static method, which acts upon an expression it is given and assigns the resulting value to `bString`.</span></span>  
  
#### <a name="instance-methods"></a><span data-ttu-id="9ca84-119">Méthodes d’instance</span><span class="sxs-lookup"><span data-stu-id="9ca84-119">Instance Methods</span></span>  
 <span data-ttu-id="9ca84-120">Méthodes d’instance, en revanche, proviennent d’une instance particulière de `String` et doivent être qualifiés avec le nom d’instance.</span><span class="sxs-lookup"><span data-stu-id="9ca84-120">Instance methods, by contrast, stem from a particular instance of `String` and must be qualified with the instance name.</span></span> <span data-ttu-id="9ca84-121">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9ca84-121">For example:</span></span>  
  
 [!code-vb[VbVbalrStrings#46](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/types-of-string-manipulation-methods_3.vb)]  
  
 <span data-ttu-id="9ca84-122">Dans cet exemple, le <xref:System.String.Substring%2A?displayProperty=nameWithType> méthode est une méthode de l’instance de `String` (autrement dit, `aString`).</span><span class="sxs-lookup"><span data-stu-id="9ca84-122">In this example, the <xref:System.String.Substring%2A?displayProperty=nameWithType> method is a method of the instance of `String` (that is, `aString`).</span></span> <span data-ttu-id="9ca84-123">Elle effectue une opération sur `aString` et assigne cette valeur à `bString`.</span><span class="sxs-lookup"><span data-stu-id="9ca84-123">It performs an operation on `aString` and assigns that value to `bString`.</span></span>  
  
 <span data-ttu-id="9ca84-124">Pour plus d’informations, consultez la documentation pour le <xref:System.String> classe.</span><span class="sxs-lookup"><span data-stu-id="9ca84-124">For more information, see the documentation for the <xref:System.String> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ca84-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ca84-125">See also</span></span>
- [<span data-ttu-id="9ca84-126">Introduction aux chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9ca84-126">Introduction to Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
