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
# <a name="activate-function-wpf-unmanaged-api-reference"></a>Activer (fonction) (référence des API non managées WPF)

Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.

Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.

## <a name="syntax"></a>Syntaxe

```cpp
void Activate(
    const ActivateParameters* pParameters,
    __deref_out_ecount(1) LPUNKNOWN* ppInner,
    );
```

## <a name="parameters"></a>Paramètres

`pParameters`\
Pointeur vers les paramètres de l’activation de la fenêtre.

`ppInner`\
Un pointeur vers l’adresse d’une mémoire tampon seul élément qui contient un pointeur vers un <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> objet.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).

**DLL :**

Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll

Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll

**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence des API non managées WPF](wpf-unmanaged-api-reference.md)
