---
title: Constructeurs statiques - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- static constructors [C#]
- constructors [C#], static
ms.assetid: 151ec95e-3c4d-4ed7-885d-95b7a3be2e7d
ms.openlocfilehash: 87a7b16d3e096f6a5bf05475ccc7c43862324ae3
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64583353"
---
# <a name="static-constructors-c-programming-guide"></a><span data-ttu-id="2d0fb-102">Constructeurs statiques (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="2d0fb-102">Static Constructors (C# Programming Guide)</span></span>
<span data-ttu-id="2d0fb-103">Un constructeur statique est utilisé pour initialiser des données [statiques](../../../csharp/language-reference/keywords/static.md) ou pour effectuer une action particulière qui ne doit être effectuée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-103">A static constructor is used to initialize any [static](../../../csharp/language-reference/keywords/static.md) data, or to perform a particular action that needs to be performed once only.</span></span> <span data-ttu-id="2d0fb-104">Il est automatiquement appelé avant la création de la première instance ou le référencement d’un membre statique.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-104">It is called automatically before the first instance is created or any static members are referenced.</span></span>  
  
 [!code-csharp[csProgGuideObjects#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#14)]  
  
 <span data-ttu-id="2d0fb-105">Les constructeurs statiques ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d0fb-105">Static constructors have the following properties:</span></span>  
  
- <span data-ttu-id="2d0fb-106">Un constructeur statique n’accepte pas de modificateur d’accès et n’a pas de paramètre.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-106">A static constructor does not take access modifiers or have parameters.</span></span>  
  
- <span data-ttu-id="2d0fb-107">Un constructeur statique est automatiquement appelé pour initialiser la [classe](../../../csharp/language-reference/keywords/class.md) avant la création de la première instance ou le référencement d’un membre statique.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-107">A static constructor is called automatically to initialize the [class](../../../csharp/language-reference/keywords/class.md) before the first instance is created or any static members are referenced.</span></span>  
  
- <span data-ttu-id="2d0fb-108">Un constructeur statique ne peut pas être appelé directement.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-108">A static constructor cannot be called directly.</span></span>  
  
- <span data-ttu-id="2d0fb-109">L’utilisateur n’a aucun contrôle sur le moment d’exécution du constructeur statique dans le programme.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-109">The user has no control on when the static constructor is executed in the program.</span></span>  
  
- <span data-ttu-id="2d0fb-110">Généralement, on utilise des constructeurs statiques quand la classe utilise un fichier journal et que le constructeur sert à écrire des entrées dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-110">A typical use of static constructors is when the class is using a log file and the constructor is used to write entries to this file.</span></span>  
  
- <span data-ttu-id="2d0fb-111">Les constructeurs statiques sont également utiles pour la création de classes wrapper pour du code non managé, quand le constructeur peut appeler la méthode `LoadLibrary`.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-111">Static constructors are also useful when creating wrapper classes for unmanaged code, when the constructor can call the `LoadLibrary` method.</span></span>  
  
- <span data-ttu-id="2d0fb-112">Si un constructeur statique lève une exception, le runtime ne l’appelle pas une deuxième fois et le type reste non initialisé pour la durée de vie du domaine d’application dans lequel votre programme s’exécute.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-112">If a static constructor throws an exception, the runtime will not invoke it a second time, and the type will remain uninitialized for the lifetime of the application domain in which your program is running.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2d0fb-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="2d0fb-113">Example</span></span>  
 <span data-ttu-id="2d0fb-114">Dans cet exemple, la classe `Bus` possède un constructeur statique.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-114">In this example, class `Bus` has a static constructor.</span></span> <span data-ttu-id="2d0fb-115">Quand la première instance de `Bus` est créée (`bus1`), le constructeur statique est appelé pour initialiser la classe.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-115">When the first instance of `Bus` is created (`bus1`), the static constructor is invoked to initialize the class.</span></span> <span data-ttu-id="2d0fb-116">L’exemple de sortie vérifie que le constructeur statique s’exécute une seule fois, même si deux instances de `Bus` sont créées, et qu’il s’exécute avant le constructeur d’instance.</span><span class="sxs-lookup"><span data-stu-id="2d0fb-116">The sample output verifies that the static constructor runs only one time, even though two instances of `Bus` are created, and that it runs before the instance constructor runs.</span></span>  
  
 [!code-csharp[csProgGuideObjects#15](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#15)]  
  
## <a name="see-also"></a><span data-ttu-id="2d0fb-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d0fb-117">See also</span></span>

- [<span data-ttu-id="2d0fb-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2d0fb-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="2d0fb-119">Classes et structs</span><span class="sxs-lookup"><span data-stu-id="2d0fb-119">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)
- [<span data-ttu-id="2d0fb-120">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="2d0fb-120">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)
- [<span data-ttu-id="2d0fb-121">Classes statiques et membres de classe statique</span><span class="sxs-lookup"><span data-stu-id="2d0fb-121">Static Classes and Static Class Members</span></span>](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)
- [<span data-ttu-id="2d0fb-122">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="2d0fb-122">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)
