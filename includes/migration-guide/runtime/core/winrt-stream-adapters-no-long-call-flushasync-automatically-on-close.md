---
ms.openlocfilehash: 60759e3d03137bb5983703cbf04719ba4946cb6e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803916"
---
### <a name="winrt-stream-adapters-no-long-call-flushasync-automatically-on-close"></a>Les adaptateurs de flux WinRT n’appellent plus FlushAsync automatiquement lors de la fermeture

|   |   |
|---|---|
|Détails|Dans les applications du Windows Store, les adaptateurs de flux Windows Runtime n’appellent plus la méthode FlushAsync à partir de la méthode Dispose.|
|Suggestion|Cette modification devrait être transparente. Les développeurs peuvent rétablir le comportement précédent en écrivant du code comme le suivant :<pre><code class="lang-csharp">using (var stream = GetWindowsRuntimeStream() as Stream)&#13;&#10;{&#13;&#10;// do something&#13;&#10;await stream.FlushAsync();&#13;&#10;}&#13;&#10;</code></pre>|
|Portée|Transparent|
|Version|4.5.1|
|Type|Runtime|
