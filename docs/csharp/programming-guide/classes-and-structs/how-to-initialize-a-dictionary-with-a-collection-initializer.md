---
title: Guide pratique pour initialiser un dictionnaire avec un initialiseur de collection - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [C#], with Dictionary
ms.assetid: 25283922-f8ee-40dc-a639-fac30804ec71
ms.openlocfilehash: 42deee85b3a425531ddadfa96cfaff6d342d1221
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243879"
---
# <a name="how-to-initialize-a-dictionary-with-a-collection-initializer-c-programming-guide"></a><span data-ttu-id="f4e8e-102">Guide pratique pour initialiser un dictionnaire avec un initialiseur de collection (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="f4e8e-102">How to initialize a dictionary with a collection initializer (C# Programming Guide)</span></span>

<span data-ttu-id="f4e8e-103">Un <xref:System.Collections.Generic.Dictionary%602> contient une collection de paires clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-103">A <xref:System.Collections.Generic.Dictionary%602> contains a collection of key/value pairs.</span></span> <span data-ttu-id="f4e8e-104">Sa méthode <xref:System.Collections.Generic.Dictionary%602.Add*> prend deux paramètres, un pour la clé et un pour la valeur.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-104">Its <xref:System.Collections.Generic.Dictionary%602.Add*> method takes two parameters, one for the key and one for the value.</span></span> <span data-ttu-id="f4e8e-105">Pour initialiser un <xref:System.Collections.Generic.Dictionary%602> ou toute collection dont la méthode `Add` prend plusieurs paramètres, mettez chaque jeu de paramètres entre accolades, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-105">To initialize a <xref:System.Collections.Generic.Dictionary%602>, or any collection whose `Add` method takes multiple parameters, enclose each set of parameters in braces as shown in the following example.</span></span>

## <a name="example"></a><span data-ttu-id="f4e8e-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="f4e8e-106">Example</span></span>

<span data-ttu-id="f4e8e-107">Dans l’exemple de code suivant, un <xref:System.Collections.Generic.Dictionary%602> est initialisé avec des instances de type `StudentName`.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-107">In the following code example, a <xref:System.Collections.Generic.Dictionary%602> is initialized with instances of type `StudentName`.</span></span>  
  
[!code-csharp[csProgGuideLINQ#34](../../../csharp/programming-guide/arrays/codesnippet/CSharp/how-to-initialize-a-dictionary-with-a-collection-initializer_1.cs)]

<span data-ttu-id="f4e8e-108">Notez les deux paires d’accolades dans chaque élément de la collection.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-108">Note the two pairs of braces in each element of the collection.</span></span> <span data-ttu-id="f4e8e-109">Les accolades les plus intérieures encadrent l’initialiseur d’objet pour `StudentName`, et les accolades les plus extérieures encadrent l’initialiseur pour la paire clé/valeur ajoutée à `students` <xref:System.Collections.Generic.Dictionary%602>.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-109">The innermost braces enclose the object initializer for the `StudentName`, and the outermost braces enclose the initializer for the key/value pair that will be added to the `students` <xref:System.Collections.Generic.Dictionary%602>.</span></span> <span data-ttu-id="f4e8e-110">Pour finir, l’initialiseur de collection entier pour le dictionnaire est placé entre accolades.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-110">Finally, the whole collection initializer for the dictionary is enclosed in braces.</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="f4e8e-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f4e8e-111">Compiling the code</span></span>

<span data-ttu-id="f4e8e-112">Pour exécuter ce code, copiez et collez la classe dans un projet d’application console Visual C# qui a été créé dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-112">To run this code, copy and paste the class into a Visual C# console application project that has been created in Visual Studio.</span></span> <span data-ttu-id="f4e8e-113">Par défaut, ce projet cible la version 3.5 du [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], et il a une référence à System.Core.dll et une directive using pour System.Linq.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-113">By default, this project targets version 3.5 of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], and it has a reference to System.Core.dll and a using directive for System.Linq.</span></span> <span data-ttu-id="f4e8e-114">Si un ou plusieurs de ces éléments sont manquants dans le projet, vous pouvez les ajouter manuellement.</span><span class="sxs-lookup"><span data-stu-id="f4e8e-114">If one or more of these requirements are missing from the project, you can add them manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4e8e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4e8e-115">See also</span></span>

- [<span data-ttu-id="f4e8e-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f4e8e-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="f4e8e-117">Initialiseurs d’objets et de collections</span><span class="sxs-lookup"><span data-stu-id="f4e8e-117">Object and Collection Initializers</span></span>](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)
