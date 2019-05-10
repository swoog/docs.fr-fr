---
title: fonction définie par modèle
ms.date: 03/30/2017
ms.assetid: 8bb2edc8-e8e7-44c2-adc7-f44e11bda4f0
ms.openlocfilehash: 4f98bbc9fdc19159354ec3e414c1a1c26029cb47
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645844"
---
# <a name="model-defined-function"></a>fonction définie par modèle
Un *fonction définie par modèle* est une fonction qui est définie dans un modèle conceptuel. Le corps d’une fonction définie par modèle est exprimé en [Entity SQL](../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md), ce qui permet la fonction exprimer indépendamment de règles ou les langues prises en charge dans la source de données.  
  
 Une définition pour une fonction définie par modèle contient les informations suivantes :  
  
- Nom de la fonction. (Requis)  
  
- Type de la valeur de retour. (facultatif)  
  
    > [!NOTE]
    >  Si aucun type de retour n’est spécifié, la valeur de retour est void.  
  
- Informations sur les paramètres. (facultatif)  
  
- Un [Entity SQL](../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md) expression qui définit le corps de la fonction.  
  
 Notez que les fonctions définies par modèle ne prennent pas en charge les paramètres de sortie. Cette restriction est en place de manière à ce que des fonctions définies par modèle puissent être composées.  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec trois types d'entités : `Book`, `Publisher` et `Author`.  
  
 ![Capture d’écran montre un modèle avec la date de publication.](./media/model-defined-function/model-published-date-three-entity-types.gif)  
  
 Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit une fonction dans le modèle conceptuel qui retourne le nombre d'années écoulées depuis la publication d'une instance de `Book` (dans le diagramme ci-dessus).  
  
 [!code-xml[EDM_Example_Model#ModelDefinedFunction](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#modeldefinedfunction)]  
  
## <a name="see-also"></a>Voir aussi

- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
- [Entity Data Model : Types de données primitifs](../../../../docs/framework/data/adonet/entity-data-model-primitive-data-types.md)
