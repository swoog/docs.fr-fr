---
title: GetHashFromBlob, fonction
ms.date: 03/30/2017
api_name:
- GetHashFromBlob
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromBlob
helpviewer_keywords:
- GetHashFromBlob function [.NET Framework strong naming]
ms.assetid: b712d862-f2d0-4b55-87d4-65bbeadef982
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6ba049723710b378a90d17c67735a05e8a09d05d
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636849"
---
# <a name="gethashfromblob-function"></a>GetHashFromBlob, fonction

Obtient un hachage de l’assembly à l’adresse mémoire spécifiée, à l’aide de l’algorithme de hachage spécifié.

Cette fonction a été déconseillée. Utilisez le [ICLRStrongName::GetHashFromBlob](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromblob-method.md) méthode à la place.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT GetHashFromBlob (
    [in]  BYTE    *pbBlob,
    [in]  DWORD   cchBlob,
    [in, out] unsigned int   *piHashAlg,
    [out] BYTE    *pbHash,
    [in]  DWORD   cchHash,
    [out] DWORD   *pchHash
);
```

## <a name="parameters"></a>Paramètres

`pbBlob`\
[in] Pointeur vers l’adresse du bloc de mémoire à hacher.

`cchBlob`\
[in] La longueur, en octets, du bloc de mémoire.

`piHashAlg`\
[in, out] Constante qui spécifie l’algorithme de hachage. Utilisez zéro pour l’algorithme par défaut.

`pbHash`\
[out] La mémoire tampon de hachage retournée.

`cchHash`\
[in] La taille maximale demandée de `pbHash`.

`pchHash`\
[out] La taille, en octets, de retourné `pbHash`.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** StrongName.h

**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll

**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [GetHashFromBlob, méthode](../hosting/iclrstrongname-gethashfromblob-method.md)
- [ICLRStrongName, interface](../hosting/iclrstrongname-interface.md)
