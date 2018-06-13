---
title: Champ de HttpWebRequest._CoreResponse
ms.date: 01/29/2018
topic_type:
- apiref
api_name:
- System.Net.HttpWebRequest._CoreResponse
api_location:
- System.dll
api_type:
- Assembly
author: stevewhims
ms.openlocfilehash: 3627c9bf0d72ccec3a0d6d9c7c89b62f83dcd4b4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33356197"
---
# <a name="httpwebrequestcoreresponse-field"></a><span data-ttu-id="6d2dc-102">HttpWebRequest. \_CoreResponse champ</span><span class="sxs-lookup"><span data-stu-id="6d2dc-102">HttpWebRequest.\_CoreResponse Field</span></span>

<span data-ttu-id="6d2dc-103">`HttpWebRequest._CoreResponse` est un objet (soit un [CoreResponseData](coreresponsedata.md) ou <xref:System.Exception>) qui contient le résultat de l’analyse de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-103">`HttpWebRequest._CoreResponse` is an object (either a [CoreResponseData](coreresponsedata.md) or an <xref:System.Exception>) containing the result of HTTP response parsing.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2dc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d2dc-104">Syntax</span></span>
  
```csharp
private object _CoreResponse
```

> [!WARNING]
> <span data-ttu-id="6d2dc-105">Cette API n’est pas destinée à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-105">This API is not meant to be used directly in your code.</span></span> <span data-ttu-id="6d2dc-106">Au lieu de cela, vous devez utiliser un <xref:System.Diagnostics.DiagnosticSource> raccordement du code de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-106">Instead, you should use a <xref:System.Diagnostics.DiagnosticSource> to hook networking code.</span></span> <span data-ttu-id="6d2dc-107">Consultez [le Guide d’utilisation de DiagnosticSource](https://github.com/dotnet/corefx/blob/master/src/System.Diagnostics.DiagnosticSource/src/DiagnosticSourceUsersGuide.md).</span><span class="sxs-lookup"><span data-stu-id="6d2dc-107">See [DiagnosticSource User's Guide](https://github.com/dotnet/corefx/blob/master/src/System.Diagnostics.DiagnosticSource/src/DiagnosticSourceUsersGuide.md).</span></span>
> 
> <span data-ttu-id="6d2dc-108">Microsoft ne prend pas en charge l’utilisation de cette classe dans une application de production en toutes circonstances.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-108">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2dc-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6d2dc-109">Requirements</span></span>

<span data-ttu-id="6d2dc-110">**Namespace :** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="6d2dc-110">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="6d2dc-111">**Assembly :** système (dans System.dll)</span><span class="sxs-lookup"><span data-stu-id="6d2dc-111">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="6d2dc-112">**Versions du .NET framework :** disponible depuis la version 2.0.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-112">**.NET Framework versions:** Available since 2.0.</span></span>
