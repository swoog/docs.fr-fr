---
title: terminaison d'ensemble d'associations
ms.date: 03/30/2017
ms.assetid: fe4bf1d3-047a-4a37-98c5-a66e70811346
ms.openlocfilehash: ea750e9f381de92233f4c9389ec6676847b56d01
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64592595"
---
# <a name="association-set-end"></a><span data-ttu-id="7d3e4-102">terminaison d'ensemble d'associations</span><span class="sxs-lookup"><span data-stu-id="7d3e4-102">association set end</span></span>
<span data-ttu-id="7d3e4-103">Un *ensemble d’associations* identifie le [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) et [jeu d’entités](../../../../docs/framework/data/adonet/entity-set.md) à la fin d’un [ensemble d’associations](../../../../docs/framework/data/adonet/association-set.md).</span><span class="sxs-lookup"><span data-stu-id="7d3e4-103">An *association set end* identifies the [entity type](../../../../docs/framework/data/adonet/entity-type.md) and the [entity set](../../../../docs/framework/data/adonet/entity-set.md) at the end of an [association set](../../../../docs/framework/data/adonet/association-set.md).</span></span> <span data-ttu-id="7d3e4-104">Les terminaisons d'ensemble d'associations sont définies dans le cadre d'un ensemble d'associations ; un ensemble d'associations doit avoir exactement deux terminaisons d'ensemble d'associations.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-104">Association set ends are defined as part of an association set; an association set must have exactly two association set ends.</span></span>  
  
 <span data-ttu-id="7d3e4-105">Une définition de terminaison d'ensemble d'associations contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d3e4-105">An association set end definition contains the following information:</span></span>  
  
- <span data-ttu-id="7d3e4-106">Un des types d'entité impliqués dans l'ensemble d'associations.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-106">One of the entity types involved in the association set.</span></span> <span data-ttu-id="7d3e4-107">(Requis)</span><span class="sxs-lookup"><span data-stu-id="7d3e4-107">(Required)</span></span>  
  
- <span data-ttu-id="7d3e4-108">Jeu d'entités pour le type d'entité impliqué dans l'ensemble d'associations.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-108">The entity set for the entity type involved in the association set.</span></span> <span data-ttu-id="7d3e4-109">(Requis)</span><span class="sxs-lookup"><span data-stu-id="7d3e4-109">(Required)</span></span>  
  
## <a name="example"></a><span data-ttu-id="7d3e4-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="7d3e4-110">Example</span></span>  
 <span data-ttu-id="7d3e4-111">Le diagramme suivant montre un modèle conceptuel avec deux associations : `WrittenBy` et `PublishedBy`.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-111">The diagram below shows a conceptual model with two associations: `WrittenBy` and `PublishedBy`.</span></span>  
  
 ![Exemple de modèle avec trois types d’entité](./media/association-set-end/example-model-three-entity-types.gif)  
  
 <span data-ttu-id="7d3e4-113">Le diagramme suivant montre un ensemble d'associations (`PublishedBy`) et deux jeux d'entités (`Books` et `Publishers`) selon le modèle conceptuel présenté ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-113">The following diagram shows an association set (`PublishedBy`) and two entity sets (`Books` and `Publishers`) based on the conceptual model shown above.</span></span> <span data-ttu-id="7d3e4-114">Les terminaisons d'ensemble d'associations sont les jeux d'entités `Books` et `Publishers`.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-114">The association set ends are the `Books` and `Publishers` entity sets.</span></span> <span data-ttu-id="7d3e4-115">BI dans le `Books` jeu d’entités représente une instance de la `Book` type d’entité en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-115">Bi in the `Books` entity set represents an instance of the `Book` entity type at run time.</span></span> <span data-ttu-id="7d3e4-116">De même, Pj représente un `Publisher` d’instance dans le `Publishers` jeu d’entités.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-116">Similarly, Pj represents a `Publisher` instance in the `Publishers` entity set.</span></span> <span data-ttu-id="7d3e4-117">BiPj représente une instance de la `PublishedBy` association dans le `PublishedBy` ensemble d’associations.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-117">BiPj represents an instance of the `PublishedBy` association in the `PublishedBy` association set.</span></span>  
  
 ![Capture d’écran montre un exemple de jeux.](./media/association-set-end/sets-example-association.gif)  
  
 <span data-ttu-id="7d3e4-119">Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage DSL appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-119">The [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) uses a DSL called conceptual schema definition language ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) to define conceptual models.</span></span> <span data-ttu-id="7d3e4-120">Le CSDL suivant définit un conteneur d'entités avec un ensemble d'associations pour chaque association dans le diagramme ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-120">The following CSDL defines an entity container with one association set for each association in the diagram above.</span></span> <span data-ttu-id="7d3e4-121">Notez que les terminaisons d'ensemble d'associations sont définies dans le cadre de chaque définition d'ensemble d'associations.</span><span class="sxs-lookup"><span data-stu-id="7d3e4-121">Note that association set ends are defined as part of each association set definition.</span></span>  
  
 [!code-xml[EDM_Example_Model#EntityContainerExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entitycontainerexample)]  
  
## <a name="see-also"></a><span data-ttu-id="7d3e4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d3e4-122">See also</span></span>

- [<span data-ttu-id="7d3e4-123">Concepts clés d’Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="7d3e4-123">Entity Data Model Key Concepts</span></span>](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [<span data-ttu-id="7d3e4-124">Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="7d3e4-124">Entity Data Model</span></span>](../../../../docs/framework/data/adonet/entity-data-model.md)
