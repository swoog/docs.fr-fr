---
title: ServiceAuthorizationBehavior
ms.date: 03/30/2017
ms.assetid: 77dad8e8-fea4-4d1c-b366-2f01a2a87f78
ms.openlocfilehash: 51555e3357b8c33a53261c4894d97798b0a05656
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59102932"
---
# <a name="serviceauthorizationbehavior"></a><span data-ttu-id="30084-102">ServiceAuthorizationBehavior</span><span class="sxs-lookup"><span data-stu-id="30084-102">ServiceAuthorizationBehavior</span></span>
<span data-ttu-id="30084-103">ServiceAuthorizationBehavior</span><span class="sxs-lookup"><span data-stu-id="30084-103">ServiceAuthorizationBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30084-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30084-104">Syntax</span></span>  
  
```csharp
class ServiceAuthorizationBehavior : Behavior  
{  
  boolean ImpersonateCallerForAllOperations;  
  string PrincipalPermissionMode;  
  string RoleProvider;  
  string ServiceAuthorizationManager;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="30084-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="30084-105">Methods</span></span>  
 <span data-ttu-id="30084-106">La classe ServiceAuthorizationBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="30084-106">The ServiceAuthorizationBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="30084-107">Properties</span><span class="sxs-lookup"><span data-stu-id="30084-107">Properties</span></span>  
 <span data-ttu-id="30084-108">La classe ServiceAuthorizationBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="30084-108">The ServiceAuthorizationBehavior class has the following properties:</span></span>  
  
### <a name="impersonatecallerforalloperations"></a><span data-ttu-id="30084-109">ImpersonateCallerForAllOperations</span><span class="sxs-lookup"><span data-stu-id="30084-109">ImpersonateCallerForAllOperations</span></span>  
 <span data-ttu-id="30084-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="30084-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="30084-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="30084-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="30084-112">Valeur qui contrôle si le service essaie d'emprunter l'identité à l'aide des informations d'identification fournies par le message entrant.</span><span class="sxs-lookup"><span data-stu-id="30084-112">A value that controls whether the service attempts to impersonate using the credentials provided by the incoming message.</span></span>  
  
### <a name="principalpermissionmode"></a><span data-ttu-id="30084-113">PrincipalPermissionMode</span><span class="sxs-lookup"><span data-stu-id="30084-113">PrincipalPermissionMode</span></span>  
 <span data-ttu-id="30084-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="30084-114">Data type: string</span></span>  
  
 <span data-ttu-id="30084-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="30084-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="30084-116">Principal de sécurité utilisée pour effectuer les opérations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="30084-116">The principal used to carry out operations on the server.</span></span>  
  
### <a name="roleprovider"></a><span data-ttu-id="30084-117">RoleProvider</span><span class="sxs-lookup"><span data-stu-id="30084-117">RoleProvider</span></span>  
 <span data-ttu-id="30084-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="30084-118">Data type: string</span></span>  
  
 <span data-ttu-id="30084-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="30084-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="30084-120">Nom du fournisseur de rôles ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="30084-120">The name of the ASP.NET role provider.</span></span>  
  
### <a name="serviceauthorizationmanager"></a><span data-ttu-id="30084-121">ServiceAuthorizationManager</span><span class="sxs-lookup"><span data-stu-id="30084-121">ServiceAuthorizationManager</span></span>  
 <span data-ttu-id="30084-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="30084-122">Data type: string</span></span>  
  
 <span data-ttu-id="30084-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="30084-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="30084-124">Gestionnaire d'autorisations utilisé pour l'autorisation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="30084-124">The authorization manager used for custom authorization.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30084-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30084-125">Requirements</span></span>  
  
|<span data-ttu-id="30084-126">MOF</span><span class="sxs-lookup"><span data-stu-id="30084-126">MOF</span></span>|<span data-ttu-id="30084-127">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="30084-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="30084-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="30084-128">Namespace</span></span>|<span data-ttu-id="30084-129">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="30084-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="30084-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30084-130">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>
