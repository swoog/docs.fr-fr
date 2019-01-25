---
title: ServiceBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 5faa266f-587f-4e03-828d-1c7dd5acfe65
ms.openlocfilehash: 420686ebda7f23a5d883deece251b034147fafa4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654579"
---
# <a name="servicebehaviorattribute"></a><span data-ttu-id="3c3c4-102">ServiceBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="3c3c4-102">ServiceBehaviorAttribute</span></span>
<span data-ttu-id="3c3c4-103">ServiceBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="3c3c4-103">ServiceBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c3c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c3c4-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="3c3c4-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3c3c4-105">Methods</span></span>  
 <span data-ttu-id="3c3c4-106">La classe ServiceBehaviorAttribute ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-106">The ServiceBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3c3c4-107">Properties</span><span class="sxs-lookup"><span data-stu-id="3c3c4-107">Properties</span></span>  
 <span data-ttu-id="3c3c4-108">La classe ServiceBehaviorAttribute a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c3c4-108">The ServiceBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="automaticsessionshutdown"></a><span data-ttu-id="3c3c4-109">AutomaticSessionShutdown</span><span class="sxs-lookup"><span data-stu-id="3c3c4-109">AutomaticSessionShutdown</span></span>  
 <span data-ttu-id="3c3c4-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3c3c4-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="3c3c4-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-112">Indique s'il faut fermer automatiquement une session lorsqu'un client ferme une session de sortie.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-112">Indicates whether to automatically close a session when a client closes an output session.</span></span>  
  
### <a name="concurrencymode"></a><span data-ttu-id="3c3c4-113">ConcurrencyMode</span><span class="sxs-lookup"><span data-stu-id="3c3c4-113">ConcurrencyMode</span></span>  
 <span data-ttu-id="3c3c4-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c3c4-114">Data type: string</span></span>  
<span data-ttu-id="3c3c4-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-116">Indique si un service prend en charge un thread, plusieurs threads ou des appels réentrants.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-116">Indicates whether a service supports one thread, multiple threads, or reentrant calls.</span></span>  
  
### <a name="configurationname"></a><span data-ttu-id="3c3c4-117">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3c3c4-117">ConfigurationName</span></span>  
 <span data-ttu-id="3c3c4-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c3c4-118">Data type: string</span></span>  
  
 <span data-ttu-id="3c3c4-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-120">Nom de la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-120">The name of the service configuration.</span></span>  
  
### <a name="ignoreextensiondataobject"></a><span data-ttu-id="3c3c4-121">IgnoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="3c3c4-121">IgnoreExtensionDataObject</span></span>  
 <span data-ttu-id="3c3c4-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3c3c4-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="3c3c4-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-124">Spécifie s'il faut envoyer des données de sérialisation inconnues sur le câble.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-124">Specifies whether to send unknown serialization data onto the wire.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="3c3c4-125">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="3c3c4-125">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="3c3c4-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3c3c4-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="3c3c4-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-128">Spécifie s'il convient d'inclure des informations d'exception gérées dans les détails des fautes SOAP renvoyées aux clients à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-128">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
### <a name="instancecontextmode"></a><span data-ttu-id="3c3c4-129">InstanceContextMode</span><span class="sxs-lookup"><span data-stu-id="3c3c4-129">InstanceContextMode</span></span>  
 <span data-ttu-id="3c3c4-130">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c3c4-130">Data type: string</span></span>  
  
 <span data-ttu-id="3c3c4-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-132">Spécifie quand un nouvel objet de service est créé.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-132">Specifies when a new service object is created.</span></span>  
  
### <a name="maxitemsinobjectgraph"></a><span data-ttu-id="3c3c4-133">MaxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="3c3c4-133">MaxItemsInObjectGraph</span></span>  
 <span data-ttu-id="3c3c4-134">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="3c3c4-134">Data type: sint32</span></span>  
  
 <span data-ttu-id="3c3c4-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-136">Nombre maximal d'éléments autorisés dans un objet sérialisé.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-136">The maximum number of items allowed in a serialized object.</span></span>  
  
