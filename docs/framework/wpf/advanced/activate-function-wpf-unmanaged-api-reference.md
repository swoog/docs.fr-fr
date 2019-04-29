---
title: Activer (fonction) (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- Activate
api_location:
- PresentationHost_v0400.dll
ms.assetid: 1400329c-b598-465f-80f2-e3dabf044811
ms.openlocfilehash: ee231653815bd5ef75d58979034e3b3be9f5ba54
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777167"
---
# <a name="activate-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="0c4ff-102">Activer (fonction) (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="0c4ff-102">Activate Function (WPF Unmanaged API Reference)</span></span>

<span data-ttu-id="0c4ff-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>

<span data-ttu-id="0c4ff-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c4ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c4ff-105">Syntax</span></span>

```cpp
void Activate(
    const ActivateParameters* pParameters,
    __deref_out_ecount(1) LPUNKNOWN* ppInner,
    );
```

## <a name="parameters"></a><span data-ttu-id="0c4ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c4ff-106">Parameters</span></span>

`pParameters`\
<span data-ttu-id="0c4ff-107">Pointeur vers les paramètres de l’activation de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-107">A pointer to the window's activation parameters.</span></span>

`ppInner`\
<span data-ttu-id="0c4ff-108">Un pointeur vers l’adresse d’une mémoire tampon seul élément qui contient un pointeur vers un <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> objet.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-108">A pointer to the address of a single-element buffer that contains a pointer to an <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4ff-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c4ff-109">Requirements</span></span>

<span data-ttu-id="0c4ff-110">**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c4ff-110">**Platforms:** See [.NET Framework System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="0c4ff-111">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="0c4ff-111">**DLL:**</span></span>

<span data-ttu-id="0c4ff-112">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="0c4ff-112">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>

<span data-ttu-id="0c4ff-113">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="0c4ff-113">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>

<span data-ttu-id="0c4ff-114">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c4ff-114">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="0c4ff-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c4ff-115">See also</span></span>

- [<span data-ttu-id="0c4ff-116">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="0c4ff-116">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
