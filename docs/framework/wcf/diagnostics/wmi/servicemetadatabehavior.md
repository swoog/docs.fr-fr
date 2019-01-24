---
title: ServiceMetadataBehavior
ms.date: 03/30/2017
ms.assetid: 0f194476-72f1-467e-bdce-674306316e64
ms.openlocfilehash: 76e28b18cd595a4a18f573dfe9539b646196c944
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720338"
---
# <a name="servicemetadatabehavior"></a><span data-ttu-id="c8363-102">ServiceMetadataBehavior</span><span class="sxs-lookup"><span data-stu-id="c8363-102">ServiceMetadataBehavior</span></span>
<span data-ttu-id="c8363-103">ServiceMetadataBehavior</span><span class="sxs-lookup"><span data-stu-id="c8363-103">ServiceMetadataBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8363-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8363-104">Syntax</span></span>  
  
```csharp
class ServiceMetadataBehavior : Behavior  
{  
  string ExternalMetadataLocation;  
  boolean HttpGetEnabled;  
  string HttpGetUrl;  
  boolean HttpsGetEnabled;  
  string HttpsGetUrl;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c8363-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c8363-105">Methods</span></span>  
 <span data-ttu-id="c8363-106">La classe ServiceMetadataBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="c8363-106">The ServiceMetadataBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c8363-107">Properties</span><span class="sxs-lookup"><span data-stu-id="c8363-107">Properties</span></span>  
 <span data-ttu-id="c8363-108">La classe ServiceMetadataBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8363-108">The ServiceMetadataBehavior class has the following properties:</span></span>  
  
### <a name="externalmetadatalocation"></a><span data-ttu-id="c8363-109">ExternalMetadataLocation</span><span class="sxs-lookup"><span data-stu-id="c8363-109">ExternalMetadataLocation</span></span>  
 <span data-ttu-id="c8363-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c8363-110">Data type: string</span></span>  
  
 <span data-ttu-id="c8363-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8363-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8363-112">Définit l'emplacement vers lequel le service redirige les demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c8363-112">Sets the location to which the service redirects metadata requests.</span></span>  
  
### <a name="httpgetenabled"></a><span data-ttu-id="c8363-113">HttpGetEnabled</span><span class="sxs-lookup"><span data-stu-id="c8363-113">HttpGetEnabled</span></span>  
 <span data-ttu-id="c8363-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="c8363-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="c8363-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8363-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8363-116">Vérifie si le service publie son WSDL à l'adresse contrôlée par l'attribut `HttpGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="c8363-116">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httpgeturl"></a><span data-ttu-id="c8363-117">HttpGetUrl</span><span class="sxs-lookup"><span data-stu-id="c8363-117">HttpGetUrl</span></span>  
 <span data-ttu-id="c8363-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c8363-118">Data type: string</span></span>  
  
 <span data-ttu-id="c8363-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8363-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8363-120">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTP.</span><span class="sxs-lookup"><span data-stu-id="c8363-120">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpsgetenabled"></a><span data-ttu-id="c8363-121">HttpsGetEnabled</span><span class="sxs-lookup"><span data-stu-id="c8363-121">HttpsGetEnabled</span></span>  
 <span data-ttu-id="c8363-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="c8363-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="c8363-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8363-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8363-124">Vérifie si le service publie son WSDL sur HTTPS à l'adresse contrôlée par l'attribut `HttpsGetUrl`.</span><span class="sxs-lookup"><span data-stu-id="c8363-124">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpsgeturl"></a><span data-ttu-id="c8363-125">HttpsGetUrl</span><span class="sxs-lookup"><span data-stu-id="c8363-125">HttpsGetUrl</span></span>  
 <span data-ttu-id="c8363-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c8363-126">Data type: string</span></span>  
  
 <span data-ttu-id="c8363-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8363-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8363-128">Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c8363-128">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c8363-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c8363-129">Requirements</span></span>  
  
|<span data-ttu-id="c8363-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c8363-130">MOF</span></span>|<span data-ttu-id="c8363-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="c8363-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c8363-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8363-132">Namespace</span></span>|<span data-ttu-id="c8363-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c8363-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c8363-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8363-134">See also</span></span>
- <xref:System.ServiceModel.Description.ServiceMetadataBehavior>
