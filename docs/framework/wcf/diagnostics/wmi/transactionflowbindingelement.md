---
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: a58d5620abbb636480ceea3020552246ae284842
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59150083"
---
# <a name="transactionflowbindingelement"></a><span data-ttu-id="0a83a-102">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="0a83a-102">TransactionFlowBindingElement</span></span>
<span data-ttu-id="0a83a-103">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="0a83a-103">TransactionFlowBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a83a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a83a-104">Syntax</span></span>  
  
```csharp
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="0a83a-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0a83a-105">Methods</span></span>  
 <span data-ttu-id="0a83a-106">La classe TransactionFlowBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="0a83a-106">The TransactionFlowBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="0a83a-107">Properties</span><span class="sxs-lookup"><span data-stu-id="0a83a-107">Properties</span></span>  
 <span data-ttu-id="0a83a-108">La classe TransactionFlowBindingElement dispose des propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a83a-108">The TransactionFlowBindingElement class has the following properties:</span></span>  
  
### <a name="issuedtokens"></a><span data-ttu-id="0a83a-109">IssuedTokens</span><span class="sxs-lookup"><span data-stu-id="0a83a-109">IssuedTokens</span></span>  
 <span data-ttu-id="0a83a-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="0a83a-110">Data type: string</span></span>  
  
 <span data-ttu-id="0a83a-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a83a-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0a83a-112">Définit les spécifications d'un en-tête de jetons de sécurité publié (IssuedTokens de WS-Trust).</span><span class="sxs-lookup"><span data-stu-id="0a83a-112">Specifies the requirement for an issued security tokens header (IssuedTokens from WS-Trust).</span></span>  
  
### <a name="transactionprotocol"></a><span data-ttu-id="0a83a-113">TransactionProtocol</span><span class="sxs-lookup"><span data-stu-id="0a83a-113">TransactionProtocol</span></span>  
 <span data-ttu-id="0a83a-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="0a83a-114">Data type: string</span></span>  
  
 <span data-ttu-id="0a83a-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a83a-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0a83a-116">Protocole de transactions utilisé par le service pour transférer les transactions.</span><span class="sxs-lookup"><span data-stu-id="0a83a-116">The transactions protocol used by the service to flow transactions.</span></span>  
  
### <a name="transactions"></a><span data-ttu-id="0a83a-117">Transactions</span><span class="sxs-lookup"><span data-stu-id="0a83a-117">Transactions</span></span>  
 <span data-ttu-id="0a83a-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="0a83a-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="0a83a-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a83a-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0a83a-120">Indique si la transaction entrante est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0a83a-120">Indicates whether the incoming transaction is supported.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a83a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a83a-121">Requirements</span></span>  
  
|<span data-ttu-id="0a83a-122">MOF</span><span class="sxs-lookup"><span data-stu-id="0a83a-122">MOF</span></span>|<span data-ttu-id="0a83a-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="0a83a-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="0a83a-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0a83a-124">Namespace</span></span>|<span data-ttu-id="0a83a-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="0a83a-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0a83a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a83a-126">See also</span></span>

- <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
