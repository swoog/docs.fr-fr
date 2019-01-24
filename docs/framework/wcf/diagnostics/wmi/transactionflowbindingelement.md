---
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: d0311837ebb8112d9492fb548492bcd3e10230e7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54514568"
---
# <a name="transactionflowbindingelement"></a><span data-ttu-id="e1626-102">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="e1626-102">TransactionFlowBindingElement</span></span>
<span data-ttu-id="e1626-103">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="e1626-103">TransactionFlowBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1626-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1626-104">Syntax</span></span>  
  
```csharp
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="e1626-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e1626-105">Methods</span></span>  
 <span data-ttu-id="e1626-106">La classe TransactionFlowBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="e1626-106">The TransactionFlowBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="e1626-107">Properties</span><span class="sxs-lookup"><span data-stu-id="e1626-107">Properties</span></span>  
 <span data-ttu-id="e1626-108">La classe TransactionFlowBindingElement dispose des propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1626-108">The TransactionFlowBindingElement class has the following properties:</span></span>  
  
### <a name="issuedtokens"></a><span data-ttu-id="e1626-109">IssuedTokens</span><span class="sxs-lookup"><span data-stu-id="e1626-109">IssuedTokens</span></span>  
 <span data-ttu-id="e1626-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="e1626-110">Data type: string</span></span>  
  
 <span data-ttu-id="e1626-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1626-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e1626-112">Définit les exigences d’un en-tête de jetons de sécurité publié (IssuedTokens de WS-Trust).</span><span class="sxs-lookup"><span data-stu-id="e1626-112">Specifies the requirement for an issued security tokens header (IssuedTokens from WS-Trust).</span></span>  
  
### <a name="transactionprotocol"></a><span data-ttu-id="e1626-113">TransactionProtocol</span><span class="sxs-lookup"><span data-stu-id="e1626-113">TransactionProtocol</span></span>  
 <span data-ttu-id="e1626-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="e1626-114">Data type: string</span></span>  
  
 <span data-ttu-id="e1626-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1626-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e1626-116">Protocole de transactions utilisé par le service pour transférer les transactions.</span><span class="sxs-lookup"><span data-stu-id="e1626-116">The transactions protocol used by the service to flow transactions.</span></span>  
  
### <a name="transactions"></a><span data-ttu-id="e1626-117">Transactions</span><span class="sxs-lookup"><span data-stu-id="e1626-117">Transactions</span></span>  
 <span data-ttu-id="e1626-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="e1626-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="e1626-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1626-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e1626-120">Indique si la transaction entrante est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e1626-120">Indicates whether the incoming transaction is supported.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e1626-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e1626-121">Requirements</span></span>  
  
|<span data-ttu-id="e1626-122">MOF</span><span class="sxs-lookup"><span data-stu-id="e1626-122">MOF</span></span>|<span data-ttu-id="e1626-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="e1626-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="e1626-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1626-124">Namespace</span></span>|<span data-ttu-id="e1626-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="e1626-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e1626-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1626-126">See also</span></span>
- <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
