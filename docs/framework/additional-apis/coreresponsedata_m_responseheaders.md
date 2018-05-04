---
title: Champ de CoreResponseData.m_ResponseHeaders
ms.date: 01/29/2018
topic_type:
- apiref
api_name:
- System.Net.CoreResponseData.m_ResponseHeaders
api_location:
- System.dll
api_type:
- Assembly
author: stevewhims
ms.openlocfilehash: ea93b70ae8e1a710b4208050d7ec823a28b218b7
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="coreresponsedatamresponseheaders-field"></a>CoreResponseData.m\_ResponseHeaders champ

`CoreResponseData.m_ResponseHeaders` est un <xref:System.Net.WebHeaderCollection> d’en-têtes associés à la réponse du serveur.

## <a name="syntax"></a>Syntaxe
  
```csharp
public WebHeaderCollection m_ResponseHeaders
```

> [!WARNING]
> Cette API n’est pas destinée à être utilisé directement dans votre code. Au lieu de cela, vous devez utiliser un <xref:System.Diagnostics.DiagnosticSource> raccordement du code de mise en réseau. Consultez [le Guide d’utilisation de DiagnosticSource](https://github.com/dotnet/corefx/blob/master/src/System.Diagnostics.DiagnosticSource/src/DiagnosticSourceUsersGuide.md).
> 
> Microsoft ne prend pas en charge l’utilisation de cette classe dans une application de production en toutes circonstances.

## <a name="requirements"></a>Spécifications

**Namespace :** <xref:System.Net>

**Assembly :** système (dans System.dll)

**Versions du .NET framework :** disponible depuis la version 2.0.
