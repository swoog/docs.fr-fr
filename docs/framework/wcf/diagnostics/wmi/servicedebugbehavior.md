---
title: ServiceDebugBehavior
ms.date: 03/30/2017
ms.assetid: a5ec9061-1e95-43fb-b0d9-dbd0a7bc3c44
ms.openlocfilehash: 68b2350f257bc95d8e17f4b9049d67c7f67becae
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452860"
---
# <a name="servicedebugbehavior"></a><span data-ttu-id="047d4-102">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="047d4-102">ServiceDebugBehavior</span></span>
<span data-ttu-id="047d4-103">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="047d4-103">ServiceDebugBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="047d4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="047d4-104">Syntax</span></span>  
  
```csharp
class ServiceDebugBehavior : Behavior  
{  
  boolean HttpHelpPageEnabled;  
  string HttpHelpPageUrl;  
  boolean HttpsHelpPageEnabled;  
  string HttpsHelpPageUrl;  
  boolean IncludeExceptionDetailInFaults;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="047d4-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="047d4-105">Methods</span></span>  
 <span data-ttu-id="047d4-106">La classe ServiceDebugBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="047d4-106">The ServiceDebugBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="047d4-107">Properties</span><span class="sxs-lookup"><span data-stu-id="047d4-107">Properties</span></span>  
 <span data-ttu-id="047d4-108">La classe ServiceDebugBehavior possède les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="047d4-108">The ServiceDebugBehavior class has the following properties:</span></span>  
  
### <a name="httphelppageenabled"></a><span data-ttu-id="047d4-109">HttpHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="047d4-109">HttpHelpPageEnabled</span></span>  
 <span data-ttu-id="047d4-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="047d4-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="047d4-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="047d4-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="047d4-112">Vérifie si le service publie son WSDL à l'adresse contrôlée par l'attribut `HttpGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="047d4-112">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httphelppageurl"></a><span data-ttu-id="047d4-113">HttpHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="047d4-113">HttpHelpPageUrl</span></span>  
 <span data-ttu-id="047d4-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="047d4-114">Data type: string</span></span>  
  
 <span data-ttu-id="047d4-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="047d4-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="047d4-116">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTP.</span><span class="sxs-lookup"><span data-stu-id="047d4-116">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpshelppageenabled"></a><span data-ttu-id="047d4-117">HttpsHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="047d4-117">HttpsHelpPageEnabled</span></span>  
 <span data-ttu-id="047d4-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="047d4-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="047d4-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="047d4-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="047d4-120">Vérifie si le service publie son WSDL sur HTTPS à l'adresse contrôlée par l'attribut `HttpsGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="047d4-120">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpshelppageurl"></a><span data-ttu-id="047d4-121">HttpsHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="047d4-121">HttpsHelpPageUrl</span></span>  
 <span data-ttu-id="047d4-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="047d4-122">Data type: string</span></span>  
  
 <span data-ttu-id="047d4-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="047d4-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="047d4-124">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="047d4-124">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="047d4-125">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="047d4-125">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="047d4-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="047d4-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="047d4-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="047d4-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="047d4-128">Spécifie s'il convient d'inclure des informations d'exception gérées dans les détails des fautes SOAP renvoyées aux clients à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="047d4-128">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="047d4-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="047d4-129">Requirements</span></span>  
  
|<span data-ttu-id="047d4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="047d4-130">MOF</span></span>|<span data-ttu-id="047d4-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="047d4-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="047d4-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="047d4-132">Namespace</span></span>|<span data-ttu-id="047d4-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="047d4-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="047d4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="047d4-134">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceDebugBehavior>
