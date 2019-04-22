---
title: L'inférence de type nullable n'est pas prise en charge dans ce contexte
ms.date: 07/20/2015
f1_keywords:
- vbc36629
- bc36629
helpviewer_keywords:
- BC36629
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
ms.openlocfilehash: 9f7f878649d8b96f050b56d5b878eb3d67e027ff
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819240"
---
# <a name="nullable-type-inference-is-not-supported-in-this-context"></a><span data-ttu-id="a5430-102">L'inférence de type nullable n'est pas prise en charge dans ce contexte</span><span class="sxs-lookup"><span data-stu-id="a5430-102">Nullable type inference is not supported in this context</span></span>
<span data-ttu-id="a5430-103">Types valeur et les structures peuvent être déclarés nullables.</span><span class="sxs-lookup"><span data-stu-id="a5430-103">Value types and structures can be declared nullable.</span></span>  
  
```vb  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 <span data-ttu-id="a5430-104">Toutefois, vous ne pouvez pas utiliser la déclaration nullable en association avec l’inférence de type.</span><span class="sxs-lookup"><span data-stu-id="a5430-104">However, you cannot use the nullable declaration in combination with type inference.</span></span> <span data-ttu-id="a5430-105">Les exemples suivants provoquent cette erreur.</span><span class="sxs-lookup"><span data-stu-id="a5430-105">The following examples cause this error.</span></span>  
  
```vb  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 <span data-ttu-id="a5430-106">**ID d’erreur :** BC36629</span><span class="sxs-lookup"><span data-stu-id="a5430-106">**Error ID:** BC36629</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a5430-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="a5430-107">To correct this error</span></span>  
  
-   <span data-ttu-id="a5430-108">Utilisez un `As` clause pour déclarer la variable nullable.</span><span class="sxs-lookup"><span data-stu-id="a5430-108">Use an `As` clause to declare the variable as nullable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5430-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5430-109">See also</span></span>

- [<span data-ttu-id="a5430-110">Types valeur Nullable</span><span class="sxs-lookup"><span data-stu-id="a5430-110">Nullable Value Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [<span data-ttu-id="a5430-111">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="a5430-111">Local Type Inference</span></span>](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
