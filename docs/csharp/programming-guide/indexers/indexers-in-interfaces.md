---
title: Indexeurs dans les interfaces - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- indexers [C#], in interfaces
- accessors [C#], indexers
ms.assetid: e16b54bd-4a83-4f52-bd75-65819fca79e8
ms.openlocfilehash: f277758a10b045a6365adfe931ce95d64eb8e445
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64608574"
---
# <a name="indexers-in-interfaces-c-programming-guide"></a><span data-ttu-id="44406-102">Indexeurs dans les interfaces (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="44406-102">Indexers in Interfaces (C# Programming Guide)</span></span>
<span data-ttu-id="44406-103">Des indexeurs peuvent être déclarés dans une [interface](../../../csharp/language-reference/keywords/interface.md).</span><span class="sxs-lookup"><span data-stu-id="44406-103">Indexers can be declared on an [interface](../../../csharp/language-reference/keywords/interface.md).</span></span> <span data-ttu-id="44406-104">Les accesseurs d’indexeurs d’interface se distinguent sur plusieurs plans des accesseurs d’indexeurs de [classe](../../../csharp/language-reference/keywords/class.md), à savoir :</span><span class="sxs-lookup"><span data-stu-id="44406-104">Accessors of interface indexers differ from the accessors of [class](../../../csharp/language-reference/keywords/class.md) indexers in the following ways:</span></span>  
  
- <span data-ttu-id="44406-105">Les accesseurs d’interface n’utilisent pas de modificateurs.</span><span class="sxs-lookup"><span data-stu-id="44406-105">Interface accessors do not use modifiers.</span></span>  
  
- <span data-ttu-id="44406-106">Un accesseur d’interface n’a pas de corps.</span><span class="sxs-lookup"><span data-stu-id="44406-106">An interface accessor does not have a body.</span></span>  
  
 <span data-ttu-id="44406-107">Par conséquent, un accesseur vise à indiquer si l’indexeur est en lecture-écriture, en lecture seule ou en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="44406-107">Thus, the purpose of the accessor is to indicate whether the indexer is read-write, read-only, or write-only.</span></span>  
  
 <span data-ttu-id="44406-108">L’exemple ci-dessous porte sur un accesseur d’indexeur d’interface :</span><span class="sxs-lookup"><span data-stu-id="44406-108">The following is an example of an interface indexer accessor:</span></span>  
  
 [!code-csharp[csProgGuideIndexers#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideIndexers/CS/Indexers.cs#3)]  
  
 <span data-ttu-id="44406-109">La signature d’un indexeur doit se distinguer de tous les autres indexeurs déclarés dans la même interface.</span><span class="sxs-lookup"><span data-stu-id="44406-109">The signature of an indexer must differ from the signatures of all other indexers declared in the same interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="44406-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="44406-110">Example</span></span>  
 <span data-ttu-id="44406-111">L’exemple suivant montre comment implémenter des indexeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="44406-111">The following example shows how to implement interface indexers.</span></span>  
  
 [!code-csharp[csProgGuideIndexers#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideIndexers/CS/Indexers.cs#4)]  
  
 <span data-ttu-id="44406-112">Dans l’exemple précédent, vous pouvez utiliser l’implémentation de membre d’interface explicite en utilisant le nom qualifié complet du membre d’interface.</span><span class="sxs-lookup"><span data-stu-id="44406-112">In the preceding example, you could use the explicit interface member implementation by using the fully qualified name of the interface member.</span></span> <span data-ttu-id="44406-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="44406-113">For example:</span></span>  
  
```  
string ISomeInterface.this[int index]   
{   
}   
```  
  
 <span data-ttu-id="44406-114">Cependant, le nom qualifié complet est seulement nécessaire pour éviter toute ambiguïté quand la classe implémente plusieurs interfaces avec la même signature d’indexeur.</span><span class="sxs-lookup"><span data-stu-id="44406-114">However, the fully qualified name is only needed to avoid ambiguity when the class is implementing more than one interface with the same indexer signature.</span></span> <span data-ttu-id="44406-115">Par exemple, si une classe `Employee` implémente deux interfaces, `ICitizen` et `IEmployee`, et que les deux interfaces ont la même signature d’indexeur, l’implémentation de membre d’interface explicite est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="44406-115">For example, if an `Employee` class is implementing two interfaces, `ICitizen` and `IEmployee`, and both interfaces have the same indexer signature, the explicit interface member implementation is necessary.</span></span> <span data-ttu-id="44406-116">Autrement dit, la déclaration d’indexeur suivante :</span><span class="sxs-lookup"><span data-stu-id="44406-116">That is, the following indexer declaration:</span></span>  
  
```  
string IEmployee.this[int index]   
{   
}   
```  
  
 <span data-ttu-id="44406-117">implémente l’indexeur dans l’interface `IEmployee`, alors que la déclaration suivante :</span><span class="sxs-lookup"><span data-stu-id="44406-117">implements the indexer on the `IEmployee` interface, while the following declaration:</span></span>  
  
```  
string ICitizen.this[int index]
{   
}   
```  
  
 <span data-ttu-id="44406-118">implémente l’interface dans l’interface `ICitizen`.</span><span class="sxs-lookup"><span data-stu-id="44406-118">implements the indexer on the `ICitizen` interface.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44406-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44406-119">See also</span></span>

- [<span data-ttu-id="44406-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="44406-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="44406-121">Indexeurs</span><span class="sxs-lookup"><span data-stu-id="44406-121">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)
- [<span data-ttu-id="44406-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="44406-122">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)
- [<span data-ttu-id="44406-123">Interfaces</span><span class="sxs-lookup"><span data-stu-id="44406-123">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)
