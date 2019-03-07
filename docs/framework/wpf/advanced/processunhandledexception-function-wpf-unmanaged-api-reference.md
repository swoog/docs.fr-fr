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
ms.openlocfilehash: 3a95e8e68361f060d843247f400043a79dc28889
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466863"
---
# <a name="processunhandledexception-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="d17a5-102">Fonction ProcessUnhandledException (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="d17a5-102">ProcessUnhandledException Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="d17a5-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="d17a5-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="d17a5-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="d17a5-104">Used by the Windows Presentation Foundation (WPF) infrastructure for exception handling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d17a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d17a5-105">Syntax</span></span>  
  
```cpp  
void __stdcall ProcessUnhandledException(  
   __in_ecount(1) BSTR errorMsg  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="d17a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d17a5-106">Parameters</span></span>  
 <span data-ttu-id="d17a5-107">errorMsg</span><span class="sxs-lookup"><span data-stu-id="d17a5-107">errorMsg</span></span>  
 <span data-ttu-id="d17a5-108">Message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="d17a5-108">The error message.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d17a5-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d17a5-109">Requirements</span></span>  
 <span data-ttu-id="d17a5-110">**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d17a5-110">**Platforms:** See [.NET Framework System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d17a5-111">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="d17a5-111">**DLL:**</span></span>  
  
 <span data-ttu-id="d17a5-112">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="d17a5-112">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="d17a5-113">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="d17a5-113">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="d17a5-114">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d17a5-114">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d17a5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d17a5-115">See also</span></span>
- [<span data-ttu-id="d17a5-116">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="d17a5-116">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
