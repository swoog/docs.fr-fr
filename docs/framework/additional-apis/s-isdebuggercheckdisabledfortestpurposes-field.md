---
title: s_isDebuggerCheckDisabledForTestPurposes champ
ms.date: 03/30/2017
ms.technology:
- dotnet-wpf
api_name:
- System.Windows.Diagnostics.VisualDiagnostics.s_isDebuggerCheckDisabledForTestPurposes
api_location:
- PresentationCore.dll
api_type:
- Assembly
ms.assetid: 9033a513-c255-4f31-b6d7-09b8d8c50e2d
robots: noindex,nofollow
ms.openlocfilehash: fbbd8d33ea163efaad1417ab4a1435df729e4897
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="sisdebuggercheckdisabledfortestpurposes-field"></a>s_isDebuggerCheckDisabledForTestPurposes champ

Ce champ privé dans la `System.Windows.Diagnostics.VisualDiagnostics` classe est utilisée par Visual Studio pour déterminer si une vérification interne pour le débogueur actif sera effectuée.

## <a name="syntax"></a>Syntaxe
  
```csharp  
private static bool s_isDebuggerCheckDisabledForTestPurposes
```
  
> [!WARNING]
>  L’API dans la `System.Windows.Diagnostics.VisualDiagnostics` classe sont disponibles uniquement quand une application s’exécute sous un débogueur. Définissez `s_isDebuggerCheckDisabledForTestPurposes` à `true` pour accéder aux API en dehors d’un débogueur.  
>   
>  Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toutes circonstances.  

## <a name="requirements"></a>Spécifications

**Namespace :** <xref:System.Windows.Diagnostics>

**Assembly :** PresentationCore (dans PresentationCore.dll)

**Versions du .NET framework :** disponible depuis 4.6.
