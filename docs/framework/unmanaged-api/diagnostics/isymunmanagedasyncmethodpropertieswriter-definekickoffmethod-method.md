---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: 4662f70d-817b-4374-8da8-e0545585939f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce3c135e031d0c8425e990811fedc40f4ec45243
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59226610"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinekickoffmethod-method"></a><span data-ttu-id="2d035-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="2d035-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod Method</span></span>
<span data-ttu-id="2d035-103">Définit la méthode de départ qui lance l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2d035-103">Sets the starting method that initiates the async operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d035-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d035-104">Syntax</span></span>  
  
```idl  
HRESULT DefineKickoffMethod(    [in] mdToken kickoffMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d035-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d035-105">Parameters</span></span>  
  
|<span data-ttu-id="2d035-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2d035-106">Parameter</span></span>|<span data-ttu-id="2d035-107">Description</span><span class="sxs-lookup"><span data-stu-id="2d035-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="2d035-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2d035-108">Return Value</span></span>  
 <span data-ttu-id="2d035-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="2d035-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d035-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d035-110">Requirements</span></span>  
 <span data-ttu-id="2d035-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2d035-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d035-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d035-112">See also</span></span>

- [<span data-ttu-id="2d035-113">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="2d035-113">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
