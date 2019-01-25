---
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: d0bf59e6064748a045f761777a2f8f3e88f1cb5a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504325"
---
# <a name="operationbehaviorattribute"></a><span data-ttu-id="93cca-102">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="93cca-102">OperationBehaviorAttribute</span></span>
<span data-ttu-id="93cca-103">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="93cca-103">OperationBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93cca-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93cca-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="93cca-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="93cca-105">Methods</span></span>  
 <span data-ttu-id="93cca-106">La classe OperationBehaviorAttribute ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="93cca-106">The OperationBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="93cca-107">Properties</span><span class="sxs-lookup"><span data-stu-id="93cca-107">Properties</span></span>  
 <span data-ttu-id="93cca-108">La classe OperationBehaviorAttribute a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="93cca-108">The OperationBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="autodisposeparameters"></a><span data-ttu-id="93cca-109">AutoDisposeParameters</span><span class="sxs-lookup"><span data-stu-id="93cca-109">AutoDisposeParameters</span></span>  
 <span data-ttu-id="93cca-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="93cca-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="93cca-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="93cca-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="93cca-112">État de la fonctionnalité d’élimination automatique pour les paramètres.</span><span class="sxs-lookup"><span data-stu-id="93cca-112">The state of the auto-dispose feature for parameters.</span></span>  
  
### <a name="impersonation"></a><span data-ttu-id="93cca-113">Emprunt d'identité</span><span class="sxs-lookup"><span data-stu-id="93cca-113">Impersonation</span></span>  
 <span data-ttu-id="93cca-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="93cca-114">Data type: string</span></span>  
  
 <span data-ttu-id="93cca-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="93cca-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="93cca-116">Indique le niveau d'emprunt d'identité de l'appelant pris en charge par l'opération.</span><span class="sxs-lookup"><span data-stu-id="93cca-116">Indicates the level of caller impersonation that the operation supports.</span></span>  
  
### <a name="releaseinstancemode"></a><span data-ttu-id="93cca-117">ReleaseInstanceMode</span><span class="sxs-lookup"><span data-stu-id="93cca-117">ReleaseInstanceMode</span></span>  
 <span data-ttu-id="93cca-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="93cca-118">Data type: string</span></span>  
  
 <span data-ttu-id="93cca-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="93cca-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="93cca-120">Indique à quel moment il convient de recycler l'objet lors de l'appel d'une opération.</span><span class="sxs-lookup"><span data-stu-id="93cca-120">Indicates when in the course of an operation invocation to recycle the object.</span></span>  
  
### <a name="transactionautocomplete"></a><span data-ttu-id="93cca-121">TransactionAutoComplete</span><span class="sxs-lookup"><span data-stu-id="93cca-121">TransactionAutoComplete</span></span>  
 <span data-ttu-id="93cca-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="93cca-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="93cca-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="93cca-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="93cca-124">Indique s’il convient de valider automatiquement la transaction actuelle si aucune exception non traitée ne se produit.</span><span class="sxs-lookup"><span data-stu-id="93cca-124">Indicates whether to automatically commit the current transaction if no unhandled exceptions occur.</span></span>  
  
### <a name="transactionscoperequired"></a><span data-ttu-id="93cca-125">TransactionScopeRequired</span><span class="sxs-lookup"><span data-stu-id="93cca-125">TransactionScopeRequired</span></span>  
 <span data-ttu-id="93cca-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="93cca-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="93cca-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="93cca-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="93cca-128">Indique si l’opération nécessite une transaction.</span><span class="sxs-lookup"><span data-stu-id="93cca-128">Indicates whether the operation requires a transaction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="93cca-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="93cca-129">Requirements</span></span>  
  
|<span data-ttu-id="93cca-130">MOF</span><span class="sxs-lookup"><span data-stu-id="93cca-130">MOF</span></span>|<span data-ttu-id="93cca-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="93cca-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="93cca-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="93cca-132">Namespace</span></span>|<span data-ttu-id="93cca-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="93cca-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="93cca-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93cca-134">See also</span></span>
- <xref:System.ServiceModel.OperationBehaviorAttribute>
