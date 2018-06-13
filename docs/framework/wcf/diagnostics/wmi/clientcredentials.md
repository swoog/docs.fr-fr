---
title: ClientCredentials
ms.date: 03/30/2017
ms.assetid: 41dffd6b-8f14-4fed-aefb-2a1bb168efb3
ms.openlocfilehash: aa852ff82c44a3b5009dbc70e1067face44cbbe9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33486374"
---
# <a name="clientcredentials"></a><span data-ttu-id="fb7b9-102">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="fb7b9-102">ClientCredentials</span></span>
<span data-ttu-id="fb7b9-103">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="fb7b9-103">ClientCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb7b9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb7b9-104">Syntax</span></span>  
  
```  
class ClientCredentials : Behavior  
{  
  string ClientCertificate;  
  string HttpDigest;  
  string IssuedToken;  
  string Peer;  
  string ServiceCertificate;  
  boolean SupportInteractive;  
  string UserName;  
  string Windows;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="fb7b9-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fb7b9-105">Methods</span></span>  
 <span data-ttu-id="fb7b9-106">La classe ClientCredentials ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-106">The ClientCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="fb7b9-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb7b9-107">Properties</span></span>  
 <span data-ttu-id="fb7b9-108">La classe ClientCredentials a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb7b9-108">The ClientCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="fb7b9-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fb7b9-109">ClientCertificate</span></span>  
 <span data-ttu-id="fb7b9-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fb7b9-110">Data type: string</span></span>  
  
 <span data-ttu-id="fb7b9-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb7b9-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fb7b9-112">Certificat X.509 que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-112">The X.509 certificate the client uses to authenticate to the service.</span></span>  
  
### <a name="httpdigest"></a><span data-ttu-id="fb7b9-113">HttpDigest</span><span class="sxs-lookup"><span data-stu-id="fb7b9-113">HttpDigest</span></span>  
 <span data-ttu-id="fb7b9-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fb7b9-114">Data type: string</span></span>  
  
 <span data-ttu-id="fb7b9-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb7b9-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fb7b9-116">Informations d'identification Http Digest actuelles.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-116">The current Http Digest credential.</span></span>  
  
### <a name="issuedtoken"></a><span data-ttu-id="fb7b9-117">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="fb7b9-117">IssuedToken</span></span>  
 <span data-ttu-id="fb7b9-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fb7b9-118">Data type: string</span></span>  
  
 <span data-ttu-id="fb7b9-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb7b9-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fb7b9-120">Adresse de point de terminaison et liaison utilisées pour contacter le service de jetons de sécurité local.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-120">The endpoint address and binding used to contact the local security token service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="fb7b9-121">Peer</span><span class="sxs-lookup"><span data-stu-id="fb7b9-121">Peer</span></span>  
 <span data-ttu-id="fb7b9-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fb7b9-122">Data type: string</span></span>  
  
 <span data-ttu-id="fb7b9-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb7b9-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fb7b9-124">Informations d'identification que le nœud d'homologue utilise pour s'authentifier auprès d'autres nœuds dans la maille.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-124">The credentials that the peer node uses to authenticate itself to other nodes in the mesh.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="fb7b9-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="fb7b9-125">ServiceCertificate</span></span>  
 <span data-ttu-id="fb7b9-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fb7b9-126">Data type: string</span></span>  
  
 <span data-ttu-id="fb7b9-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb7b9-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fb7b9-128">Certificat X.509 du service.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-128">The service's X.509 certificate.</span></span>  
  
### <a name="supportinteractive"></a><span data-ttu-id="fb7b9-129">SupportInteractive</span><span class="sxs-lookup"><span data-stu-id="fb7b9-129">SupportInteractive</span></span>  
 <span data-ttu-id="fb7b9-130">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="fb7b9-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="fb7b9-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb7b9-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fb7b9-132">Valeur booléenne qui spécifie si les informations d'identification prennent en charge la négociation interactive.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-132">A Boolean value that specifies whether the credential supports interactive negotiation.</span></span>  
  
### <a name="username"></a><span data-ttu-id="fb7b9-133">UserName</span><span class="sxs-lookup"><span data-stu-id="fb7b9-133">UserName</span></span>  
 <span data-ttu-id="fb7b9-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fb7b9-134">Data type: string</span></span>  
  
 <span data-ttu-id="fb7b9-135">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb7b9-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fb7b9-136">Nom d'utilisateur et mot de passe que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-136">The username and password the client uses to authenticate itself to the service.</span></span>  
  
### <a name="windows"></a><span data-ttu-id="fb7b9-137">Windows</span><span class="sxs-lookup"><span data-stu-id="fb7b9-137">Windows</span></span>  
 <span data-ttu-id="fb7b9-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fb7b9-138">Data type: string</span></span>  
  
 <span data-ttu-id="fb7b9-139">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb7b9-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fb7b9-140">Informations d'identification que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-140">The windows credentials the client uses to authenticate itself to the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fb7b9-141">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fb7b9-141">Requirements</span></span>  
  
|<span data-ttu-id="fb7b9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fb7b9-142">MOF</span></span>|<span data-ttu-id="fb7b9-143">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="fb7b9-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="fb7b9-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fb7b9-144">Namespace</span></span>|<span data-ttu-id="fb7b9-145">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="fb7b9-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fb7b9-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb7b9-146">See Also</span></span>  
 <xref:System.ServiceModel.Description.ClientCredentials>
