---
title: WSAT_TraceRecord
ms.date: 03/30/2017
ms.assetid: 99bc7f66-1335-40d8-aa68-e754d569dc0d
ms.openlocfilehash: 907e764cf032e595c7aba455fd4808a640f68016
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49373994"
---
# <a name="wsattracerecord"></a><span data-ttu-id="65a35-102">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="65a35-102">WSAT_TraceRecord</span></span>
<span data-ttu-id="65a35-103">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="65a35-103">WSAT_TraceRecord</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65a35-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65a35-104">Syntax</span></span>  
  
```csharp
class WSAT_TraceRecord : WSAT_TraceEvent  
{  
  object ActivityID;  
  sint32 EventID;  
  string TraceRecord;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="65a35-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="65a35-105">Methods</span></span>  
 <span data-ttu-id="65a35-106">La classe WSAT_TraceRecord ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="65a35-106">The WSAT_TraceRecord class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="65a35-107">Properties</span><span class="sxs-lookup"><span data-stu-id="65a35-107">Properties</span></span>  
 <span data-ttu-id="65a35-108">La classe WSAT_TraceRecord a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="65a35-108">The WSAT_TraceRecord class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="65a35-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="65a35-109">ActivityID</span></span>  
 <span data-ttu-id="65a35-110">Type de données : objet</span><span class="sxs-lookup"><span data-stu-id="65a35-110">Data type: object</span></span>  
<span data-ttu-id="65a35-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="65a35-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="65a35-112">ID d'activité de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="65a35-112">The activity ID of the trace record.</span></span>  
  
### <a name="eventid"></a><span data-ttu-id="65a35-113">ID de l’événement</span><span class="sxs-lookup"><span data-stu-id="65a35-113">EventID</span></span>  
 <span data-ttu-id="65a35-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="65a35-114">Data type: sint32</span></span>  
<span data-ttu-id="65a35-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="65a35-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="65a35-116">ID d'événement de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="65a35-116">The event ID of the trace record.</span></span>  
  
### <a name="tracerecord"></a><span data-ttu-id="65a35-117">TraceRecord</span><span class="sxs-lookup"><span data-stu-id="65a35-117">TraceRecord</span></span>  
 <span data-ttu-id="65a35-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="65a35-118">Data type: string</span></span>  
<span data-ttu-id="65a35-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="65a35-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="65a35-120">Enregistrement de suivi</span><span class="sxs-lookup"><span data-stu-id="65a35-120">Trace Record</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65a35-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65a35-121">Requirements</span></span>  
  
|<span data-ttu-id="65a35-122">MOF</span><span class="sxs-lookup"><span data-stu-id="65a35-122">MOF</span></span>|<span data-ttu-id="65a35-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="65a35-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="65a35-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="65a35-124">Namespace</span></span>|<span data-ttu-id="65a35-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="65a35-125">Defined in root\ServiceModel</span></span>|
