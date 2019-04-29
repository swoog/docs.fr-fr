---
title: WSAT_TraceRecord
ms.date: 03/30/2017
ms.assetid: 99bc7f66-1335-40d8-aa68-e754d569dc0d
ms.openlocfilehash: 907e764cf032e595c7aba455fd4808a640f68016
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61923407"
---
# <a name="wsattracerecord"></a><span data-ttu-id="f45f2-102">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="f45f2-102">WSAT_TraceRecord</span></span>
<span data-ttu-id="f45f2-103">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="f45f2-103">WSAT_TraceRecord</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f45f2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f45f2-104">Syntax</span></span>  
  
```csharp
class WSAT_TraceRecord : WSAT_TraceEvent  
{  
  object ActivityID;  
  sint32 EventID;  
  string TraceRecord;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f45f2-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f45f2-105">Methods</span></span>  
 <span data-ttu-id="f45f2-106">La classe WSAT_TraceRecord ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="f45f2-106">The WSAT_TraceRecord class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f45f2-107">Properties</span><span class="sxs-lookup"><span data-stu-id="f45f2-107">Properties</span></span>  
 <span data-ttu-id="f45f2-108">La classe WSAT_TraceRecord a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f45f2-108">The WSAT_TraceRecord class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="f45f2-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="f45f2-109">ActivityID</span></span>  
 <span data-ttu-id="f45f2-110">Type de données : objet</span><span class="sxs-lookup"><span data-stu-id="f45f2-110">Data type: object</span></span>  
<span data-ttu-id="f45f2-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f45f2-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f45f2-112">ID d'activité de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="f45f2-112">The activity ID of the trace record.</span></span>  
  
### <a name="eventid"></a><span data-ttu-id="f45f2-113">ID de l’événement</span><span class="sxs-lookup"><span data-stu-id="f45f2-113">EventID</span></span>  
 <span data-ttu-id="f45f2-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="f45f2-114">Data type: sint32</span></span>  
<span data-ttu-id="f45f2-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f45f2-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f45f2-116">ID d'événement de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="f45f2-116">The event ID of the trace record.</span></span>  
  
### <a name="tracerecord"></a><span data-ttu-id="f45f2-117">TraceRecord</span><span class="sxs-lookup"><span data-stu-id="f45f2-117">TraceRecord</span></span>  
 <span data-ttu-id="f45f2-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f45f2-118">Data type: string</span></span>  
<span data-ttu-id="f45f2-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f45f2-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f45f2-120">Enregistrement de suivi</span><span class="sxs-lookup"><span data-stu-id="f45f2-120">Trace Record</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f45f2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f45f2-121">Requirements</span></span>  
  
|<span data-ttu-id="f45f2-122">MOF</span><span class="sxs-lookup"><span data-stu-id="f45f2-122">MOF</span></span>|<span data-ttu-id="f45f2-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="f45f2-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f45f2-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f45f2-124">Namespace</span></span>|<span data-ttu-id="f45f2-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f45f2-125">Defined in root\ServiceModel</span></span>|
