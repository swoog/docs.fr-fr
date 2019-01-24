---
title: ServiceSecurityAuditBehavior
ms.date: 03/30/2017
ms.assetid: 2c5809e7-5364-44ce-bc71-848be4672e2a
ms.openlocfilehash: dc48b8742c60714720be3cf4b22ba672f73c720a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54570224"
---
# <a name="servicesecurityauditbehavior"></a><span data-ttu-id="16d97-102">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="16d97-102">ServiceSecurityAuditBehavior</span></span>
<span data-ttu-id="16d97-103">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="16d97-103">ServiceSecurityAuditBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16d97-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16d97-104">Syntax</span></span>  
  
```csharp  
class ServiceSecurityAuditBehavior : Behavior  
{  
  string AuditLogLocation;  
  string MessageAuthenticationAuditLevel;  
  string ServiceAuthorizationAuditLevel;  
  boolean SuppressAuditFailure;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="16d97-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="16d97-105">Methods</span></span>  
 <span data-ttu-id="16d97-106">La classe ServiceSecurityAuditBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="16d97-106">The ServiceSecurityAuditBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="16d97-107">Properties</span><span class="sxs-lookup"><span data-stu-id="16d97-107">Properties</span></span>  
 <span data-ttu-id="16d97-108">La classe ServiceSecurityAuditBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="16d97-108">The ServiceSecurityAuditBehavior class has the following properties:</span></span>  
  
### <a name="auditloglocation"></a><span data-ttu-id="16d97-109">AuditLogLocation</span><span class="sxs-lookup"><span data-stu-id="16d97-109">AuditLogLocation</span></span>  
 <span data-ttu-id="16d97-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="16d97-110">Data type: string</span></span>  
  
 <span data-ttu-id="16d97-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="16d97-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="16d97-112">Emplacement du journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="16d97-112">The location of the audit log.</span></span>  
  
### <a name="messageauthenticationauditlevel"></a><span data-ttu-id="16d97-113">MessageAuthenticationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="16d97-113">MessageAuthenticationAuditLevel</span></span>  
 <span data-ttu-id="16d97-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="16d97-114">Data type: string</span></span>  
  
 <span data-ttu-id="16d97-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="16d97-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="16d97-116">Type de niveau d'authentification de message utilisé pour enregistrer des événements d'audit.</span><span class="sxs-lookup"><span data-stu-id="16d97-116">The type of message authentication level that is used to log audit events.</span></span>  
  
### <a name="serviceauthorizationauditlevel"></a><span data-ttu-id="16d97-117">ServiceAuthorizationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="16d97-117">ServiceAuthorizationAuditLevel</span></span>  
 <span data-ttu-id="16d97-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="16d97-118">Data type: string</span></span>  
  
 <span data-ttu-id="16d97-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="16d97-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="16d97-120">Types d'événement d'autorisation enregistrés dans le journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="16d97-120">The types of authorization events that are recorded in the audit log.</span></span>  
  
### <a name="suppressauditfailure"></a><span data-ttu-id="16d97-121">SuppressAuditFailure</span><span class="sxs-lookup"><span data-stu-id="16d97-121">SuppressAuditFailure</span></span>  
 <span data-ttu-id="16d97-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="16d97-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="16d97-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="16d97-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="16d97-124">Valeur booléenne qui spécifie le comportement permettant de supprimer les erreurs d'écriture dans le journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="16d97-124">A boolean value that specifies the behavior for suppressing failures of writing to the audit log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="16d97-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="16d97-125">Requirements</span></span>  
  
|<span data-ttu-id="16d97-126">MOF</span><span class="sxs-lookup"><span data-stu-id="16d97-126">MOF</span></span>|<span data-ttu-id="16d97-127">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="16d97-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="16d97-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="16d97-128">Namespace</span></span>|<span data-ttu-id="16d97-129">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="16d97-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="16d97-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16d97-130">See also</span></span>
- <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior>
