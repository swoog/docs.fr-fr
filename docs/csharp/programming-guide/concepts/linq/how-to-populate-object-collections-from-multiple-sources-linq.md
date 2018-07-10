---
title: Guide pratique pour remplir des collections d’objets issues de plusieurs sources (LINQ) (C#)
ms.date: 06/12/2018
ms.assetid: 8ad7d480-b46c-4ccc-8c57-76f2d04ccc6d
ms.openlocfilehash: 5f0c0e92c7448eebc6f395fcdb16cfca840bb2ea
ms.sourcegitcommit: 9e18e4a18284ae9e54c515e30d019c0bbff9cd37
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37071082"
---
# <a name="how-to-populate-object-collections-from-multiple-sources-linq-c"></a><span data-ttu-id="c44b9-102">Guide pratique pour remplir des collections d’objets issues de plusieurs sources (LINQ) (C#)</span><span class="sxs-lookup"><span data-stu-id="c44b9-102">How to: Populate Object Collections from Multiple Sources (LINQ) (C#)</span></span>

<span data-ttu-id="c44b9-103">Cet exemple montre comment fusionner des données de différentes sources en une séquence de nouveaux types.</span><span class="sxs-lookup"><span data-stu-id="c44b9-103">This example shows how to merge data from different sources into a sequence of new types.</span></span>

> [!NOTE]
> <span data-ttu-id="c44b9-104">N’essayez pas de joindre des données du système de fichiers ou des données en mémoire à des données qui se trouvent encore dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="c44b9-104">Don't try to join in-memory data or data in the file system with data that is still in a database.</span></span> <span data-ttu-id="c44b9-105">Ces jointures interdomaines peuvent générer des résultats indéfinis, en raison des différentes façons par lesquelles les opérations de jointure peuvent être définies pour les requêtes de base de données et autres types de sources.</span><span class="sxs-lookup"><span data-stu-id="c44b9-105">Such cross-domain joins can yield undefined results because of different ways in which join operations might be defined for database queries and other types of sources.</span></span> <span data-ttu-id="c44b9-106">En outre, une telle opération risque de provoquer une exception de mémoire insuffisante si la quantité de données dans la base de données est assez élevée.</span><span class="sxs-lookup"><span data-stu-id="c44b9-106">Additionally, there is a risk that such an operation could cause an out-of-memory exception if the amount of data in the database is large enough.</span></span> <span data-ttu-id="c44b9-107">Pour joindre des données d’une base de données à des données en mémoire, appelez d’abord `ToList` ou `ToArray` sur la requête de base de données, puis effectuez la jointure sur la collection retournée.</span><span class="sxs-lookup"><span data-stu-id="c44b9-107">To join data from a database to in-memory data, first call `ToList` or `ToArray` on the database query, and then perform the join on the returned collection.</span></span>

## <a name="to-create-the-data-file"></a><span data-ttu-id="c44b9-108">Pour créer le fichier de données</span><span class="sxs-lookup"><span data-stu-id="c44b9-108">To create the data file</span></span>

<span data-ttu-id="c44b9-109">Copiez les fichiers names.csv et scores.csv dans votre dossier de projet, comme décrit dans [Guide pratique pour joindre du contenu issu de différents fichiers (LINQ) (C#)](../../../../csharp/programming-guide/concepts/linq/how-to-join-content-from-dissimilar-files-linq.md).</span><span class="sxs-lookup"><span data-stu-id="c44b9-109">Copy the names.csv and scores.csv files into your project folder, as described in [How to: Join Content from Dissimilar Files (LINQ) (C#)](../../../../csharp/programming-guide/concepts/linq/how-to-join-content-from-dissimilar-files-linq.md).</span></span>

## <a name="example"></a><span data-ttu-id="c44b9-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="c44b9-110">Example</span></span>

<span data-ttu-id="c44b9-111">L’exemple suivant montre comment utiliser un type nommé `Student` pour stocker des données fusionnées de deux collections en mémoire de chaînes qui simulent des données de feuille de calcul au format .csv.</span><span class="sxs-lookup"><span data-stu-id="c44b9-111">The following example shows how to use a named type `Student` to store merged data from two in-memory collections of strings that simulate spreadsheet data in .csv format.</span></span> <span data-ttu-id="c44b9-112">La première collection de chaînes représente les noms et les ID des étudiants, et la deuxième collection représente l’ID d’étudiant (dans la première colonne) et quatre notes d’examen.</span><span class="sxs-lookup"><span data-stu-id="c44b9-112">The first collection of strings represents the student names and IDs, and the second collection represents the student ID (in the first column) and four exam scores.</span></span> <span data-ttu-id="c44b9-113">L’ID est utilisé comme clé étrangère.</span><span class="sxs-lookup"><span data-stu-id="c44b9-113">The ID is used as the foreign key.</span></span>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;

class Student
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
    public int ID { get; set; }
    public List<int> ExamScores { get; set; }
}

class PopulateCollection
{
    static void Main()
    {
        // These data files are defined in How to: Join Content from
        // Dissimilar Files (LINQ).

        // Each line of names.csv consists of a last name, a first name, and an
        // ID number, separated by commas. For example, Omelchenko,Svetlana,111
        string[] names = System.IO.File.ReadAllLines(@"../../../names.csv");

        // Each line of scores.csv consists of an ID number and four test
        // scores, separated by commas. For example, 111, 97, 92, 81, 60
        string[] scores = System.IO.File.ReadAllLines(@"../../../scores.csv");

        // Merge the data sources using a named type.
        // var could be used instead of an explicit type. Note the dynamic
        // creation of a list of ints for the ExamScores member. The first item
        // is skipped in the split string because it is the student ID,
        // not an exam score.
        IEnumerable<Student> queryNamesScores =
            from nameLine in names
            let splitName = nameLine.Split(',')
            from scoreLine in scores
            let splitScoreLine = scoreLine.Split(',')
            where Convert.ToInt32(splitName[2]) == Convert.ToInt32(splitScoreLine[0])
            select new Student()
            {
                FirstName = splitName[0],
                LastName = splitName[1],
                ID = Convert.ToInt32(splitName[2]),
                ExamScores = (from scoreAsText in splitScoreLine.Skip(1)
                              select Convert.ToInt32(scoreAsText)).
                              ToList()
            };

        // Optional. Store the newly created student objects in memory
        // for faster access in future queries. This could be useful with
        // very large data files.
        List<Student> students = queryNamesScores.ToList();

        // Display each student's name and exam score average.
        foreach (var student in students)
        {
            Console.WriteLine("The average score of {0} {1} is {2}.",
                student.FirstName, student.LastName,
                student.ExamScores.Average());
        }

        //Keep console window open in debug mode
        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
    }
}
/* Output:
    The average score of Omelchenko Svetlana is 82.5.
    The average score of O'Donnell Claire is 72.25.
    The average score of Mortensen Sven is 84.5.
    The average score of Garcia Cesar is 88.25.
    The average score of Garcia Debra is 67.
    The average score of Fakhouri Fadi is 92.25.
    The average score of Feng Hanying is 88.
    The average score of Garcia Hugo is 85.75.
    The average score of Tucker Lance is 81.75.
    The average score of Adams Terry is 85.25.
    The average score of Zabokritski Eugene is 83.
    The average score of Tucker Michael is 92.
 */
```

<span data-ttu-id="c44b9-114">Dans la clause [select](../../../../csharp/language-reference/keywords/select-clause.md), un initialiseur d’objet est utilisé pour instancier chaque nouvel objet `Student` à l’aide des données des deux sources.</span><span class="sxs-lookup"><span data-stu-id="c44b9-114">In the [select](../../../../csharp/language-reference/keywords/select-clause.md) clause, an object initializer is used to instantiate each new `Student` object by using the data from the two sources.</span></span>

<span data-ttu-id="c44b9-115">Si vous n’êtes pas obligé de stocker les résultats d’une requête, les types anonymes peuvent être plus pratiques que les types nommés.</span><span class="sxs-lookup"><span data-stu-id="c44b9-115">If you don't have to store the results of a query, anonymous types can be more convenient than named types.</span></span> <span data-ttu-id="c44b9-116">Les types nommés sont nécessaires si vous passez les résultats de requête en dehors de la méthode dans laquelle la requête est exécutée.</span><span class="sxs-lookup"><span data-stu-id="c44b9-116">Named types are required if you pass the query results outside the method in which the query is executed.</span></span> <span data-ttu-id="c44b9-117">L’exemple suivant exécute la même tâche que l’exemple précédent, mais utilise des types anonymes plutôt que des types nommés :</span><span class="sxs-lookup"><span data-stu-id="c44b9-117">The following example executes the same task as the previous example, but uses anonymous types instead of named types:</span></span>

```csharp
// Merge the data sources by using an anonymous type.
// Note the dynamic creation of a list of ints for the
// ExamScores member. We skip 1 because the first string
// in the array is the student ID, not an exam score.
var queryNamesScores2 =
    from nameLine in names
    let splitName = nameLine.Split(',')
    from scoreLine in scores
    let splitScoreLine = scoreLine.Split(',')
    where Convert.ToInt32(splitName[2]) == Convert.ToInt32(splitScoreLine[0])
    select new
    {
        First = splitName[0],
        Last = splitName[1],
        ExamScores = (from scoreAsText in splitScoreLine.Skip(1)
                      select Convert.ToInt32(scoreAsText))
                      .ToList()
    };

// Display each student's name and exam score average.
foreach (var student in queryNamesScores2)
{
    Console.WriteLine("The average score of {0} {1} is {2}.",
        student.First, student.Last, student.ExamScores.Average());
}
```

## <a name="compiling-the-code"></a><span data-ttu-id="c44b9-118">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="c44b9-118">Compiling the code</span></span>

<span data-ttu-id="c44b9-119">Créez et compilez un projet qui cible une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="c44b9-119">Create and compile a project that targets one of the following options:</span></span>

- <span data-ttu-id="c44b9-120">.NET Framework version 3.5 avec une référence à System.Core.dll.</span><span class="sxs-lookup"><span data-stu-id="c44b9-120">.NET Framework version 3.5 with a reference to System.Core.dll.</span></span>
- <span data-ttu-id="c44b9-121">.NET Framework version 4.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c44b9-121">.NET Framework version 4.0 or higher.</span></span>
- <span data-ttu-id="c44b9-122">.NET Core version 1.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c44b9-122">.NET Core version 1.0 or higher.</span></span>

## <a name="see-also"></a><span data-ttu-id="c44b9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c44b9-123">See also</span></span>

[<span data-ttu-id="c44b9-124">LINQ et chaînes (C#)</span><span class="sxs-lookup"><span data-stu-id="c44b9-124">LINQ and Strings (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-and-strings.md)  
[<span data-ttu-id="c44b9-125">Initialiseurs d’objets et de collections</span><span class="sxs-lookup"><span data-stu-id="c44b9-125">Object and Collection Initializers</span></span>](../../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)  
[<span data-ttu-id="c44b9-126">Types anonymes</span><span class="sxs-lookup"><span data-stu-id="c44b9-126">Anonymous Types</span></span>](../../../../csharp/programming-guide/classes-and-structs/anonymous-types.md)  
