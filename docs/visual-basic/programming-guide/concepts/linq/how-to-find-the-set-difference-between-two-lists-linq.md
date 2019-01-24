---
title: 'Procédure : Rechercher la différence définie entre deux listes (LINQ) (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: b5b25474-10a8-4df6-aab5-75621bb6b68e
ms.openlocfilehash: e1c012dbe252c494c5f77e61b56deccbb07490fc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54579717"
---
# <a name="how-to-find-the-set-difference-between-two-lists-linq-visual-basic"></a><span data-ttu-id="5f5dd-102">Procédure : Rechercher la différence définie entre deux listes (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5f5dd-102">How to: Find the Set Difference Between Two Lists (LINQ) (Visual Basic)</span></span>
<span data-ttu-id="5f5dd-103">Cet exemple montre comment utiliser LINQ pour comparer deux listes de chaînes et sortir les lignes qui sont présentes dans names1.txt, mais pas dans names2.txt.</span><span class="sxs-lookup"><span data-stu-id="5f5dd-103">This example shows how to use LINQ to compare two lists of strings and output those lines that are in names1.txt but not in names2.txt.</span></span>  
  
### <a name="to-create-the-data-files"></a><span data-ttu-id="5f5dd-104">Pour créer les fichiers de données</span><span class="sxs-lookup"><span data-stu-id="5f5dd-104">To create the data files</span></span>  
  
1.  <span data-ttu-id="5f5dd-105">Copiez names1.txt et names2.txt dans votre dossier de solution, comme indiqué dans [Comment : Combiner et comparer des Collections de chaînes (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-combine-and-compare-string-collections-linq.md).</span><span class="sxs-lookup"><span data-stu-id="5f5dd-105">Copy names1.txt and names2.txt to your solution folder as shown in [How to: Combine and Compare String Collections (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-combine-and-compare-string-collections-linq.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5f5dd-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f5dd-106">Example</span></span>  
  
```vb  
Class CompareLists  
  
    Shared Sub Main()  
  
        ' Create the IEnumerable data sources.  
        Dim names1 As String() = System.IO.File.ReadAllLines("../../../names1.txt")  
        Dim names2 As String() = System.IO.File.ReadAllLines("../../../names2.txt")  
  
        ' Create the query. Note that method syntax must be used here.  
        Dim differenceQuery = names1.Except(names2)  
        Console.WriteLine("The following lines are in names1.txt but not names2.txt")  
  
        ' Execute the query.  
        For Each name As String In differenceQuery  
            Console.WriteLine(name)  
        Next  
  
        ' Keep console window open in debug mode.  
        Console.WriteLine("Press any key to exit.")  
        Console.ReadKey()  
    End Sub  
End Class  
' Output:  
' The following lines are in names1.txt but not names2.txt  
' Potra, Cristina  
' Noriega, Fabricio  
' Aw, Kam Foo  
' Toyoshima, Tim  
' Guy, Wey Yuan  
' Garcia, Debra  
```  
  
 <span data-ttu-id="5f5dd-107">Certains types d’opérations de requête en Visual Basic, tel que <xref:System.Linq.Enumerable.Except%2A>, <xref:System.Linq.Enumerable.Distinct%2A>, <xref:System.Linq.Enumerable.Union%2A>, et <xref:System.Linq.Enumerable.Concat%2A>, peuvent être exprimées uniquement dans la syntaxe fondée sur une méthode.</span><span class="sxs-lookup"><span data-stu-id="5f5dd-107">Some types of query operations in Visual Basic, such as <xref:System.Linq.Enumerable.Except%2A>, <xref:System.Linq.Enumerable.Distinct%2A>, <xref:System.Linq.Enumerable.Union%2A>, and <xref:System.Linq.Enumerable.Concat%2A>, can only be expressed in method-based syntax.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5f5dd-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="5f5dd-108">Compiling the Code</span></span>  
 <span data-ttu-id="5f5dd-109">Créez un projet qui cible le .NET Framework version 3.5 ou ultérieure, avec une référence à System.Core.dll et une déclaration `Imports` pour l’espace de noms System.Linq.</span><span class="sxs-lookup"><span data-stu-id="5f5dd-109">Create a project that targets the .NET Framework version 3.5 or higher with a reference to System.Core.dll and a `Imports` statement for the System.Linq namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f5dd-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f5dd-110">See also</span></span>
- [<span data-ttu-id="5f5dd-111">LINQ et chaînes (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5f5dd-111">LINQ and Strings (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-and-strings.md)
