---
title: GetRawInputDevices
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
ms.assetid: c4d37ecd-065a-4d1c-9e6c-26804ae968ca
ms.openlocfilehash: 763767514f5f157c676f2e5c86ff9b1e4e64f233
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57495245"
---
# <a name="getrawinputdevices"></a><span data-ttu-id="f5778-102">GetRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="f5778-102">GetRawInputDevices</span></span>
<span data-ttu-id="f5778-103">Permet à PresentationHost.exe de découvrir les périphériques d'entrée brute (périphériques d'interface utilisateur) qui intéressent l'application hôte.</span><span class="sxs-lookup"><span data-stu-id="f5778-103">Allows PresentationHost.exe to discover the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5778-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5778-104">Syntax</span></span>  
  
```  
HRESULT GetRawInputDevices( [out] IEnumRAWINPUTDEVICE **ppEnum );  
```  
  
## <a name="parameters"></a><span data-ttu-id="f5778-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5778-105">Parameters</span></span>  
 `ppEnum`  
  
 <span data-ttu-id="f5778-106">[out] Un pointeur vers un [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) pour l’énumération des périphériques d’entrée brutes.</span><span class="sxs-lookup"><span data-stu-id="f5778-106">[out] A pointer to an [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) for enumerating the raw input devices.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f5778-107">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f5778-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="f5778-108">HRESULT :</span><span class="sxs-lookup"><span data-stu-id="f5778-108">HRESULT:</span></span>  
  
 <span data-ttu-id="f5778-109">S_OK - [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) servira uniquement par PresentationHost.exe si S_OK est retourné.</span><span class="sxs-lookup"><span data-stu-id="f5778-109">S_OK - [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) will only be used by PresentationHost.exe if S_OK is returned.</span></span>  
  
 <span data-ttu-id="f5778-110">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f5778-110">E_NOTIMPL</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f5778-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f5778-111">Remarks</span></span>  
 <span data-ttu-id="f5778-112">Les périphériques d'entrée brute correspondent à l'ensemble des périphériques d'entrée, notamment les claviers, les souris et, dans une moindre mesure, les périphériques classiques tels que les télécommandes.</span><span class="sxs-lookup"><span data-stu-id="f5778-112">Raw input devices are the set of input devices that includes keyboards, mice, and less traditional devices like remote controls.</span></span>  
  
 <span data-ttu-id="f5778-113">Une fois la liste de périphériques d'entrée brute extraite, PresentationHost.exe s'inscrit auprès des périphériques pour recevoir les messages de notification WM_INPUT.</span><span class="sxs-lookup"><span data-stu-id="f5778-113">Once the list of raw input devices has been retrieved, PresentationHost.exe registers with the devices to receive WM_INPUT notification messages.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5778-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5778-114">See also</span></span>
- [<span data-ttu-id="f5778-115">GetRawInputDeviceList</span><span class="sxs-lookup"><span data-stu-id="f5778-115">GetRawInputDeviceList</span></span>](/windows/desktop/api/winuser/nf-winuser-getrawinputdevicelist)
- [<span data-ttu-id="f5778-116">FilterInputMessage</span><span class="sxs-lookup"><span data-stu-id="f5778-116">FilterInputMessage</span></span>](filterinputmessage.md)
