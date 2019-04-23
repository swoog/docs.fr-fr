---
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: 79601308c66abe43dd5a7f72bd2a05b9d2346c2b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59975154"
---
# <a name="operationbehaviorattribute"></a><span data-ttu-id="e2149-102">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="e2149-102">OperationBehaviorAttribute</span></span>
<span data-ttu-id="e2149-103">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="e2149-103">OperationBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2149-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2149-104">Syntax</span></span>  
  
```csharp
class OperationBehaviorAttribute : Behavior  
{  
  boolean AutoDisposeParameters;  
  string Impersonation;  
  string ReleaseInstanceMode;  
  boolean TransactionAutoComplete;  
  boolean TransactionScopeRequired;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="e2149-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e2149-105">Methods</span></span>  
 <span data-ttu-id="e2149-106">La classe OperationBehaviorAttribute ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="e2149-106">The OperationBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="e2149-107">Properties</span><span class="sxs-lookup"><span data-stu-id="e2149-107">Properties</span></span>  
 <span data-ttu-id="e2149-108">La classe OperationBehaviorAttribute a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2149-108">The OperationBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="autodisposeparameters"></a><span data-ttu-id="e2149-109">AutoDisposeParameters</span><span class="sxs-lookup"><span data-stu-id="e2149-109">AutoDisposeParameters</span></span>  
 <span data-ttu-id="e2149-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="e2149-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="e2149-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2149-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e2149-112">État de la fonctionnalité d’élimination automatique pour les paramètres.</span><span class="sxs-lookup"><span data-stu-id="e2149-112">The state of the auto-dispose feature for parameters.</span></span>  
  
### <a name="impersonation"></a><span data-ttu-id="e2149-113">Emprunt d'identité</span><span class="sxs-lookup"><span data-stu-id="e2149-113">Impersonation</span></span>  
 <span data-ttu-id="e2149-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="e2149-114">Data type: string</span></span>  
  
 <span data-ttu-id="e2149-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2149-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e2149-116">Indique le niveau d'emprunt d'identité de l'appelant pris en charge par l'opération.</span><span class="sxs-lookup"><span data-stu-id="e2149-116">Indicates the level of caller impersonation that the operation supports.</span></span>  
  
### <a name="releaseinstancemode"></a><span data-ttu-id="e2149-117">ReleaseInstanceMode</span><span class="sxs-lookup"><span data-stu-id="e2149-117">ReleaseInstanceMode</span></span>  
 <span data-ttu-id="e2149-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="e2149-118">Data type: string</span></span>  
  
 <span data-ttu-id="e2149-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2149-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e2149-120">Indique à quel moment il convient de recycler l'objet lors de l'appel d'une opération.</span><span class="sxs-lookup"><span data-stu-id="e2149-120">Indicates when in the course of an operation invocation to recycle the object.</span></span>  
  
### <a name="transactionautocomplete"></a><span data-ttu-id="e2149-121">TransactionAutoComplete</span><span class="sxs-lookup"><span data-stu-id="e2149-121">TransactionAutoComplete</span></span>  
 <span data-ttu-id="e2149-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="e2149-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="e2149-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2149-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e2149-124">Indique s’il convient de valider automatiquement la transaction actuelle si aucune exception non traitée ne se produit.</span><span class="sxs-lookup"><span data-stu-id="e2149-124">Indicates whether to automatically commit the current transaction if no unhandled exceptions occur.</span></span>  
  
### <a name="transactionscoperequired"></a><span data-ttu-id="e2149-125">TransactionScopeRequired</span><span class="sxs-lookup"><span data-stu-id="e2149-125">TransactionScopeRequired</span></span>  
 <span data-ttu-id="e2149-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="e2149-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="e2149-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2149-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e2149-128">Indique si l’opération nécessite une transaction.</span><span class="sxs-lookup"><span data-stu-id="e2149-128">Indicates whether the operation requires a transaction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e2149-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2149-129">Requirements</span></span>  
  
|<span data-ttu-id="e2149-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e2149-130">MOF</span></span>|<span data-ttu-id="e2149-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="e2149-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="e2149-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e2149-132">Namespace</span></span>|<span data-ttu-id="e2149-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="e2149-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e2149-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2149-134">See also</span></span>

- <xref:System.ServiceModel.OperationBehaviorAttribute>
