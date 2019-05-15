---
title: 'Procédure : Trier un tableau en Visual Basic'
ms.date: 07/20/2015
f1_keywords:
- Array.Sort
helpviewer_keywords:
- arrays [Visual Basic], sorting
- examples [Visual Basic], arrays
ms.assetid: 9289aeaa-9626-4698-94a7-1d1fd3702b87
ms.openlocfilehash: 680f488a98d6e7e31b3d077843514fd12f75481c
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65586442"
---
# <a name="how-to-sort-an-array-in-visual-basic"></a><span data-ttu-id="e544a-102">Procédure : Trier un tableau en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e544a-102">How to: Sort An Array in Visual Basic</span></span>
<span data-ttu-id="e544a-103">Cet exemple déclare un tableau de `String` objets nommés `zooAnimals`, il remplit, puis le tri par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="e544a-103">This example declares an array of `String` objects named `zooAnimals`, populates it, and then sorts it alphabetically.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e544a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e544a-104">Example</span></span>  
  
```  
Private Sub sortAnimals()  
    Dim zooAnimals(2) As String  
    zooAnimals(0) = "lion"  
    zooAnimals(1) = "turtle"  
    zooAnimals(2) = "ostrich"  
    Array.Sort(zooAnimals)  
End Sub  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e544a-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e544a-105">Compiling the Code</span></span>  
 <span data-ttu-id="e544a-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="e544a-106">This example requires:</span></span>  
  
- <span data-ttu-id="e544a-107">L’accès à la <xref:System> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e544a-107">Access to the <xref:System> namespace.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="e544a-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="e544a-108">Robust Programming</span></span>  
 <span data-ttu-id="e544a-109">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="e544a-109">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="e544a-110">Tableau est vide (<xref:System.ArgumentNullException> classe)</span><span class="sxs-lookup"><span data-stu-id="e544a-110">Array is empty (<xref:System.ArgumentNullException> class)</span></span>  
  
- <span data-ttu-id="e544a-111">Tableau est multidimensionnel (<xref:System.RankException> classe)</span><span class="sxs-lookup"><span data-stu-id="e544a-111">Array is multidimensional (<xref:System.RankException> class)</span></span>  
  
- <span data-ttu-id="e544a-112">Un ou plusieurs éléments du tableau n’implémentent pas le <xref:System.IComparable> interface (<xref:System.InvalidOperationException> classe)</span><span class="sxs-lookup"><span data-stu-id="e544a-112">One or more elements of the array do not implement the <xref:System.IComparable> interface (<xref:System.InvalidOperationException> class)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e544a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e544a-113">See also</span></span>

- <xref:System.Array.Sort%2A?displayProperty=nameWithType>
- [<span data-ttu-id="e544a-114">Tableaux</span><span class="sxs-lookup"><span data-stu-id="e544a-114">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [<span data-ttu-id="e544a-115">Dépannage des tableaux</span><span class="sxs-lookup"><span data-stu-id="e544a-115">Troubleshooting Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)
- [<span data-ttu-id="e544a-116">Collections</span><span class="sxs-lookup"><span data-stu-id="e544a-116">Collections</span></span>](../../concepts/collections.md)
- [<span data-ttu-id="e544a-117">For Each...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="e544a-117">For Each...Next Statement</span></span>](../../../../visual-basic/language-reference/statements/for-each-next-statement.md)
