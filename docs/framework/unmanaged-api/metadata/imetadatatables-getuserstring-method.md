---
title: IMetaDataTables::GetUserString, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetUserString
helpviewer_keywords:
- IMetaDataTables::GetUserString method [.NET Framework metadata]
- GetUserString method, IMetaDataTables interface [.NET Framework metadata]
ms.assetid: 35b8f0d6-9aba-4714-adb2-62020a38fb7e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0fefbab6b2ea9fbbfd90e03c41578a924f99c7a0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645199"
---
# <a name="imetadatatablesgetuserstring-method"></a>IMetaDataTables::GetUserString, méthode

Obtient la chaîne codée en dur à l’index spécifié dans la colonne de chaîne dans la portée actuelle.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT GetUserString (
    [in]  ULONG       ixUserString,
    [out] ULONG       *pcbData,
    [out] const void  **ppData
);
```

## <a name="parameters"></a>Paramètres

`ixUserString`\
[in] La valeur d’index à partir de laquelle la chaîne codée en dur est récupérée.

`pcbData`\
[out] Un pointeur vers la taille de `ppData`.

`ppData`\
[out] Pointeur vers un pointeur vers la chaîne retournée.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** Cor.h

**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll

**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [IMetaDataTables, interface](imetadatatables-interface.md)
- [IMetaDataTables2, interface](imetadatatables2-interface.md)