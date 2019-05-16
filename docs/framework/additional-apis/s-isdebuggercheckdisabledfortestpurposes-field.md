---
title: s_isDebuggerCheckDisabledForTestPurposes, champ
ms.date: 03/30/2017
ms.technology: dotnet-wpf
topic_type:
- apiref
api_name:
- System.Windows.Diagnostics.VisualDiagnostics.s_isDebuggerCheckDisabledForTestPurposes
api_location:
- PresentationCore.dll
api_type:
- Assembly
ms.assetid: 9033a513-c255-4f31-b6d7-09b8d8c50e2d
ms.openlocfilehash: ad9bc0ecf4b7a8e5f3ef13fdff5aa59ca8915922
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65634657"
---
# <a name="sisdebuggercheckdisabledfortestpurposes-field"></a>s_isDebuggerCheckDisabledForTestPurposes, champ

Ce champ privé dans le `System.Windows.Diagnostics.VisualDiagnostics` classe est utilisée par Visual Studio pour déterminer si une vérification interne de débogueur actif sera effectuée.

## <a name="syntax"></a>Syntaxe

```csharp
private static bool s_isDebuggerCheckDisabledForTestPurposes
```

> [!WARNING]
> API dans le `System.Windows.Diagnostics.VisualDiagnostics` classe sont disponibles uniquement quand une application s’exécute sous un débogueur. Définissez `s_isDebuggerCheckDisabledForTestPurposes` à `true` pour accéder aux API en dehors d’un débogueur.
>
> Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.

## <a name="requirements"></a>Configuration requise

**Espace de noms :** <xref:System.Windows.Diagnostics>

**Assembly :** PresentationCore (dans PresentationCore.dll)

**Versions du .NET framework :** Disponible à partir de 4.6.
