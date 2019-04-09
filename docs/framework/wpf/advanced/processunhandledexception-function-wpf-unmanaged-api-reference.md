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
ms.openlocfilehash: 0c8751454be6e0eed547c38e9d0bc7931abaec3d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59196968"
---
# <a name="processunhandledexception-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="6720a-102">Fonction ProcessUnhandledException (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="6720a-102">ProcessUnhandledException Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="6720a-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="6720a-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="6720a-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="6720a-104">Used by the Windows Presentation Foundation (WPF) infrastructure for exception handling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6720a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6720a-105">Syntax</span></span>  
  
```cpp  
void __stdcall ProcessUnhandledException(  
   __in_ecount(1) BSTR errorMsg  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="6720a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6720a-106">Parameters</span></span>  
 <span data-ttu-id="6720a-107">errorMsg</span><span class="sxs-lookup"><span data-stu-id="6720a-107">errorMsg</span></span>  
 <span data-ttu-id="6720a-108">Message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="6720a-108">The error message.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6720a-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6720a-109">Requirements</span></span>  
 <span data-ttu-id="6720a-110">**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6720a-110">**Platforms:** See [.NET Framework System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 **<span data-ttu-id="6720a-111">DLL :</span><span class="sxs-lookup"><span data-stu-id="6720a-111">DLL:</span></span>**  
  
 <span data-ttu-id="6720a-112">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="6720a-112">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="6720a-113">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="6720a-113">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 **<span data-ttu-id="6720a-114">Version du .NET framework :</span><span class="sxs-lookup"><span data-stu-id="6720a-114">.NET Framework Version:</span></span>** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="6720a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6720a-115">See also</span></span>

- [<span data-ttu-id="6720a-116">Informations de référence sur les API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="6720a-116">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
