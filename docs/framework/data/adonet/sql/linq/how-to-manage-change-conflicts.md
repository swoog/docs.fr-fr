---
title: 'Comment : gérer les conflits de changement'
ms.date: 03/30/2017
ms.assetid: cd292c51-a3d1-4c6f-8d8e-04323c36054e
ms.openlocfilehash: 7858dc304d281dfb99755d83eec19b421f63d2ce
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361664"
---
# <a name="how-to-manage-change-conflicts"></a><span data-ttu-id="5a009-102">Comment : gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="5a009-102">How to: Manage Change Conflicts</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="5a009-103"> fournit un ensemble d’API pour vous aider à identifier, évaluer et résoudre les conflits d’accès concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="5a009-103"> provides a collection of APIs to help you discover, evaluate, and resolve concurrency conflicts.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5a009-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5a009-104">In This Section</span></span>  
 [<span data-ttu-id="5a009-105">Guide pratique pour détecter et résoudre des soumissions en conflit</span><span class="sxs-lookup"><span data-stu-id="5a009-105">How to: Detect and Resolve Conflicting Submissions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-detect-and-resolve-conflicting-submissions.md)  
 <span data-ttu-id="5a009-106">Explique comment détecter et résoudre les conflits d'accès concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="5a009-106">Describes how to detect and resolve concurrency conflicts.</span></span>  
  
 [<span data-ttu-id="5a009-107">Guide pratique pour spécifier le moment où des exceptions d’accès concurrentiel sont levées</span><span class="sxs-lookup"><span data-stu-id="5a009-107">How to: Specify When Concurrency Exceptions are Thrown</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-specify-when-concurrency-exceptions-are-thrown.md)  
 <span data-ttu-id="5a009-108">Explique comment spécifier dans quel cas vous devez être informé de conflits d'accès concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="5a009-108">Describes how to specify when you should be informed of concurrency conflicts.</span></span>  
  
 [<span data-ttu-id="5a009-109">Guide pratique pour spécifier les membres dont les conflits d’accès concurrentiel doivent être vérifiés</span><span class="sxs-lookup"><span data-stu-id="5a009-109">How to: Specify Which Members are Tested for Concurrency Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-specify-which-members-are-tested-for-concurrency-conflicts.md)  
 <span data-ttu-id="5a009-110">Explique comment attribuer des membres pour spécifier si les conflits d'accès concurrentiel sont vérifiés.</span><span class="sxs-lookup"><span data-stu-id="5a009-110">Describes how to attribute members to specify whether they are checked for concurrency conflicts.</span></span>  
  
 [<span data-ttu-id="5a009-111">Guide pratique pour récupérer des informations sur les conflits entre entités</span><span class="sxs-lookup"><span data-stu-id="5a009-111">How to: Retrieve Entity Conflict Information</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-retrieve-entity-conflict-information.md)  
 <span data-ttu-id="5a009-112">Explique comment réunir des informations à propos des conflits d'entité.</span><span class="sxs-lookup"><span data-stu-id="5a009-112">Describes how to gather information about entity conflicts.</span></span>  
  
 [<span data-ttu-id="5a009-113">Guide pratique pour récupérer des informations sur les conflits entre membres</span><span class="sxs-lookup"><span data-stu-id="5a009-113">How to: Retrieve Member Conflict Information</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-retrieve-member-conflict-information.md)  
 <span data-ttu-id="5a009-114">Explique comment réunir des informations à propos des conflits de membre.</span><span class="sxs-lookup"><span data-stu-id="5a009-114">Describes how to gather information about member conflicts.</span></span>  
  
 [<span data-ttu-id="5a009-115">Guide pratique pour résoudre des conflits en conservant des valeurs de bases de données</span><span class="sxs-lookup"><span data-stu-id="5a009-115">How to: Resolve Conflicts by Retaining Database Values</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-resolve-conflicts-by-retaining-database-values.md)  
 <span data-ttu-id="5a009-116">Explique comment substituer les valeurs actuelles par les valeurs de la base de données.</span><span class="sxs-lookup"><span data-stu-id="5a009-116">Describes how to overwrite current values with database values.</span></span>  
  
 [<span data-ttu-id="5a009-117">Guide pratique pour résoudre des conflits en remplaçant des valeurs de bases de données</span><span class="sxs-lookup"><span data-stu-id="5a009-117">How to: Resolve Conflicts by Overwriting Database Values</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-resolve-conflicts-by-overwriting-database-values.md)  
 <span data-ttu-id="5a009-118">Explique comment conserver les valeurs actuelles en substituant les valeurs de la base de données.</span><span class="sxs-lookup"><span data-stu-id="5a009-118">Describes how to keep current values by overwriting database values.</span></span>  
  
 [<span data-ttu-id="5a009-119">Guide pratique pour résoudre des conflits en fusionnant des valeurs de bases de données</span><span class="sxs-lookup"><span data-stu-id="5a009-119">How to: Resolve Conflicts by Merging with Database Values</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-resolve-conflicts-by-merging-with-database-values.md)  
 <span data-ttu-id="5a009-120">Explique comment résoudre un conflit en fusionnant les valeurs actuelles et les valeurs de la base de données.</span><span class="sxs-lookup"><span data-stu-id="5a009-120">Describes how to resolve a conflict by merging database and current values.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="5a009-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a009-121">Related Sections</span></span>  
 [<span data-ttu-id="5a009-122">Accès concurrentiel optimiste : vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="5a009-122">Optimistic Concurrency: Overview</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md)  
 <span data-ttu-id="5a009-123">Détaille les termes qui s'appliquent à l'accès concurrentiel optimiste dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="5a009-123">Explains the terms that apply to optimistic concurrency in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span>
