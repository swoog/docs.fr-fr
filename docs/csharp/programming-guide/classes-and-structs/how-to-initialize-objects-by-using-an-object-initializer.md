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
# <a name="how-to-initialize-objects-by-using-an-object-initializer-c-programming-guide"></a>Procédure : Initialiser des objets à l'aide d'un initialiseur d'objet (Guide de programmation C#)

Vous pouvez utiliser des initialiseurs d’objets pour initialiser des objets de type de façon déclarative sans appeler explicitement un constructeur pour le type.  
  
Les exemples suivants montrent comment utiliser des initialiseurs d’objets avec des objets nommés. Le compilateur traite les initialiseurs d’objets en accédant d’abord au constructeur d’instance par défaut, puis en traitant les initialisations des membres. Ainsi, si le constructeur par défaut est déclaré comme `private` dans la classe, les initialiseurs d’objets qui nécessitent un accès public échoueront.
  
Vous devez utiliser un initialiseur d’objet si vous définissez un type anonyme. Pour plus d'informations, voir [Procédure : Retourner des sous-ensembles de propriétés d’éléments dans une requête](how-to-return-subsets-of-element-properties-in-a-query.md).  
  
## <a name="example"></a>Exemple  

L’exemple suivant montre comment initialiser un nouveau type `StudentName` à l’aide d’initialiseurs d’objets. Cet exemple définit des propriétés dans le type `StudentName` :
  
[!code-csharp-interactive[InitializerObjectExample](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/object-collection-initializers/HowToObjectInitializers.cs#HowToObjectInitializers)]  

Des initialiseurs d’objet peuvent être utilisés pour définir des indexeurs dans un objet. L’exemple suivant définit une classe `BaseballTeam` qui utilise un indexeur pour obtenir et définir des joueurs à des positions différentes. L’initialiseur peut affecter des joueurs en fonction de l’abréviation de la position ou du chiffre utilisé pour désigner la position sur les feuilles de match :

[!code-csharp-interactive[InitializerIndexerExample](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/object-collection-initializers/HowToIndexInitializer.cs#HowToIndexInitializer)]  

## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../index.md)  
- [Initialiseurs d’objets et de collections](object-and-collection-initializers.md)
