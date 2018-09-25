---
title: ServiceSecurityAuditBehavior
ms.date: 03/30/2017
ms.assetid: 2c5809e7-5364-44ce-bc71-848be4672e2a
author: BrucePerlerMS
ms.openlocfilehash: 8f43ee752830d95db6bbbdbe311b6d77735e31b5
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47070147"
---
# <a name="servicesecurityauditbehavior"></a><span data-ttu-id="3c7cb-102">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="3c7cb-102">ServiceSecurityAuditBehavior</span></span>
<span data-ttu-id="3c7cb-103">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="3c7cb-103">ServiceSecurityAuditBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c7cb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c7cb-104">Syntax</span></span>  
  
```  
class ServiceSecurityAuditBehavior : Behavior  
{  
  string AuditLogLocation;  
  string MessageAuthenticationAuditLevel;  
  string ServiceAuthorizationAuditLevel;  
  boolean SuppressAuditFailure;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3c7cb-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3c7cb-105">Methods</span></span>  
 <span data-ttu-id="3c7cb-106">La classe ServiceSecurityAuditBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-106">The ServiceSecurityAuditBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3c7cb-107">Properties</span><span class="sxs-lookup"><span data-stu-id="3c7cb-107">Properties</span></span>  
 <span data-ttu-id="3c7cb-108">La classe ServiceSecurityAuditBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c7cb-108">The ServiceSecurityAuditBehavior class has the following properties:</span></span>  
  
### <a name="auditloglocation"></a><span data-ttu-id="3c7cb-109">AuditLogLocation</span><span class="sxs-lookup"><span data-stu-id="3c7cb-109">AuditLogLocation</span></span>  
 <span data-ttu-id="3c7cb-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c7cb-110">Data type: string</span></span>  
  
 <span data-ttu-id="3c7cb-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c7cb-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c7cb-112">Emplacement du journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-112">The location of the audit log.</span></span>  
  
### <a name="messageauthenticationauditlevel"></a><span data-ttu-id="3c7cb-113">MessageAuthenticationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="3c7cb-113">MessageAuthenticationAuditLevel</span></span>  
 <span data-ttu-id="3c7cb-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c7cb-114">Data type: string</span></span>  
  
 <span data-ttu-id="3c7cb-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c7cb-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c7cb-116">Type de niveau d'authentification de message utilisé pour enregistrer des événements d'audit.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-116">The type of message authentication level that is used to log audit events.</span></span>  
  
### <a name="serviceauthorizationauditlevel"></a><span data-ttu-id="3c7cb-117">ServiceAuthorizationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="3c7cb-117">ServiceAuthorizationAuditLevel</span></span>  
 <span data-ttu-id="3c7cb-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3c7cb-118">Data type: string</span></span>  
  
 <span data-ttu-id="3c7cb-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c7cb-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c7cb-120">Types d'événement d'autorisation enregistrés dans le journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-120">The types of authorization events that are recorded in the audit log.</span></span>  
  
### <a name="suppressauditfailure"></a><span data-ttu-id="3c7cb-121">SuppressAuditFailure</span><span class="sxs-lookup"><span data-stu-id="3c7cb-121">SuppressAuditFailure</span></span>  
 <span data-ttu-id="3c7cb-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3c7cb-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="3c7cb-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c7cb-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3c7cb-124">Valeur booléenne qui spécifie le comportement permettant de supprimer les erreurs d'écriture dans le journal d'audit.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-124">A boolean value that specifies the behavior for suppressing failures of writing to the audit log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c7cb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c7cb-125">Requirements</span></span>  
  
|<span data-ttu-id="3c7cb-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3c7cb-126">MOF</span></span>|<span data-ttu-id="3c7cb-127">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3c7cb-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c7cb-128">Namespace</span></span>|<span data-ttu-id="3c7cb-129">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="3c7cb-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3c7cb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c7cb-130">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior>
