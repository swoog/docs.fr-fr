---
title: ActivityTransfer
ms.date: 03/30/2017
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
ms.openlocfilehash: 480670f19407321eb0928d07752936b2ece1f7e9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33484186"
---
# <a name="activitytransfer"></a><span data-ttu-id="347c0-102">ActivityTransfer</span><span class="sxs-lookup"><span data-stu-id="347c0-102">ActivityTransfer</span></span>
<span data-ttu-id="347c0-103">Événement du transfert de l'activité</span><span class="sxs-lookup"><span data-stu-id="347c0-103">Activity Transfer Event</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="347c0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="347c0-104">Syntax</span></span>  
  
```  
class ActivityTransfer : WSAT_TraceEvent  
{  
  object ActivityID;  
  object RelatedActivityID;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="347c0-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="347c0-105">Methods</span></span>  
 <span data-ttu-id="347c0-106">La classe ActivityTransfer ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="347c0-106">The ActivityTransfer class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="347c0-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="347c0-107">Properties</span></span>  
 <span data-ttu-id="347c0-108">La classe ActivityTransfer a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="347c0-108">The ActivityTransfer class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="347c0-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="347c0-109">ActivityID</span></span>  
  
-   <span data-ttu-id="347c0-110">Type de données : objet</span><span class="sxs-lookup"><span data-stu-id="347c0-110">Data type: object</span></span>  
    <span data-ttu-id="347c0-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="347c0-111">Access type: Read-only</span></span>  
  
-   <span data-ttu-id="347c0-112">ID d'activité</span><span class="sxs-lookup"><span data-stu-id="347c0-112">Activity ID</span></span>  
  
### <a name="relatedactivityid"></a><span data-ttu-id="347c0-113">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="347c0-113">RelatedActivityID</span></span>  
  
-   <span data-ttu-id="347c0-114">Type de données : objet</span><span class="sxs-lookup"><span data-stu-id="347c0-114">Data type: object</span></span>  
    <span data-ttu-id="347c0-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="347c0-115">Access type: Read-only</span></span>  
  
-   <span data-ttu-id="347c0-116">ID d'activité connexe</span><span class="sxs-lookup"><span data-stu-id="347c0-116">Related Activity ID</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="347c0-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="347c0-117">Requirements</span></span>  
  
|<span data-ttu-id="347c0-118">MOF</span><span class="sxs-lookup"><span data-stu-id="347c0-118">MOF</span></span>|<span data-ttu-id="347c0-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="347c0-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="347c0-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="347c0-120">Namespace</span></span>|<span data-ttu-id="347c0-121">Défini dans root\ServiceModel.</span><span class="sxs-lookup"><span data-stu-id="347c0-121">Defined in root\ServiceModel.</span></span>|
