---
title: 'Comment : écrire un constructeur de copie (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- C# Language, copy constructor
- copy constructor [C#]
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
ms.openlocfilehash: d6ecfc3659dcf533db0f4e7b67fdffd620a584fd
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2018
ms.locfileid: "46705275"
---
# <a name="how-to-write-a-copy-constructor-c-programming-guide"></a><span data-ttu-id="0d387-102">Comment : écrire un constructeur de copie (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="0d387-102">How to: Write a Copy Constructor (C# Programming Guide)</span></span>
<span data-ttu-id="0d387-103">C# ne fournit pas de constructeur de copie pour les objets, mais vous pouvez en écrire un vous-même.</span><span class="sxs-lookup"><span data-stu-id="0d387-103">C# doesn't provide a copy constructor for objects, but you can write one yourself.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0d387-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0d387-104">Example</span></span>  
 <span data-ttu-id="0d387-105">Dans l’exemple suivant, la `Person`[classe](../../../csharp/language-reference/keywords/class.md) définit un constructeur de copie qui prend comme argument une instance de `Person`.</span><span class="sxs-lookup"><span data-stu-id="0d387-105">In the following example, the `Person`[class](../../../csharp/language-reference/keywords/class.md) defines a copy constructor that takes, as its argument, an instance of `Person`.</span></span> <span data-ttu-id="0d387-106">Les valeurs des propriétés de l’argument sont assignées aux propriétés de la nouvelle instance de `Person`.</span><span class="sxs-lookup"><span data-stu-id="0d387-106">The values of the properties of the argument are assigned to the properties of the new instance of `Person`.</span></span> <span data-ttu-id="0d387-107">Le code contient un autre constructeur de copie qui envoie les propriétés `Name` et `Age` de l’instance que vous voulez copier au constructeur d’instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="0d387-107">The code contains an alternative copy constructor that sends the `Name` and `Age` properties of the instance that you want to copy to the instance constructor of the class.</span></span>  
  
 [!code-csharp[csProgGuideObjects#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-write-a-copy-constructor_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="0d387-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d387-108">See Also</span></span>

- <xref:System.ICloneable>  
- [<span data-ttu-id="0d387-109">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0d387-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="0d387-110">Classes et structs</span><span class="sxs-lookup"><span data-stu-id="0d387-110">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)  
- [<span data-ttu-id="0d387-111">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="0d387-111">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
- [<span data-ttu-id="0d387-112">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="0d387-112">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)
