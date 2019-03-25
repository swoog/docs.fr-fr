---
title: clé d'entité
ms.date: 03/30/2017
ms.assetid: 0d447a6d-fa7a-4db0-8e7a-fd45e385fca0
ms.openlocfilehash: 0c3a809884fc7b7c1f188af9881f784527fa87ba
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58408962"
---
# <a name="entity-key"></a>clé d'entité
Un *clé d’entité* est un [propriété](../../../../docs/framework/data/adonet/property.md) ou un jeu de propriétés d’un [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) qui servent à déterminer l’identité. Les propriétés qui composent une clé d'entité sont choisies au moment du design. Les valeurs des propriétés de clé d’entité doivent identifier de manière unique une instance de type d’entité dans un [jeu d’entités](../../../../docs/framework/data/adonet/entity-set.md) en cours d’exécution. Les propriétés qui composent une clé d'entité doivent être choisies pour garantir l'unicité des instances dans un jeu d'entités.  
  
 Pour être une clé d’entité, un jeu de propriétés doit répondre aux exigences suivantes :  
  
-   Il ne peut pas y avoir deux clés d'entité identiques dans un même jeu d'entités. Autrement dit, pour deux entités quelconques dans un jeu d'entités, les valeurs de toutes les propriétés qui constituent une clé ne peuvent pas être les mêmes. Toutefois, quelques-unes des valeurs (mais pas toutes) qui composent une clé d'entité peuvent être les mêmes.  
  
-   Une clé d’entité doit se composer d’un ensemble de non nullable, immuable, [propriétés de type primitif](../../../../docs/framework/data/adonet/entity-data-model-primitive-data-types.md).  
  
-   Les propriétés qui composent une clé d'entité pour un type d'entité donné ne peuvent pas être modifiées. Vous ne pouvez pas autoriser plusieurs clés d'entité possibles pour un type d'entité donné ; les clés de substitution ne sont pas prises en charge.  
  
-   Lorsqu'une entité est impliquée dans une hiérarchie d'héritage, l'entité racine doit contenir toutes les propriétés qui composent la clé d'entité, et la clé d'entité doit être définie sur le type d'entité racine. Pour plus d’informations, consultez [Entity Data Model : L’héritage](../../../../docs/framework/data/adonet/entity-data-model-inheritance.md).  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec trois types d'entités : `Book`, `Publisher` et `Author`. Les propriétés de chaque type d'entité qui composent sa clé d'entité sont signalées par « (Key) ». Notez que le type d'entité `Author` possède une clé d'entité composée de deux propriétés : `Name` et `Address`.  
  
 ![Exemple de modèle avec trois types d’entité](./media/entity-key/example-model-three-entity-types.gif)  
  
 Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit le type d'entité `Book` présenté dans le diagramme ci-dessus. Notez que la clé d'entité est définie en référençant la propriété `ISBN` du type d'entité.  
  
 [!code-xml[EDM_Example_Model#EntityExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entityexample)]  
  
 La propriété `ISBN` est un bon choix pour la clé d'entité, car un numéro ISBN (International Standard Book Number) identifie un livre de façon unique.  
  
 Le CSDL suivant définit le type d'entité `Author` présenté dans le diagramme ci-dessus. Notez que la clé d'entité comprend deux propriétés : `Name` et `Address`.  
  
 [!code-xml[EDM_Example_Model#CompositeKeyExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#compositekeyexample)]  
  
 L'utilisation de `Name` et d'`Address` pour la clé d'entité est un choix raisonnable, car il est improbable que deux auteurs du même nom habitent à la même adresse. Toutefois, ce choix pour une clé d'entité ne garantit pas vraiment l'unicité des clés d'entité dans un jeu d'entités. Il est recommandé dans ce cas d'ajouter une propriété, telle qu'`AuthorId`, qui peut être utilisée pour identifier un auteur de façon unique.  
  
## <a name="see-also"></a>Voir aussi
- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
