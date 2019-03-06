---
title: StrongNameKeyDelete, fonction
ms.date: 03/30/2017
api_name:
- StrongNameKeyDelete
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyDelete
helpviewer_keywords:
- StrongNameKeyDelete function [.NET Framework strong naming]
ms.assetid: 313e71e4-1790-4d2f-b68b-5040ebd1c149
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dfc785a48d0cdf1cf2fdc0245a27b8ef35fd2d81
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57364513"
---
# <a name="strongnamekeydelete-function"></a>StrongNameKeyDelete, fonction

Supprime le conteneur de clé spécifié.

Cette fonction a été déconseillée. Utilisez le [ICLRStrongName::StrongNameKeyDelete](../hosting/iclrstrongname-strongnamekeydelete-method.md) méthode à la place.

## <a name="syntax"></a>Syntaxe

```cpp
BOOLEAN StrongNameKeyDelete (
    [in]  LPCWSTR   wszKeyContainer
);
```

## <a name="parameters"></a>Paramètres

`wszKeyContainer`\
[in] Le nom du conteneur de clé à supprimer.

## <a name="return-value"></a>Valeur de retour

`true` de réussite ; Sinon, `false`.

## <a name="remarks"></a>Notes

Utilisez le [StrongNameKeyInstall](strongnamekeyinstall-function.md) (fonction) pour importer une paire de clés publique/privée dans un conteneur.

Si le `StrongNameKeyDelete` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** StrongName.h

**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll

**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [StrongNameKeyDelete, méthode](../hosting/iclrstrongname-strongnamekeydelete-method.md)
- [StrongNameKeyInstall, méthode](../hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [ICLRStrongName, interface](../hosting/iclrstrongname-interface.md)