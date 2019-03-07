---
title: Fonction ForwardTranslateAccelerator (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ForwardTranslateAccelerator
api_location:
- PresentationHost_v0400.dll
ms.assetid: fff47a86-9d9f-4176-9530-10e1876e393f
ms.openlocfilehash: 2b1914b9a0e478c7ab15fca77b7df952123153ac
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57502284"
---
# <a name="forwardtranslateaccelerator-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="e555f-102">Fonction ForwardTranslateAccelerator (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="e555f-102">ForwardTranslateAccelerator Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="e555f-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="e555f-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="e555f-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="e555f-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e555f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e555f-105">Syntax</span></span>  
  
```cpp  
HRESULT ForwardTranslateAccelerator(  
   MSG* pMsg,   
   VARIANT_BOOL appUnhandled  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="e555f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e555f-106">Parameters</span></span>  
 <span data-ttu-id="e555f-107">pMsg</span><span class="sxs-lookup"><span data-stu-id="e555f-107">pMsg</span></span>  
 <span data-ttu-id="e555f-108">Pointeur vers un message.</span><span class="sxs-lookup"><span data-stu-id="e555f-108">A pointer to a message.</span></span>  
  
 <span data-ttu-id="e555f-109">appUnhandled</span><span class="sxs-lookup"><span data-stu-id="e555f-109">appUnhandled</span></span>  
 <span data-ttu-id="e555f-110">`true` Lorsque l’application a déjà reçue une chance de traiter le message d’entrée, mais n’a pas gérée Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="e555f-110">`true` when the app has already been given a chance to handle the input message, but has not handled it; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e555f-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e555f-111">Requirements</span></span>  
 <span data-ttu-id="e555f-112">**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e555f-112">**Platforms:** See [.NET Framework System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e555f-113">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="e555f-113">**DLL:**</span></span>  
  
 <span data-ttu-id="e555f-114">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="e555f-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="e555f-115">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="e555f-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="e555f-116">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e555f-116">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e555f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e555f-117">See also</span></span>
- [<span data-ttu-id="e555f-118">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="e555f-118">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
