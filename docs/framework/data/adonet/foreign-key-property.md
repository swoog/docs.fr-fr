---
title: Propriété de clé étrangère
ms.date: 03/30/2017
ms.assetid: 23cb6729-544d-4f67-9ee7-44e8a6545587
ms.openlocfilehash: 8680019f6f1a53233b5c49163f474cf33409b69b
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57674469"
---
# <a name="foreign-key-property"></a>Propriété de clé étrangère
Un *propriété de clé étrangère* dans le modèle EDM (Entity Data Model) est un type primitif [propriété](../../../../docs/framework/data/adonet/property.md) (ou un ensemble de propriétés de type primitif) sur un [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) qui contient le [clé d’entité](../../../../docs/framework/data/adonet/entity-key.md) d’un autre type d’entité.  
  
 Une propriété de clé étrangère est analogue à une colonne clé étrangère dans une base de données relationnelle. Dans la même façon que les colonnes clés étrangères sont utilisés dans une base de données relationnel pour créer des relations entre les lignes dans les tables, les propriétés de clé étrangère dans un modèle conceptuel sont utilisées pour établir [associations](../../../../docs/framework/data/adonet/association-type.md) entre types d’entité. Un [contrainte d’intégrité référentielle](../../../../docs/framework/data/adonet/referential-integrity-constraint.md) est utilisé pour définir une association entre deux types d’entités lorsqu’un des types a une propriété de clé étrangère.  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec trois types d'entités : `Book`, `Publisher` et `Author`. Le type d'entité `Book` a une propriété, `PublisherId`, qui référence la clé d'entité du type d'entité `Publisher` lorsque vous définissez une contrainte d'intégrité référentielle sur l'association `PublishedBy`.  
  
 ![RefConstraintModel](./media/foreign-key-property/reference-constraint-model.gif "exemple d’un modèle de contrainte référentielle")  
  
 Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant utilise la propriété de clé étrangère `PublisherId` pour définir une contrainte d'intégrité référentielle sur l'association `PublishedBy` présentée dans le modèle conceptuel ci-dessus.  
  
 [!code-xml[EDM_Example_Model#RefConstraint](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#refconstraint)]  
  
## <a name="see-also"></a>Voir aussi
- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
