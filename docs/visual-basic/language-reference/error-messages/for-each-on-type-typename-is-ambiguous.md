---
title: "'For Each' pour le type '<typename>' est ambigu, car le type implémente plusieurs instanciations de 'System.Collections.Generic.IEnumerable(Of T)'"
ms.date: 07/20/2015
f1_keywords:
- vbc32096
- bc32096
helpviewer_keywords:
- BC32096
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
ms.openlocfilehash: af2340e8e514391503d5f9b706d13ba93336698e
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662119"
---
# <a name="for-each-on-type-typename-is-ambiguous-because-the-type-implements-multiple-instantiations-of-systemcollectionsgenericienumerableof-t"></a><span data-ttu-id="cfc25-102">'For Each' pour le type '\<nom_type >' est ambigu, car le type implémente plusieurs instanciations de 'System.Collections.Generic.IEnumerable (Of T)'</span><span class="sxs-lookup"><span data-stu-id="cfc25-102">'For Each' on type '\<typename>' is ambiguous because the type implements multiple instantiations of 'System.Collections.Generic.IEnumerable(Of T)'</span></span>
<span data-ttu-id="cfc25-103">Un `For Each` instruction spécifie une variable d’itérateur qui a plusieurs <xref:System.Collections.IEnumerable.GetEnumerator%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="cfc25-103">A `For Each` statement specifies an iterator variable that has more than one <xref:System.Collections.IEnumerable.GetEnumerator%2A> method.</span></span>  
  
 <span data-ttu-id="cfc25-104">La variable d’itérateur doit être d’un type qui implémente le <xref:System.Collections.IEnumerable?displayProperty=nameWithType> ou <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface dans un de le `Collections` espaces de noms de la [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="cfc25-104">The iterator variable must be of a type that implements the <xref:System.Collections.IEnumerable?displayProperty=nameWithType> or <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface in one of the `Collections` namespaces of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span></span> <span data-ttu-id="cfc25-105">Il est possible pour une classe implémenter plusieurs interfaces génériques construits, à l’aide d’un argument de type différent pour chaque construction.</span><span class="sxs-lookup"><span data-stu-id="cfc25-105">It is possible for a class to implement more than one constructed generic interface, using a different type argument for each construction.</span></span> <span data-ttu-id="cfc25-106">Si une classe qui s’en charge est utilisée pour la variable d’itérateur, cette variable a plusieurs <xref:System.Collections.IEnumerable.GetEnumerator%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="cfc25-106">If a class that does this is used for the iterator variable, that variable has more than one <xref:System.Collections.IEnumerable.GetEnumerator%2A> method.</span></span> <span data-ttu-id="cfc25-107">Dans ce cas, Visual Basic ne peut pas choisir la méthode à appeler.</span><span class="sxs-lookup"><span data-stu-id="cfc25-107">In such a case, Visual Basic cannot choose which method to call.</span></span>  
  
 <span data-ttu-id="cfc25-108">**ID d’erreur :** BC32096</span><span class="sxs-lookup"><span data-stu-id="cfc25-108">**Error ID:** BC32096</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="cfc25-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="cfc25-109">To correct this error</span></span>  
  
- <span data-ttu-id="cfc25-110">Utilisez [opérateur DirectCast](../../../visual-basic/language-reference/operators/directcast-operator.md) ou [opérateur TryCast](../../../visual-basic/language-reference/operators/trycast-operator.md) un cast du type de variable itérateur vers l’interface définissant le <xref:System.Collections.IEnumerable.GetEnumerator%2A> méthode que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="cfc25-110">Use [DirectCast Operator](../../../visual-basic/language-reference/operators/directcast-operator.md) or [TryCast Operator](../../../visual-basic/language-reference/operators/trycast-operator.md) to cast the iterator variable type to the interface defining the <xref:System.Collections.IEnumerable.GetEnumerator%2A> method you want to use.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfc25-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfc25-111">See also</span></span>

- [<span data-ttu-id="cfc25-112">For Each...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="cfc25-112">For Each...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
- [<span data-ttu-id="cfc25-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="cfc25-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
