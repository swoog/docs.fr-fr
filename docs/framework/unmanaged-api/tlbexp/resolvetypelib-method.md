---
title: ResolveTypeLib, méthode
ms.date: 03/30/2017
api_name:
- ResolveTypeLib
api_location:
- tlbref.dll
f1_keywords:
- ResolveTypeLib
helpviewer_keywords:
- ITypeLibResolver::ResolveTypeLib method [.NET Framework]
- ResolveTypeLib method [.NET Framework]
ms.assetid: 95d2aa0d-8eeb-4a9f-a216-5249f7e2c167
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d734f35b5878ec39e4f2159c326283d168e3be2b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62040844"
---
# <a name="resolvetypelib-method"></a>ResolveTypeLib, méthode
Résout le nom simple d’une bibliothèque de types en retournant son chemin d’accès qualifié complet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ResolveTypeLib(  
    [in]  BSTR      bstrSimpleName,  
    [in]  GUID      tlbid,  
    [in]  LCID      lcid,  
    [in]  USHORT    wMajorVersion,  
    [in]  USHORT    wMinorVersion,  
    [in]  SYSKIND   syskind,  
    [out] BSTR     *pbstrResolvedTlbName);  
```  
  
## <a name="parameters"></a>Paramètres  
 `bstrSimpleName`  
 [in] Un [BSTR](https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr) qui contient le nom simple de la bibliothèque de types.  
  
 `tlbid`  
 [in] Le GUID affecté à la bibliothèque de types dans le Registre.  
  
 `lcid`  
 [in] ID de localisation de la bibliothèque de types.  
  
 `wMajorVersion`  
 [in] Numéro de version principale de la bibliothèque de types. Par exemple, pour la version *x.y*, le numéro de version majeure est *x*.  
  
 `wMinorVersion`  
 [in] Numéro de version secondaire de la bibliothèque de types. Par exemple, pour la version *x.y*, le numéro de version mineure est *y*.  
  
 `syskind`  
 [in] Un [SYSKIND](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ne-oaidl-tagsyskind) indicateur qui identifie l’environnement d’exploitation. Les valeurs courantes sont SYS_WIN32 et SYS_WIN64.  
  
 `pbstrResolvedTlbName`  
 [out] Un pointeur vers un [BSTR](https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr) qui contient le chemin d’accès complet de la bibliothèque de types nommée dans le `bstrSimpleName` paramètre.  
  
## <a name="remarks"></a>Notes  
 Le `ResolveTypeLib` méthode est appelée par le [LoadTypeLibWithResolver, fonction](../../../../docs/framework/unmanaged-api/tlbexp/loadtypelibwithresolver-function.md) pendant [Tlbexp.exe (exportateur)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md) de traitement.  
  
 Les implémentations personnalisées de cette interface doivent retourner un [BSTR](https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr) qui contient le chemin d’accès complet de la bibliothèque de types nommée dans le `bstrSimpleName` paramètre.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** TlbRef.idl, TlbRef.h  
  
 **Bibliothèque :** TlbRef.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Fonctions d’assistance Tlbexp](../../../../docs/framework/unmanaged-api/tlbexp/index.md)
- [LoadTypeLibEx](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
