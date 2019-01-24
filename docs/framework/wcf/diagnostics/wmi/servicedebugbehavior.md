---
title: ServiceDebugBehavior
ms.date: 03/30/2017
ms.assetid: a5ec9061-1e95-43fb-b0d9-dbd0a7bc3c44
ms.openlocfilehash: d6f0e4741aa10bff450a29cfd7a9e63e226c6495
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498880"
---
# <a name="servicedebugbehavior"></a><span data-ttu-id="3f83a-102">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="3f83a-102">ServiceDebugBehavior</span></span>
<span data-ttu-id="3f83a-103">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="3f83a-103">ServiceDebugBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f83a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f83a-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="3f83a-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f83a-105">Methods</span></span>  
 <span data-ttu-id="3f83a-106">La classe ServiceDebugBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="3f83a-106">The ServiceDebugBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3f83a-107">Properties</span><span class="sxs-lookup"><span data-stu-id="3f83a-107">Properties</span></span>  
 <span data-ttu-id="3f83a-108">La classe ServiceDebugBehavior possède les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f83a-108">The ServiceDebugBehavior class has the following properties:</span></span>  
  
### <a name="httphelppageenabled"></a><span data-ttu-id="3f83a-109">HttpHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="3f83a-109">HttpHelpPageEnabled</span></span>  
 <span data-ttu-id="3f83a-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3f83a-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="3f83a-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f83a-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3f83a-112">Vérifie si le service publie son WSDL à l'adresse contrôlée par l'attribut `HttpGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="3f83a-112">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httphelppageurl"></a><span data-ttu-id="3f83a-113">HttpHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="3f83a-113">HttpHelpPageUrl</span></span>  
 <span data-ttu-id="3f83a-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3f83a-114">Data type: string</span></span>  
  
 <span data-ttu-id="3f83a-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f83a-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3f83a-116">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTP.</span><span class="sxs-lookup"><span data-stu-id="3f83a-116">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpshelppageenabled"></a><span data-ttu-id="3f83a-117">HttpsHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="3f83a-117">HttpsHelpPageEnabled</span></span>  
 <span data-ttu-id="3f83a-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3f83a-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="3f83a-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f83a-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3f83a-120">Vérifie si le service publie son WSDL sur HTTPS à l'adresse contrôlée par l'attribut `HttpsGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="3f83a-120">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpshelppageurl"></a><span data-ttu-id="3f83a-121">HttpsHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="3f83a-121">HttpsHelpPageUrl</span></span>  
 <span data-ttu-id="3f83a-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3f83a-122">Data type: string</span></span>  
  
 <span data-ttu-id="3f83a-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f83a-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3f83a-124">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3f83a-124">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="3f83a-125">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="3f83a-125">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="3f83a-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3f83a-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="3f83a-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f83a-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3f83a-128">Spécifie s'il convient d'inclure des informations d'exception gérées dans les détails des fautes SOAP renvoyées aux clients à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="3f83a-128">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f83a-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f83a-129">Requirements</span></span>  
  
|<span data-ttu-id="3f83a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3f83a-130">MOF</span></span>|<span data-ttu-id="3f83a-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="3f83a-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3f83a-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3f83a-132">Namespace</span></span>|<span data-ttu-id="3f83a-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="3f83a-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3f83a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f83a-134">See also</span></span>
- <xref:System.ServiceModel.Description.ServiceDebugBehavior>
