---
title: ServiceMetadataBehavior
ms.date: 03/30/2017
ms.assetid: 0f194476-72f1-467e-bdce-674306316e64
ms.openlocfilehash: e96a732f8b3b4d78d597429905cc7dd290dcc606
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485998"
---
# <a name="servicemetadatabehavior"></a><span data-ttu-id="6970c-102">ServiceMetadataBehavior</span><span class="sxs-lookup"><span data-stu-id="6970c-102">ServiceMetadataBehavior</span></span>
<span data-ttu-id="6970c-103">ServiceMetadataBehavior</span><span class="sxs-lookup"><span data-stu-id="6970c-103">ServiceMetadataBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6970c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6970c-104">Syntax</span></span>  
  
```  
class ServiceMetadataBehavior : Behavior  
{  
  string ExternalMetadataLocation;  
  boolean HttpGetEnabled;  
  string HttpGetUrl;  
  boolean HttpsGetEnabled;  
  string HttpsGetUrl;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6970c-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6970c-105">Methods</span></span>  
 <span data-ttu-id="6970c-106">La classe ServiceMetadataBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="6970c-106">The ServiceMetadataBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="6970c-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6970c-107">Properties</span></span>  
 <span data-ttu-id="6970c-108">La classe ServiceMetadataBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="6970c-108">The ServiceMetadataBehavior class has the following properties:</span></span>  
  
### <a name="externalmetadatalocation"></a><span data-ttu-id="6970c-109">ExternalMetadataLocation</span><span class="sxs-lookup"><span data-stu-id="6970c-109">ExternalMetadataLocation</span></span>  
 <span data-ttu-id="6970c-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="6970c-110">Data type: string</span></span>  
  
 <span data-ttu-id="6970c-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="6970c-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6970c-112">Définit l'emplacement vers lequel le service redirige les demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="6970c-112">Sets the location to which the service redirects metadata requests.</span></span>  
  
### <a name="httpgetenabled"></a><span data-ttu-id="6970c-113">HttpGetEnabled</span><span class="sxs-lookup"><span data-stu-id="6970c-113">HttpGetEnabled</span></span>  
 <span data-ttu-id="6970c-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="6970c-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="6970c-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="6970c-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6970c-116">Vérifie si le service publie son WSDL à l'adresse contrôlée par l'attribut `HttpGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="6970c-116">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httpgeturl"></a><span data-ttu-id="6970c-117">HttpGetUrl</span><span class="sxs-lookup"><span data-stu-id="6970c-117">HttpGetUrl</span></span>  
 <span data-ttu-id="6970c-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="6970c-118">Data type: string</span></span>  
  
 <span data-ttu-id="6970c-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="6970c-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6970c-120">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTP.</span><span class="sxs-lookup"><span data-stu-id="6970c-120">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpsgetenabled"></a><span data-ttu-id="6970c-121">HttpsGetEnabled</span><span class="sxs-lookup"><span data-stu-id="6970c-121">HttpsGetEnabled</span></span>  
 <span data-ttu-id="6970c-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="6970c-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="6970c-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="6970c-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6970c-124">Vérifie si le service publie son WSDL sur HTTPS à l'adresse contrôlée par l'attribut `HttpsGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="6970c-124">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpsgeturl"></a><span data-ttu-id="6970c-125">HttpsGetUrl</span><span class="sxs-lookup"><span data-stu-id="6970c-125">HttpsGetUrl</span></span>  
 <span data-ttu-id="6970c-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="6970c-126">Data type: string</span></span>  
  
 <span data-ttu-id="6970c-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="6970c-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6970c-128">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6970c-128">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6970c-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6970c-129">Requirements</span></span>  
  
|<span data-ttu-id="6970c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6970c-130">MOF</span></span>|<span data-ttu-id="6970c-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="6970c-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="6970c-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6970c-132">Namespace</span></span>|<span data-ttu-id="6970c-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="6970c-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6970c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6970c-134">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceMetadataBehavior>
