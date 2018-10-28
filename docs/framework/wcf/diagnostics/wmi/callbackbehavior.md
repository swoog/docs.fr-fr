---
title: CallbackBehavior
ms.date: 03/30/2017
ms.assetid: 42acd302-2b62-4849-a2d1-a03084343ecd
ms.openlocfilehash: 38a38a71db2927d187ccdd93e5e364b0d4955373
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452610"
---
# <a name="callbackbehavior"></a><span data-ttu-id="4ca0f-102">CallbackBehavior</span><span class="sxs-lookup"><span data-stu-id="4ca0f-102">CallbackBehavior</span></span>
<span data-ttu-id="4ca0f-103">CallbackBehavior</span><span class="sxs-lookup"><span data-stu-id="4ca0f-103">CallbackBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ca0f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ca0f-104">Syntax</span></span>  
  
```csharp
class CallbackBehavior : Behavior  
{  
  boolean AutomaticSessionShutdown;  
  string ConcurrencyMode;  
  boolean IgnoreExtensionDataObject;  
  boolean IncludeExceptionDetailInFaults;  
  boolean MaxItemsInObjectGraph;  
  boolean UseSynchronizationContext;  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="4ca0f-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4ca0f-105">Methods</span></span>  
 <span data-ttu-id="4ca0f-106">La classe CallbackBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-106">The CallbackBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="4ca0f-107">Properties</span><span class="sxs-lookup"><span data-stu-id="4ca0f-107">Properties</span></span>  
 <span data-ttu-id="4ca0f-108">La classe CallbackBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ca0f-108">The CallbackBehavior class has the following properties:</span></span>  
  
### <a name="automaticsessionshutdown"></a><span data-ttu-id="4ca0f-109">AutomaticSessionShutdown</span><span class="sxs-lookup"><span data-stu-id="4ca0f-109">AutomaticSessionShutdown</span></span>  
 <span data-ttu-id="4ca0f-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="4ca0f-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="4ca0f-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ca0f-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ca0f-112">Lorsque sa valeur est « true », la session est fermée automatiquement lorsqu'un service ferme une session duplex.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-112">When true, the session is automatically closed when a service closes a duplex session.</span></span>  
  
### <a name="concurrencymode"></a><span data-ttu-id="4ca0f-113">ConcurrencyMode</span><span class="sxs-lookup"><span data-stu-id="4ca0f-113">ConcurrencyMode</span></span>  
 <span data-ttu-id="4ca0f-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="4ca0f-114">Data type: string</span></span>  
<span data-ttu-id="4ca0f-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ca0f-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ca0f-116">Spécifie si le service prend en charge un thread, plusieurs threads ou les appels réentrants.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-116">Specifies whether the service supports one thread, multiple threads, or reentrant calls.</span></span>  
  
### <a name="ignoreextensiondataobject"></a><span data-ttu-id="4ca0f-117">IgnoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="4ca0f-117">IgnoreExtensionDataObject</span></span>  
 <span data-ttu-id="4ca0f-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="4ca0f-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="4ca0f-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ca0f-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ca0f-120">Valeur qui spécifie s'il faut envoyer des données de sérialisation inconnues sur le câble.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-120">A value that specifies whether to send unknown serialization data onto the wire.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="4ca0f-121">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="4ca0f-121">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="4ca0f-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="4ca0f-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="4ca0f-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ca0f-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ca0f-124">En cas d'activation, des détails au sujet des exceptions levées sur le rappel sont joints aux erreurs retournées au service.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-124">When enabled, details about exceptions on the callback are attached to the faults returned to the service.</span></span>  
  
### <a name="maxitemsinobjectgraph"></a><span data-ttu-id="4ca0f-125">MaxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="4ca0f-125">MaxItemsInObjectGraph</span></span>  
 <span data-ttu-id="4ca0f-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="4ca0f-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="4ca0f-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ca0f-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ca0f-128">Nombre maximal d'éléments autorisés dans un objet sérialisé.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-128">The maximum number of items allowed in a serialized object.</span></span>  
  
### <a name="usesynchronizationcontext"></a><span data-ttu-id="4ca0f-129">UseSynchronizationContext</span><span class="sxs-lookup"><span data-stu-id="4ca0f-129">UseSynchronizationContext</span></span>  
 <span data-ttu-id="4ca0f-130">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="4ca0f-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="4ca0f-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ca0f-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ca0f-132">Spécifie s’il faut utiliser le contexte de synchronisation actuel pour choisir le thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-132">Specifies whether to use the current synchronization context to choose the thread of execution.</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="4ca0f-133">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="4ca0f-133">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="4ca0f-134">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="4ca0f-134">Data type: boolean</span></span>  
  
 <span data-ttu-id="4ca0f-135">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ca0f-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ca0f-136">Spécifie si le système ou l'application applique le traitement d'en-tête SOAP MustUnderstand.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-136">Specifies whether the system or the application enforces SOAP MustUnderstand header processing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4ca0f-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ca0f-137">Requirements</span></span>  
  
|<span data-ttu-id="4ca0f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4ca0f-138">MOF</span></span>|<span data-ttu-id="4ca0f-139">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="4ca0f-139">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="4ca0f-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4ca0f-140">Namespace</span></span>|<span data-ttu-id="4ca0f-141">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="4ca0f-141">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4ca0f-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ca0f-142">See Also</span></span>  
 <xref:System.ServiceModel.CallbackBehaviorAttribute>
