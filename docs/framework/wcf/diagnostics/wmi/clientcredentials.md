---
title: ClientCredentials
ms.date: 03/30/2017
ms.assetid: 41dffd6b-8f14-4fed-aefb-2a1bb168efb3
ms.openlocfilehash: c3adc675bb6c1e9011459a88fd7dc8e8cf63a880
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59771203"
---
# <a name="clientcredentials"></a><span data-ttu-id="29388-102">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="29388-102">ClientCredentials</span></span>
<span data-ttu-id="29388-103">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="29388-103">ClientCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29388-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29388-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="29388-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="29388-105">Methods</span></span>  
 <span data-ttu-id="29388-106">La classe ClientCredentials ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="29388-106">The ClientCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="29388-107">Properties</span><span class="sxs-lookup"><span data-stu-id="29388-107">Properties</span></span>  
 <span data-ttu-id="29388-108">La classe ClientCredentials a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="29388-108">The ClientCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="29388-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="29388-109">ClientCertificate</span></span>  
 <span data-ttu-id="29388-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="29388-110">Data type: string</span></span>  
  
 <span data-ttu-id="29388-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="29388-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="29388-112">Certificat X.509 que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="29388-112">The X.509 certificate the client uses to authenticate to the service.</span></span>  
  
### <a name="httpdigest"></a><span data-ttu-id="29388-113">HttpDigest</span><span class="sxs-lookup"><span data-stu-id="29388-113">HttpDigest</span></span>  
 <span data-ttu-id="29388-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="29388-114">Data type: string</span></span>  
  
 <span data-ttu-id="29388-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="29388-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="29388-116">Informations d’identification HTTP Digest actuelles.</span><span class="sxs-lookup"><span data-stu-id="29388-116">The current Http Digest credential.</span></span>  
  
### <a name="issuedtoken"></a><span data-ttu-id="29388-117">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="29388-117">IssuedToken</span></span>  
 <span data-ttu-id="29388-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="29388-118">Data type: string</span></span>  
  
 <span data-ttu-id="29388-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="29388-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="29388-120">Adresse de point de terminaison et liaison utilisées pour contacter le service de jetons de sécurité local.</span><span class="sxs-lookup"><span data-stu-id="29388-120">The endpoint address and binding used to contact the local security token service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="29388-121">Peer</span><span class="sxs-lookup"><span data-stu-id="29388-121">Peer</span></span>  
 <span data-ttu-id="29388-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="29388-122">Data type: string</span></span>  
  
 <span data-ttu-id="29388-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="29388-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="29388-124">Informations d'identification que le nœud d'homologue utilise pour s'authentifier auprès d'autres nœuds dans la maille.</span><span class="sxs-lookup"><span data-stu-id="29388-124">The credentials that the peer node uses to authenticate itself to other nodes in the mesh.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="29388-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="29388-125">ServiceCertificate</span></span>  
 <span data-ttu-id="29388-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="29388-126">Data type: string</span></span>  
  
 <span data-ttu-id="29388-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="29388-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="29388-128">Certificat X.509 du service.</span><span class="sxs-lookup"><span data-stu-id="29388-128">The service's X.509 certificate.</span></span>  
  
### <a name="supportinteractive"></a><span data-ttu-id="29388-129">SupportInteractive</span><span class="sxs-lookup"><span data-stu-id="29388-129">SupportInteractive</span></span>  
 <span data-ttu-id="29388-130">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="29388-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="29388-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="29388-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="29388-132">Valeur booléenne qui spécifie si les informations d'identification prennent en charge la négociation interactive.</span><span class="sxs-lookup"><span data-stu-id="29388-132">A Boolean value that specifies whether the credential supports interactive negotiation.</span></span>  
  
### <a name="username"></a><span data-ttu-id="29388-133">UserName</span><span class="sxs-lookup"><span data-stu-id="29388-133">UserName</span></span>  
 <span data-ttu-id="29388-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="29388-134">Data type: string</span></span>  
  
 <span data-ttu-id="29388-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="29388-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="29388-136">Nom d'utilisateur et mot de passe que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="29388-136">The username and password the client uses to authenticate itself to the service.</span></span>  
  
### <a name="windows"></a><span data-ttu-id="29388-137">Windows</span><span class="sxs-lookup"><span data-stu-id="29388-137">Windows</span></span>  
 <span data-ttu-id="29388-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="29388-138">Data type: string</span></span>  
  
 <span data-ttu-id="29388-139">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="29388-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="29388-140">Informations d'identification que le client utilise pour s'authentifier auprès du service.</span><span class="sxs-lookup"><span data-stu-id="29388-140">The windows credentials the client uses to authenticate itself to the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="29388-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29388-141">Requirements</span></span>  
  
|<span data-ttu-id="29388-142">MOF</span><span class="sxs-lookup"><span data-stu-id="29388-142">MOF</span></span>|<span data-ttu-id="29388-143">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="29388-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="29388-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29388-144">Namespace</span></span>|<span data-ttu-id="29388-145">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="29388-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="29388-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29388-146">See also</span></span>

- <xref:System.ServiceModel.Description.ClientCredentials>
