---
title: IMetaDataError, interface
ms.date: 03/30/2017
api_name:
- IMetaDataError
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataError
helpviewer_keywords:
- IMetaDataError interface [.NET Framework metadata]
ms.assetid: 0020b62c-ea88-40c7-a9ee-16b064f81624
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fe2f683ae46d1ee6205f97536976a358e86fc53d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720377"
---
# <a name="imetadataerror-interface"></a><span data-ttu-id="c02f9-102">IMetaDataError, interface</span><span class="sxs-lookup"><span data-stu-id="c02f9-102">IMetaDataError Interface</span></span>
<span data-ttu-id="c02f9-103">Fournit un mécanisme de rappel pour signaler les erreurs pendant la fusion des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c02f9-103">Provides a callback mechanism for reporting errors during the metadata merge.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c02f9-104">Le `IMetaDataError` interface doit être implémentée par le client.</span><span class="sxs-lookup"><span data-stu-id="c02f9-104">The `IMetaDataError` interface must be implemented by the client.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c02f9-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c02f9-105">Methods</span></span>  
  
|<span data-ttu-id="c02f9-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="c02f9-106">Method</span></span>|<span data-ttu-id="c02f9-107">Description</span><span class="sxs-lookup"><span data-stu-id="c02f9-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c02f9-108">OnError, méthode</span><span class="sxs-lookup"><span data-stu-id="c02f9-108">OnError Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-onerror-method.md)|<span data-ttu-id="c02f9-109">Fournit une notification des erreurs qui se produisent pendant la fusion des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c02f9-109">Provides notification of errors that occur during the metadata merge.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c02f9-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c02f9-110">Requirements</span></span>  
 <span data-ttu-id="c02f9-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c02f9-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c02f9-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c02f9-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c02f9-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c02f9-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c02f9-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c02f9-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c02f9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c02f9-115">See also</span></span>
- [<span data-ttu-id="c02f9-116">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="c02f9-116">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
