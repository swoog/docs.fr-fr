---
title: StrongNameKeyInstall, fonction
ms.date: 03/30/2017
api_name:
- StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyInstall
helpviewer_keywords:
- StrongNameKeyInstall function [.NET Framework strong naming]
ms.assetid: e32fd546-7757-4681-be3d-658e93281e50
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7121ace6777e7cf947fcc6ff30b1ea314851feff
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636717"
---
# <a name="strongnamekeyinstall-function"></a>StrongNameKeyInstall, fonction

Importe une paire de clés publique/privée dans un conteneur.

Cette fonction a été déconseillée. Utilisez le [ICLRStrongName::StrongNameKeyInstall](../hosting/iclrstrongname-strongnamekeyinstall-method.md) méthode à la place.

## <a name="syntax"></a>Syntaxe

```cpp
BOOLEAN StrongNameKeyInstall (
    [in]  LPCWSTR   wszKeyContainer,
    [in]  BYTE      *pbKeyBlob,
    [in]  ULONG     cbKeyBlob
);
```

## <a name="parameters"></a>Paramètres

`wszKeyContainer`\
[in] Le nom du conteneur de clé. `wszKeyContainer` doit être une chaîne non vide.

`pbKeyBlob`\
[in] La paire de clés binaire.

`cbKeyBlob`\
[in] La taille, en octets, de `pbKeyBlob`.

## <a name="return-value"></a>Valeur de retour

`true` de réussite ; Sinon, `false`.

## <a name="remarks"></a>Notes

Utilisez le [StrongNameKeyDelete](strongnamekeydelete-function.md) (fonction) pour supprimer le conteneur de clé.

Si le `StrongNameKeyInstall` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** StrongName.h

**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll

**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [StrongNameKeyInstall, méthode](../hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [StrongNameKeyDelete, méthode](../hosting/iclrstrongname-strongnamekeydelete-method.md)
- [ICLRStrongName, interface](../hosting/iclrstrongname-interface.md)
