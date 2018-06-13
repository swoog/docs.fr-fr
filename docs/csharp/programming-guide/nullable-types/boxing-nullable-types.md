---
title: Boxing des types Nullable (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- boxing [C#], nullable types
- unboxing [C#], nullable types
- nullable types [C#], boxing and unboxing
ms.assetid: bdb5b626-abc0-405d-8f64-0f0a0bf883a4
ms.openlocfilehash: e2c7602bf45f1861d3a32a73824e9fedf0a4d29d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33334754"
---
# <a name="boxing-nullable-types-c-programming-guide"></a><span data-ttu-id="9efa1-102">Boxing des types Nullable (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="9efa1-102">Boxing Nullable Types (C# Programming Guide)</span></span>
<span data-ttu-id="9efa1-103">Les objets basés sur des types Nullable sont boxed uniquement si l’objet n’est pas Null.</span><span class="sxs-lookup"><span data-stu-id="9efa1-103">Objects based on nullable types are only boxed if the object is non-null.</span></span> <span data-ttu-id="9efa1-104">Si <xref:System.Nullable%601.HasValue%2A> a la valeur `false`, la référence d’objet est affectée à `null` au lieu du boxing.</span><span class="sxs-lookup"><span data-stu-id="9efa1-104">If <xref:System.Nullable%601.HasValue%2A> is `false`, the object reference is assigned to `null` instead of boxing.</span></span> <span data-ttu-id="9efa1-105">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9efa1-105">For example:</span></span>  
  
```csharp  
bool? b = null;  
object o = b;  
// Now o is null.  
```  
  
 <span data-ttu-id="9efa1-106">Si l’objet n’est pas null (si <xref:System.Nullable%601.HasValue%2A> a la valeur `true`), le boxing s’applique uniquement au type sous-jacent sur lequel repose l’objet Nullable.</span><span class="sxs-lookup"><span data-stu-id="9efa1-106">If the object is non-null -- if <xref:System.Nullable%601.HasValue%2A> is `true` -- then boxing occurs, but only the underlying type that the nullable object is based on is boxed.</span></span> <span data-ttu-id="9efa1-107">Le boxing d’un type de valeur Nullable non null convertit le type de valeur lui-même, et non pas le <xref:System.Nullable%601?displayProperty=nameWithType> qui encapsule le type de valeur.</span><span class="sxs-lookup"><span data-stu-id="9efa1-107">Boxing a non-null nullable value type boxes the value type itself, not the <xref:System.Nullable%601?displayProperty=nameWithType> that wraps the value type.</span></span> <span data-ttu-id="9efa1-108">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9efa1-108">For example:</span></span>  
  
```csharp  
bool? b = false;  
int? i = 44;  
object bBoxed = b; // bBoxed contains a boxed bool.  
object iBoxed = i; // iBoxed contains a boxed int.  
```  
  
 <span data-ttu-id="9efa1-109">Les deux objets boxed sont identiques à ceux créés par le boxing des types non Nullable.</span><span class="sxs-lookup"><span data-stu-id="9efa1-109">The two boxed objects are identical to those created by boxing non-nullable types.</span></span> <span data-ttu-id="9efa1-110">Comme les types boxed non Nullable, ils peuvent être unboxed en types Nullable, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="9efa1-110">And, just like non-nullable boxed types, they can be unboxed into nullable types, as in the following example:</span></span>  
  
```csharp  
bool? b2 = (bool?)bBoxed;  
int? i2 = (int?)iBoxed;  
```  
  
## <a name="remarks"></a><span data-ttu-id="9efa1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9efa1-111">Remarks</span></span>  
 <span data-ttu-id="9efa1-112">Le comportement de types Nullable quand ils sont boxed présente deux avantages :</span><span class="sxs-lookup"><span data-stu-id="9efa1-112">The behavior of nullable types when boxed provides two advantages:</span></span>  
  
1.  <span data-ttu-id="9efa1-113">Les objets Nullable et leur équivalent boxed peuvent être testés pour chercher des valeurs Null :</span><span class="sxs-lookup"><span data-stu-id="9efa1-113">Nullable objects and their boxed counterpart can be tested for null:</span></span>  
  
    ```csharp  
    bool? b = null;  
    object boxedB = b;  
    if (b == null)  
    {  
      // True.  
    }  
    if (boxedB == null)  
    {  
      // Also true.  
    }  
    ```  
  
2.  <span data-ttu-id="9efa1-114">Les types Nullable boxed prennent en charge pleinement les fonctionnalités du type sous-jacent :</span><span class="sxs-lookup"><span data-stu-id="9efa1-114">Boxed nullable types fully support the functionality of the underlying type:</span></span>  
  
    ```csharp  
    double? d = 44.4;  
    object iBoxed = d;  
    // Access IConvertible interface implemented by double.  
    IConvertible ic = (IConvertible)iBoxed;  
    int i = ic.ToInt32(null);  
    string str = ic.ToString();  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="9efa1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9efa1-115">See Also</span></span>  
 [<span data-ttu-id="9efa1-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9efa1-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="9efa1-117">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="9efa1-117">Nullable Types</span></span>](../../../csharp/programming-guide/nullable-types/index.md)  
 [<span data-ttu-id="9efa1-118">Comment : identifier un type Nullable</span><span class="sxs-lookup"><span data-stu-id="9efa1-118">How to: Identify a Nullable Type</span></span>](../../../csharp/programming-guide/nullable-types/how-to-identify-a-nullable-type.md)
