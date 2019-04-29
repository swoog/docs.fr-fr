---
title: ICLRDataTarget3::GetExceptionContextRecord, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICLRDataTarget3.GetContextRecord
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 66076ed5-f05c-4114-9788-94cb143abb8a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4b43ab8cdeff3866bb51e8634f367cf86ee483d4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698016"
---
# <a name="iclrdatatarget3getexceptioncontextrecord-method"></a>ICLRDataTarget3::GetExceptionContextRecord, méthode
Appelée par les services d'accès aux données du CLR (Common Langage Runtime) pour récupérer l'enregistrement de contexte associé au processus cible. Par exemple, pour une cible d’image mémoire, ceci serait équivalent à l’enregistrement de contexte transmis le `ExceptionParam` l’argument de la [MiniDumpWriteDump](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) fonction dans le Windows déboguer bibliothèque d’aide (DbgHelp).  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetExceptionContextRecord(  
    [in] ULONG32 bufferSize,  
    [out] ULONG32* bufferUsed,  
    [out, size_is(bufferSize)] BYTE* buffer  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `bufferSize`  
 [en entrée] La taille de la mémoire tampon d'entrée, en octets. Elle doit être d'une taille suffisante pour contenir l'enregistrement de contexte.  
  
 `bufferUsed`  
 [en sortie] Un pointeur vers un type `ULONG32` qui reçoit le nombre d'octets réellement écrits dans la mémoire tampon.  
  
 `buffer`  
 [en sortie] Un pointeur vers une mémoire tampon qui reçoit une copie de l'enregistrement de contexte. L’enregistrement d’exception est retourné comme un [contexte](/windows/desktop/api/winnt/ns-winnt-_arm64_nt_context) type.  
  
## <a name="return-value"></a>Valeur de retour  
 La valeur de retour est `S_OK` en cas de réussite ou un code d'échec `HRESULT` en cas d'échec. Les codes `HRESULT` peuvent comprendre, sans y être limités, ce qui suit :  
  
|Code de retour|Description|  
|-----------------|-----------------|  
|`S_OK`|La méthode a réussi. L'enregistrement de contexte a été copié dans la mémoire tampon de sortie.|  
|`HRESULT_FROM_WIN32(ERROR_NOT_FOUND)`|Aucun enregistrement de contexte n'est associé à la cible.|  
|`HRESULT_FROM_WIN32(ERROR_BAD_LENGTH)`|La taille de la mémoire tampon d'entrée est insuffisante pour contenir l'enregistrement de contexte.|  
  
## <a name="remarks"></a>Notes  
 [CONTEXTE](/windows/desktop/api/winnt/ns-winnt-_arm64_nt_context) est une structure spécifique à la plateforme définie dans les en-têtes fournis par le Kit de développement Windows.  
  
 Cette méthode est implémentée par le writer de l'application de débogage.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** ClrData.idl, ClrData.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRDataTarget3, interface](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-interface.md)
- [GetExceptionRecord, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionrecord-method.md)
- [GetExceptionThreadID, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionthreadid-method.md)
