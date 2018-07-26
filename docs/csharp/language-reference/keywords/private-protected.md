---
title: private protected (Référence C#)
ms.date: 11/15/2017
author: sputier
ms.openlocfilehash: 0d511f55f44511590fbe92a98cef118e0cb482e2
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2018
ms.locfileid: "37961130"
---
# <a name="private-protected-c-reference"></a><span data-ttu-id="46534-102">private protected (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="46534-102">private protected (C# Reference)</span></span>
<span data-ttu-id="46534-103">La combinaison de mots clés `private protected` est un modificateur d’accès de membre.</span><span class="sxs-lookup"><span data-stu-id="46534-103">The `private protected` keyword combination is a member access modifier.</span></span> <span data-ttu-id="46534-104">Un membre protégé privé est accessible par les types dérivés de la classe conteneur, mais seulement au sein de son assembly conteneur.</span><span class="sxs-lookup"><span data-stu-id="46534-104">A private protected member is accessible by types derived from the containing class, but only within its containing assembly.</span></span> <span data-ttu-id="46534-105">Pour obtenir une comparaison de `private protected` et des autres modificateurs d’accès, consultez [Niveaux d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md).</span><span class="sxs-lookup"><span data-stu-id="46534-105">For a comparison of `private protected` with the other access modifiers, see [Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md).</span></span> 

> [!NOTE]
> <span data-ttu-id="46534-106">Le modificateur d’accès `private protected` est valide dans C# 7.2 et ultérieur.</span><span class="sxs-lookup"><span data-stu-id="46534-106">The `private protected` access modifier is valid in C# version 7.2 and later.</span></span>
   
## <a name="example"></a><span data-ttu-id="46534-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="46534-107">Example</span></span>  
 <span data-ttu-id="46534-108">Un membre protégé privé d’une classe de base est accessible à partir des types dérivés de son assembly conteneur seulement si le type statique de la variable est le type de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="46534-108">A private protected member of a base class is accessible from derived types in its containing assembly only if the static type of the variable is the derived class type.</span></span> <span data-ttu-id="46534-109">Prenons l’exemple de l’extrait de code suivant :</span><span class="sxs-lookup"><span data-stu-id="46534-109">For example, consider the following code segment:</span></span>  
  
 ```csharp
 // Assembly1.cs  
 // Compile with: /target:library  
 public class BaseClass
 {
     private protected int myValue = 0;
 }
 
 public class DerivedClass1 : BaseClass
 {
     void Access()
     {
         BaseClass baseObject = new BaseClass();
 
         // Error CS1540, because myValue can only be accessed by
         // classes derived from BaseClass.
         // baseObject.myValue = 5;  
 
         // OK, accessed through the current derived class instance
         myValue = 5;
     }
 }
```  
  
```csharp  
 // Assembly2.cs  
 // Compile with: /reference:Assembly1.dll  
 class DerivedClass2 : BaseClass
 {
     void Access()
     {
         // Error CS0122, because myValue can only be
         // accessed by types in Assembly1
         // myValue = 10;
     }
 }
```  
 <span data-ttu-id="46534-110">Cet exemple contient deux fichiers : `Assembly1.cs` et `Assembly2.cs`.</span><span class="sxs-lookup"><span data-stu-id="46534-110">This example contains two files, `Assembly1.cs` and `Assembly2.cs`.</span></span> <span data-ttu-id="46534-111">Le premier fichier contient une classe de base publique, `BaseClass`, et un type qui en est dérivé, `DerivedClass1`.</span><span class="sxs-lookup"><span data-stu-id="46534-111">The first file contains a public base class, `BaseClass`, and a type derived from it, `DerivedClass1`.</span></span> <span data-ttu-id="46534-112">`BaseClass` possède un membre protégé privé, `myValue`, auquel `DerivedClass1` tente d’accéder de deux manières.</span><span class="sxs-lookup"><span data-stu-id="46534-112">`BaseClass` owns a private protected member, `myValue`, which `DerivedClass1` tries to access in two ways.</span></span> <span data-ttu-id="46534-113">La première tentative d’accès à `myValue` via une instance de `BaseClass` génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="46534-113">The first attempt to access `myValue` through an instance of `BaseClass` will produce an error.</span></span> <span data-ttu-id="46534-114">Cependant, la tentative de l’utiliser comme un membre hérité dans `DerivedClass1` réussit.</span><span class="sxs-lookup"><span data-stu-id="46534-114">However, the attempt to use it as an inherited member in `DerivedClass1` will succeed.</span></span>
<span data-ttu-id="46534-115">Dans le deuxième fichier, une tentative d’accès à `myValue` en tant que membre hérité de `DerivedClass2` génère une erreur, car il est accessible seulement par des types dérivés dans Assembly1.</span><span class="sxs-lookup"><span data-stu-id="46534-115">In the second file, an attempt to access `myValue` as an inherited member of `DerivedClass2` will produce an error, as it is only accessible by derived types in Assembly1.</span></span> 

 <span data-ttu-id="46534-116">Les membres de struct ne peuvent pas être `private protected`, car le struct ne peut pas être hérité.</span><span class="sxs-lookup"><span data-stu-id="46534-116">Struct members cannot be `private protected` because the struct cannot be inherited.</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="46534-117">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="46534-117">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="46534-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46534-118">See Also</span></span>  
 <span data-ttu-id="46534-119">[Référence du langage C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="46534-119">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="46534-120">[Guide de programmation C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="46534-120">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="46534-121">[Mots clés C#](../../../csharp/language-reference/keywords/index.md) </span><span class="sxs-lookup"><span data-stu-id="46534-121">[C# Keywords](../../../csharp/language-reference/keywords/index.md) </span></span>  
 <span data-ttu-id="46534-122">[Modificateurs d’accès](../../../csharp/language-reference/keywords/access-modifiers.md) </span><span class="sxs-lookup"><span data-stu-id="46534-122">[Access Modifiers](../../../csharp/language-reference/keywords/access-modifiers.md) </span></span>  
 <span data-ttu-id="46534-123">[Niveaux d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md) </span><span class="sxs-lookup"><span data-stu-id="46534-123">[Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md) </span></span>  
 <span data-ttu-id="46534-124">[Modificateurs](../../../csharp/language-reference/keywords/modifiers.md) </span><span class="sxs-lookup"><span data-stu-id="46534-124">[Modifiers](../../../csharp/language-reference/keywords/modifiers.md) </span></span>  
 <span data-ttu-id="46534-125">[public](../../../csharp/language-reference/keywords/public.md) </span><span class="sxs-lookup"><span data-stu-id="46534-125">[public](../../../csharp/language-reference/keywords/public.md) </span></span>  
 <span data-ttu-id="46534-126">[private](../../../csharp/language-reference/keywords/private.md) </span><span class="sxs-lookup"><span data-stu-id="46534-126">[private](../../../csharp/language-reference/keywords/private.md) </span></span>  
 <span data-ttu-id="46534-127">[internal](../../../csharp/language-reference/keywords/internal.md) </span><span class="sxs-lookup"><span data-stu-id="46534-127">[internal](../../../csharp/language-reference/keywords/internal.md) </span></span>  
 <span data-ttu-id="46534-128">[Problèmes de sécurité pour les mots clés virtuels internes](https://msdn.microsoft.com/library/heyd8kky(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="46534-128">[Security concerns for internal virtual keywords](https://msdn.microsoft.com/library/heyd8kky(v=vs.110))</span></span>
