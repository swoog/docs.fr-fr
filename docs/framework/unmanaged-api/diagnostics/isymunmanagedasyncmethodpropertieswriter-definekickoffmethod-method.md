---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: 4662f70d-817b-4374-8da8-e0545585939f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 24560ed4b0bb7ca04d5859280baa594fbb2e4097
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473463"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinekickoffmethod-method"></a><span data-ttu-id="67e62-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="67e62-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod Method</span></span>
<span data-ttu-id="67e62-103">Définit la méthode de départ qui lance l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="67e62-103">Sets the starting method that initiates the async operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67e62-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67e62-104">Syntax</span></span>  
  
```idl  
HRESULT DefineKickoffMethod(    [in] mdToken kickoffMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="67e62-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67e62-105">Parameters</span></span>  
  
|<span data-ttu-id="67e62-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="67e62-106">Parameter</span></span>|<span data-ttu-id="67e62-107">Description</span><span class="sxs-lookup"><span data-stu-id="67e62-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="67e62-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="67e62-108">Return Value</span></span>  
 <span data-ttu-id="67e62-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="67e62-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67e62-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="67e62-110">Requirements</span></span>  
 <span data-ttu-id="67e62-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="67e62-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67e62-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67e62-112">See also</span></span>
- [<span data-ttu-id="67e62-113">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="67e62-113">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
