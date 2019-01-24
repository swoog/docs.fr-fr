---
title: BinaryMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: e2bb3cdd-3bbd-4bb5-85fe-570457500a66
ms.openlocfilehash: 330496d5f0f80affcb6bc44a1f66f4321a635f00
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580588"
---
# <a name="binarymessageencodingbindingelement"></a><span data-ttu-id="f3be5-102">BinaryMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="f3be5-102">BinaryMessageEncodingBindingElement</span></span>
<span data-ttu-id="f3be5-103">BinaryMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="f3be5-103">BinaryMessageEncodingBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3be5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3be5-104">Syntax</span></span>  
  
```csharp  
class BinaryMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  sint32 MaxReadPoolSize;  
  sint32 MaxSessionSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f3be5-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f3be5-105">Methods</span></span>  
 <span data-ttu-id="f3be5-106">La classe BinaryMessageEncodingBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="f3be5-106">The BinaryMessageEncodingBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f3be5-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f3be5-107">Properties</span></span>  
 <span data-ttu-id="f3be5-108">La classe BinaryMessageEncodingBindingElement a les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f3be5-108">The BinaryMessageEncodingBindingElement class has the following properties.</span></span>  
  
## <a name="maxreadpoolsize"></a><span data-ttu-id="f3be5-109">MaxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="f3be5-109">MaxReadPoolSize</span></span>  
 <span data-ttu-id="f3be5-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="f3be5-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="f3be5-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3be5-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f3be5-112">Entier qui définit combien de messages peuvent être lus de manière simultanée sans allouer de nouveaux lecteurs.</span><span class="sxs-lookup"><span data-stu-id="f3be5-112">An integer that defines how many messages can be read simultaneously without allocating new readers.</span></span>  
  
## <a name="maxsessionsize"></a><span data-ttu-id="f3be5-113">MaxSessionSize</span><span class="sxs-lookup"><span data-stu-id="f3be5-113">MaxSessionSize</span></span>  
 <span data-ttu-id="f3be5-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="f3be5-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="f3be5-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3be5-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f3be5-116">Valeur qui spécifie la taille, en octets, de la mémoire tampon utilisée pour l'encodage.</span><span class="sxs-lookup"><span data-stu-id="f3be5-116">A value that specifies the size, in bytes, of the buffer used for encoding.</span></span>  
  
## <a name="maxwritepoolsize"></a><span data-ttu-id="f3be5-117">MaxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="f3be5-117">MaxWritePoolSize</span></span>  
 <span data-ttu-id="f3be5-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="f3be5-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="f3be5-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3be5-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f3be5-120">Entier qui définit combien de messages peuvent être envoyés simultanément sans allouer de nouveaux enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="f3be5-120">An integer that defines how many messages can be sent simultaneously without allocating new writers.</span></span>  
  
## <a name="readerquotas"></a><span data-ttu-id="f3be5-121">ReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="f3be5-121">ReaderQuotas</span></span>  
 <span data-ttu-id="f3be5-122">Type de données : XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="f3be5-122">Data type: XmlDictionaryReaderQuotas</span></span>  
  
 <span data-ttu-id="f3be5-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3be5-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f3be5-124">Quotas des lecteurs.</span><span class="sxs-lookup"><span data-stu-id="f3be5-124">The quotas of the readers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3be5-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f3be5-125">Requirements</span></span>  
  
|<span data-ttu-id="f3be5-126">MOF</span><span class="sxs-lookup"><span data-stu-id="f3be5-126">MOF</span></span>|<span data-ttu-id="f3be5-127">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="f3be5-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f3be5-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f3be5-128">Namespace</span></span>|<span data-ttu-id="f3be5-129">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f3be5-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f3be5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3be5-130">See also</span></span>
- <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement>
