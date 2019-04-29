---
title: GetRawInputDevices
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
ms.assetid: c4d37ecd-065a-4d1c-9e6c-26804ae968ca
ms.openlocfilehash: 3531ff9f42289a3ad3b029f090f2dd4987e5886c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947912"
---
# <a name="getrawinputdevices"></a><span data-ttu-id="f7918-102">GetRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="f7918-102">GetRawInputDevices</span></span>
<span data-ttu-id="f7918-103">Permet à PresentationHost.exe de découvrir les périphériques d'entrée brute (périphériques d'interface utilisateur) qui intéressent l'application hôte.</span><span class="sxs-lookup"><span data-stu-id="f7918-103">Allows PresentationHost.exe to discover the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f7918-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7918-104">Syntax</span></span>  
  
```  
HRESULT GetRawInputDevices( [out] IEnumRAWINPUTDEVICE **ppEnum );  
```  
  
## <a name="parameters"></a><span data-ttu-id="f7918-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7918-105">Parameters</span></span>  
 `ppEnum`  
  
 <span data-ttu-id="f7918-106">[out] Un pointeur vers un [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) pour l’énumération des périphériques d’entrée brutes.</span><span class="sxs-lookup"><span data-stu-id="f7918-106">[out] A pointer to an [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) for enumerating the raw input devices.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f7918-107">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f7918-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="f7918-108">HRESULT :</span><span class="sxs-lookup"><span data-stu-id="f7918-108">HRESULT:</span></span>  
  
 <span data-ttu-id="f7918-109">S_OK - [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) servira uniquement par PresentationHost.exe si S_OK est retourné.</span><span class="sxs-lookup"><span data-stu-id="f7918-109">S_OK - [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) will only be used by PresentationHost.exe if S_OK is returned.</span></span>  
  
 <span data-ttu-id="f7918-110">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f7918-110">E_NOTIMPL</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f7918-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f7918-111">Remarks</span></span>  
 <span data-ttu-id="f7918-112">Les périphériques d'entrée brute correspondent à l'ensemble des périphériques d'entrée, notamment les claviers, les souris et, dans une moindre mesure, les périphériques classiques tels que les télécommandes.</span><span class="sxs-lookup"><span data-stu-id="f7918-112">Raw input devices are the set of input devices that includes keyboards, mice, and less traditional devices like remote controls.</span></span>  
  
 <span data-ttu-id="f7918-113">Une fois la liste de périphériques d'entrée brute extraite, PresentationHost.exe s'inscrit auprès des périphériques pour recevoir les messages de notification WM_INPUT.</span><span class="sxs-lookup"><span data-stu-id="f7918-113">Once the list of raw input devices has been retrieved, PresentationHost.exe registers with the devices to receive WM_INPUT notification messages.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7918-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7918-114">See also</span></span>

- [<span data-ttu-id="f7918-115">GetRawInputDeviceList</span><span class="sxs-lookup"><span data-stu-id="f7918-115">GetRawInputDeviceList</span></span>](/windows/desktop/api/winuser/nf-winuser-getrawinputdevicelist)
- [<span data-ttu-id="f7918-116">FilterInputMessage</span><span class="sxs-lookup"><span data-stu-id="f7918-116">FilterInputMessage</span></span>](filterinputmessage.md)
