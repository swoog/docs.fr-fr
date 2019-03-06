---
title: IEnumRAWINPUTDEVIC:Clone
ms.date: 03/30/2017
helpviewer_keywords:
- Clone method [WPF]
ms.assetid: 2a6a1900-aa55-45fa-9382-241d569a2dc4
ms.openlocfilehash: a4c5e7db813089d1dd138416ac54dd4be467b87b
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57355017"
---
# <a name="ienumrawinputdevicclone"></a>IEnumRAWINPUTDEVIC:Clone
Crée un autre énumérateur de périphériques d'entrée brute avec le même état que l'énumérateur actif pour itérer au sein de la même liste.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Clone( [out] IEnumRAWINPUTDEVICE **ppenum);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppenum`  
  
 [out] Adresse de variable de sortie qui reçoit le [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) pointeur d’interface. Si la méthode échoue, la valeur de cette variable de sortie est indéfinie.  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 HRESULT : Cette méthode prend en charge les valeurs de retournés E_INVALIDARG et E_OUTOFMEMORY E_UNEXPECTED standard.  
  
## <a name="remarks"></a>Notes  
 Cette méthode rend possible l’enregistrement d’un point dans la séquence d’énumération afin de retourner à ce point plus tard. L’appelant doit libérer ce nouvel énumérateur séparément à partir du premier énumérateur.
