---
title: multiplicité de terminaison d'association
ms.date: 03/30/2017
ms.assetid: 340926ee-aefb-4bef-92cc-453e5251fd03
ms.openlocfilehash: 59eed56204543adf405cfc7c71a49697a9e18374
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769669"
---
# <a name="association-end-multiplicity"></a>multiplicité de terminaison d'association
*Multiplicité de terminaison d’association* définit le nombre de [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) instances qui peuvent être à l’extrémité d’une [association](../../../../docs/framework/data/adonet/association-type.md).  
  
 La multiplicité de terminaison d'association peut avoir l'une des valeurs suivantes :  
  
- un (1) : Indique que cette instance de type exactement une entité existe à la fin de l’association.  
  
- zéro ou une (valeur 0.. 1) : Indique que zéro ou une instance de type d’entité existe au niveau de la terminaison d’association.  
  
- nombre (\*) : Indique que zéro, une ou plusieurs instances de type d’entité existent à la fin de l’association.  
  
 Une association est souvent caractérisée par ses multiplicités de terminaison d'association. Par exemple, si les terminaisons d’une association ont les multiplicités un (1) et plusieurs (\*), l’association est appelée une association un-à-plusieurs. Dans l'exemple ci-dessous, l'association `PublishedBy` est une association un-à-plusieurs (un éditeur publie de nombreux livres, et un livre est publié par un seul éditeur). L'association `WrittenBy` est une association plusieurs-à-plusieurs (un livre peut avoir plusieurs auteurs, et un auteur peut écrire plusieurs livres).  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec deux associations : `PublishedBy` et `WrittenBy`. Les terminaisons d'association pour l'association `PublishedBy` sont les types d'entité `Book` et `Publisher`. La multiplicité de la `Publisher` fin est un (1) et la multiplicité de la `Book` fin est plusieurs (\*).  
  
 ![Exemple de modèle avec trois types d’entité](./media/association-end-multiplicity/example-model-three-entity-types.gif)  
  
 ADO.NET Entity Framework utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit l'association `PublishedBy` présentée dans le diagramme ci-dessus :  
  
 [!code-xml[EDM_Example_Model#AssociationExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#associationexample)]  
  
## <a name="see-also"></a>Voir aussi

- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
