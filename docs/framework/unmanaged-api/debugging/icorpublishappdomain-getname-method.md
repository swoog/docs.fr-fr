---
title: ICorPublishAppDomain::GetName, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomain.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomain::GetName
helpviewer_keywords:
- GetName method, ICorPublishAppDomain interface [.NET Framework debugging]
- ICorPublishAppDomain::GetName method [.NET Framework debugging]
ms.assetid: 6ef8ac9b-9803-4b65-8b13-25f3e0b1bc6b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 796f8ea42cc5cbe13729f7b92e15bc214d62734d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423856"
---
# <a name="icorpublishappdomaingetname-method"></a>ICorPublishAppDomain::GetName, méthode
Obtient le nom du domaine d’application qui est représenté par ce [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetName (  
    [in]  ULONG32   cchName,   
    [out] ULONG32   *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]   
        WCHAR       *szName  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `cchName`  
 [in] Taille du tableau `szName`.  
  
 `pcchName`  
 [out] Un pointeur vers le nombre de caractères larges, y compris le caractère null, retourné dans le `szName` tableau.  
  
 `szName`  
 [out] Tableau dans lequel stocker le nom.  
  
## <a name="remarks"></a>Notes  
 Si `szName` n’est pas null, le `GetName` méthode copie jusqu'à `cchName` caractères (y compris la marque de fin null) dans `szName`. Si une valeur non null est retournée dans `pcchName`, le nombre réel de caractères dans le nom (y compris la marque de fin null) est stocké dans le `szName` tableau.  
  
 Le `GetName` méthode retourne un HRESULT S_OK, quelle que soit le nombre de caractères ont été copié.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorPub.idl, CorPub.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorPublishAppDomain, interface](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md)
