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
ms.openlocfilehash: 78031ed80fe83b736a351886457f9200534f470b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591511"
---
# <a name="forwardtranslateaccelerator-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="d0143-102">Fonction ForwardTranslateAccelerator (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="d0143-102">ForwardTranslateAccelerator Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="d0143-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="d0143-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="d0143-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="d0143-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0143-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0143-105">Syntax</span></span>  
  
```cpp  
HRESULT ForwardTranslateAccelerator(  
   MSG* pMsg,   
   VARIANT_BOOL appUnhandled  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d0143-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0143-106">Parameters</span></span>  
 <span data-ttu-id="d0143-107">pMsg</span><span class="sxs-lookup"><span data-stu-id="d0143-107">pMsg</span></span>  
 <span data-ttu-id="d0143-108">Pointeur vers un message.</span><span class="sxs-lookup"><span data-stu-id="d0143-108">A pointer to a message.</span></span>  
  
 <span data-ttu-id="d0143-109">appUnhandled</span><span class="sxs-lookup"><span data-stu-id="d0143-109">appUnhandled</span></span>  
 <span data-ttu-id="d0143-110">`true` Lorsque l’application a déjà reçue une chance de traiter le message d’entrée, mais n’a pas gérée Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="d0143-110">`true` when the app has already been given a chance to handle the input message, but has not handled it; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0143-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d0143-111">Requirements</span></span>  
 <span data-ttu-id="d0143-112">**Plateformes :** Consultez [requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d0143-112">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0143-113">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="d0143-113">**DLL:**</span></span>  
  
 <span data-ttu-id="d0143-114">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="d0143-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="d0143-115">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="d0143-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="d0143-116">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0143-116">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0143-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0143-117">See also</span></span>
- [<span data-ttu-id="d0143-118">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="d0143-118">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
