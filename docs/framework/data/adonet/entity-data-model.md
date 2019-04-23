---
title: Entity Data Model
ms.date: 03/30/2017
ms.assetid: 2dda3d5b-4582-4ba0-a91d-fcd7a1498137
ms.openlocfilehash: 8e96890d97f652295a3fdb67c48ec37710280eec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59197917"
---
# <a name="entity-data-model"></a>Entity Data Model
Le modèle EDM (Entity Data Model) est un jeu de concepts qui décrivent la structure des données, indépendamment de la forme sous laquelle elles sont stockées. Inspiré du modèle entité-relation décrit par Peter Chen en 1976, le modèle EDM le complète et étend ses utilisations traditionnelles.  
  
 Le modèle EDM aborde les difficultés qui se présentent lors du stockage de données sous plusieurs formes. Par exemple, prenons une entreprise qui stocke des données dans des bases de données relationnelles, des fichiers texte, des fichiers XML, des feuilles de calcul et des rapports. Cette diversité pose des problèmes importants en termes de modélisation des données, de conception d'application et d'accès aux données. Lors de la conception d'une application orientée données, l'écriture de code efficace et gérable sans nuire à l'efficacité de l'accès aux données, du stockage et de l'évolutivité relève du défi. Lorsque les données ont une structure relationnelle, l'accès aux données, le stockage et l'évolutivité sont très efficaces, mais l'écriture de code efficace et gérable devient plus difficile. Lorsque les données ont une structure d’objet, les compromis sont inversées : Écriture de code efficace et gérable vient au détriment de l’évolutivité, de stockage et accès efficace aux données. Même s'il est possible de trouver un juste équilibre entre ces deux aspects, de nouvelles difficultés se présentent lorsque des données passent d'une forme à une autre. Le modèle Entity Data Model aborde ces difficultés en décrivant la structure des données en termes d'entités et de relations qui sont indépendantes de tout schéma de stockage. La forme sous laquelle les données sont stockées n'a alors plus aucune incidence sur la conception et le développement de l'application. Par ailleurs, comme les entités et les relations décrivent la structure des données telles qu'elles sont utilisées dans une application (et non la forme sous laquelle elles sont stockées), elles peuvent évoluer parallèlement à une application.  
  
 Un `conceptual model` est une représentation spécifique de la structure des données sous forme d'entités et de relations. Il est en général défini dans un langage spécifique à un domaine (DSL) qui implémente les concepts du modèle EDM. [Langage de définition de schéma conceptuel (CSDL)](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md) est un exemple de ces langages spécifiques à un domaine. Les entités et les relations décrites dans un modèle conceptuel peuvent être considérées comme des abstractions d'objets et d'associations dans une application. Cela permet aux développeurs de se concentrer sur le modèle conceptuel sans se soucier du schéma de stockage, et d'écrire du code en favorisant son efficacité et sa maintenabilité. Pendant ce temps, les concepteurs de schémas de stockage peuvent se concentrer sur l'efficacité de l'accès aux données, du stockage et de l'évolutivité.  
  
## <a name="in-this-section"></a>Dans cette section  
 Les rubriques de cette section décrivent les concepts du modèle EDM. Tout langage DSL qui implémente le modèle EDM doit inclure les concepts décrits ici. Notez que le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise le langage CSDL pour définir des modèles conceptuels. Pour plus d'informations, consultez [CSDL Specification](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md).  
  
 [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)  
  
 [Entity Data Model : Espaces de noms](../../../../docs/framework/data/adonet/entity-data-model-namespaces.md)  
  
 [Entity Data Model : Types de données primitifs](../../../../docs/framework/data/adonet/entity-data-model-primitive-data-types.md)  
  
 [Entity Data Model : Héritage](../../../../docs/framework/data/adonet/entity-data-model-inheritance.md)  
  
 [terminaison d’association](../../../../docs/framework/data/adonet/association-end.md)  
  
 [multiplicité de terminaison d’association](../../../../docs/framework/data/adonet/association-end-multiplicity.md)  
  
 [ensemble d’associations](../../../../docs/framework/data/adonet/association-set.md)  
  
 [terminaison d’ensemble d’associations](../../../../docs/framework/data/adonet/association-set-end.md)  
  
 [type d’association](../../../../docs/framework/data/adonet/association-type.md)  
  
 [type complexe](../../../../docs/framework/data/adonet/complex-type.md)  
  
 [conteneur d’entités](../../../../docs/framework/data/adonet/entity-container.md)  
  
 [clé d’entité](../../../../docs/framework/data/adonet/entity-key.md)  
  
 [jeu d’entités](../../../../docs/framework/data/adonet/entity-set.md)  
  
 [type d’entité](../../../../docs/framework/data/adonet/entity-type.md)  
  
 [facet](../../../../docs/framework/data/adonet/facet.md)  
  
 [propriété de clé étrangère](../../../../docs/framework/data/adonet/foreign-key-property.md)  
  
 [fonction déclarée par modèle](../../../../docs/framework/data/adonet/model-declared-function.md)  
  
 [fonction définie par modèle](../../../../docs/framework/data/adonet/model-defined-function.md)  
  
 [propriété de navigation](../../../../docs/framework/data/adonet/navigation-property.md)  
  
 [propriété](../../../../docs/framework/data/adonet/property.md)  
  
 [contrainte d’intégrité référentielle](../../../../docs/framework/data/adonet/referential-integrity-constraint.md)  
  
## <a name="see-also"></a>Voir aussi

- [ADO.NET Entity Data Model Tools](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))
- [vue d’ensemble du fichier .edmx](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100))
- [Spécification CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)
