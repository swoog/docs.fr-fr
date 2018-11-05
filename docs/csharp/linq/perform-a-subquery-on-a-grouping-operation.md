---
title: Effectuer une sous-requête sur une opération de regroupement (LINQ en C#)
description: Découvrez comment effectuer une sous-requête sur une opération de regroupement à l’aide de LINQ en C#.
ms.date: 12/1/2016
ms.assetid: d75a588e-9b6f-4f37-b195-f99ec8503855
ms.openlocfilehash: 19be93fe695982e93abea9a59153a4245dce4a60
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2018
ms.locfileid: "48846316"
---
# <a name="perform-a-subquery-on-a-grouping-operation"></a><span data-ttu-id="ec98f-103">Effectuer une sous-requête sur une opération de regroupement</span><span class="sxs-lookup"><span data-stu-id="ec98f-103">Perform a subquery on a grouping operation</span></span>

<span data-ttu-id="ec98f-104">Cet article présente deux façons de créer une requête qui organise les données sources en groupes et effectue ensuite une sous-requête sur chacun de ces groupes.</span><span class="sxs-lookup"><span data-stu-id="ec98f-104">This article shows two different ways to create a query that orders the source data into groups, and then performs a subquery over each group individually.</span></span> <span data-ttu-id="ec98f-105">Dans chaque exemple, la technique de base consiste à regrouper les éléments sources en utilisant une *continuation* nommée `newGroup`, puis en créant une sous-requête sur `newGroup`.</span><span class="sxs-lookup"><span data-stu-id="ec98f-105">The basic technique in each example is to group the source elements by using a *continuation* named `newGroup`, and then generating a new subquery against `newGroup`.</span></span> <span data-ttu-id="ec98f-106">Cette sous-requête est exécutée sur chaque groupe créé par la requête externe.</span><span class="sxs-lookup"><span data-stu-id="ec98f-106">This subquery is run against each new group that is created by the outer query.</span></span> <span data-ttu-id="ec98f-107">Notez que, dans cet exemple particulier, le résultat final n’est pas un groupe, mais une séquence plate de types anonymes.</span><span class="sxs-lookup"><span data-stu-id="ec98f-107">Note that in this particular example the final output is not a group, but a flat sequence of anonymous types.</span></span>  
  
<span data-ttu-id="ec98f-108">Pour plus d’informations sur les regroupements, consultez [group, clause](../language-reference/keywords/group-clause.md).</span><span class="sxs-lookup"><span data-stu-id="ec98f-108">For more information about how to group, see [group clause](../language-reference/keywords/group-clause.md).</span></span>  
  
<span data-ttu-id="ec98f-109">Pour plus d’informations sur les continuations, consultez [into](../language-reference/keywords/into.md).</span><span class="sxs-lookup"><span data-stu-id="ec98f-109">For more information about continuations, see [into](../language-reference/keywords/into.md).</span></span> <span data-ttu-id="ec98f-110">L’exemple suivant utilise une structure de données en mémoire comme source de données, mais les mêmes principes s’appliquent à tous les types de sources de données LINQ.</span><span class="sxs-lookup"><span data-stu-id="ec98f-110">The following example uses an in-memory data structure as the data source, but the same principles apply for any kind of LINQ data source.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec98f-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec98f-111">Example</span></span>

> [!NOTE]
> <span data-ttu-id="ec98f-112">Cet exemple contient des références aux objets définis dans l’exemple de code qui est présenté dans [Interroger une collection d’objets](query-a-collection-of-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ec98f-112">This example contains references to objects that are defined in the sample code in [Query a collection of objects](query-a-collection-of-objects.md).</span></span>

[!code-csharp[csProgGuideLINQ#23](~/samples/snippets/csharp/concepts/linq/how-to-perform-a-subquery-on-a-grouping-operation_1.cs)] 

<span data-ttu-id="ec98f-113">La requête de l’extrait de code ci-dessus peut également s’écrire avec la syntaxe de méthode.</span><span class="sxs-lookup"><span data-stu-id="ec98f-113">The query in the snippet above can also be written using method syntax.</span></span> <span data-ttu-id="ec98f-114">L’extrait de code suivant comporte une requête sémantiquement équivalente, écrite avec la syntaxe de méthode.</span><span class="sxs-lookup"><span data-stu-id="ec98f-114">The following code snippet has a semantically equivalent query written using method syntax.</span></span>

[!code-csharp[csProgGuideLINQ#86](~/samples/snippets/csharp/concepts/linq/how-to-perform-a-subquery-on-a-grouping-operation_2.cs)]

## <a name="see-also"></a><span data-ttu-id="ec98f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec98f-115">See also</span></span>

- [<span data-ttu-id="ec98f-116">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="ec98f-116">Language Integrated Query (LINQ)</span></span>](index.md)
