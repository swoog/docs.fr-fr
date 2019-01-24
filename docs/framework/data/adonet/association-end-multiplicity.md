---
title: multiplicité de terminaison d'association
ms.date: 03/30/2017
ms.assetid: 340926ee-aefb-4bef-92cc-453e5251fd03
ms.openlocfilehash: 6d1b31c5b5ead701fbe808b91d7191fb84dc86c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54502635"
---
# <a name="association-end-multiplicity"></a>multiplicité de terminaison d'association
*Multiplicité de terminaison d’association* définit le nombre de [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) instances qui peuvent être à l’extrémité d’une [association](../../../../docs/framework/data/adonet/association-type.md).  
  
 La multiplicité de terminaison d'association peut avoir l'une des valeurs suivantes :  
  
-   un (1) : Indique que cette instance de type exactement une entité existe à la fin de l’association.  
  
-   zéro ou une (valeur 0.. 1) : Indique que zéro ou une instance de type d’entité existe au niveau de la terminaison d’association.  
  
-   plusieurs (*) : Indique que zéro, une ou plusieurs instances de type d’entité existent à la fin de l’association.  
  
 Une association est souvent caractérisée par ses multiplicités de terminaison d'association. Par exemple, si les terminaisons d'une association ont les multiplicités un (1) et plusieurs (*), l'association est appelée « association un-à-plusieurs ». Dans l'exemple ci-dessous, l'association `PublishedBy` est une association un-à-plusieurs (un éditeur publie de nombreux livres, et un livre est publié par un seul éditeur). L'association `WrittenBy` est une association plusieurs-à-plusieurs (un livre peut avoir plusieurs auteurs, et un auteur peut écrire plusieurs livres).  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec deux associations : `PublishedBy` et `WrittenBy`. Les terminaisons d'association pour l'association `PublishedBy` sont les types d'entité `Book` et `Publisher`. La multiplicité de la terminaison `Publisher` est un (1) et celle de la terminaison `Book` est plusieurs (*).  
  
 ![Exemple de modèle](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")  
  
 ADO.NET Entity Framework utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit l'association `PublishedBy` présentée dans le diagramme ci-dessus :  
  
 [!code-xml[EDM_Example_Model#AssociationExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#associationexample)]  
  
## <a name="see-also"></a>Voir aussi
- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
