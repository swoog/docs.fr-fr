---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: 4662f70d-817b-4374-8da8-e0545585939f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce3c135e031d0c8425e990811fedc40f4ec45243
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59226610"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinekickoffmethod-method"></a><span data-ttu-id="501bd-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="501bd-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod Method</span></span>
<span data-ttu-id="501bd-103">Définit la méthode de départ qui lance l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="501bd-103">Sets the starting method that initiates the async operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="501bd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="501bd-104">Syntax</span></span>  
  
```idl  
HRESULT DefineKickoffMethod(    [in] mdToken kickoffMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="501bd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="501bd-105">Parameters</span></span>  
  
|<span data-ttu-id="501bd-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="501bd-106">Parameter</span></span>|<span data-ttu-id="501bd-107">Description</span><span class="sxs-lookup"><span data-stu-id="501bd-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="501bd-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="501bd-108">Return Value</span></span>  
 <span data-ttu-id="501bd-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="501bd-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="501bd-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="501bd-110">Requirements</span></span>  
 <span data-ttu-id="501bd-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="501bd-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="501bd-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="501bd-112">See also</span></span>

- [<span data-ttu-id="501bd-113">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="501bd-113">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
