---
title: System.Convert, méthodes
ms.date: 03/30/2017
ms.assetid: 3ca6c5b6-ea5d-4ab0-b675-f082135b342c
ms.openlocfilehash: 0d98d159c24e1a47723aeb07a9654fe22b1d9464
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59198216"
---
# <a name="systemconvert-methods"></a><span data-ttu-id="ed788-102">System.Convert, méthodes</span><span class="sxs-lookup"><span data-stu-id="ed788-102">System.Convert Methods</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="ed788-103">ne prend pas en charge les éléments suivants <xref:System.Convert> méthodes.</span><span class="sxs-lookup"><span data-stu-id="ed788-103">does not support the following <xref:System.Convert> methods.</span></span>  
  
-   <span data-ttu-id="ed788-104">Versions avec un paramètre <xref:System.IFormatProvider>.</span><span class="sxs-lookup"><span data-stu-id="ed788-104">Versions with an <xref:System.IFormatProvider> parameter.</span></span>  
  
-   <span data-ttu-id="ed788-105">Méthodes impliquant des tableaux de caractères ou d'octets :</span><span class="sxs-lookup"><span data-stu-id="ed788-105">Methods that involve char arrays or byte arrays:</span></span>  
  
    -   <xref:System.Convert.FromBase64CharArray%2A>  
  
    -   <xref:System.Convert.ToBase64CharArray%2A>  
  
    -   <xref:System.Convert.FromBase64String%2A>  
  
    -   <xref:System.Convert.ToBase64String%2A>  
  
-   <span data-ttu-id="ed788-106">Les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ed788-106">The following methods:</span></span>  
  
    -   `public static <Type2> To<Type2>(<Type1> value);` <span data-ttu-id="ed788-107">où</span><span class="sxs-lookup"><span data-stu-id="ed788-107">where</span></span>  
  
         `Type1` <span data-ttu-id="ed788-108">et `Type2` sont chacun des `sbyte`, `uint`, `ulong`, ou `ushort`.</span><span class="sxs-lookup"><span data-stu-id="ed788-108">and `Type2` are each one of `sbyte`, `uint`, `ulong`, or `ushort`.</span></span>  
  
    -   <span data-ttu-id="ed788-109">C# :</span><span class="sxs-lookup"><span data-stu-id="ed788-109">C#:</span></span>  
  
         `int To<int type>(string value, int fromBase),`  
  
         `ToString(... value, int toBase)`  
  
    -   <span data-ttu-id="ed788-110">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="ed788-110">Visual Basic:</span></span>  
  
         `Function To(Of [Numeric])(value as String, fromBase As Integer)`  
  
         `As [Numeric], ToString( value As …, toBase As Integer)`  
  
    -   <xref:System.Convert.IsDBNull%2A>  
  
    -   <xref:System.Convert.GetTypeCode%2A>  
  
    -   <xref:System.Convert.ChangeType%2A>  
  
## <a name="see-also"></a><span data-ttu-id="ed788-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed788-111">See also</span></span>

- [<span data-ttu-id="ed788-112">Fonctions et types de données</span><span class="sxs-lookup"><span data-stu-id="ed788-112">Data Types and Functions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
