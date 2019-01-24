---
title: Fonction ProcessUnhandledException (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ProcessUnhandledException
api_location:
- PresentationHost_v0400.dll
ms.assetid: 495ce5f6-bb4d-4b30-807a-c3c35f1ca95c
ms.openlocfilehash: 73480f7cd8be7bcb5296782a8503eb689442a14c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54578638"
---
# <a name="processunhandledexception-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="0c657-102">Fonction ProcessUnhandledException (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="0c657-102">ProcessUnhandledException Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="0c657-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="0c657-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="0c657-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="0c657-104">Used by the Windows Presentation Foundation (WPF) infrastructure for exception handling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c657-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c657-105">Syntax</span></span>  
  
```cpp  
void __stdcall ProcessUnhandledException(  
   __in_ecount(1) BSTR errorMsg  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0c657-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c657-106">Parameters</span></span>  
 <span data-ttu-id="0c657-107">errorMsg</span><span class="sxs-lookup"><span data-stu-id="0c657-107">errorMsg</span></span>  
 <span data-ttu-id="0c657-108">Message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="0c657-108">The error message.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c657-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0c657-109">Requirements</span></span>  
 <span data-ttu-id="0c657-110">**Plateformes :** Consultez [requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c657-110">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c657-111">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="0c657-111">**DLL:**</span></span>  
  
 <span data-ttu-id="0c657-112">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="0c657-112">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="0c657-113">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="0c657-113">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="0c657-114">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c657-114">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c657-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c657-115">See also</span></span>
- [<span data-ttu-id="0c657-116">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="0c657-116">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
