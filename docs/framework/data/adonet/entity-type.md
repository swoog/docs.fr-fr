---
title: type d'entité
ms.date: 03/30/2017
ms.assetid: a6dee9ab-9e4a-48f2-a169-3f79cc15821c
ms.openlocfilehash: 026b0aef7cf2de8fe222721191afa459859701ee
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59108262"
---
# <a name="entity-type"></a><span data-ttu-id="889ee-102">type d'entité</span><span class="sxs-lookup"><span data-stu-id="889ee-102">entity type</span></span>
<span data-ttu-id="889ee-103">Le *type d’entité* est le bloc de construction fondamental pour décrire la structure de données avec le modèle EDM (Entity Data Model).</span><span class="sxs-lookup"><span data-stu-id="889ee-103">The *entity type* is the fundamental building block for describing the structure of data with the Entity Data Model (EDM).</span></span> <span data-ttu-id="889ee-104">Dans un modèle conceptuel, un type d'entité représente la structure des concepts de niveau supérieur, comme les clients ou les commandes.</span><span class="sxs-lookup"><span data-stu-id="889ee-104">In a conceptual model, an entity type represents the structure of top-level concepts, such as customers or orders.</span></span> <span data-ttu-id="889ee-105">Un type d'entité est un modèle pour les instances de type d'entité.</span><span class="sxs-lookup"><span data-stu-id="889ee-105">An entity type is a template for entity type instances.</span></span> <span data-ttu-id="889ee-106">Chaque modèle contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="889ee-106">Each template contains the following information:</span></span>  
  
-   <span data-ttu-id="889ee-107">Nom unique.</span><span class="sxs-lookup"><span data-stu-id="889ee-107">A unique name.</span></span> <span data-ttu-id="889ee-108">(Obligatoire.)</span><span class="sxs-lookup"><span data-stu-id="889ee-108">(Required.)</span></span>  
  
-   <span data-ttu-id="889ee-109">Un [clé d’entité](../../../../docs/framework/data/adonet/entity-key.md) défini par une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="889ee-109">An [entity key](../../../../docs/framework/data/adonet/entity-key.md) defined by one or more properties.</span></span> <span data-ttu-id="889ee-110">(Obligatoire.)</span><span class="sxs-lookup"><span data-stu-id="889ee-110">(Required.)</span></span>  
  
-   <span data-ttu-id="889ee-111">Données sous la forme de [propriétés](../../../../docs/framework/data/adonet/property.md).</span><span class="sxs-lookup"><span data-stu-id="889ee-111">Data in the form of [properties](../../../../docs/framework/data/adonet/property.md).</span></span> <span data-ttu-id="889ee-112">(Facultatif)</span><span class="sxs-lookup"><span data-stu-id="889ee-112">(Optional.)</span></span>  
  
-   <span data-ttu-id="889ee-113">[Propriétés de navigation](../../../../docs/framework/data/adonet/navigation-property.md) qui permettent de naviguer parmi [fin](../../../../docs/framework/data/adonet/association-end.md) d’un [association](../../../../docs/framework/data/adonet/association-type.md) à l’autre extrémité.</span><span class="sxs-lookup"><span data-stu-id="889ee-113">[Navigation properties](../../../../docs/framework/data/adonet/navigation-property.md) that allow for navigation from one [end](../../../../docs/framework/data/adonet/association-end.md) of an [association](../../../../docs/framework/data/adonet/association-type.md) to the other end.</span></span> <span data-ttu-id="889ee-114">(facultatif)</span><span class="sxs-lookup"><span data-stu-id="889ee-114">(Optional)</span></span>  
  
 <span data-ttu-id="889ee-115">Dans une application, une instance d'un type d'entité représente un objet spécifique (tel qu'un client ou une commande spécifique).</span><span class="sxs-lookup"><span data-stu-id="889ee-115">In an application, an instance of an entity type represents a specific object (such as a specific customer or order).</span></span> <span data-ttu-id="889ee-116">Chaque instance d’un type d’entité doit avoir une valeur unique [clé d’entité](../../../../docs/framework/data/adonet/entity-key.md) au sein d’un [jeu d’entités](../../../../docs/framework/data/adonet/entity-set.md).</span><span class="sxs-lookup"><span data-stu-id="889ee-116">Each instance of an entity type must have a unique [entity key](../../../../docs/framework/data/adonet/entity-key.md) within an [entity set](../../../../docs/framework/data/adonet/entity-set.md).</span></span>  
  
 <span data-ttu-id="889ee-117">Deux instances de type d'entité sont considérées égales seulement si elles sont du même type et si les valeurs de leurs clés d'entité sont identiques.</span><span class="sxs-lookup"><span data-stu-id="889ee-117">Two entity type instances are considered equal only if they are of the same type and the values of their entity keys are the same.</span></span>  
  
## <a name="example"></a><span data-ttu-id="889ee-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="889ee-118">Example</span></span>  
 <span data-ttu-id="889ee-119">Le diagramme suivant montre un modèle conceptuel avec trois types d'entité : `Book`, `Publisher` et `Author`.</span><span class="sxs-lookup"><span data-stu-id="889ee-119">The diagram below shows a conceptual model with three entity types: `Book`, `Publisher`, and `Author`:</span></span>  
  
 ![Exemple de modèle avec trois types d’entité](./media/entity-type/example-model-three-entity-types.gif)  
  
 <span data-ttu-id="889ee-121">Notez que les propriétés de chaque type d'entité qui composent sa clé d'entité sont signalées par « (Key) ».</span><span class="sxs-lookup"><span data-stu-id="889ee-121">Note that the properties of each entity type that make up its entity key are denoted with "(Key)".</span></span>  
  
 <span data-ttu-id="889ee-122">Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels.</span><span class="sxs-lookup"><span data-stu-id="889ee-122">The [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) to define conceptual models.</span></span> <span data-ttu-id="889ee-123">Le CSDL suivant définit le type d'entité `Book` présenté dans le diagramme ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="889ee-123">The following CSDL defines the `Book` entity type shown in the diagram above:</span></span>  
  
 [!code-xml[EDM_Example_Model#EntityExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entityexample)]  
  
## <a name="see-also"></a><span data-ttu-id="889ee-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="889ee-124">See also</span></span>

- [<span data-ttu-id="889ee-125">Concepts clés d’Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="889ee-125">Entity Data Model Key Concepts</span></span>](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [<span data-ttu-id="889ee-126">Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="889ee-126">Entity Data Model</span></span>](../../../../docs/framework/data/adonet/entity-data-model.md)
- [<span data-ttu-id="889ee-127">facet</span><span class="sxs-lookup"><span data-stu-id="889ee-127">facet</span></span>](../../../../docs/framework/data/adonet/facet.md)
