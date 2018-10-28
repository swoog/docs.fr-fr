---
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: 027ace6ea9fc2a0e5ce63efa84e1a49c0ed2cd0a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188025"
---
# <a name="transactionflowbindingelement"></a><span data-ttu-id="9b3e1-102">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="9b3e1-102">TransactionFlowBindingElement</span></span>
<span data-ttu-id="9b3e1-103">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="9b3e1-103">TransactionFlowBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b3e1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b3e1-104">Syntax</span></span>  
  
```csharp
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="9b3e1-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9b3e1-105">Methods</span></span>  
 <span data-ttu-id="9b3e1-106">La classe TransactionFlowBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="9b3e1-106">The TransactionFlowBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="9b3e1-107">Properties</span><span class="sxs-lookup"><span data-stu-id="9b3e1-107">Properties</span></span>  
 <span data-ttu-id="9b3e1-108">La classe TransactionFlowBindingElement dispose des propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="9b3e1-108">The TransactionFlowBindingElement class has the following properties:</span></span>  
  
### <a name="issuedtokens"></a><span data-ttu-id="9b3e1-109">IssuedTokens</span><span class="sxs-lookup"><span data-stu-id="9b3e1-109">IssuedTokens</span></span>  
 <span data-ttu-id="9b3e1-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="9b3e1-110">Data type: string</span></span>  
  
 <span data-ttu-id="9b3e1-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b3e1-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9b3e1-112">Définit les exigences d’un en-tête de jetons de sécurité publié (IssuedTokens de WS-Trust).</span><span class="sxs-lookup"><span data-stu-id="9b3e1-112">Specifies the requirement for an issued security tokens header (IssuedTokens from WS-Trust).</span></span>  
  
### <a name="transactionprotocol"></a><span data-ttu-id="9b3e1-113">TransactionProtocol</span><span class="sxs-lookup"><span data-stu-id="9b3e1-113">TransactionProtocol</span></span>  
 <span data-ttu-id="9b3e1-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="9b3e1-114">Data type: string</span></span>  
  
 <span data-ttu-id="9b3e1-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b3e1-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9b3e1-116">Protocole de transactions utilisé par le service pour transférer les transactions.</span><span class="sxs-lookup"><span data-stu-id="9b3e1-116">The transactions protocol used by the service to flow transactions.</span></span>  
  
### <a name="transactions"></a><span data-ttu-id="9b3e1-117">Transactions</span><span class="sxs-lookup"><span data-stu-id="9b3e1-117">Transactions</span></span>  
 <span data-ttu-id="9b3e1-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="9b3e1-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="9b3e1-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b3e1-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9b3e1-120">Indique si la transaction entrante est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9b3e1-120">Indicates whether the incoming transaction is supported.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b3e1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b3e1-121">Requirements</span></span>  
  
|<span data-ttu-id="9b3e1-122">MOF</span><span class="sxs-lookup"><span data-stu-id="9b3e1-122">MOF</span></span>|<span data-ttu-id="9b3e1-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="9b3e1-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="9b3e1-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9b3e1-124">Namespace</span></span>|<span data-ttu-id="9b3e1-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="9b3e1-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9b3e1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b3e1-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
