---
ms.openlocfilehash: 4c9fde24a4c3260cf5b9e265dfd03080c5cd1d04
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760844"
---
### <a name="stack-traces-obtained-when-using-portable-pdbs-now-include-source-file-and-line-information-if-requested"></a>Les traces obtenues durant l’utilisation de fichiers PDB portables incluent désormais les informations sur les lignes et les fichiers sources, si elles sont demandées

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.7.2, les traces obtenues durant l’utilisation de fichiers PDB portables incluent les informations sur les lignes et les fichiers sources quand elles sont demandées. Dans les versions antérieures de .NET Framework 4.7.2, les informations sur les lignes et les fichiers sources n’étaient pas disponibles pendant l’utilisation de fichiers PDB portables même si elles étaient explicitement demandées.|
|Suggestion|Pour les applications qui ciblent .NET Framework 4.7.2, vous pouvez refuser les informations sur les lignes et les fichiers sources durant l’utilisation de fichiers PDB portables en ajoutant le code suivant à la section <code>&lt;runtime&gt;</code> de votre fichier <code>app.config</code> :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Diagnostics.IgnorePortablePDBsInStackTraces=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Pour les applications qui ciblent des versions antérieures de .NET Framework mais qui s’exécutent sur .NET Framework 4.7.2 ou une version ultérieure, vous pouvez accepter les informations sur les lignes et les fichiers sources durant l’utilisation de fichiers PDB portables en ajoutant le code suivant à la section <code>&lt;runtime&gt;</code> de votre fichier <code>app.config</code> :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Diagnostics.IgnorePortablePDBsInStackTraces=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Diagnostics.StackTrace.%23ctor(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.StackTrace.%23ctor(System.Exception,System.Boolean)?displayProperty=nameWithType><li><xref:System.Diagnostics.StackTrace.%23ctor(System.Exception,System.Int32,System.Boolean)?displayProperty=nameWithType></li></ul>|

