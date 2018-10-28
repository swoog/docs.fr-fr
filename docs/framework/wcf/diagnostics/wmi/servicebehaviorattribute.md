---
title: ServiceBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 5faa266f-587f-4e03-828d-1c7dd5acfe65
ms.openlocfilehash: c2915c636aec26cfb1f58d12da49151915c52c05
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50182955"
---
# <a name="servicebehaviorattribute"></a><span data-ttu-id="8925b-102">ServiceBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="8925b-102">ServiceBehaviorAttribute</span></span>
<span data-ttu-id="8925b-103">ServiceBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="8925b-103">ServiceBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8925b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8925b-104">Syntax</span></span>  
  
```csharp
class ServiceBehaviorAttribute : Behavior  
{  
  boolean AutomaticSessionShutdown;  
  string ConcurrencyMode;  
  string ConfigurationName;  
  boolean IgnoreExtensionDataObject;  
  boolean IncludeExceptionDetailInFaults;  
  string InstanceContextMode;  
  sint32 MaxItemsInObjectGraph;  
  string Name;  
  string Namespace;  
  boolean ReleaseServiceInstanceOnTransactionComplete;  
  boolean TransactionAutoCompleteOnSessionClose;  
  string TransactionIsolationLevel;  
  datetime TransactionTimeout;  
  boolean UseSynchronizationContext;  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="8925b-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8925b-105">Methods</span></span>  
 <span data-ttu-id="8925b-106">La classe ServiceBehaviorAttribute ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="8925b-106">The ServiceBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="8925b-107">Properties</span><span class="sxs-lookup"><span data-stu-id="8925b-107">Properties</span></span>  
 <span data-ttu-id="8925b-108">La classe ServiceBehaviorAttribute a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="8925b-108">The ServiceBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="automaticsessionshutdown"></a><span data-ttu-id="8925b-109">AutomaticSessionShutdown</span><span class="sxs-lookup"><span data-stu-id="8925b-109">AutomaticSessionShutdown</span></span>  
 <span data-ttu-id="8925b-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="8925b-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="8925b-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-112">Indique s'il faut fermer automatiquement une session lorsqu'un client ferme une session de sortie.</span><span class="sxs-lookup"><span data-stu-id="8925b-112">Indicates whether to automatically close a session when a client closes an output session.</span></span>  
  
### <a name="concurrencymode"></a><span data-ttu-id="8925b-113">ConcurrencyMode</span><span class="sxs-lookup"><span data-stu-id="8925b-113">ConcurrencyMode</span></span>  
 <span data-ttu-id="8925b-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="8925b-114">Data type: string</span></span>  
<span data-ttu-id="8925b-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-116">Indique si un service prend en charge un thread, plusieurs threads ou des appels réentrants.</span><span class="sxs-lookup"><span data-stu-id="8925b-116">Indicates whether a service supports one thread, multiple threads, or reentrant calls.</span></span>  
  
### <a name="configurationname"></a><span data-ttu-id="8925b-117">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8925b-117">ConfigurationName</span></span>  
 <span data-ttu-id="8925b-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="8925b-118">Data type: string</span></span>  
  
 <span data-ttu-id="8925b-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-120">Nom de la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="8925b-120">The name of the service configuration.</span></span>  
  
### <a name="ignoreextensiondataobject"></a><span data-ttu-id="8925b-121">IgnoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="8925b-121">IgnoreExtensionDataObject</span></span>  
 <span data-ttu-id="8925b-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="8925b-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="8925b-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-124">Spécifie s'il faut envoyer des données de sérialisation inconnues sur le câble.</span><span class="sxs-lookup"><span data-stu-id="8925b-124">Specifies whether to send unknown serialization data onto the wire.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="8925b-125">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="8925b-125">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="8925b-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="8925b-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="8925b-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-128">Spécifie s'il convient d'inclure des informations d'exception gérées dans les détails des fautes SOAP renvoyées aux clients à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="8925b-128">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
### <a name="instancecontextmode"></a><span data-ttu-id="8925b-129">InstanceContextMode</span><span class="sxs-lookup"><span data-stu-id="8925b-129">InstanceContextMode</span></span>  
 <span data-ttu-id="8925b-130">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="8925b-130">Data type: string</span></span>  
  
 <span data-ttu-id="8925b-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-132">Spécifie quand un nouvel objet de service est créé.</span><span class="sxs-lookup"><span data-stu-id="8925b-132">Specifies when a new service object is created.</span></span>  
  
### <a name="maxitemsinobjectgraph"></a><span data-ttu-id="8925b-133">MaxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="8925b-133">MaxItemsInObjectGraph</span></span>  
 <span data-ttu-id="8925b-134">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="8925b-134">Data type: sint32</span></span>  
  
 <span data-ttu-id="8925b-135">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-136">Nombre maximal d'éléments autorisés dans un objet sérialisé.</span><span class="sxs-lookup"><span data-stu-id="8925b-136">The maximum number of items allowed in a serialized object.</span></span>  
  
### <a name="name"></a><span data-ttu-id="8925b-137">Name</span><span class="sxs-lookup"><span data-stu-id="8925b-137">Name</span></span>  
 <span data-ttu-id="8925b-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="8925b-138">Data type: string</span></span>  
  
 <span data-ttu-id="8925b-139">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-140">Attribut de nom du service dans WSDL.</span><span class="sxs-lookup"><span data-stu-id="8925b-140">The name attribute of the service in WSDL.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="8925b-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8925b-141">Namespace</span></span>  
 <span data-ttu-id="8925b-142">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="8925b-142">Data type: string</span></span>  
  
 <span data-ttu-id="8925b-143">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-144">Espace de noms cible du service dans WSDL.</span><span class="sxs-lookup"><span data-stu-id="8925b-144">The target namespace of the service in WSDL.</span></span>  
  
### <a name="releaseserviceinstanceontransactioncomplete"></a><span data-ttu-id="8925b-145">ReleaseServiceInstanceOnTransactionComplete</span><span class="sxs-lookup"><span data-stu-id="8925b-145">ReleaseServiceInstanceOnTransactionComplete</span></span>  
 <span data-ttu-id="8925b-146">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="8925b-146">Data type: boolean</span></span>  
  
 <span data-ttu-id="8925b-147">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-148">Spécifie si l'objet de service est recyclé lorsque la transaction actuelle se termine.</span><span class="sxs-lookup"><span data-stu-id="8925b-148">Specifies whether the service object is recycled when the current transaction completes.</span></span>  
  
### <a name="transactionautocompleteonsessionclose"></a><span data-ttu-id="8925b-149">TransactionAutoCompleteOnSessionClose</span><span class="sxs-lookup"><span data-stu-id="8925b-149">TransactionAutoCompleteOnSessionClose</span></span>  
 <span data-ttu-id="8925b-150">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="8925b-150">Data type: boolean</span></span>  
  
 <span data-ttu-id="8925b-151">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-152">Spécifie si les transactions en attente sont complétées lorsque la session actuelle se ferme.</span><span class="sxs-lookup"><span data-stu-id="8925b-152">Specifies whether pending transactions are completed when the current session closes.</span></span>  
  
### <a name="transactionisolationlevel"></a><span data-ttu-id="8925b-153">TransactionIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="8925b-153">TransactionIsolationLevel</span></span>  
 <span data-ttu-id="8925b-154">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="8925b-154">Data type: string</span></span>  
  
 <span data-ttu-id="8925b-155">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-156">Spécifie le niveau d'isolation de la transaction.</span><span class="sxs-lookup"><span data-stu-id="8925b-156">Specifies the transaction isolation level.</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="8925b-157">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="8925b-157">TransactionTimeout</span></span>  
 <span data-ttu-id="8925b-158">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="8925b-158">Data type: datetime</span></span>  
  
 <span data-ttu-id="8925b-159">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-160">Période pendant laquelle une transaction doit s’effectuer.</span><span class="sxs-lookup"><span data-stu-id="8925b-160">The period within which a transaction must complete.</span></span>  
  
### <a name="usesynchronizationcontext"></a><span data-ttu-id="8925b-161">UseSynchronizationContext</span><span class="sxs-lookup"><span data-stu-id="8925b-161">UseSynchronizationContext</span></span>  
 <span data-ttu-id="8925b-162">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="8925b-162">Data type: boolean</span></span>  
  
 <span data-ttu-id="8925b-163">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-163">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-164">Spécifie s'il faut utiliser le contexte de synchronisation actuel pour choisir l'exécution d'un thread.</span><span class="sxs-lookup"><span data-stu-id="8925b-164">Specifies whether to use the current synchronization context to choose the thread execution.</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="8925b-165">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="8925b-165">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="8925b-166">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="8925b-166">Data type: boolean</span></span>  
  
 <span data-ttu-id="8925b-167">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="8925b-167">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8925b-168">Spécifie si le système ou l'application applique le traitement d'en-tête SOAP MustUnderstand.</span><span class="sxs-lookup"><span data-stu-id="8925b-168">Specifies whether the system or the application enforces SOAP MustUnderstand header processing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8925b-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8925b-169">Requirements</span></span>  
  
|<span data-ttu-id="8925b-170">MOF</span><span class="sxs-lookup"><span data-stu-id="8925b-170">MOF</span></span>|<span data-ttu-id="8925b-171">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="8925b-171">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="8925b-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8925b-172">Namespace</span></span>|<span data-ttu-id="8925b-173">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="8925b-173">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8925b-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8925b-174">See Also</span></span>  
 <xref:System.ServiceModel.ServiceBehaviorAttribute>
