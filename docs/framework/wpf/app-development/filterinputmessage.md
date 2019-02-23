---
title: FilterInputMessage
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
- FilterInputMessage method [WPF]
ms.assetid: 4d74c6cf-7d1d-49ff-96c1-231340ce54f5
ms.openlocfilehash: c3620e13951afddc8de25c314de17704548d2366
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "56746164"
---
# <a name="filterinputmessage"></a>FilterInputMessage
Appelé par PresentationHost.exe chaque fois qu'un message est reçu, à moins que E_NOTIMPL soit retourné.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT FilterInputMessage( [in] MSG* pMsg ) ;  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pMsg`  
  
 [in] Message WM_INPUT envoyé à la fenêtre qui obtient l'entrée brute.  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 HRESULT :  
  
 S_OK : le filtre n'a pas traité le message et le traitement peut se poursuivre.  
  
 S_FALSE : le filtre a traité ce message et aucun autre traitement ne doit se produire.  
  
 E_NOTIMPL : Si cette valeur est retournée, [FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md) n’est pas appelée à nouveau. Cette valeur peut être retournée par une application hôte qui cherche seulement à fournir une progression personnalisée et des interfaces utilisateur d'erreur à PresentationHost.exe, mais pas à se faire transférer des messages d'entrée brute depuis PresentationHost.exe.  
  
## <a name="remarks"></a>Notes  
 PresentationHost.exe est la cible de divers périphériques d'entrée brute, notamment les claviers, les souris et les télécommandes. Le comportement de l'application hôte est parfois dépendant de l'entrée qui serait autrement consommée par PresentationHost.exe. Par exemple, une application hôte peut être tributaire de la réception de certains messages d'entrée pour déterminer s'il faut ou non afficher des éléments d'interface utilisateur spécifiques.  
  
 Pour autoriser l’application hôte recevoir les messages d’entrée nécessaires pour fournir ces comportements, PresentationHost.exe transfère les messages d’entrée brutes appropriés à l’application hébergée en appelant [FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md).  
  
 L’application hébergée reçoit des messages d’entrée brute en s’inscrivant auprès de l’ensemble des périphériques d’entrée brute (périphériques d’Interface utilisateur) retourné par [GetRawInputDevices](../../../../docs/framework/wpf/app-development/getrawinputdevices.md).  
  
## <a name="see-also"></a>Voir aussi
- [Message WM_INPUT](/windows/desktop/inputdev/wm-input)
