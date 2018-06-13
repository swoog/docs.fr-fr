---
title: 'Comment : identifier un type Nullable (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- nullable types [C#], identifying
ms.assetid: d4b67ee2-66e8-40c1-ae9d-545d32c71387
ms.openlocfilehash: f3ac4ebd77fc92a133eb326919d5ba55264ced97
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33333181"
---
# <a name="how-to-identify-a-nullable-type-c-programming-guide"></a><span data-ttu-id="b6425-102">Comment : identifier un type Nullable (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="b6425-102">How to: Identify a Nullable Type (C# Programming Guide)</span></span>
<span data-ttu-id="b6425-103">Vous pouvez utiliser l’opérateur C# [typeof](../../../csharp/language-reference/keywords/typeof.md) pour créer un objet <xref:System.Type> qui représente un type Nullable :</span><span class="sxs-lookup"><span data-stu-id="b6425-103">You can use the C# [typeof](../../../csharp/language-reference/keywords/typeof.md) operator to create a <xref:System.Type> object that represents a Nullable type:</span></span>  
  
```  
System.Type type = typeof(int?);  
```  
  
 <span data-ttu-id="b6425-104">Vous pouvez également utiliser les classes et méthodes de l’espace de noms <xref:System.Reflection> pour générer des objets <xref:System.Type> qui représentent des types Nullable.</span><span class="sxs-lookup"><span data-stu-id="b6425-104">You can also use the classes and methods of the <xref:System.Reflection> namespace to generate <xref:System.Type> objects that represent Nullable types.</span></span> <span data-ttu-id="b6425-105">Toutefois, si, pendant l’exécution, vous essayez d’obtenir des informations de type à partir de variables Nullable à l’aide de la méthode <xref:System.Object.GetType%2A> ou de l’opérateur `is`, le résultat est un objet <xref:System.Type> qui représente le type sous-jacent, pas le type Nullable lui-même.</span><span class="sxs-lookup"><span data-stu-id="b6425-105">However, if you try to obtain type information from Nullable variables at runtime by using the <xref:System.Object.GetType%2A> method or the `is` operator, the result is a <xref:System.Type> object that represents the underlying type, not the Nullable type itself.</span></span>  
  
 <span data-ttu-id="b6425-106">L’appel de `GetType` sur un type Nullable entraîne l’exécution d’une opération de boxing quand le type est converti implicitement en <xref:System.Object>.</span><span class="sxs-lookup"><span data-stu-id="b6425-106">Calling `GetType` on a Nullable type causes a boxing operation to be performed when the type is implicitly converted to <xref:System.Object>.</span></span> <span data-ttu-id="b6425-107">Par conséquent, <xref:System.Object.GetType%2A> retourne toujours un objet <xref:System.Type> qui représente le type sous-jacent, pas le type Nullable.</span><span class="sxs-lookup"><span data-stu-id="b6425-107">Therefore <xref:System.Object.GetType%2A> always returns a <xref:System.Type> object that represents the underlying type, not the Nullable type.</span></span>  
  
```  
int? i = 5;  
Type t = i.GetType();  
Console.WriteLine(t.FullName); //"System.Int32"  
```  
  
 <span data-ttu-id="b6425-108">L’opérateur C# [is](../../../csharp/language-reference/keywords/is.md) fonctionne également sur le type sous-jacent d’un type Nullable.</span><span class="sxs-lookup"><span data-stu-id="b6425-108">The C# [is](../../../csharp/language-reference/keywords/is.md) operator also operates on a Nullable's underlying type.</span></span> <span data-ttu-id="b6425-109">Par conséquent, vous ne pouvez pas utiliser `is` pour déterminer si une variable est un type Nullable.</span><span class="sxs-lookup"><span data-stu-id="b6425-109">Therefore you cannot use `is` to determine whether a variable is a Nullable type.</span></span> <span data-ttu-id="b6425-110">L’exemple suivant montre que l’opérateur `is` traite une variable Nullable\<int> comme un int.</span><span class="sxs-lookup"><span data-stu-id="b6425-110">The following example shows that the `is` operator treats a Nullable\<int> variable as an int.</span></span>  
  
```  
static void Main(string[] args)  
{  
  int? i = 5;  
  if (i is int) // true  
    //…  
}  
```  
  
## <a name="example"></a><span data-ttu-id="b6425-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6425-111">Example</span></span>  
 <span data-ttu-id="b6425-112">Utilisez le code suivant pour déterminer si un objet <xref:System.Type> représente un type Nullable.</span><span class="sxs-lookup"><span data-stu-id="b6425-112">Use the following code to determine whether a <xref:System.Type> object represents a Nullable type.</span></span> <span data-ttu-id="b6425-113">N’oubliez pas que ce code retourne toujours la valeur false si l’objet`Type` a été retourné à partir d’un appel à <xref:System.Object.GetType%2A>, comme expliqué plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b6425-113">Remember that this code always returns false if the `Type` object was returned from a call to <xref:System.Object.GetType%2A>, as explained earlier in this topic.</span></span>  
  
```  
if (type.IsGenericType && type.GetGenericTypeDefinition() == typeof(Nullable<>)) {…}  
```  
  
## <a name="see-also"></a><span data-ttu-id="b6425-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6425-114">See Also</span></span>  
 [<span data-ttu-id="b6425-115">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="b6425-115">Nullable Types</span></span>](../../../csharp/programming-guide/nullable-types/index.md)  
 [<span data-ttu-id="b6425-116">Boxing des types Nullable</span><span class="sxs-lookup"><span data-stu-id="b6425-116">Boxing Nullable Types</span></span>](../../../csharp/programming-guide/nullable-types/boxing-nullable-types.md)
