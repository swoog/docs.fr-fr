---
title: 'Guide pratique pour créer une méthode pour une énumération (Guide de programmation C#) '
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [C#]
- extension methods [C#], for enums
- enum extensibility [C#]
ms.assetid: 100106f9-1e54-462c-8ebe-3892fe23b6eb
ms.openlocfilehash: 8de44cbddf26af45245709d0e28d2d157256ce59
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932213"
---
# <a name="how-to-create-a-new-method-for-an-enumeration-c-programming-guide"></a><span data-ttu-id="4db89-102">Guide pratique pour créer une méthode pour une énumération (Guide de programmation C#) </span><span class="sxs-lookup"><span data-stu-id="4db89-102">How to: Create a New Method for an Enumeration (C# Programming Guide)</span></span>
<span data-ttu-id="4db89-103">Vous pouvez utiliser des méthodes d’extension pour ajouter des fonctionnalités propres à un type enum particulier.</span><span class="sxs-lookup"><span data-stu-id="4db89-103">You can use extension methods to add functionality specific to a particular enum type.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4db89-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="4db89-104">Example</span></span>  
 <span data-ttu-id="4db89-105">Dans l’exemple suivant, l’énumération `Grades` représente les notes qu’un étudiant peut obtenir dans une classe.</span><span class="sxs-lookup"><span data-stu-id="4db89-105">In the following example, the `Grades` enumeration represents the possible letter grades that a student may receive in a class.</span></span> <span data-ttu-id="4db89-106">Une méthode d’extension nommée `Passing` est ajoutée au type `Grades` pour que chaque instance de ce type « sache » maintenant si elle représente une note au-dessus de la moyenne.</span><span class="sxs-lookup"><span data-stu-id="4db89-106">An extension method named `Passing` is added to the `Grades` type so that each instance of that type now "knows" whether it represents a passing grade or not.</span></span>  
  
 [!code-csharp[csProgGuideExtensionMethods#2](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-create-a-new-method-for-an-enumeration_1.cs)]  
  
 <span data-ttu-id="4db89-107">Notez que la classe `Extensions` contient également une variable statique qui est mise à jour de manière dynamique, et que la valeur de retour de la méthode d’extension reflète la valeur actuelle de cette variable.</span><span class="sxs-lookup"><span data-stu-id="4db89-107">Note that the `Extensions` class also contains a static variable that is updated dynamically and that the return value of the extension method reflects the current value of that variable.</span></span> <span data-ttu-id="4db89-108">Cela démontre que, dans les coulisses, les méthodes d’extension sont appelées directement sur la classe statique dans laquelle elles sont définies.</span><span class="sxs-lookup"><span data-stu-id="4db89-108">This demonstrates that, behind the scenes, extension methods are invoked directly on the static class in which they are defined.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="4db89-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="4db89-109">Compiling the Code</span></span>  
 <span data-ttu-id="4db89-110">Pour exécuter ce code, copiez et collez-le dans un projet d’application console Visual C# qui a été créé dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4db89-110">To run this code, copy and paste it into a Visual C# console application project that has been created in Visual Studio.</span></span> <span data-ttu-id="4db89-111">Par défaut, ce projet cible la version 3.5 du [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], et il a une référence à System.Core.dll et une directive `using` pour System.Linq.</span><span class="sxs-lookup"><span data-stu-id="4db89-111">By default, this project targets version 3.5 of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], and it has a reference to System.Core.dll and a `using` directive for System.Linq.</span></span> <span data-ttu-id="4db89-112">Si un ou plusieurs de ces éléments sont manquants dans le projet, vous pouvez les ajouter manuellement.</span><span class="sxs-lookup"><span data-stu-id="4db89-112">If one or more of these requirements are missing from the project, you can add them manually.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4db89-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4db89-113">See Also</span></span>  
 [<span data-ttu-id="4db89-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4db89-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="4db89-115">Méthodes d’extension</span><span class="sxs-lookup"><span data-stu-id="4db89-115">Extension Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/extension-methods.md)
