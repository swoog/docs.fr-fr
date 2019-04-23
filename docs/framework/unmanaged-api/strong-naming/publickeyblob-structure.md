---
title: PublicKeyBlob, structure
ms.date: 03/30/2017
api_name:
- PublicKeyBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- PublicKeyBlob
helpviewer_keywords:
- PublicKeyBlob structure [.NET Framework strong naming]
ms.assetid: b9240712-829c-4c8d-9a09-a6e7aa63f63a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1a361e04b6f8f39ec0083471d8cb47d5a29376c5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59214817"
---
# <a name="publickeyblob-structure"></a><span data-ttu-id="694e9-102">PublicKeyBlob, structure</span><span class="sxs-lookup"><span data-stu-id="694e9-102">PublicKeyBlob Structure</span></span>
<span data-ttu-id="694e9-103">Représente, dans un format binaire, la clé publique d’une paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="694e9-103">Represents, in binary format, the public key of a public/private key pair.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="694e9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="694e9-104">Syntax</span></span>  
  
```  
typedef struct {  
    unsigned int SigAlgId;  
    unsigned int HashAlgId;  
    ULONG cbPublicKey;  
    BYTE PublicKey[1]  
} PublicKeyBlob;   
```  
  
## <a name="members"></a><span data-ttu-id="694e9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="694e9-105">Members</span></span>  
  
|<span data-ttu-id="694e9-106">Membre</span><span class="sxs-lookup"><span data-stu-id="694e9-106">Member</span></span>|<span data-ttu-id="694e9-107">Description</span><span class="sxs-lookup"><span data-stu-id="694e9-107">Description</span></span>|  
|------------|-----------------|  
|`SigAlgId`|<span data-ttu-id="694e9-108">L’identificateur de l’algorithme de signature (de type `ALG_ID`, comme défini dans WinCrypt.h) de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="694e9-108">The identifier for the signature algorithm (of type `ALG_ID`, as defined in WinCrypt.h) of the public key.</span></span>|  
|`HashAlgId`|<span data-ttu-id="694e9-109">L’identificateur de l’algorithme de hachage (de type `ALG_ID`, comme défini dans WinCrypt.h) de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="694e9-109">The identifier for the hash algorithm (of type `ALG_ID`, as defined in WinCrypt.h) of the public key.</span></span>|  
|`cbPublicKey`|<span data-ttu-id="694e9-110">La longueur de la clé en octets.</span><span class="sxs-lookup"><span data-stu-id="694e9-110">The length of the key in bytes.</span></span>|  
|`PublicKey`|<span data-ttu-id="694e9-111">Tableau d’octets de longueur variable qui contient la valeur de clé dans le format retourné par l’interface CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="694e9-111">A variable-length byte array that contains the key value in the format returned by the CryptoAPI.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="694e9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="694e9-112">Remarks</span></span>  
 <span data-ttu-id="694e9-113">Le `PublicKeyBlob` structure est utilisée par [StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md), [StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md)et d’autres fonctions de nom fort pour représenter la clé publique d’une paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="694e9-113">The `PublicKeyBlob` structure is used by [StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md), [StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md), and other strong name functions to represent the public key of a public/private key pair.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="694e9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="694e9-114">Requirements</span></span>  
 <span data-ttu-id="694e9-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="694e9-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="694e9-116">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="694e9-116">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="694e9-117">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="694e9-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="694e9-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="694e9-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="694e9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="694e9-119">See also</span></span>

- [<span data-ttu-id="694e9-120">StrongNameGetPublicKey, fonction</span><span class="sxs-lookup"><span data-stu-id="694e9-120">StrongNameGetPublicKey Function</span></span>](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md)
- [<span data-ttu-id="694e9-121">StrongNameSignatureGeneration, fonction</span><span class="sxs-lookup"><span data-stu-id="694e9-121">StrongNameSignatureGeneration Function</span></span>](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md)
