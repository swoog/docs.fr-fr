---
ms.openlocfilehash: ad624a665dbe8e989ea05acc20213809e515e6ac
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803891"
---
### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>Génération de code incorrecte lors de la transmission et de la comparaison de valeurs UInt16

|   |   |
|---|---|
|Détails|En raison de modifications introduites dans .NET Framework 4.7, le code généré par le compilateur JIT dans les applications exécutées sur .NET Framework 4.7 compare parfois de façon incorrecte deux valeurs <code>T:System.UInt16</code>. Pour plus d’informations, consultez [Problème n°11508 : codegen incorrect non signalé lors de la transmission et de la comparaison d’arguments ushort](https://github.com/dotnet/coreclr/issues/11508) sur GitHub.com.|
|Suggestion|Si vous rencontrez des problèmes lors de la comparaison de valeurs non signées 16 bits dans .NET Framework 4.7, effectuez la mise à niveau vers .NET Framework 4.7.1.|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Runtime|
