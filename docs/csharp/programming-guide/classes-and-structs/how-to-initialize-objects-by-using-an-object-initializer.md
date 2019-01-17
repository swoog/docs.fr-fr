---
title: "Procédure : Initialiser des objets à l'aide d'un initialiseur d'objet - Guide de programmation C#"
ms.custom: seodec18
ms.date: 12/20/2018
helpviewer_keywords:
- object initializers [C#], how to use
- objects [C#], initializing
ms.assetid: 4b75ebb2-2e29-43de-929c-d736a8f27ce6
ms.openlocfilehash: 29987b9ba1f1f18f4e768766bd2391ebb5862f97
ms.sourcegitcommit: d09c77414e9e4fc72c79b04deee7a756a120674e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54084873"
---
# <a name="how-to-initialize-objects-by-using-an-object-initializer-c-programming-guide"></a><span data-ttu-id="8d138-102">Procédure : Initialiser des objets à l'aide d'un initialiseur d'objet (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="8d138-102">How to: Initialize Objects by Using an Object Initializer (C# Programming Guide)</span></span>

<span data-ttu-id="8d138-103">Vous pouvez utiliser des initialiseurs d’objets pour initialiser des objets de type de façon déclarative sans appeler explicitement un constructeur pour le type.</span><span class="sxs-lookup"><span data-stu-id="8d138-103">You can use object initializers to initialize type objects in a declarative manner without explicitly invoking a constructor for the type.</span></span>  
  
<span data-ttu-id="8d138-104">Les exemples suivants montrent comment utiliser des initialiseurs d’objets avec des objets nommés.</span><span class="sxs-lookup"><span data-stu-id="8d138-104">The following examples show how to use object initializers with named objects.</span></span> <span data-ttu-id="8d138-105">Le compilateur traite les initialiseurs d’objets en accédant d’abord au constructeur d’instance par défaut, puis en traitant les initialisations des membres.</span><span class="sxs-lookup"><span data-stu-id="8d138-105">The compiler processes object initializers by first accessing the default instance constructor and then processing the member initializations.</span></span> <span data-ttu-id="8d138-106">Ainsi, si le constructeur par défaut est déclaré comme `private` dans la classe, les initialiseurs d’objets qui nécessitent un accès public échoueront.</span><span class="sxs-lookup"><span data-stu-id="8d138-106">Therefore, if the default constructor is declared as `private` in the class, object initializers that require public access will fail.</span></span>
  
<span data-ttu-id="8d138-107">Vous devez utiliser un initialiseur d’objet si vous définissez un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="8d138-107">You must use an object initializer if you're defining an anonymous type.</span></span> <span data-ttu-id="8d138-108">Pour plus d'informations, voir [Procédure : Retourner des sous-ensembles de propriétés d’éléments dans une requête](how-to-return-subsets-of-element-properties-in-a-query.md).</span><span class="sxs-lookup"><span data-stu-id="8d138-108">For more information, see [How to: Return Subsets of Element Properties in a Query](how-to-return-subsets-of-element-properties-in-a-query.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8d138-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="8d138-109">Example</span></span>  

<span data-ttu-id="8d138-110">L’exemple suivant montre comment initialiser un nouveau type `StudentName` à l’aide d’initialiseurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="8d138-110">The following example shows how to initialize a new `StudentName` type by using object initializers.</span></span> <span data-ttu-id="8d138-111">Cet exemple définit des propriétés dans le type `StudentName` :</span><span class="sxs-lookup"><span data-stu-id="8d138-111">This example sets properties in the `StudentName` type:</span></span>
  
[!code-csharp-interactive[InitializerObjectExample](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/object-collection-initializers/HowToObjectInitializers.cs#HowToObjectInitializers)]  

<span data-ttu-id="8d138-112">Des initialiseurs d’objet peuvent être utilisés pour définir des indexeurs dans un objet.</span><span class="sxs-lookup"><span data-stu-id="8d138-112">Object initializers can be used to set indexers in an object.</span></span> <span data-ttu-id="8d138-113">L’exemple suivant définit une classe `BaseballTeam` qui utilise un indexeur pour obtenir et définir des joueurs à des positions différentes.</span><span class="sxs-lookup"><span data-stu-id="8d138-113">The following example defines a `BaseballTeam` class that uses an indexer to get and set players at different positions.</span></span> <span data-ttu-id="8d138-114">L’initialiseur peut affecter des joueurs en fonction de l’abréviation de la position ou du chiffre utilisé pour désigner la position sur les feuilles de match :</span><span class="sxs-lookup"><span data-stu-id="8d138-114">The initializer can assign players, based on the abbreviation for the position, or the number used for each position baseball scorecards:</span></span>

[!code-csharp-interactive[InitializerIndexerExample](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/object-collection-initializers/HowToIndexInitializer.cs#HowToIndexInitializer)]  

## <a name="see-also"></a><span data-ttu-id="8d138-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d138-115">See Also</span></span>

- [<span data-ttu-id="8d138-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="8d138-116">C# Programming Guide</span></span>](../index.md)  
- [<span data-ttu-id="8d138-117">Initialiseurs d’objets et de collections</span><span class="sxs-lookup"><span data-stu-id="8d138-117">Object and Collection Initializers</span></span>](object-and-collection-initializers.md)
