---
title: Propriété de navigation - ADO.NET
ms.date: 03/30/2017
ms.assetid: d0bf1a6a-1d84-484c-b7c3-b410fd8dc0b1
ms.openlocfilehash: b57ecf9329aa9ea8afc07507613c9e3961bfd0a9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58836595"
---
# <a name="navigation-property"></a>Propriété de navigation

Un *propriété de navigation* est une propriété facultative sur un [type d’entité](entity-type.md) qui permet de naviguer d’une [fin](association-end.md) d’un [association](association-type.md) à l’autre extrémité. Contrairement à d’autres [propriétés](property.md), propriétés de navigation ne comportant pas de données.

Une définition de propriété de navigation comprend les éléments suivants :

- Nom. (Requis)

- Association faisant l'objet de la navigation. (Requis)

- Terminaisons de l'association faisant l'objet de la navigation. (Requis)

Notez que les propriétés de navigation sont facultatives sur les deux types d'entités au niveau des terminaisons d'une association. Si vous définissez une propriété de navigation sur un type d'entité au niveau de la terminaison d'une association, il n'est pas nécessaire de définir une propriété de navigation sur le type d'entité à l'autre terminaison de l'association.

Le type de données d’une propriété de navigation est déterminé par le [multiplicité](association-end-multiplicity.md) de son remote [terminaison d’association](association-end.md). Par exemple, considérez une propriété de navigation, `OrdersNavProp`, qui existe sur un type d'entité `Customer` et qui navigue dans une association un-à-plusieurs entre `Customer` et `Order`. Étant donné que la terminaison d’association distante pour la propriété de navigation a une multiplicité d’un grand nombre (\*), son type de données est une collection (de `Order`). De même, si une propriété de navigation, `CustomerNavProp`, existe sur le type d'entité `Order`, son type de données est `Customer`, car la multiplicité de la terminaison distante est un (1).

## <a name="example"></a>Exemple

Le diagramme suivant montre un modèle conceptuel avec trois types d'entités : `Book`, `Publisher` et `Author`. Les propriétés de navigation, `Publisher` et `Authors`, sont définies sur le type d'entité Book. La propriété de navigation `Books` est définie sur le type d'entité Publisher et le type d'entité `Author`.

 ![Diagramme montrant un modèle conceptuel avec trois types d’entité.](./media/navigation-property/conceptual-model-entity-types-associations.gif)  

Le [ADO.NET Entity Framework](./ef/index.md) utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](./ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit le type d'entité `Book` présenté dans le diagramme ci-dessus :

[!code-xml[EDM_Example_Model#EntityExample](~/samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entityexample)]

Notez que les attributs XML sont utilisées pour communiquer les informations nécessaires pour définir une propriété de navigation : L’attribut `Name` contient le nom de la propriété, `Relationship` contient le nom de l’association, il accède, et `FromRole` et `ToRole` contiennent les terminaisons de l’association.

## <a name="see-also"></a>Voir aussi

- [Concepts clés d’Entity Data Model](entity-data-model-key-concepts.md)
- [Entity Data Model](entity-data-model.md)
- [Relations, les propriétés de navigation et les clés étrangères](/ef/ef6/fundamentals/relationships)
