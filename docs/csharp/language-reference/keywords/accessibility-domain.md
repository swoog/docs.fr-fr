---
title: Domaine d'accessibilité - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- accessibility domain [C#]
ms.assetid: 8af779c1-275b-44be-a864-9edfbca71bcc
ms.openlocfilehash: 6028ec3184d7b9e61a62bf185fd37072636c6bc5
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235687"
---
# <a name="accessibility-domain-c-reference"></a><span data-ttu-id="79293-102">Domaine d'accessibilité (référence C#)</span><span class="sxs-lookup"><span data-stu-id="79293-102">Accessibility Domain (C# Reference)</span></span>
<span data-ttu-id="79293-103">Le domaine d’accessibilité d’un membre indique dans quelles sections du programme un membre peut être référencé.</span><span class="sxs-lookup"><span data-stu-id="79293-103">The accessibility domain of a member specifies in which program sections a member can be referenced.</span></span> <span data-ttu-id="79293-104">Si le membre est imbriqué dans un autre type, son domaine d’accessibilité est déterminé à la fois par le [niveau d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md) du membre et par le domaine d’accessibilité du type conteneur immédiat.</span><span class="sxs-lookup"><span data-stu-id="79293-104">If the member is nested within another type, its accessibility domain is determined by both the [accessibility level](../../../csharp/language-reference/keywords/accessibility-levels.md) of the member and the accessibility domain of the immediately containing type.</span></span>  
  
 <span data-ttu-id="79293-105">Le domaine d’accessibilité d’un type de niveau supérieur est au moins le texte du programme du projet dans lequel il est déclaré.</span><span class="sxs-lookup"><span data-stu-id="79293-105">The accessibility domain of a top-level type is at least the program text of the project that it is declared in.</span></span> <span data-ttu-id="79293-106">Cela signifie que le domaine inclut tous les fichiers sources de ce projet.</span><span class="sxs-lookup"><span data-stu-id="79293-106">That is, the domain includes all of the source files of this project.</span></span> <span data-ttu-id="79293-107">Le domaine d’accessibilité d’un type imbriqué est au moins le texte de programme du type dans lequel il est déclaré.</span><span class="sxs-lookup"><span data-stu-id="79293-107">The accessibility domain of a nested type is at least the program text of the type in which it is declared.</span></span> <span data-ttu-id="79293-108">Autrement dit, le domaine est le corps du type, qui inclut tous les types imbriqués.</span><span class="sxs-lookup"><span data-stu-id="79293-108">That is, the domain is the type body, which includes all nested types.</span></span> <span data-ttu-id="79293-109">Le domaine d’accessibilité d’un type imbriqué ne dépasse jamais celui du type conteneur.</span><span class="sxs-lookup"><span data-stu-id="79293-109">The accessibility domain of a nested type never exceeds that of the containing type.</span></span> <span data-ttu-id="79293-110">Ces concepts sont illustrés dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="79293-110">These concepts are demonstrated in the following example.</span></span>  
  
## <a name="example"></a><span data-ttu-id="79293-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="79293-111">Example</span></span>  
 <span data-ttu-id="79293-112">Cet exemple comporte un type de niveau supérieur, `T1`, et deux classes imbriquées, `M1` et `M2`.</span><span class="sxs-lookup"><span data-stu-id="79293-112">This example contains a top-level type, `T1`, and two nested classes, `M1` and `M2`.</span></span> <span data-ttu-id="79293-113">Les classes contiennent des champs qui ont des accessibilités déclarées différentes.</span><span class="sxs-lookup"><span data-stu-id="79293-113">The classes contain fields that have different declared accessibilities.</span></span> <span data-ttu-id="79293-114">Dans la méthode `Main`, un commentaire suit chaque instruction pour indiquer le domaine d’accessibilité de chaque membre.</span><span class="sxs-lookup"><span data-stu-id="79293-114">In the `Main` method, a comment follows each statement to indicate the accessibility domain of each member.</span></span> <span data-ttu-id="79293-115">Notez que les instructions qui tentent de référencer les membres inaccessibles sont commentées. Si vous voulez examiner les erreurs du compilateur causées par une référence à un membre inaccessible, supprimez les commentaires un à un.</span><span class="sxs-lookup"><span data-stu-id="79293-115">Notice that the statements that try to reference the inaccessible members are commented out. If you want to see the compiler errors caused by referencing an inaccessible member, remove the comments one at a time.</span></span>  
  
[!code-csharp[csrefKeywordsModifiers#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#4)]
  
## <a name="c-language-specification"></a><span data-ttu-id="79293-116">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="79293-116">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="79293-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79293-117">See Also</span></span>  
- [<span data-ttu-id="79293-118">Référence C#</span><span class="sxs-lookup"><span data-stu-id="79293-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="79293-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="79293-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="79293-120">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="79293-120">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="79293-121">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="79293-121">Access Modifiers</span></span>](../../../csharp/language-reference/keywords/access-modifiers.md)  
- [<span data-ttu-id="79293-122">Niveaux d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="79293-122">Accessibility Levels</span></span>](../../../csharp/language-reference/keywords/accessibility-levels.md)  
- [<span data-ttu-id="79293-123">Limitations sur l’utilisation des niveaux d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="79293-123">Restrictions on Using Accessibility Levels</span></span>](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md)  
- [<span data-ttu-id="79293-124">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="79293-124">Access Modifiers</span></span>](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
- [<span data-ttu-id="79293-125">public</span><span class="sxs-lookup"><span data-stu-id="79293-125">public</span></span>](../../../csharp/language-reference/keywords/public.md)  
- [<span data-ttu-id="79293-126">private</span><span class="sxs-lookup"><span data-stu-id="79293-126">private</span></span>](../../../csharp/language-reference/keywords/private.md)  
- [<span data-ttu-id="79293-127">protected</span><span class="sxs-lookup"><span data-stu-id="79293-127">protected</span></span>](../../../csharp/language-reference/keywords/protected.md)  
- [<span data-ttu-id="79293-128">internal</span><span class="sxs-lookup"><span data-stu-id="79293-128">internal</span></span>](../../../csharp/language-reference/keywords/internal.md)
