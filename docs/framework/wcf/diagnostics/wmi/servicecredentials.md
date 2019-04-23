---
title: ServiceCredentials
ms.date: 03/30/2017
ms.assetid: 9c780793-4785-46f7-add9-ac1ebeadb614
ms.openlocfilehash: d9563bd3bfe067ad83bfa03e7c6375a9db933f14
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59772100"
---
# <a name="servicecredentials"></a><span data-ttu-id="c732b-102">ServiceCredentials</span><span class="sxs-lookup"><span data-stu-id="c732b-102">ServiceCredentials</span></span>
<span data-ttu-id="c732b-103">ServiceCredentials</span><span class="sxs-lookup"><span data-stu-id="c732b-103">ServiceCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c732b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c732b-104">Syntax</span></span>  
  
```csharp
class ServiceCredentials : Behavior  
{  
  string ClientCertificate;  
  string IssuedTokenAuthentication;  
  string Peer;  
  string SecureConversationAuthentication;  
  string ServiceCertificate;  
  string UserNameAuthentication;  
  string WindowsAuthentication;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c732b-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c732b-105">Methods</span></span>  
 <span data-ttu-id="c732b-106">La classe ServiceCredentials ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="c732b-106">The ServiceCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c732b-107">Properties</span><span class="sxs-lookup"><span data-stu-id="c732b-107">Properties</span></span>  
 <span data-ttu-id="c732b-108">La classe ServiceCredentials a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="c732b-108">The ServiceCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="c732b-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c732b-109">ClientCertificate</span></span>  
 <span data-ttu-id="c732b-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c732b-110">Data type: string</span></span>  
  
 <span data-ttu-id="c732b-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c732b-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c732b-112">Paramètres d'authentification et d'approvisionnement des certificats clients pour ce service.</span><span class="sxs-lookup"><span data-stu-id="c732b-112">The client certificate authentication and provisioning settings for this service.</span></span>  
  
### <a name="issuedtokenauthentication"></a><span data-ttu-id="c732b-113">IssuedTokenAuthentication</span><span class="sxs-lookup"><span data-stu-id="c732b-113">IssuedTokenAuthentication</span></span>  
 <span data-ttu-id="c732b-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c732b-114">Data type: string</span></span>  
  
 <span data-ttu-id="c732b-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c732b-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c732b-116">Paramètres actuels d'authentification de jeton émis pour ce service.</span><span class="sxs-lookup"><span data-stu-id="c732b-116">The current issued token authentication settings for this service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="c732b-117">Peer</span><span class="sxs-lookup"><span data-stu-id="c732b-117">Peer</span></span>  
 <span data-ttu-id="c732b-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c732b-118">Data type: string</span></span>  
  
 <span data-ttu-id="c732b-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c732b-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c732b-120">Authentification des informations d'identification actuelles et fourniture des paramètres à utiliser par les points de terminaison de transport d'homologue.</span><span class="sxs-lookup"><span data-stu-id="c732b-120">The current credential authentication and provisioning settings to be used by peer transport endpoints.</span></span>  
  
### <a name="secureconversationauthentication"></a><span data-ttu-id="c732b-121">SecureConversationAuthentication</span><span class="sxs-lookup"><span data-stu-id="c732b-121">SecureConversationAuthentication</span></span>  
 <span data-ttu-id="c732b-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c732b-122">Data type: string</span></span>  
  
 <span data-ttu-id="c732b-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c732b-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c732b-124">Spécifie les paramètres actuels de conversation sécurisée.</span><span class="sxs-lookup"><span data-stu-id="c732b-124">Specifies the current secure conversation settings.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="c732b-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="c732b-125">ServiceCertificate</span></span>  
 <span data-ttu-id="c732b-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c732b-126">Data type: string</span></span>  
  
 <span data-ttu-id="c732b-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c732b-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c732b-128">Certificat associé à ce service.</span><span class="sxs-lookup"><span data-stu-id="c732b-128">The certificate associated with this service.</span></span>  
  
### <a name="usernameauthentication"></a><span data-ttu-id="c732b-129">UserNameAuthentication</span><span class="sxs-lookup"><span data-stu-id="c732b-129">UserNameAuthentication</span></span>  
 <span data-ttu-id="c732b-130">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c732b-130">Data type: string</span></span>  
  
 <span data-ttu-id="c732b-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c732b-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c732b-132">Paramètres de nom d'utilisateur/mot de passe pour ce service.</span><span class="sxs-lookup"><span data-stu-id="c732b-132">The username/password settings for this service.</span></span>  
  
### <a name="windowsauthentication"></a><span data-ttu-id="c732b-133">WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c732b-133">WindowsAuthentication</span></span>  
 <span data-ttu-id="c732b-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c732b-134">Data type: string</span></span>  
  
 <span data-ttu-id="c732b-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c732b-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c732b-136">Paramètres d'authentification Windows pour ce service.</span><span class="sxs-lookup"><span data-stu-id="c732b-136">The Windows authentication settings for this service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c732b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c732b-137">Requirements</span></span>  
  
|<span data-ttu-id="c732b-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c732b-138">MOF</span></span>|<span data-ttu-id="c732b-139">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="c732b-139">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c732b-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c732b-140">Namespace</span></span>|<span data-ttu-id="c732b-141">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c732b-141">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c732b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c732b-142">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceCredentials>
