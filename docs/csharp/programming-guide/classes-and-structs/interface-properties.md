---
title: Propriétés d'interface - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- properties [C#], on interfaces
- interfaces [C#], properties
ms.assetid: 6503e9ed-33d7-44ec-b4c1-cc16c084b795
ms.openlocfilehash: c51064f9bb5e834648e0086fd8d28f9c0bd84b61
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53241585"
---
# <a name="interface-properties-c-programming-guide"></a><span data-ttu-id="dbba4-102">Propriétés d'interface (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="dbba4-102">Interface Properties (C# Programming Guide)</span></span>
<span data-ttu-id="dbba4-103">Des propriétés peuvent être déclarées dans une [interface](../../../csharp/language-reference/keywords/interface.md).</span><span class="sxs-lookup"><span data-stu-id="dbba4-103">Properties can be declared on an [interface](../../../csharp/language-reference/keywords/interface.md).</span></span> <span data-ttu-id="dbba4-104">L’exemple ci-dessous porte sur un accesseur de propriété d’interface :</span><span class="sxs-lookup"><span data-stu-id="dbba4-104">The following is an example of an interface property accessor:</span></span>  
  
 [!code-csharp[csProgGuideProperties#14](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_1.cs)]  
  
 <span data-ttu-id="dbba4-105">L’accesseur d’une propriété d’interface n’a pas de corps.</span><span class="sxs-lookup"><span data-stu-id="dbba4-105">The accessor of an interface property does not have a body.</span></span> <span data-ttu-id="dbba4-106">Par conséquent, les accesseurs visent à indiquer si la propriété est en lecture-écriture, en lecture seule ou en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="dbba4-106">Thus, the purpose of the accessors is to indicate whether the property is read-write, read-only, or write-only.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dbba4-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="dbba4-107">Example</span></span>  
 <span data-ttu-id="dbba4-108">Dans cet exemple, l’interface `IEmployee` a une propriété en lecture-écriture, `Name`, et une propriété en lecture seule, `Counter`.</span><span class="sxs-lookup"><span data-stu-id="dbba4-108">In this example, the interface `IEmployee` has a read-write property, `Name`, and a read-only property, `Counter`.</span></span> <span data-ttu-id="dbba4-109">La classe `Employee` implémente l’interface `IEmployee` et utilise ces deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="dbba4-109">The class `Employee` implements the `IEmployee` interface and uses these two properties.</span></span> <span data-ttu-id="dbba4-110">Le programme lit le nom d’un nouvel employé et le nombre actuel d’employés et affiche le nom de l’employé et le nombre d’employés calculé.</span><span class="sxs-lookup"><span data-stu-id="dbba4-110">The program reads the name of a new employee and the current number of employees and displays the employee name and the computed employee number.</span></span>  
  
 <span data-ttu-id="dbba4-111">Vous pouvez utiliser le nom qualifié complet de la propriété, qui fait référence à l’interface dans laquelle le membre est déclaré.</span><span class="sxs-lookup"><span data-stu-id="dbba4-111">You could use the fully qualified name of the property, which references the interface in which the member is declared.</span></span> <span data-ttu-id="dbba4-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dbba4-112">For example:</span></span>  
  
 [!code-csharp[csProgGuideProperties#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_2.cs)]  
  
 <span data-ttu-id="dbba4-113">Ceci s’appelle une [implémentation d’interface explicite](../../../csharp/programming-guide/interfaces/explicit-interface-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="dbba4-113">This is called [Explicit Interface Implementation](../../../csharp/programming-guide/interfaces/explicit-interface-implementation.md).</span></span> <span data-ttu-id="dbba4-114">Par exemple, si la classe `Employee` implémente deux interfaces, `ICitizen` et `IEmployee`, et que les deux interfaces ont la même propriété `Name`, l’implémentation de membre d’interface explicite est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dbba4-114">For example, if the class `Employee` is implementing two interfaces `ICitizen` and `IEmployee` and both interfaces have the `Name` property, the explicit interface member implementation will be necessary.</span></span> <span data-ttu-id="dbba4-115">Autrement dit, la déclaration de propriété suivante :</span><span class="sxs-lookup"><span data-stu-id="dbba4-115">That is, the following property declaration:</span></span>  
  
 [!code-csharp[csProgGuideProperties#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_2.cs)]  
  
 <span data-ttu-id="dbba4-116">implémente la propriété `Name` dans l’interface `IEmployee`, alors que la déclaration suivante :</span><span class="sxs-lookup"><span data-stu-id="dbba4-116">implements the `Name` property on the `IEmployee` interface, while the following declaration:</span></span>  
  
 [!code-csharp[csProgGuideProperties#17](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_3.cs)]  
  
 <span data-ttu-id="dbba4-117">implémente la propriété `Name` dans l’interface `ICitizen`.</span><span class="sxs-lookup"><span data-stu-id="dbba4-117">implements the `Name` property on the `ICitizen` interface.</span></span>  
  
 [!code-csharp[csProgGuideProperties#15](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_4.cs)]  
  
  **`210 Hazem Abolrous`**    
## <a name="sample-output"></a><span data-ttu-id="dbba4-118">Résultat de l'exemple</span><span class="sxs-lookup"><span data-stu-id="dbba4-118">Sample Output</span></span>  
 `Enter number of employees: 210`  
  
 `Enter the name of the new employee: Hazem Abolrous`  
  
 `The employee information:`  
  
 `Employee number: 211`  
  
 `Employee name: Hazem Abolrous`  
  
## <a name="see-also"></a><span data-ttu-id="dbba4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbba4-119">See Also</span></span>

- [<span data-ttu-id="dbba4-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="dbba4-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="dbba4-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dbba4-121">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)  
- [<span data-ttu-id="dbba4-122">Utilisation de propriétés</span><span class="sxs-lookup"><span data-stu-id="dbba4-122">Using Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/using-properties.md)  
- [<span data-ttu-id="dbba4-123">Comparaison entre propriétés et indexeurs</span><span class="sxs-lookup"><span data-stu-id="dbba4-123">Comparison Between Properties and Indexers</span></span>](../../../csharp/programming-guide/indexers/comparison-between-properties-and-indexers.md)  
- [<span data-ttu-id="dbba4-124">Indexeurs</span><span class="sxs-lookup"><span data-stu-id="dbba4-124">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)  
- [<span data-ttu-id="dbba4-125">Interfaces</span><span class="sxs-lookup"><span data-stu-id="dbba4-125">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)
