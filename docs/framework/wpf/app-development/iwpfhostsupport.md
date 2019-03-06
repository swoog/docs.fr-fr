---
title: IWpfHostSupport
ms.date: 03/30/2017
helpviewer_keywords:
- IWpfHostSupport interface [WPF]
ms.assetid: cc5a0281-de81-4cc1-87e4-0e46b1a811e9
ms.openlocfilehash: 074167111b78edc517dda019465260d0acd54737
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57376011"
---
# <a name="iwpfhostsupport"></a>IWpfHostSupport
Les applications qui hébergent [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] contenu via PresentationHost.exe implémentent cette interface pour fournir un point d’intégration entre l’hôte et PresentationHost.exe.  
  
## <a name="remarks"></a>Notes  
 [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] applications telles que les navigateurs Web peuvent héberger [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] de contenu, y compris [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] et libre de XAML. À l’hôte [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] contenu, [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] applications créent une instance de la [contrôle WebBrowser](https://go.microsoft.com/fwlink/?LinkId=97911). Doit être hébergé, [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] crée une instance de PresentationHost.exe, qui fournit le texte hébergé [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] contenu à l’hôte pour l’affichage dans le [contrôle WebBrowser](https://go.microsoft.com/fwlink/?LinkId=97911).  
  
 L’intégration activée par `IWpfHostSupport` permet à PresentationHost.exe de :  
  
-   Découvrir et enregistrer avec les périphériques d’entrée brute (périphériques d’Interface utilisateur) qui intéresse l’application hôte.  
  
-   Recevoir des messages d’entrée à partir des périphériques d’entrée brute et transférer les messages appropriés à l’application hôte.  
  
-   L’application hôte pour les interfaces d’utilisateur de progression et d’erreur personnalisées de la requête.  
  
> [!NOTE]
>  Cette API est conçue et pris en charge uniquement sur l'ordinateur client local  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|[GetRawInputDevices](getrawinputdevices.md)|Permet à PresentationHost.exe de découvrir les périphériques d'entrée brute (périphériques d'interface utilisateur) qui intéressent l'application hôte.|  
|[FilterInputMessage](filterinputmessage.md)|Appelé par PresentationHost.exe chaque fois qu'un message est reçu, à moins que E_NOTIMPL soit retourné.|  
|[GetCustomUI](getcustomui.md)|Par défaut, PresentationHost.exe fournit sa propre progression du déploiement et une erreur de déploiement des interfaces utilisateur qui sont affichent lorsque le contenu WPF est déployé.|
