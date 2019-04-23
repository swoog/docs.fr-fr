---
title: terminaison d'association
ms.date: 03/30/2017
ms.assetid: 2c345213-0296-4d90-ac6d-cef179798a75
ms.openlocfilehash: e549254533f8362ce3475fb3aa5dbaffb3e900e5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59108288"
---
# <a name="association-end"></a>terminaison d'association
Un *terminaison d’association* identifie le [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) sur une extrémité d’une [association](../../../../docs/framework/data/adonet/association-type.md) et le numéro d’entité de type des instances qui peuvent exister à cette fin d’une association. Les terminaisons d'association sont définies dans le cadre d'une association ; une association doit avoir exactement deux terminaisons d'association. [Propriétés de navigation](../../../../docs/framework/data/adonet/navigation-property.md) permettent de naviguer à partir d’une terminaison d’association à l’autre.  
  
 Une définition de terminaison d'association contient les informations suivantes :  
  
-   Un des types d'entité impliqués dans l'association. (Requis)  
  
    > [!NOTE]
    >  Pour une association donnée, le type d'entité spécifié pour chaque terminaison d'association peut être le même. Ceci crée une association automatique.  
  
-   Un [multiplicité de terminaison d’association](../../../../docs/framework/data/adonet/association-end-multiplicity.md) qui indique le nombre d’instances de type d’entité qui peut être une des extrémités de l’association. Une multiplicité de terminaison d’association peut avoir une valeur d’un (1), zéro ou un (0.. 1) ou plusieurs (\*).  
  
-   Nom de la terminaison de l'association. (facultatif)  
  
-   Informations sur les opérations effectuées sur la terminaison d'association, telles que CASCADE sur DELETE. (facultatif)  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec deux associations : `PublishedBy` et `WrittenBy`. Les terminaisons d'association pour l'association `PublishedBy` sont les types d'entité `Book` et `Publisher`. La multiplicité de la `Publisher` fin est un (1) et la multiplicité de la `Book` fin est plusieurs (\*), indiquant qu’un éditeur publie de nombreux livres et un livre est publié par un seul éditeur.  
  
 ![Exemple de modèle avec trois types d’entité](./media/association-end/example-model-three-entity-types.gif)  
  
 ADO.NET Entity Framework utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit l'association `PublishedBy` présentée dans le diagramme ci-dessus. Notez que le type, le nom et la multiplicité de chaque terminaison d'association sont spécifiés par des attributs XML (`Type`, `Role` et `Multiplicity`, respectivement). Des informations facultatives sur les opérations effectuées sur une terminaison sont spécifiées dans un élément XML (`OnDelete`). Dans ce cas, si un éditeur est supprimé, tous les livres associés le sont aussi.  
  
 [!code-xml[EDM_Example_Model#AssociationEnd](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books3.edmx#associationend)]  
  
## <a name="see-also"></a>Voir aussi

- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
