---
title: ServiceSecurityAuditBehavior
ms.date: 03/30/2017
ms.assetid: 2c5809e7-5364-44ce-bc71-848be4672e2a
ms.openlocfilehash: 30679e1f67c6943bf674a6bbd8bf12be090765a8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59203507"
---
# <a name="servicesecurityauditbehavior"></a><span data-ttu-id="b3358-102">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="b3358-102">ServiceSecurityAuditBehavior</span></span>
<span data-ttu-id="b3358-103">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="b3358-103">ServiceSecurityAuditBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3358-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3358-104">Syntax</span></span>  
  
```csharp  
class ServiceSecurityAuditBehavior : Behavior  
{  
  string AuditLogLocation;  
  string MessageAuthenticationAuditLevel;  
  string ServiceAuthorizationAuditLevel;  
  boolean SuppressAuditFailure;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b3358-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b3358-105">Methods</span></span>  
 <span data-ttu-id="b3358-106">La classe ServiceSecurityAuditBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="b3358-106">The ServiceSecurityAuditBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b3358-107">Properties</span><span class="sxs-lookup"><span data-stu-id="b3358-107">Properties</span></span>  
 <span data-ttu-id="b3358-108">La classe ServiceSecurityAuditBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3358-108">The ServiceSecurityAuditBehavior class has the following properties:</span></span>  
  
### <a name="auditloglocation"></a><span data-ttu-id="b3358-109">AuditLogLocation</span><span class="sxs-lookup"><span data-stu-id="b3358-109">AuditLogLocation</span></span>  
 <span data-ttu-id="b3358-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="b3358-110">Data type: string</span></span>  
  
 <span data-ttu-id="b3358-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3358-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b3358-112">Emplacement du journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="b3358-112">The location of the audit log.</span></span>  
  
### <a name="messageauthenticationauditlevel"></a><span data-ttu-id="b3358-113">MessageAuthenticationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="b3358-113">MessageAuthenticationAuditLevel</span></span>  
 <span data-ttu-id="b3358-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="b3358-114">Data type: string</span></span>  
  
 <span data-ttu-id="b3358-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3358-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b3358-116">Type de niveau d'authentification de message utilisé pour enregistrer des événements d'audit.</span><span class="sxs-lookup"><span data-stu-id="b3358-116">The type of message authentication level that is used to log audit events.</span></span>  
  
### <a name="serviceauthorizationauditlevel"></a><span data-ttu-id="b3358-117">ServiceAuthorizationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="b3358-117">ServiceAuthorizationAuditLevel</span></span>  
 <span data-ttu-id="b3358-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="b3358-118">Data type: string</span></span>  
  
 <span data-ttu-id="b3358-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3358-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b3358-120">Types d'événement d'autorisation enregistrés dans le journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="b3358-120">The types of authorization events that are recorded in the audit log.</span></span>  
  
### <a name="suppressauditfailure"></a><span data-ttu-id="b3358-121">SuppressAuditFailure</span><span class="sxs-lookup"><span data-stu-id="b3358-121">SuppressAuditFailure</span></span>  
 <span data-ttu-id="b3358-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="b3358-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="b3358-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3358-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b3358-124">Valeur booléenne qui spécifie le comportement permettant de supprimer les erreurs d'écriture dans le journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="b3358-124">A boolean value that specifies the behavior for suppressing failures of writing to the audit log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3358-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3358-125">Requirements</span></span>  
  
|<span data-ttu-id="b3358-126">MOF</span><span class="sxs-lookup"><span data-stu-id="b3358-126">MOF</span></span>|<span data-ttu-id="b3358-127">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="b3358-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b3358-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b3358-128">Namespace</span></span>|<span data-ttu-id="b3358-129">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="b3358-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b3358-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3358-130">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior>
