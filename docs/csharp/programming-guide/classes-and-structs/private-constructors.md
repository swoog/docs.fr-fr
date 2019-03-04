---
title: Constructeurs privés - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, private constructors
- private constructors [C#]
ms.assetid: 29eeaa7d-8d81-453c-94b9-0e2800172621
ms.openlocfilehash: c0fd99cb9b9251de62c11c67dcb2ca696e24faf9
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57201779"
---
# <a name="private-constructors-c-programming-guide"></a><span data-ttu-id="466d6-102">Constructeurs privés (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="466d6-102">Private Constructors (C# Programming Guide)</span></span>
<span data-ttu-id="466d6-103">Un constructeur privé est un constructeur d’instance spécial.</span><span class="sxs-lookup"><span data-stu-id="466d6-103">A private constructor is a special instance constructor.</span></span> <span data-ttu-id="466d6-104">Il est généralement utilisé dans les classes qui contiennent uniquement des membres statiques.</span><span class="sxs-lookup"><span data-stu-id="466d6-104">It is generally used in classes that contain static members only.</span></span> <span data-ttu-id="466d6-105">Si une classe a un ou plusieurs constructeurs privés, mais n’a aucun constructeur public, les autres classes (à l’exception des classes imbriquées) ne peuvent pas créer d’instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="466d6-105">If a class has one or more private constructors and no public constructors, other classes (except nested classes) cannot create instances of this class.</span></span> <span data-ttu-id="466d6-106">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="466d6-106">For example:</span></span>  
  
 [!code-csharp[csProgGuideObjects#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#11)]  
  
 <span data-ttu-id="466d6-107">La déclaration du constructeur vide empêche la génération automatique d’un constructeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="466d6-107">The declaration of the empty constructor prevents the automatic generation of a default constructor.</span></span> <span data-ttu-id="466d6-108">Notez que si vous n’utilisez pas de modificateur d’accès avec le constructeur, le constructeur est toujours privé par défaut.</span><span class="sxs-lookup"><span data-stu-id="466d6-108">Note that if you do not use an access modifier with the constructor it will still be private by default.</span></span> <span data-ttu-id="466d6-109">En règle générale, le modificateur [private](../../../csharp/language-reference/keywords/private.md) est explicitement utilisé pour spécifier que la classe ne peut pas être instanciée.</span><span class="sxs-lookup"><span data-stu-id="466d6-109">However, the [private](../../../csharp/language-reference/keywords/private.md) modifier is usually used explicitly to make it clear that the class cannot be instantiated.</span></span>  
  
 <span data-ttu-id="466d6-110">Les constructeurs privés servent à empêcher la création d’instances d’une classe quand il n’y a pas de champs ou de méthodes d’instance (par exemple, la classe <xref:System.Math>) ou quand une méthode est appelée pour obtenir une instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="466d6-110">Private constructors are used to prevent creating instances of a class when there are no instance fields or methods, such as the <xref:System.Math> class, or when a method is called to obtain an instance of a class.</span></span> <span data-ttu-id="466d6-111">Si toutes les méthodes dans la classe sont statiques, définissez la classe entière comme statique.</span><span class="sxs-lookup"><span data-stu-id="466d6-111">If all the methods in the class are static, consider making the complete class static.</span></span> <span data-ttu-id="466d6-112">Pour plus d’informations, consultez [Classes statiques et membres de classe statique](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).</span><span class="sxs-lookup"><span data-stu-id="466d6-112">For more information see [Static Classes and Static Class Members](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="466d6-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="466d6-113">Example</span></span>  
 <span data-ttu-id="466d6-114">L’exemple suivant montre une classe qui utilise un constructeur privé.</span><span class="sxs-lookup"><span data-stu-id="466d6-114">The following is an example of a class using a private constructor.</span></span>  
  
 [!code-csharp[csProgGuideObjects#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#12)]  
  
 <span data-ttu-id="466d6-115">Notez que si vous décommentez l’instruction suivante dans l’exemple, une erreur est générée, car le constructeur a un niveau de protection qui le rend inaccessible :</span><span class="sxs-lookup"><span data-stu-id="466d6-115">Notice that if you uncomment the following statement from the example, it will generate an error because the constructor is inaccessible because of its protection level:</span></span>  
  
 [!code-csharp[csProgGuideObjects#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#13)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="466d6-116">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="466d6-116">C# Language Specification</span></span>  

<span data-ttu-id="466d6-117">Pour plus d’informations, consultez [Constructeurs privés](~/_csharplang/spec/classes.md#private-constructors) dans la [spécification du langage C#](../../language-reference/language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="466d6-117">For more information, see [Private constructors](~/_csharplang/spec/classes.md#private-constructors) in the [C# Language Specification](../../language-reference/language-specification/index.md).</span></span> <span data-ttu-id="466d6-118">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="466d6-118">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="466d6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="466d6-119">See also</span></span>

- [<span data-ttu-id="466d6-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="466d6-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="466d6-121">Classes et structs</span><span class="sxs-lookup"><span data-stu-id="466d6-121">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)
- [<span data-ttu-id="466d6-122">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="466d6-122">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)
- [<span data-ttu-id="466d6-123">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="466d6-123">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)
- [<span data-ttu-id="466d6-124">private</span><span class="sxs-lookup"><span data-stu-id="466d6-124">private</span></span>](../../../csharp/language-reference/keywords/private.md)
- [<span data-ttu-id="466d6-125">public</span><span class="sxs-lookup"><span data-stu-id="466d6-125">public</span></span>](../../../csharp/language-reference/keywords/public.md)
