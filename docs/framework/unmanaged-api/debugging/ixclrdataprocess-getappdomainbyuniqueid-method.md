---
title: IXCLRDataProcess::GetAppDomainByUniqueId Method
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
helpviewer.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 8b468d40ef8eb523ba8881627fae15cf9b7c7b80
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775256"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a>IXCLRDataProcess::GetAppDomainByUniqueId Method

Obtient un `AppDomain` dans un processus en fonction de son identificateur unique.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

## <a name="parameters"></a>Paramètres

`id`\
[in] L’identificateur unique du domaine d’application

`appDomain`\
[out] Le domaine d’application

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 20. Le `IXCLRDataAppDomain*` retourné est utilisé pour l’interaction avec d’autres API.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).
**En-tête :** Aucun **bibliothèque :** Aucun **Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]

## <a name="see-also"></a>Voir aussi

- [Débogage](index.md)
- [Interface de IXCLRDataProcess](ixclrdataprocess-interface.md)
