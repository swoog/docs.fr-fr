---
title: s_isDebuggerCheckDisabledForTestPurposes, champ
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
ms.openlocfilehash: f490ccb4675a434e3f3336723e321f256b10093d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149174"
---
# <a name="sisdebuggercheckdisabledfortestpurposes-field"></a>s_isDebuggerCheckDisabledForTestPurposes, champ

Ce champ privé dans le `System.Windows.Diagnostics.VisualDiagnostics` classe est utilisée par Visual Studio pour déterminer si une vérification interne de débogueur actif sera effectuée.

## <a name="syntax"></a>Syntaxe
  
```csharp  
private static bool s_isDebuggerCheckDisabledForTestPurposes
```
  
> [!WARNING]
>  API dans le `System.Windows.Diagnostics.VisualDiagnostics` classe sont disponibles uniquement quand une application s’exécute sous un débogueur. Définissez `s_isDebuggerCheckDisabledForTestPurposes` à `true` pour accéder aux API en dehors d’un débogueur.  
>   
>  Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.  

## <a name="requirements"></a>Spécifications

**Espace de noms :** <xref:System.Windows.Diagnostics>

**Assembly :** PresentationCore (dans PresentationCore.dll)

**Versions du .NET framework :** Disponible à partir de 4.6.