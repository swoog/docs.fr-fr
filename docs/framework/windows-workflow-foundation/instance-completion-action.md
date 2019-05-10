---
title: Action d'achèvement de l'instance
ms.date: 03/30/2017
ms.assetid: 90cc99d2-9fef-42fd-bcbf-a56917993721
ms.openlocfilehash: d68f41a586e44f96c9ca26cf8a142a2782adaa36
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662975"
---
# <a name="instance-completion-action"></a><span data-ttu-id="4c530-102">Action d'achèvement de l'instance</span><span class="sxs-lookup"><span data-stu-id="4c530-102">Instance Completion Action</span></span>
<span data-ttu-id="4c530-103">Le **Instance Completion Action** propriété du Store d’Instance de Workflow SQL vous permet de spécifier si les données et métadonnées d’instances de workflow sont supprimées à partir de la base de données de persistance une fois que les instances ont abouti.</span><span class="sxs-lookup"><span data-stu-id="4c530-103">The **Instance Completion Action** property of the SQL Workflow Instance Store lets you specify whether the data and metadata of workflow instances is deleted from the persistence database after the instances are completed.</span></span> <span data-ttu-id="4c530-104">Les valeurs autorisées pour cette propriété sont **DeleteAll** et **DeleteNothing**.</span><span class="sxs-lookup"><span data-stu-id="4c530-104">The allowed values for this property are **DeleteAll** and **DeleteNothing**.</span></span> <span data-ttu-id="4c530-105">La liste suivante décrit ces trois options :</span><span class="sxs-lookup"><span data-stu-id="4c530-105">The following list describes these options:</span></span>  
  
- <span data-ttu-id="4c530-106">**DeleteAll (valeur par défaut).**</span><span class="sxs-lookup"><span data-stu-id="4c530-106">**DeleteAll (default).**</span></span> <span data-ttu-id="4c530-107">Si la valeur de la propriété est définie sur DeleteAll, les données et métadonnées d'instances de workflow sont supprimées de la base de données de persistance après que les instances ont abouti.</span><span class="sxs-lookup"><span data-stu-id="4c530-107">If the value of the property is set to DeleteAll, the data and metadata of workflow instances is deleted from the persistence database after the instances are completed.</span></span>  
  
- <span data-ttu-id="4c530-108">**DeleteNothing.**</span><span class="sxs-lookup"><span data-stu-id="4c530-108">**DeleteNothing.**</span></span> <span data-ttu-id="4c530-109">Si la valeur de la propriété est définie sur DeleteNothing, les données et métadonnées d'instances de workflow sont conservées dans la base de données de persistance même après que les instances ont abouti.</span><span class="sxs-lookup"><span data-stu-id="4c530-109">If the value of the property is set to DeleteNothing, the data and metadata of workflow instances is kept in the persistence database even after the instances are completed.</span></span>  
  
    > [!CAUTION]
    >  <span data-ttu-id="4c530-110">Garder les informations d'état de l'instance après que les instances ont abouti entraîne l'augmentation de la taille de la base de données de persistance.</span><span class="sxs-lookup"><span data-stu-id="4c530-110">Keeping instance state information after the instances are completed causes the persistence database to grow in size.</span></span> <span data-ttu-id="4c530-111">À mesure que la taille de la base de données augmente, les opérations de base de données que le sous-système de persistance effectue prennent plus de temps pour s'exécuter, donc vous devez régulièrement vider les informations d'état de l'instance de la base de données de persistance pour optimiser l'exécution de ces services.</span><span class="sxs-lookup"><span data-stu-id="4c530-111">As the size of the database grows the database operations that the persistence subsystem performs take longer, so you need to purge the instance state information from the persistence database periodically to have services perform at the level that satisfy your performance needs.</span></span>
