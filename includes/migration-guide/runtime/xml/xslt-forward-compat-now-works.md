---
ms.openlocfilehash: 2dd97fcce13ed1ac7baf4cd02f5881d31d7a9c4b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803837"
---
### <a name="xslt-forward-compat-now-works"></a>La compatibilité ascendante de XSLT fonctionne désormais

|   |   |
|---|---|
|Détails|Dans .NET Framework 4, la compatibilité ascendante de XSLT 1.0 avait les problèmes suivants :<ul><li>Le chargement d'une feuille de style échouait si sa version avait la valeur 2.0 et si l'analyseur rencontrait une construction XSLT 1.0 non reconnue.</li><li>La construction <code>xsl:sort</code> ne pouvait pas trier les données si la version de la feuille de style était définie sur 1.1.</li></ul>Dans le .NET Framework 4.5, ces problèmes ont été résolus et le mode de compatibilité ascendante de XSLT 1.0 fonctionne correctement.|
|Suggestion|La plupart des applications ne devraient pas être affectées, mais les données sont triées différemment dans certains cas maintenant que xsl:sort est respecté. Si <code>xsl:sort</code> est utilisé dans des feuilles de style 1.1, vérifiez que les applications ne dépendaient pas de l’ordre non trié des données. Si des applications s’appuient sur le comportement de tri de la version 4.0, supprimez <code>xsl:sort</code> de la feuille de style.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|
