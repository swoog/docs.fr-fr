---
title: type d'association
ms.date: 03/30/2017
ms.assetid: 26c409f6-06e8-4441-ac78-1b1076a3c005
ms.openlocfilehash: 895d7fdc464741723322717c3ace027dc49eed9c
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58411445"
---
# <a name="association-type"></a>type d'association
Un *type d’association* (également appelé une association) est le bloc de construction fondamental pour la description des relations dans le modèle EDM (Entity Data Model). Dans un modèle conceptuel, une association représente une relation entre deux [types d’entité](../../../../docs/framework/data/adonet/entity-type.md) (tel que `Customer` et `Order`). Dans une application, une instance d'une association représente une association spécifique (comme une association entre une instance de `Customer` et une instance d'`Order`). Instances d’association sont regroupées logiquement dans un [ensemble d’associations](../../../../docs/framework/data/adonet/association-set.md).  
  
 Une définition d'association contient les informations suivantes :  
  
-   Nom unique. (Requis)  
  
-   Deux [terminaisons d’association](../../../../docs/framework/data/adonet/association-end.md), un pour chaque type d’entité dans la relation. (Requis)  
  
    > [!NOTE]
    >  Une association ne peut pas représenter de relation entre plus de deux types d'entité. Toutefois, une association peut définir une relation réciproque en spécifiant le même type d'entité pour chacune de ses terminaisons d'association.  
  
-   Un [contrainte d’intégrité référentielle](../../../../docs/framework/data/adonet/referential-integrity-constraint.md). (facultatif)  
  
 Chaque terminaison d’association doit spécifier un [multiplicité de terminaison d’association](../../../../docs/framework/data/adonet/association-end-multiplicity.md) qui indique le nombre d’instances de type d’entité qui peut être une des extrémités de l’association. Une multiplicité de terminaison d’association peut avoir une valeur d’un (1), zéro ou un (0.. 1) ou plusieurs (\*). Instances de type d’entité à une extrémité d’une association est accessible via [propriétés de navigation](../../../../docs/framework/data/adonet/navigation-property.md) ou les clés étrangères si elles sont exposées sur un type d’entité. Pour plus d’informations, consultez [Entity Data Model : Clés étrangères](../../../../docs/framework/data/adonet/foreign-key-property.md).  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec deux associations : `PublishedBy` et `WrittenBy`. Les terminaisons d'association pour l'association `PublishedBy` sont les types d'entité `Book` et `Publisher`. La multiplicité de la `Publisher` fin est un (1) et la multiplicité de la `Book` fin est plusieurs (\*), indiquant qu’un éditeur publie de nombreux livres et un livre est publié par un seul éditeur.  
  
 ![Exemple de modèle avec trois types d’entité](./media/association-type/example-model-three-entity-types.gif)  
  
 Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit l'association `PublishedBy` présentée dans le diagramme ci-dessus :  
  
 [!code-xml[EDM_Example_Model#AssociationExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#associationexample)]  
  
## <a name="see-also"></a>Voir aussi

- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
