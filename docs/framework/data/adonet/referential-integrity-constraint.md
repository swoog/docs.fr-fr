---
title: contrainte d'intégrité référentielle
ms.date: 03/30/2017
ms.assetid: 3d3ba44b-4302-40d8-a7a9-62932e0395e5
ms.openlocfilehash: 7d3304393ef4e97887d9b8afec94ed265e38eaf0
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57679110"
---
# <a name="referential-integrity-constraint"></a>contrainte d'intégrité référentielle
Un *contrainte d’intégrité référentielle* dans le modèle EDM (Entity Data Model) est similaire à une contrainte d’intégrité référentielle dans une base de données relationnelle. Dans la même façon qu’une (ou plusieurs colonnes) à partir d’une table de base de données peuvent faire référence à la clé primaire d’une autre table, un [propriété](../../../../docs/framework/data/adonet/property.md) (ou propriétés) d’un [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) peut faire référence à la [clé d’entité ](../../../../docs/framework/data/adonet/entity-key.md) d’un autre type d’entité. Le type d’entité référencé est appelé le *terminaison principale* de la contrainte. Le type d’entité qui fait référence à la terminaison principale est appelé le *terminaison dépendante* de la contrainte.  
  
 Une contrainte d’intégrité référentielle est définie en tant que partie d’un [association](../../../../docs/framework/data/adonet/association-type.md) entre deux types d’entité. La définition d'une contrainte d'intégrité référentielle spécifie les informations suivantes :  
  
-   Terminaison principale de la contrainte. (Type d'entité dont la clé d'entité est référencée par la terminaison dépendante.)  
  
-   Clé d'entité de la terminaison principale.  
  
-   Terminaison dépendante de la contrainte. (Type d'entité dont une ou plusieurs propriétés référencent la clé d'entité de la terminaison principale.)  
  
-   Propriété ou propriétés de référence de la terminaison dépendante.  
  
 Les contraintes d'intégrité référentielle dans le modèle EDM ont pour objectif de vérifier que des associations valides existent toujours. Pour plus d’informations, consultez [propriété de clé étrangère](../../../../docs/framework/data/adonet/foreign-key-property.md).  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec deux associations : `WrittenBy` et `PublishedBy`. Le type d'entité `Book` a une propriété, `PublisherId`, qui référence la clé d'entité du type d'entité `Publisher` lorsque vous définissez une contrainte d'intégrité référentielle sur l'association `PublishedBy`.  
  
 ![RefConstraintModel](./media/referential-integrity-constraint/reference-constraint-model.gif "exemple d’un modèle de contrainte référentielle")  
  
 Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit une contrainte d'intégrité référentielle sur l'association `PublishedBy` présentée dans le modèle conceptuel ci-dessus.  
  
 [!code-xml[EDM_Example_Model#RefConstraint](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#refconstraint)]  
  
## <a name="see-also"></a>Voir aussi
- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
