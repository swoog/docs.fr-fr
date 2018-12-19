---
title: Constructeurs privés - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, private constructors
- private constructors [C#]
ms.assetid: 29eeaa7d-8d81-453c-94b9-0e2800172621
ms.openlocfilehash: a0ff8f69f7725b40eaac01acef74857c2a99247c
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240500"
---
# <a name="private-constructors-c-programming-guide"></a><span data-ttu-id="9f2f8-102">Constructeurs privés (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="9f2f8-102">Private Constructors (C# Programming Guide)</span></span>
<span data-ttu-id="9f2f8-103">Un constructeur privé est un constructeur d’instance spécial.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-103">A private constructor is a special instance constructor.</span></span> <span data-ttu-id="9f2f8-104">Il est généralement utilisé dans les classes qui contiennent uniquement des membres statiques.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-104">It is generally used in classes that contain static members only.</span></span> <span data-ttu-id="9f2f8-105">Si une classe a un ou plusieurs constructeurs privés, mais n’a aucun constructeur public, les autres classes (à l’exception des classes imbriquées) ne peuvent pas créer d’instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-105">If a class has one or more private constructors and no public constructors, other classes (except nested classes) cannot create instances of this class.</span></span> <span data-ttu-id="9f2f8-106">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9f2f8-106">For example:</span></span>  
  
 [!code-csharp[csProgGuideObjects#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_1.cs)]  
  
 <span data-ttu-id="9f2f8-107">La déclaration du constructeur vide empêche la génération automatique d’un constructeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-107">The declaration of the empty constructor prevents the automatic generation of a default constructor.</span></span> <span data-ttu-id="9f2f8-108">Notez que si vous n’utilisez pas de modificateur d’accès avec le constructeur, le constructeur est toujours privé par défaut.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-108">Note that if you do not use an access modifier with the constructor it will still be private by default.</span></span> <span data-ttu-id="9f2f8-109">En règle générale, le modificateur [private](../../../csharp/language-reference/keywords/private.md) est explicitement utilisé pour spécifier que la classe ne peut pas être instanciée.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-109">However, the [private](../../../csharp/language-reference/keywords/private.md) modifier is usually used explicitly to make it clear that the class cannot be instantiated.</span></span>  
  
 <span data-ttu-id="9f2f8-110">Les constructeurs privés servent à empêcher la création d’instances d’une classe quand il n’y a pas de champs ou de méthodes d’instance (par exemple, la classe <xref:System.Math>) ou quand une méthode est appelée pour obtenir une instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-110">Private constructors are used to prevent creating instances of a class when there are no instance fields or methods, such as the <xref:System.Math> class, or when a method is called to obtain an instance of a class.</span></span> <span data-ttu-id="9f2f8-111">Si toutes les méthodes dans la classe sont statiques, définissez la classe entière comme statique.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-111">If all the methods in the class are static, consider making the complete class static.</span></span> <span data-ttu-id="9f2f8-112">Pour plus d’informations, consultez [Classes statiques et membres de classe statique](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).</span><span class="sxs-lookup"><span data-stu-id="9f2f8-112">For more information see [Static Classes and Static Class Members](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="9f2f8-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="9f2f8-113">Example</span></span>  
 <span data-ttu-id="9f2f8-114">L’exemple suivant montre une classe qui utilise un constructeur privé.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-114">The following is an example of a class using a private constructor.</span></span>  
  
 [!code-csharp[csProgGuideObjects#12](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_2.cs)]  
  
 <span data-ttu-id="9f2f8-115">Notez que si vous décommentez l’instruction suivante dans l’exemple, une erreur est générée, car le constructeur a un niveau de protection qui le rend inaccessible :</span><span class="sxs-lookup"><span data-stu-id="9f2f8-115">Notice that if you uncomment the following statement from the example, it will generate an error because the constructor is inaccessible because of its protection level:</span></span>  
  
 [!code-csharp[csProgGuideObjects#13](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_3.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="9f2f8-116">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9f2f8-116">C# Language Specification</span></span>  

<span data-ttu-id="9f2f8-117">Pour plus d’informations, consultez [Constructeurs privés](~/_csharplang/spec/classes.md#private-constructors) dans la [spécification du langage C#](../../language-reference/language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="9f2f8-117">For more information, see [Private constructors](~/_csharplang/spec/classes.md#private-constructors) in the [C# Language Specification](../../language-reference/language-specification/index.md).</span></span> <span data-ttu-id="9f2f8-118">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="9f2f8-118">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f2f8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f2f8-119">See Also</span></span>

- [<span data-ttu-id="9f2f8-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9f2f8-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="9f2f8-121">Classes et structs</span><span class="sxs-lookup"><span data-stu-id="9f2f8-121">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)  
- [<span data-ttu-id="9f2f8-122">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="9f2f8-122">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
- [<span data-ttu-id="9f2f8-123">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="9f2f8-123">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)  
- [<span data-ttu-id="9f2f8-124">private</span><span class="sxs-lookup"><span data-stu-id="9f2f8-124">private</span></span>](../../../csharp/language-reference/keywords/private.md)  
- [<span data-ttu-id="9f2f8-125">public</span><span class="sxs-lookup"><span data-stu-id="9f2f8-125">public</span></span>](../../../csharp/language-reference/keywords/public.md)
