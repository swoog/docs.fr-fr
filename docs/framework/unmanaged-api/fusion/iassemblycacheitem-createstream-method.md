---
title: IAssemblyCacheItem::CreateStream, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem.CreateStream
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem::CreateStream
helpviewer_keywords:
- CreateStream method [.NET Framework fusion]
- IAssemblyCacheItem::CreateStream method [.NET Framework fusion]
ms.assetid: 697ab0f4-470c-4baa-a415-4a975c42d0d5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a98273307003485202d8c12d5c27fda04ff5a0ae
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65629872"
---
# <a name="iassemblycacheitemcreatestream-method"></a>IAssemblyCacheItem::CreateStream, méthode

Crée un flux avec le format et le nom spécifié.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT CreateStream (
    [in]  DWORD dwFlags,
    [in]  LPCWSTR pszStreamName,
    [in]  DWORD dwFormat,
    [in]  DWORD dwFormatFlags,
    [out] IStream **ppIStream,
    [in, optional] ULARGE_INTEGER *puliMaxSize
);
```

## <a name="parameters"></a>Paramètres

`dwFlags`\
[in] Indicateurs définis dans Fusion.idl.

`pszStreamName`\
[in] Le nom du flux doit être créé.

`dwFormat`\
[in] Le format du fichier à être diffusé en continu.

`dwFormatFlags`\
[in] Indicateurs spécifiques au format définis dans Fusion.idl.

`ppIStream`\
[out] Un pointeur vers l’adresse de retourné [IStream](/windows/desktop/api/objidl/nn-objidl-istream) instance.

`puliMaxSize`\
[in, optional] La taille maximale du flux référencé par `ppIStream`.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** Fusion.h

**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [IAssemblyCacheItem, interface](iassemblycacheitem-interface.md)