### <a name="name"></a><span data-ttu-id="3c3c4-137">Name</span><span class="sxs-lookup"><span data-stu-id="3c3c4-137">Name</span></span>  
 <span data-ttu-id="3c3c4-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c3c4-138">Data type: string</span></span>  
  
 <span data-ttu-id="3c3c4-139">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-140">Attribut de nom du service dans WSDL.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-140">The name attribute of the service in WSDL.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="3c3c4-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c3c4-141">Namespace</span></span>  
 <span data-ttu-id="3c3c4-142">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c3c4-142">Data type: string</span></span>  
  
 <span data-ttu-id="3c3c4-143">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-144">Espace de noms cible du service dans WSDL.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-144">The target namespace of the service in WSDL.</span></span>  
  
### <a name="releaseserviceinstanceontransactioncomplete"></a><span data-ttu-id="3c3c4-145">ReleaseServiceInstanceOnTransactionComplete</span><span class="sxs-lookup"><span data-stu-id="3c3c4-145">ReleaseServiceInstanceOnTransactionComplete</span></span>  
 <span data-ttu-id="3c3c4-146">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3c3c4-146">Data type: boolean</span></span>  
  
 <span data-ttu-id="3c3c4-147">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-148">Spécifie si l’objet de service est recyclé lorsque la transaction actuelle se termine.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-148">Specifies whether the service object is recycled when the current transaction completes.</span></span>  
  
### <a name="transactionautocompleteonsessionclose"></a><span data-ttu-id="3c3c4-149">TransactionAutoCompleteOnSessionClose</span><span class="sxs-lookup"><span data-stu-id="3c3c4-149">TransactionAutoCompleteOnSessionClose</span></span>  
 <span data-ttu-id="3c3c4-150">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3c3c4-150">Data type: boolean</span></span>  
  
 <span data-ttu-id="3c3c4-151">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-152">Spécifie si les transactions en attente sont complétées lorsque la session actuelle se ferme.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-152">Specifies whether pending transactions are completed when the current session closes.</span></span>  
  
### <a name="transactionisolationlevel"></a><span data-ttu-id="3c3c4-153">TransactionIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="3c3c4-153">TransactionIsolationLevel</span></span>  
 <span data-ttu-id="3c3c4-154">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c3c4-154">Data type: string</span></span>  
  
 <span data-ttu-id="3c3c4-155">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-156">Spécifie le niveau d’isolation de la transaction.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-156">Specifies the transaction isolation level.</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="3c3c4-157">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="3c3c4-157">TransactionTimeout</span></span>  
 <span data-ttu-id="3c3c4-158">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="3c3c4-158">Data type: datetime</span></span>  
  
 <span data-ttu-id="3c3c4-159">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-160">Période pendant laquelle une transaction doit s’effectuer.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-160">The period within which a transaction must complete.</span></span>  
  
### <a name="usesynchronizationcontext"></a><span data-ttu-id="3c3c4-161">UseSynchronizationContext</span><span class="sxs-lookup"><span data-stu-id="3c3c4-161">UseSynchronizationContext</span></span>  
 <span data-ttu-id="3c3c4-162">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3c3c4-162">Data type: boolean</span></span>  
  
 <span data-ttu-id="3c3c4-163">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-163">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-164">Spécifie s’il faut utiliser le contexte de synchronisation actuel pour choisir l’exécution d’un thread.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-164">Specifies whether to use the current synchronization context to choose the thread execution.</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="3c3c4-165">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="3c3c4-165">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="3c3c4-166">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3c3c4-166">Data type: boolean</span></span>  
  
 <span data-ttu-id="3c3c4-167">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c3c4-167">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c3c4-168">Spécifie si le système ou l'application applique le traitement d'en-tête SOAP MustUnderstand.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-168">Specifies whether the system or the application enforces SOAP MustUnderstand header processing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c3c4-169">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3c3c4-169">Requirements</span></span>  
  
|<span data-ttu-id="3c3c4-170">MOF</span><span class="sxs-lookup"><span data-stu-id="3c3c4-170">MOF</span></span>|<span data-ttu-id="3c3c4-171">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-171">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3c3c4-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c3c4-172">Namespace</span></span>|<span data-ttu-id="3c3c4-173">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="3c3c4-173">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3c3c4-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c3c4-174">See also</span></span>
- <xref:System.ServiceModel.ServiceBehaviorAttribute>
