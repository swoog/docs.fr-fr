---
title: ISymUnmanagedENCUpdate::InitializeForEnc, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.InitializeForEnc
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::InitializeForEnc
helpviewer_keywords:
- ISymUnmanagedENCUpdate::InitializeForEnc method [.NET Framework debugging]
- InitializeForEnc method [.NET Framework debugging]
ms.assetid: 796b2154-b53c-4d07-9e67-80fd6064725a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 135ae21c2281c545aa701ac2a22a43cea63f5242
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939709"
---
# <a name="isymunmanagedencupdateinitializeforenc-method"></a><span data-ttu-id="55c15-102">ISymUnmanagedENCUpdate::InitializeForEnc, méthode</span><span class="sxs-lookup"><span data-stu-id="55c15-102">ISymUnmanagedENCUpdate::InitializeForEnc Method</span></span>
<span data-ttu-id="55c15-103">Permet le calcul des limites de méthode avant le premier appel à la [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="55c15-103">Allows method boundaries to be computed before the first call to the [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55c15-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55c15-104">Syntax</span></span>  
  
```  
HRESULT InitializeForEnc();  
```  
  
## <a name="return-value"></a><span data-ttu-id="55c15-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="55c15-105">Return Value</span></span>  
 <span data-ttu-id="55c15-106">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="55c15-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="55c15-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55c15-107">Requirements</span></span>  
 <span data-ttu-id="55c15-108">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="55c15-108">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55c15-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55c15-109">See also</span></span>

- [<span data-ttu-id="55c15-110">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="55c15-110">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
