---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: 4662f70d-817b-4374-8da8-e0545585939f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 38b4564aeb3c8ed4674e755e5691bb0a9d417bca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624173"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinekickoffmethod-method"></a><span data-ttu-id="9b989-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="9b989-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod Method</span></span>
<span data-ttu-id="9b989-103">Définit la méthode de départ qui lance l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9b989-103">Sets the starting method that initiates the async operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b989-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b989-104">Syntax</span></span>  
  
```idl  
HRESULT DefineKickoffMethod(    [in] mdToken kickoffMethod);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9b989-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b989-105">Parameters</span></span>  
  
|<span data-ttu-id="9b989-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9b989-106">Parameter</span></span>|<span data-ttu-id="9b989-107">Description</span><span class="sxs-lookup"><span data-stu-id="9b989-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="9b989-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9b989-108">Return Value</span></span>  
 <span data-ttu-id="9b989-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="9b989-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b989-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9b989-110">Requirements</span></span>  
 <span data-ttu-id="9b989-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9b989-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b989-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b989-112">See also</span></span>
- [<span data-ttu-id="9b989-113">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="9b989-113">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
