---
ms.openlocfilehash: 69b25db88c7580787bbb47fb0902b6bb072f8dde
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235374"
---
### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>Les assemblys compilés avec Regex.CompileToAssembly sont rompus entre 4.0 et 4.5

|   |   |
|---|---|
|Détails|Si un assembly d’expressions régulières compilées est généré avec .NET Framework 4.5 mais qu’il cible .NET Framework 4, toute tentative d’utiliser l’une des expressions régulières dans cet assembly sur un système sur lequel .NET Framework 4 est installé lève une exception.|
|Suggestion|Pour contourner ce problème, vous pouvez procéder de l'une des manières suivantes :<ul><li>Générez l’assembly qui contient les expressions régulières avec .NET Framework 4.</li><li>Utilisez une expression régulière interprétée.</li></ul>|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|
