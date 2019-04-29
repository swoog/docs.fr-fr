---
title: Action d'achèvement de l'instance
ms.date: 03/30/2017
ms.assetid: 90cc99d2-9fef-42fd-bcbf-a56917993721
ms.openlocfilehash: 646015fbcdb7c734ae8584c7ca3979d64b81339f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791116"
---
# <a name="instance-completion-action"></a><span data-ttu-id="64202-102">Action d'achèvement de l'instance</span><span class="sxs-lookup"><span data-stu-id="64202-102">Instance Completion Action</span></span>
<span data-ttu-id="64202-103">Le **Instance Completion Action** propriété du Store d’Instance de Workflow SQL vous permet de spécifier si les données et métadonnées d’instances de workflow sont supprimées à partir de la base de données de persistance une fois que les instances ont abouti.</span><span class="sxs-lookup"><span data-stu-id="64202-103">The **Instance Completion Action** property of the SQL Workflow Instance Store lets you specify whether the data and metadata of workflow instances is deleted from the persistence database after the instances are completed.</span></span> <span data-ttu-id="64202-104">Les valeurs autorisées pour cette propriété sont **DeleteAll** et **DeleteNothing**.</span><span class="sxs-lookup"><span data-stu-id="64202-104">The allowed values for this property are **DeleteAll** and **DeleteNothing**.</span></span> <span data-ttu-id="64202-105">La liste suivante décrit ces trois options :</span><span class="sxs-lookup"><span data-stu-id="64202-105">The following list describes these options:</span></span>  
  
- <span data-ttu-id="64202-106">**DeleteAll (valeur par défaut).**</span><span class="sxs-lookup"><span data-stu-id="64202-106">**DeleteAll (default).**</span></span> <span data-ttu-id="64202-107">Si la valeur de la propriété est définie sur DeleteAll, les données et métadonnées d'instances de workflow sont supprimées de la base de données de persistance après que les instances ont abouti.</span><span class="sxs-lookup"><span data-stu-id="64202-107">If the value of the property is set to DeleteAll, the data and metadata of workflow instances is deleted from the persistence database after the instances are completed.</span></span>  
  
- <span data-ttu-id="64202-108">**DeleteNothing.**</span><span class="sxs-lookup"><span data-stu-id="64202-108">**DeleteNothing.**</span></span> <span data-ttu-id="64202-109">Si la valeur de la propriété est définie sur DeleteNothing, les données et métadonnées d'instances de workflow sont conservées dans la base de données de persistance même après que les instances ont abouti.</span><span class="sxs-lookup"><span data-stu-id="64202-109">If the value of the property is set to DeleteNothing, the data and metadata of workflow instances is kept in the persistence database even after the instances are completed.</span></span>  
  
    > [!CAUTION]
    >  <span data-ttu-id="64202-110">Garder les informations d'état de l'instance après que les instances ont abouti entraîne l'augmentation de la taille de la base de données de persistance.</span><span class="sxs-lookup"><span data-stu-id="64202-110">Keeping instance state information after the instances are completed causes the persistence database to grow in size.</span></span> <span data-ttu-id="64202-111">À mesure que la taille de la base de données augmente, les opérations de base de données que le sous-système de persistance effectue prennent plus de temps pour s'exécuter, donc vous devez régulièrement vider les informations d'état de l'instance de la base de données de persistance pour optimiser l'exécution de ces services.</span><span class="sxs-lookup"><span data-stu-id="64202-111">As the size of the database grows the database operations that the persistence subsystem performs take longer, so you need to purge the instance state information from the persistence database periodically to have services perform at the level that satisfy your performance needs.</span></span>
