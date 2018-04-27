---
title: '&#39;Pour chaque&#39; sur le type &#39; &lt;typename&gt; &#39; est ambigu, car le type implémente plusieurs instanciations de &#39;System.Collections.Generic.IEnumerable (Of T)&#39;'
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc32096
- bc32096
helpviewer_keywords:
- BC32096
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
caps.latest.revision: 7
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 81cb37cc4b61fa96e64f59150d95356b2fb0a355
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="39for-each39-on-type-39lttypenamegt39-is-ambiguous-because-the-type-implements-multiple-instantiations-of-39systemcollectionsgenericienumerableof-t39"></a><span data-ttu-id="fd1e1-102">&#39;Pour chaque&#39; sur le type &#39; &lt;typename&gt; &#39; est ambigu, car le type implémente plusieurs instanciations de &#39;System.Collections.Generic.IEnumerable (Of T)&#39;</span><span class="sxs-lookup"><span data-stu-id="fd1e1-102">&#39;For Each&#39; on type &#39;&lt;typename&gt;&#39; is ambiguous because the type implements multiple instantiations of &#39;System.Collections.Generic.IEnumerable(Of T)&#39;</span></span>
<span data-ttu-id="fd1e1-103">A `For Each` instruction spécifie une variable itérateur qui a plusieurs <xref:System.Collections.IEnumerable.GetEnumerator%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="fd1e1-103">A `For Each` statement specifies an iterator variable that has more than one <xref:System.Collections.IEnumerable.GetEnumerator%2A> method.</span></span>  
  
 <span data-ttu-id="fd1e1-104">La variable d’itérateur doit être d’un type qui implémente le <xref:System.Collections.IEnumerable?displayProperty=nameWithType> ou <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface dans un de le `Collections` espaces de noms de la [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd1e1-104">The iterator variable must be of a type that implements the <xref:System.Collections.IEnumerable?displayProperty=nameWithType> or <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface in one of the `Collections` namespaces of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span></span> <span data-ttu-id="fd1e1-105">Il est possible qu’une classe implémente plusieurs interfaces génériques construits, à l’aide d’un argument de type différent pour chaque construction.</span><span class="sxs-lookup"><span data-stu-id="fd1e1-105">It is possible for a class to implement more than one constructed generic interface, using a different type argument for each construction.</span></span> <span data-ttu-id="fd1e1-106">Si une classe qui effectue l’opération est utilisée pour la variable d’itérateur, cette variable a plusieurs <xref:System.Collections.IEnumerable.GetEnumerator%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="fd1e1-106">If a class that does this is used for the iterator variable, that variable has more than one <xref:System.Collections.IEnumerable.GetEnumerator%2A> method.</span></span> <span data-ttu-id="fd1e1-107">Dans ce cas, Visual Basic ne peut pas choisir la méthode à appeler.</span><span class="sxs-lookup"><span data-stu-id="fd1e1-107">In such a case, Visual Basic cannot choose which method to call.</span></span>  
  
 <span data-ttu-id="fd1e1-108">**ID d’erreur :** BC32096</span><span class="sxs-lookup"><span data-stu-id="fd1e1-108">**Error ID:** BC32096</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="fd1e1-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="fd1e1-109">To correct this error</span></span>  
  
-   <span data-ttu-id="fd1e1-110">Utilisez [opérateur DirectCast](../../../visual-basic/language-reference/operators/directcast-operator.md) ou [opérateur TryCast](../../../visual-basic/language-reference/operators/trycast-operator.md) pour effectuer un cast du type de variable itérateur vers l’interface qui définit la <xref:System.Collections.IEnumerable.GetEnumerator%2A> méthode que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="fd1e1-110">Use [DirectCast Operator](../../../visual-basic/language-reference/operators/directcast-operator.md) or [TryCast Operator](../../../visual-basic/language-reference/operators/trycast-operator.md) to cast the iterator variable type to the interface defining the <xref:System.Collections.IEnumerable.GetEnumerator%2A> method you want to use.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd1e1-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd1e1-111">See Also</span></span>  
 [<span data-ttu-id="fd1e1-112">For Each...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="fd1e1-112">For Each...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-each-next-statement.md)  
 [<span data-ttu-id="fd1e1-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="fd1e1-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
