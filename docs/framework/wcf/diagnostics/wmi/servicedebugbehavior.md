---
title: ServiceDebugBehavior
ms.date: 03/30/2017
ms.assetid: a5ec9061-1e95-43fb-b0d9-dbd0a7bc3c44
ms.openlocfilehash: 2e38eb2c2d42ffc5436562b254a42215ccabbab2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59090912"
---
# <a name="servicedebugbehavior"></a><span data-ttu-id="19de7-102">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="19de7-102">ServiceDebugBehavior</span></span>
<span data-ttu-id="19de7-103">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="19de7-103">ServiceDebugBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19de7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19de7-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="19de7-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19de7-105">Methods</span></span>  
 <span data-ttu-id="19de7-106">La classe ServiceDebugBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="19de7-106">The ServiceDebugBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="19de7-107">Properties</span><span class="sxs-lookup"><span data-stu-id="19de7-107">Properties</span></span>  
 <span data-ttu-id="19de7-108">La classe ServiceDebugBehavior possède les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="19de7-108">The ServiceDebugBehavior class has the following properties:</span></span>  
  
### <a name="httphelppageenabled"></a><span data-ttu-id="19de7-109">HttpHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="19de7-109">HttpHelpPageEnabled</span></span>  
 <span data-ttu-id="19de7-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="19de7-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="19de7-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="19de7-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="19de7-112">Vérifie si le service publie son WSDL à l'adresse contrôlée par l'attribut `HttpGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="19de7-112">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httphelppageurl"></a><span data-ttu-id="19de7-113">HttpHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="19de7-113">HttpHelpPageUrl</span></span>  
 <span data-ttu-id="19de7-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="19de7-114">Data type: string</span></span>  
  
 <span data-ttu-id="19de7-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="19de7-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="19de7-116">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTP.</span><span class="sxs-lookup"><span data-stu-id="19de7-116">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpshelppageenabled"></a><span data-ttu-id="19de7-117">HttpsHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="19de7-117">HttpsHelpPageEnabled</span></span>  
 <span data-ttu-id="19de7-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="19de7-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="19de7-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="19de7-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="19de7-120">Vérifie si le service publie son WSDL sur HTTPS à l'adresse contrôlée par l'attribut `HttpsGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="19de7-120">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpshelppageurl"></a><span data-ttu-id="19de7-121">HttpsHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="19de7-121">HttpsHelpPageUrl</span></span>  
 <span data-ttu-id="19de7-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="19de7-122">Data type: string</span></span>  
  
 <span data-ttu-id="19de7-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="19de7-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="19de7-124">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="19de7-124">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="19de7-125">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="19de7-125">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="19de7-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="19de7-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="19de7-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="19de7-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="19de7-128">Spécifie s'il convient d'inclure des informations d'exception gérées dans les détails des fautes SOAP renvoyées aux clients à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="19de7-128">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19de7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19de7-129">Requirements</span></span>  
  
|<span data-ttu-id="19de7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="19de7-130">MOF</span></span>|<span data-ttu-id="19de7-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="19de7-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="19de7-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="19de7-132">Namespace</span></span>|<span data-ttu-id="19de7-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="19de7-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="19de7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19de7-134">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceDebugBehavior>
