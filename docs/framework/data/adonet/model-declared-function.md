---
title: fonction déclarée par modèle
ms.date: 03/30/2017
ms.assetid: aba87f13-5685-4f6b-ad14-918e8a7d5c2a
ms.openlocfilehash: a0bea36693122c77d9c1abdf4484ee8e68627a0c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645871"
---
# <a name="model-declared-function"></a><span data-ttu-id="503b5-102">fonction déclarée par modèle</span><span class="sxs-lookup"><span data-stu-id="503b5-102">model-declared function</span></span>
<span data-ttu-id="503b5-103">Un *fonction déclarée par modèle* est une fonction qui est déclarée dans un modèle conceptuel, mais n’est pas définie dans ce modèle conceptuel.</span><span class="sxs-lookup"><span data-stu-id="503b5-103">A *model-declared function* is a function that is declared in a conceptual model, but is not defined in that conceptual model.</span></span> <span data-ttu-id="503b5-104">La fonction peut être définie dans l'environnement d'hébergement ou de stockage.</span><span class="sxs-lookup"><span data-stu-id="503b5-104">The function might be defined in the hosting or storage environment.</span></span> <span data-ttu-id="503b5-105">Par exemple, une fonction déclarée par modèle peut être mappée à une fonction définie dans une base de données, exposant ainsi les fonctionnalités côté serveur dans le modèle conceptuel.</span><span class="sxs-lookup"><span data-stu-id="503b5-105">For example, a model-declared function might be mapped to a function that is defined in a database, thus exposing server-side functionality in the conceptual model.</span></span>  
  
 <span data-ttu-id="503b5-106">La déclaration d'une fonction déclarée par modèle contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="503b5-106">The declaration of a model-declared function contains the following information:</span></span>  
  
- <span data-ttu-id="503b5-107">Nom de la fonction.</span><span class="sxs-lookup"><span data-stu-id="503b5-107">The name of the function.</span></span> <span data-ttu-id="503b5-108">(Requis)</span><span class="sxs-lookup"><span data-stu-id="503b5-108">(Required)</span></span>  
  
- <span data-ttu-id="503b5-109">Type de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="503b5-109">The type of the return value.</span></span> <span data-ttu-id="503b5-110">(facultatif)</span><span class="sxs-lookup"><span data-stu-id="503b5-110">(Optional)</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="503b5-111">Si aucune valeur de retour n'est spécifiée, le type de retour est void.</span><span class="sxs-lookup"><span data-stu-id="503b5-111">If no return value is specified, the return type is void.</span></span>  
  
- <span data-ttu-id="503b5-112">Informations sur les paramètres, notamment le nom et le type des paramètres.</span><span class="sxs-lookup"><span data-stu-id="503b5-112">Parameter information, including parameter name and type.</span></span> <span data-ttu-id="503b5-113">(facultatif)</span><span class="sxs-lookup"><span data-stu-id="503b5-113">(Optional)</span></span>  
  
## <a name="example"></a><span data-ttu-id="503b5-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="503b5-114">Example</span></span>  
 <span data-ttu-id="503b5-115">Le [ADO.NET Entity Framework](./ef/index.md) utilise un langage spécifique à un domaine (DSL) appelé langage de définition de schéma conceptuel ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) pour définir des modèles conceptuels.</span><span class="sxs-lookup"><span data-stu-id="503b5-115">The [ADO.NET Entity Framework](./ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) to define conceptual models.</span></span> <span data-ttu-id="503b5-116">Dans le langage CSDL, une implémentation d’une fonction déclarée par modèle est une importation de fonction (à l’aide de la [élément FunctionImport](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#functionimport-element-csdl)).</span><span class="sxs-lookup"><span data-stu-id="503b5-116">In CSDL, one implementation of a model-declared function is a function import (using the [FunctionImport element](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#functionimport-element-csdl)).</span></span> <span data-ttu-id="503b5-117">Le CSDL suivant définit un conteneur d'entités avec une définition d'importation de fonction.</span><span class="sxs-lookup"><span data-stu-id="503b5-117">The following CSDL defines an entity container with a function import definition.</span></span> <span data-ttu-id="503b5-118">Notez que le type de retour pour la fonction est void, car aucun type de retour n'est spécifié.</span><span class="sxs-lookup"><span data-stu-id="503b5-118">Note that the return type for the function is void since no return type is specified.</span></span>  
  
 [!code-xml[EDM_Example_Model#FunctionImport](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#functionimport)]  
  
## <a name="see-also"></a><span data-ttu-id="503b5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="503b5-119">See also</span></span>

- [<span data-ttu-id="503b5-120">Concepts clés d’Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="503b5-120">Entity Data Model Key Concepts</span></span>](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [<span data-ttu-id="503b5-121">Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="503b5-121">Entity Data Model</span></span>](../../../../docs/framework/data/adonet/entity-data-model.md)
