---
title: multiplicité de terminaison d'association
ms.date: 03/30/2017
ms.assetid: 340926ee-aefb-4bef-92cc-453e5251fd03
ms.openlocfilehash: 2f70fa4b163b957ea1e43506033863c3540b0418
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="association-end-multiplicity"></a>multiplicité de terminaison d'association
*Multiplicité de terminaison d’association* définit le nombre de [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) instances qui peuvent être à l’extrémité d’une [association](../../../../docs/framework/data/adonet/association-type.md).  
  
 La multiplicité de terminaison d'association peut avoir l'une des valeurs suivantes :  
  
-   Un (1) : indique qu'il existe exactement une instance de type d'entité au niveau de la terminaison d'association.  
  
-   Zéro ou un (0..1) : indique qu'il existe zéro ou une instance de type d'entité au niveau de la terminaison d'association.  
  
-   Plusieurs (*) : indique qu'il existe zéro, une ou plusieurs instances de type d'entité au niveau de la terminaison d'association.  
  
 Une association est souvent caractérisée par ses multiplicités de terminaison d'association. Par exemple, si les terminaisons d'une association ont les multiplicités un (1) et plusieurs (*), l'association est appelée « association un-à-plusieurs ». Dans l'exemple ci-dessous, l'association `PublishedBy` est une association un-à-plusieurs (un éditeur publie de nombreux livres, et un livre est publié par un seul éditeur). L'association `WrittenBy` est une association plusieurs-à-plusieurs (un livre peut avoir plusieurs auteurs, et un auteur peut écrire plusieurs livres).  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec deux associations : `PublishedBy` et `WrittenBy`. Les terminaisons d'association pour l'association `PublishedBy` sont les types d'entité `Book` et `Publisher`. La multiplicité de la terminaison `Publisher` est un (1) et celle de la terminaison `Book` est plusieurs (*).  
  
 ![Exemple de modèle](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")  
  
 ADO.NET Entity Framework utilise un langage spécifique à un domaine (DSL) appelé conceptual schema definition language ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit l'association `PublishedBy` présentée dans le diagramme ci-dessus :  
  
 [!code-xml[EDM_Example_Model#AssociationExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#associationexample)]  
  
## <a name="see-also"></a>Voir aussi  
 [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)  
 [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
