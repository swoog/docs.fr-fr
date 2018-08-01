---
title: Interroger une collection d’objets (LINQ en C#)
description: Découvrez comment interroger des collections à l’aide de LINQ en C#.
ms.date: 11/30/2016
ms.assetid: 87a76f8a-0b58-4791-90ea-2fe0a30416c9
ms.openlocfilehash: 87c7bbe789c165a6e189231df1979fc264a34dce
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37403919"
---
# <a name="query-a-collection-of-objects"></a><span data-ttu-id="4993a-103">Interroger une collection d’objets</span><span class="sxs-lookup"><span data-stu-id="4993a-103">Query a collection of objects</span></span>

<span data-ttu-id="4993a-104">Cet exemple montre comment effectuer une requête simple sur une liste d’objets `Student`.</span><span class="sxs-lookup"><span data-stu-id="4993a-104">This example shows how to perform a simple query over a list of `Student` objects.</span></span> <span data-ttu-id="4993a-105">Chaque objet `Student` contient des informations de base sur l’étudiant et une liste qui représente les notes de l’étudiant lors de quatre examens.</span><span class="sxs-lookup"><span data-stu-id="4993a-105">Each `Student` object contains some basic information about the student, and a list that represents the student's scores on four examinations.</span></span>  
  
<span data-ttu-id="4993a-106">Cette application sert de cadre pour de nombreux autres exemples dans cette section qui utilisent la même source de données `students`.</span><span class="sxs-lookup"><span data-stu-id="4993a-106">This application serves as the framework for many other examples in this section that use the same `students` data source.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4993a-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="4993a-107">Example</span></span>

<span data-ttu-id="4993a-108">La requête suivante retourne les étudiants qui ont reçu une note supérieure ou égale à 90 lors de leur premier examen.</span><span class="sxs-lookup"><span data-stu-id="4993a-108">The following query returns the students who received a score of 90 or greater on their first exam.</span></span>  
  
[!code-csharp[csProgGuideLINQ#15](~/samples/snippets/csharp/concepts/linq/how-to-query-a-collection-of-objects_1.cs)]  
  
<span data-ttu-id="4993a-109">Cette requête est volontairement simple pour vous permettre de faire des essais.</span><span class="sxs-lookup"><span data-stu-id="4993a-109">This query is intentionally simple to enable you to experiment.</span></span> <span data-ttu-id="4993a-110">Par exemple, vous pouvez essayer plus de conditions dans la clause `where` ou utiliser une clause `orderby` pour trier les résultats.</span><span class="sxs-lookup"><span data-stu-id="4993a-110">For example, you can try more conditions in the `where` clause, or use an `orderby` clause to sort the results.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4993a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4993a-111">See also</span></span>

[<span data-ttu-id="4993a-112">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="4993a-112">Language Integrated Query (LINQ)</span></span>](index.md)  
[<span data-ttu-id="4993a-113">Interpolation de chaîne</span><span class="sxs-lookup"><span data-stu-id="4993a-113">String interpolation</span></span>](../language-reference/tokens/interpolated.md)