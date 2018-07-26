---
title: Constructeurs privés (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, private constructors
- private constructors [C#]
ms.assetid: 29eeaa7d-8d81-453c-94b9-0e2800172621
ms.openlocfilehash: e8f1f097a62f022d305987800e89353b038f42ae
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2018
ms.locfileid: "39244463"
---
# <a name="private-constructors-c-programming-guide"></a><span data-ttu-id="3d047-102">Constructeurs privés (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="3d047-102">Private Constructors (C# Programming Guide)</span></span>
<span data-ttu-id="3d047-103">Un constructeur privé est un constructeur d’instance spécial.</span><span class="sxs-lookup"><span data-stu-id="3d047-103">A private constructor is a special instance constructor.</span></span> <span data-ttu-id="3d047-104">Il est généralement utilisé dans les classes qui contiennent uniquement des membres statiques.</span><span class="sxs-lookup"><span data-stu-id="3d047-104">It is generally used in classes that contain static members only.</span></span> <span data-ttu-id="3d047-105">Si une classe a un ou plusieurs constructeurs privés, mais n’a aucun constructeur public, les autres classes (à l’exception des classes imbriquées) ne peuvent pas créer d’instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3d047-105">If a class has one or more private constructors and no public constructors, other classes (except nested classes) cannot create instances of this class.</span></span> <span data-ttu-id="3d047-106">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3d047-106">For example:</span></span>  
  
 [!code-csharp[csProgGuideObjects#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_1.cs)]  
  
 <span data-ttu-id="3d047-107">La déclaration du constructeur vide empêche la génération automatique d’un constructeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3d047-107">The declaration of the empty constructor prevents the automatic generation of a default constructor.</span></span> <span data-ttu-id="3d047-108">Notez que si vous n’utilisez pas de modificateur d’accès avec le constructeur, le constructeur est toujours privé par défaut.</span><span class="sxs-lookup"><span data-stu-id="3d047-108">Note that if you do not use an access modifier with the constructor it will still be private by default.</span></span> <span data-ttu-id="3d047-109">En règle générale, le modificateur [private](../../../csharp/language-reference/keywords/private.md) est explicitement utilisé pour spécifier que la classe ne peut pas être instanciée.</span><span class="sxs-lookup"><span data-stu-id="3d047-109">However, the [private](../../../csharp/language-reference/keywords/private.md) modifier is usually used explicitly to make it clear that the class cannot be instantiated.</span></span>  
  
 <span data-ttu-id="3d047-110">Les constructeurs privés servent à empêcher la création d’instances d’une classe quand il n’y a pas de champs ou de méthodes d’instance (par exemple, la classe <xref:System.Math>) ou quand une méthode est appelée pour obtenir une instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="3d047-110">Private constructors are used to prevent creating instances of a class when there are no instance fields or methods, such as the <xref:System.Math> class, or when a method is called to obtain an instance of a class.</span></span> <span data-ttu-id="3d047-111">Si toutes les méthodes dans la classe sont statiques, définissez la classe entière comme statique.</span><span class="sxs-lookup"><span data-stu-id="3d047-111">If all the methods in the class are static, consider making the complete class static.</span></span> <span data-ttu-id="3d047-112">Pour plus d’informations, consultez [Classes statiques et membres de classe statique](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).</span><span class="sxs-lookup"><span data-stu-id="3d047-112">For more information see [Static Classes and Static Class Members](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="3d047-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="3d047-113">Example</span></span>  
 <span data-ttu-id="3d047-114">L’exemple suivant montre une classe qui utilise un constructeur privé.</span><span class="sxs-lookup"><span data-stu-id="3d047-114">The following is an example of a class using a private constructor.</span></span>  
  
 [!code-csharp[csProgGuideObjects#12](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_2.cs)]  
  
 <span data-ttu-id="3d047-115">Notez que si vous décommentez l’instruction suivante dans l’exemple, une erreur est générée, car le constructeur a un niveau de protection qui le rend inaccessible :</span><span class="sxs-lookup"><span data-stu-id="3d047-115">Notice that if you uncomment the following statement from the example, it will generate an error because the constructor is inaccessible because of its protection level:</span></span>  
  
 [!code-csharp[csProgGuideObjects#13](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_3.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="3d047-116">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="3d047-116">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3d047-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d047-117">See Also</span></span>  
 [<span data-ttu-id="3d047-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="3d047-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="3d047-119">Classes et structs</span><span class="sxs-lookup"><span data-stu-id="3d047-119">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)  
 [<span data-ttu-id="3d047-120">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="3d047-120">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
 [<span data-ttu-id="3d047-121">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="3d047-121">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)  
 [<span data-ttu-id="3d047-122">private</span><span class="sxs-lookup"><span data-stu-id="3d047-122">private</span></span>](../../../csharp/language-reference/keywords/private.md)  
 [<span data-ttu-id="3d047-123">public</span><span class="sxs-lookup"><span data-stu-id="3d047-123">public</span></span>](../../../csharp/language-reference/keywords/public.md)
