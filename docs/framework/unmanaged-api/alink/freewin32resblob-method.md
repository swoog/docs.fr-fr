---
title: FreeWin32ResBlob, méthode
ms.date: 03/30/2017
api_name:
- IALink.FreeWin32ResBlob
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- FreeWin32ResBlob
helpviewer_keywords:
- FreeWin32ResBlob method
ms.assetid: d941102b-2679-4c49-b15e-c0fc9c53e11f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 196a57b3e919ea4ccbc0b91e5b6f281ad3c30b62
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789881"
---
# <a name="freewin32resblob-method"></a><span data-ttu-id="e15d5-102">FreeWin32ResBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="e15d5-102">FreeWin32ResBlob Method</span></span>
<span data-ttu-id="e15d5-103">Libère le blob de ressources Win32 et les ressources associées.</span><span class="sxs-lookup"><span data-stu-id="e15d5-103">Releases the Win32 resource blob and associated resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e15d5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e15d5-104">Syntax</span></span>  
  
```  
HRESULT FreeWin32ResBlob(  
    const void** ppResBlob  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="e15d5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e15d5-105">Parameters</span></span>  
 `ppResBlob`  
 <span data-ttu-id="e15d5-106">Le blob de ressources à libérer.</span><span class="sxs-lookup"><span data-stu-id="e15d5-106">The resource blob to be released.</span></span> <span data-ttu-id="e15d5-107">Cette méthode attribue le pointeur d’objet blob avec la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="e15d5-107">This method assigns the blob pointer to NULL.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e15d5-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e15d5-108">Return Value</span></span>  
 <span data-ttu-id="e15d5-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="e15d5-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e15d5-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e15d5-110">Requirements</span></span>  
 <span data-ttu-id="e15d5-111">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="e15d5-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e15d5-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e15d5-112">See also</span></span>

- [<span data-ttu-id="e15d5-113">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="e15d5-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="e15d5-114">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="e15d5-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="e15d5-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="e15d5-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
