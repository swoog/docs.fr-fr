---
title: ClientCredentials
ms.date: 03/30/2017
ms.assetid: 41dffd6b-8f14-4fed-aefb-2a1bb168efb3
ms.openlocfilehash: c3adc675bb6c1e9011459a88fd7dc8e8cf63a880
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61963971"
---
# <a name="clientcredentials"></a><span data-ttu-id="7b941-102">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="7b941-102">ClientCredentials</span></span>
<span data-ttu-id="7b941-103">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="7b941-103">ClientCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b941-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b941-104">Syntax</span></span>  
  
```csharp
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
  
## <a name="methods"></a><span data-ttu-id="7b941-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7b941-105">Methods</span></span>  
 <span data-ttu-id="7b941-106">La classe ClientCredentials ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="7b941-106">The ClientCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="7b941-107">Properties</span><span class="sxs-lookup"><span data-stu-id="7b941-107">Properties</span></span>  
 <span data-ttu-id="7b941-108">La classe ClientCredentials a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b941-108">The ClientCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="7b941-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7b941-109">ClientCertificate</span></span>  
 <span data-ttu-id="7b941-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="7b941-110">Data type: string</span></span>  
  
 <span data-ttu-id="7b941-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b941-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7b941-112">Certificat X.509 que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="7b941-112">The X.509 certificate the client uses to authenticate to the service.</span></span>  
  
### <a name="httpdigest"></a><span data-ttu-id="7b941-113">HttpDigest</span><span class="sxs-lookup"><span data-stu-id="7b941-113">HttpDigest</span></span>  
 <span data-ttu-id="7b941-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="7b941-114">Data type: string</span></span>  
  
 <span data-ttu-id="7b941-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b941-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7b941-116">Informations d’identification HTTP Digest actuelles.</span><span class="sxs-lookup"><span data-stu-id="7b941-116">The current Http Digest credential.</span></span>  
  
### <a name="issuedtoken"></a><span data-ttu-id="7b941-117">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="7b941-117">IssuedToken</span></span>  
 <span data-ttu-id="7b941-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="7b941-118">Data type: string</span></span>  
  
 <span data-ttu-id="7b941-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b941-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7b941-120">Adresse de point de terminaison et liaison utilisées pour contacter le service de jetons de sécurité local.</span><span class="sxs-lookup"><span data-stu-id="7b941-120">The endpoint address and binding used to contact the local security token service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="7b941-121">Peer</span><span class="sxs-lookup"><span data-stu-id="7b941-121">Peer</span></span>  
 <span data-ttu-id="7b941-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="7b941-122">Data type: string</span></span>  
  
 <span data-ttu-id="7b941-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b941-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7b941-124">Informations d'identification que le nœud d'homologue utilise pour s'authentifier auprès d'autres nœuds dans la maille.</span><span class="sxs-lookup"><span data-stu-id="7b941-124">The credentials that the peer node uses to authenticate itself to other nodes in the mesh.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="7b941-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="7b941-125">ServiceCertificate</span></span>  
 <span data-ttu-id="7b941-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="7b941-126">Data type: string</span></span>  
  
 <span data-ttu-id="7b941-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b941-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7b941-128">Certificat X.509 du service.</span><span class="sxs-lookup"><span data-stu-id="7b941-128">The service's X.509 certificate.</span></span>  
  
### <a name="supportinteractive"></a><span data-ttu-id="7b941-129">SupportInteractive</span><span class="sxs-lookup"><span data-stu-id="7b941-129">SupportInteractive</span></span>  
 <span data-ttu-id="7b941-130">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="7b941-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="7b941-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b941-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7b941-132">Valeur booléenne qui spécifie si les informations d'identification prennent en charge la négociation interactive.</span><span class="sxs-lookup"><span data-stu-id="7b941-132">A Boolean value that specifies whether the credential supports interactive negotiation.</span></span>  
  
### <a name="username"></a><span data-ttu-id="7b941-133">UserName</span><span class="sxs-lookup"><span data-stu-id="7b941-133">UserName</span></span>  
 <span data-ttu-id="7b941-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="7b941-134">Data type: string</span></span>  
  
 <span data-ttu-id="7b941-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b941-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7b941-136">Nom d'utilisateur et mot de passe que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="7b941-136">The username and password the client uses to authenticate itself to the service.</span></span>  
  
### <a name="windows"></a><span data-ttu-id="7b941-137">Windows</span><span class="sxs-lookup"><span data-stu-id="7b941-137">Windows</span></span>  
 <span data-ttu-id="7b941-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="7b941-138">Data type: string</span></span>  
  
 <span data-ttu-id="7b941-139">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b941-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7b941-140">Informations d'identification que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="7b941-140">The windows credentials the client uses to authenticate itself to the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b941-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b941-141">Requirements</span></span>  
  
|<span data-ttu-id="7b941-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7b941-142">MOF</span></span>|<span data-ttu-id="7b941-143">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="7b941-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="7b941-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7b941-144">Namespace</span></span>|<span data-ttu-id="7b941-145">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="7b941-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7b941-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b941-146">See also</span></span>

- <xref:System.ServiceModel.Description.ClientCredentials>
