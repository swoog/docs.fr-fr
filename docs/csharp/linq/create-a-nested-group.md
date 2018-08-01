---
title: Créer un groupe imbriqué (LINQ en C#)
description: Découvrez comment créer un groupe imbriqué dans une expression de requête LINQ en C#.
ms.date: 12/1/2016
ms.assetid: e9f00708-362e-4d13-98c5-d77549347ba0
ms.openlocfilehash: c973048d0859f61596c62c294131b8c00d0039f8
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404747"
---
# <a name="create-a-nested-group"></a><span data-ttu-id="e76b6-103">Créer un groupe imbriqué</span><span class="sxs-lookup"><span data-stu-id="e76b6-103">Create a nested group</span></span>

<span data-ttu-id="e76b6-104">L’exemple suivant montre comment créer des groupes imbriqués dans une expression de requête LINQ.</span><span class="sxs-lookup"><span data-stu-id="e76b6-104">The following example shows how to create nested groups in a LINQ query expression.</span></span> <span data-ttu-id="e76b6-105">Chaque groupe créé en fonction de l’année/du niveau d’étude est ensuite encore subdivisé en groupes en fonction des noms des individus.</span><span class="sxs-lookup"><span data-stu-id="e76b6-105">Each group that is created according to student year or grade level is then further subdivided into groups based on the individuals' names.</span></span>

## <a name="example"></a><span data-ttu-id="e76b6-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="e76b6-106">Example</span></span>

> [!NOTE]
> <span data-ttu-id="e76b6-107">Cet exemple contient des références aux objets définis dans l’exemple de code qui est présenté dans [Interroger une collection d’objets](query-a-collection-of-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e76b6-107">This example contains references to objects that are defined in the sample code in [Query a collection of objects](query-a-collection-of-objects.md).</span></span>

[!code-csharp[csProgGuideLINQ#24](~/samples/snippets/csharp/concepts/linq/how-to-create-a-nested-group_1.cs)]

<span data-ttu-id="e76b6-108">Notez que trois boucles `foreach` imbriquées sont nécessaires pour effectuer une itération sur les éléments internes d’un groupe imbriqué.</span><span class="sxs-lookup"><span data-stu-id="e76b6-108">Note that three nested `foreach` loops are required to iterate over the inner elements of a nested group.</span></span>

## <a name="see-also"></a><span data-ttu-id="e76b6-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e76b6-109">See also</span></span>

[<span data-ttu-id="e76b6-110">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="e76b6-110">Language Integrated Query (LINQ)</span></span>](index.md)
