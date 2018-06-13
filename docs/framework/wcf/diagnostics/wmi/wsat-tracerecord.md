---
title: WSAT_TraceRecord
ms.date: 03/30/2017
ms.assetid: 99bc7f66-1335-40d8-aa68-e754d569dc0d
ms.openlocfilehash: 1136647ce668dbb69bdb8acf8ed62343831464b3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33487774"
---
# <a name="wsattracerecord"></a><span data-ttu-id="437eb-102">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="437eb-102">WSAT_TraceRecord</span></span>
<span data-ttu-id="437eb-103">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="437eb-103">WSAT_TraceRecord</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="437eb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="437eb-104">Syntax</span></span>  
  
```  
class WSAT_TraceRecord : WSAT_TraceEvent  
{  
  object ActivityID;  
  sint32 EventID;  
  string TraceRecord;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="437eb-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="437eb-105">Methods</span></span>  
 <span data-ttu-id="437eb-106">La classe WSAT_TraceRecord ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="437eb-106">The WSAT_TraceRecord class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="437eb-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="437eb-107">Properties</span></span>  
 <span data-ttu-id="437eb-108">La classe WSAT_TraceRecord a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="437eb-108">The WSAT_TraceRecord class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="437eb-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="437eb-109">ActivityID</span></span>  
 <span data-ttu-id="437eb-110">Type de données : objet</span><span class="sxs-lookup"><span data-stu-id="437eb-110">Data type: object</span></span>  
<span data-ttu-id="437eb-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="437eb-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="437eb-112">ID d'activité de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="437eb-112">The activity ID of the trace record.</span></span>  
  
### <a name="eventid"></a><span data-ttu-id="437eb-113">ID de l’événement</span><span class="sxs-lookup"><span data-stu-id="437eb-113">EventID</span></span>  
 <span data-ttu-id="437eb-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="437eb-114">Data type: sint32</span></span>  
<span data-ttu-id="437eb-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="437eb-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="437eb-116">ID d'événement de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="437eb-116">The event ID of the trace record.</span></span>  
  
### <a name="tracerecord"></a><span data-ttu-id="437eb-117">TraceRecord</span><span class="sxs-lookup"><span data-stu-id="437eb-117">TraceRecord</span></span>  
 <span data-ttu-id="437eb-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="437eb-118">Data type: string</span></span>  
<span data-ttu-id="437eb-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="437eb-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="437eb-120">Enregistrement de suivi</span><span class="sxs-lookup"><span data-stu-id="437eb-120">Trace Record</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="437eb-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="437eb-121">Requirements</span></span>  
  
|<span data-ttu-id="437eb-122">MOF</span><span class="sxs-lookup"><span data-stu-id="437eb-122">MOF</span></span>|<span data-ttu-id="437eb-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="437eb-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="437eb-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="437eb-124">Namespace</span></span>|<span data-ttu-id="437eb-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="437eb-125">Defined in root\ServiceModel</span></span>|
