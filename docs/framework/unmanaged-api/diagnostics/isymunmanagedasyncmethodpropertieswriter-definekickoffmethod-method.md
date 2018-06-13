---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: 4662f70d-817b-4374-8da8-e0545585939f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a476d92486d7f2523dfbcc8b25e9c11e26c55f2d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425613"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinekickoffmethod-method"></a><span data-ttu-id="7b496-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="7b496-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod Method</span></span>
<span data-ttu-id="7b496-103">Définit la méthode de démarrage qui lance l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7b496-103">Sets the starting method that initiates the async operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b496-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b496-104">Syntax</span></span>  
  
```idl  
HRESULT DefineKickoffMethod(    [in] mdToken kickoffMethod);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7b496-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b496-105">Parameters</span></span>  
  
|<span data-ttu-id="7b496-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7b496-106">Parameter</span></span>|<span data-ttu-id="7b496-107">Description</span><span class="sxs-lookup"><span data-stu-id="7b496-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="7b496-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7b496-108">Return Value</span></span>  
 <span data-ttu-id="7b496-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="7b496-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b496-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7b496-110">Requirements</span></span>  
 <span data-ttu-id="7b496-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7b496-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b496-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b496-112">See Also</span></span>  
 [<span data-ttu-id="7b496-113">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="7b496-113">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
