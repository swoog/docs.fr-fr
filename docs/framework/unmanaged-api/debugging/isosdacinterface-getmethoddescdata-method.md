---
title: ISOSDacInterface::GetMethodDescData (méthode)
ms.date: 01/16/2019
api.name:
- ISOSDacInterface::GetMethodDescData Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescData Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescData Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 47cea4810b764005e87d00966c15cf138f5913a7
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55825951"
---
# <a name="isosdacinterfacegetmethoddescdata-method"></a>ISOSDacInterface::GetMethodDescData (méthode)

Obtient les données pour le pointeur MethodDesc donné.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
HRESULT GetMethodDescData(
    CLRDATA_ADDRESS            methodDesc,
    CLRDATA_ADDRESS            ip,
    DacpMethodDescData *data,
    ULONG                      cRevertedRejitVersions,
    DacpReJitData      *rgRevertedRejitData,
    void                      *pcNeededRevertedRejitData
);
```

### <a name="parameters"></a>Paramètres

`methodDesc` [in] L’adresse de la MethodDesc.

`ip` [in] L’adresse IP de la méthode.

`data` [out] Les données associées à la MethodDesc tel que retourné par l’API internes.

`cRevertedRejitVersions` [out] Le nombre de versions de rejit rétablie.

`rgRevertedRejitData` [out] Les données associées aux versions rejit rétabli tel que retourné par l’API internes.

`pcNeededRevertedRejitData` [out] Le nombre d’octets requis pour stocker les données associées avec les versions ReJit rétablies.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `ISOSDacInterface` interface et correspond à l’emplacement de la table de la méthode virtuelle de 20. Pour pouvoir les utiliser, [ `CLRDATA_ADDRESS` ](../common-data-types-unmanaged-api-reference.md) doit être définie comme un entier non signé 64 bits.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Interface de ISOSDacInterface](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-interface.md)
