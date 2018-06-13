---
title: Activer la fonction (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- Acrivate
api_location:
- PresentationHost_v0400.dll
ms.assetid: 1400329c-b598-465f-80f2-e3dabf044811
ms.openlocfilehash: 4931f64a525f14ad5b0b69c582a81cd15d98e541
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33539051"
---
# <a name="activate-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="ce0c5-102">Activer la fonction (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="ce0c5-102">Activate Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="ce0c5-103">Cette API prend en charge l’infrastructure de Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="ce0c5-104">Utilisée par l’infrastructure de Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce0c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce0c5-105">Syntax</span></span>  
  
```cpp  
void Activate(  
    const ActivateParameters* pParameters,  
    __deref_out_ecount(1) LPUNKNOWN* ppInner,  
    );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ce0c5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce0c5-106">Parameters</span></span>  
 <span data-ttu-id="ce0c5-107">pParameters</span><span class="sxs-lookup"><span data-stu-id="ce0c5-107">pParameters</span></span>  
 <span data-ttu-id="ce0c5-108">Pointeur vers les paramètres d’activation de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-108">A pointer to the window's activation parameters.</span></span>  
  
 <span data-ttu-id="ce0c5-109">ppInner</span><span class="sxs-lookup"><span data-stu-id="ce0c5-109">ppInner</span></span>  
 <span data-ttu-id="ce0c5-110">Un pointeur vers l’adresse d’une mémoire tampon seul élément qui contient un pointeur vers un <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> objet.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-110">A pointer to the address of a single-element buffer that contains a pointer to an <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce0c5-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce0c5-111">Requirements</span></span>  
 <span data-ttu-id="ce0c5-112">**Plateformes :** consultez [configuration système requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ce0c5-112">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce0c5-113">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="ce0c5-113">**DLL:**</span></span>  
  
 <span data-ttu-id="ce0c5-114">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="ce0c5-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="ce0c5-115">Dans le .NET Framework 4 et versions ultérieures : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="ce0c5-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="ce0c5-116">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce0c5-116">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce0c5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce0c5-117">See Also</span></span>  
 [<span data-ttu-id="ce0c5-118">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="ce0c5-118">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
