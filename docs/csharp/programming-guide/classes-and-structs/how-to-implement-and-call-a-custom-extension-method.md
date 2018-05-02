---
title: Guide pratique pour implémenter et appeler une méthode d’extension personnalisée (Guide de programmation C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- extension methods [C#], implementing and calling
ms.assetid: 7dab2a56-cf8e-4a47-a444-fe610a02772a
caps.latest.revision: 15
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e73ccee84c35678a4923347ab04619bb6017aca5
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-implement-and-call-a-custom-extension-method-c-programming-guide"></a><span data-ttu-id="63304-102">Guide pratique pour implémenter et appeler une méthode d’extension personnalisée (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="63304-102">How to: Implement and Call a Custom Extension Method (C# Programming Guide)</span></span>
<span data-ttu-id="63304-103">Cette rubrique montre comment implémenter vos propres méthodes d’extension pour n’importe quel type .NET.</span><span class="sxs-lookup"><span data-stu-id="63304-103">This topic shows how to implement your own extension methods for any .NET type.</span></span> <span data-ttu-id="63304-104">Le code client peut utiliser vos méthodes d’extension en ajoutant une référence à la DLL qui les contient, et en ajoutant une directive [using](../../../csharp/language-reference/keywords/using-directive.md) qui spécifie l’espace de noms dans lequel les méthodes d’extension sont définies.</span><span class="sxs-lookup"><span data-stu-id="63304-104">Client code can use your extension methods by adding a reference to the DLL that contains them, and adding a [using](../../../csharp/language-reference/keywords/using-directive.md) directive that specifies the namespace in which the extension methods are defined.</span></span>  
  
## <a name="to-define-and-call-the-extension-method"></a><span data-ttu-id="63304-105">Pour définir et appeler la méthode d’extension</span><span class="sxs-lookup"><span data-stu-id="63304-105">To define and call the extension method</span></span>  
  
1.  <span data-ttu-id="63304-106">Définissez une [classe](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md) statique pour contenir la méthode d’extension.</span><span class="sxs-lookup"><span data-stu-id="63304-106">Define a static [class](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md) to contain the extension method.</span></span>  
  
     <span data-ttu-id="63304-107">La classe doit être visible par le code client.</span><span class="sxs-lookup"><span data-stu-id="63304-107">The class must be visible to client code.</span></span> <span data-ttu-id="63304-108">Pour plus d’informations sur les règles d’accessibilité, consultez [Modificateurs d’accès](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span><span class="sxs-lookup"><span data-stu-id="63304-108">For more information about accessibility rules, see [Access Modifiers](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span></span>  
  
2.  <span data-ttu-id="63304-109">Implémentez la méthode d’extension en tant que méthode statique avec au moins la même visibilité que la classe conteneur.</span><span class="sxs-lookup"><span data-stu-id="63304-109">Implement the extension method as a static method with at least the same visibility as the containing class.</span></span>  
  
3.  <span data-ttu-id="63304-110">Le premier paramètre de la méthode spécifie le type sur lequel la méthode opère. Il doit être précédé du modificateur [this](../../../csharp/language-reference/keywords/this.md).</span><span class="sxs-lookup"><span data-stu-id="63304-110">The first parameter of the method specifies the type that the method operates on; it must be preceded with the [this](../../../csharp/language-reference/keywords/this.md) modifier.</span></span>  
  
4.  <span data-ttu-id="63304-111">Dans le code appelant, ajoutez une directive `using` pour spécifier l’[espace de noms](../../../csharp/language-reference/keywords/namespace.md) qui contient la classe de méthode d’extension.</span><span class="sxs-lookup"><span data-stu-id="63304-111">In the calling code, add a `using` directive to specify the [namespace](../../../csharp/language-reference/keywords/namespace.md) that contains the extension method class.</span></span>  
  
5.  <span data-ttu-id="63304-112">Appelez les méthodes comme s’il s’agissait de méthodes d’instance sur le type.</span><span class="sxs-lookup"><span data-stu-id="63304-112">Call the methods as if they were instance methods on the type.</span></span>  
  
     <span data-ttu-id="63304-113">Notez que le premier paramètre n’est pas spécifié par le code appelant, car il représente le type sur lequel l’opérateur est appliqué, et le compilateur connaît déjà le type de votre objet.</span><span class="sxs-lookup"><span data-stu-id="63304-113">Note that the first parameter is not specified by calling code because it represents the type on which the operator is being applied, and the compiler already knows the type of your object.</span></span> <span data-ttu-id="63304-114">Vous devez fournir des arguments uniquement pour les paramètres 2 à `n`.</span><span class="sxs-lookup"><span data-stu-id="63304-114">You only have to provide arguments for parameters 2 through `n`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="63304-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="63304-115">Example</span></span>  
 <span data-ttu-id="63304-116">L’exemple suivant implémente une méthode d’extension nommée `WordCount` dans la classe `CustomExtensions.StringExtension`.</span><span class="sxs-lookup"><span data-stu-id="63304-116">The following example implements an extension method named `WordCount` in the `CustomExtensions.StringExtension` class.</span></span> <span data-ttu-id="63304-117">La méthode opère sur la classe <xref:System.String>, qui est spécifiée comme premier paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="63304-117">The method operates on the <xref:System.String> class, which is specified as the first method parameter.</span></span> <span data-ttu-id="63304-118">L’espace de noms `CustomExtensions` est importé dans l’espace de noms d’application, et la méthode est appelée à l’intérieur de la méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="63304-118">The `CustomExtensions` namespace is imported into the application namespace, and the method is called inside the `Main` method.</span></span>  
  
 [!code-csharp[csProgGuideExtensionMethods#1](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-implement-and-call-a-custom-extension-method_1.cs)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="63304-119">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="63304-119">Compiling the Code</span></span>  
 <span data-ttu-id="63304-120">Pour exécuter ce code, copiez et collez-le dans un projet d’application console Visual C# qui a été créé dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="63304-120">To run this code, copy and paste it into a Visual C# console application project that has been created in Visual Studio.</span></span> <span data-ttu-id="63304-121">Par défaut, ce projet cible la version 3.5 du [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], et il a une référence à System.Core.dll et une directive `using` pour System.Linq.</span><span class="sxs-lookup"><span data-stu-id="63304-121">By default, this project targets version 3.5 of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], and it has a reference to System.Core.dll and a `using` directive for System.Linq.</span></span> <span data-ttu-id="63304-122">Si un ou plusieurs de ces éléments sont manquants dans le projet, vous pouvez les ajouter manuellement.</span><span class="sxs-lookup"><span data-stu-id="63304-122">If one or more of these requirements are missing from the project, you can add them manually.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="63304-123">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="63304-123">.NET Framework Security</span></span>  
 <span data-ttu-id="63304-124">Les méthodes d’extension ne présentent aucune faille de sécurité spécifique.</span><span class="sxs-lookup"><span data-stu-id="63304-124">Extension methods present no specific security vulnerabilities.</span></span> <span data-ttu-id="63304-125">Elles ne peuvent jamais être utilisées pour emprunter l’identité des méthodes existantes sur un type, car toutes les collisions de noms sont résolues en faveur de l’instance ou de la méthode statique définie par le type lui-même.</span><span class="sxs-lookup"><span data-stu-id="63304-125">They can never be used to impersonate existing methods on a type, because all name collisions are resolved in favor of the instance or static method defined by the type itself.</span></span> <span data-ttu-id="63304-126">Les méthodes d’extension ne peuvent pas accéder à des données privées dans la classe étendue.</span><span class="sxs-lookup"><span data-stu-id="63304-126">Extension methods cannot access any private data in the extended class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63304-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63304-127">See Also</span></span>  
 [<span data-ttu-id="63304-128">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="63304-128">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="63304-129">Méthodes d’extension</span><span class="sxs-lookup"><span data-stu-id="63304-129">Extension Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/extension-methods.md)  
 [<span data-ttu-id="63304-130">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="63304-130">LINQ (Language-Integrated Query)</span></span>](http://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)  
 [<span data-ttu-id="63304-131">Classes statiques et membres de classe statique</span><span class="sxs-lookup"><span data-stu-id="63304-131">Static Classes and Static Class Members</span></span>](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)  
 [<span data-ttu-id="63304-132">protected</span><span class="sxs-lookup"><span data-stu-id="63304-132">protected</span></span>](../../../csharp/language-reference/keywords/protected.md)  
 [<span data-ttu-id="63304-133">internal</span><span class="sxs-lookup"><span data-stu-id="63304-133">internal</span></span>](../../../csharp/language-reference/keywords/internal.md)  
 [<span data-ttu-id="63304-134">public</span><span class="sxs-lookup"><span data-stu-id="63304-134">public</span></span>](../../../csharp/language-reference/keywords/public.md)  
 [<span data-ttu-id="63304-135">this</span><span class="sxs-lookup"><span data-stu-id="63304-135">this</span></span>](../../../csharp/language-reference/keywords/this.md)  
 [<span data-ttu-id="63304-136">namespace</span><span class="sxs-lookup"><span data-stu-id="63304-136">namespace</span></span>](../../../csharp/language-reference/keywords/namespace.md)
