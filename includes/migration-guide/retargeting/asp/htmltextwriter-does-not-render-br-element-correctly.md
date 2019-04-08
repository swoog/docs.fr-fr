---
ms.openlocfilehash: 0ab6be6f2c6d8ebbe67051e4e3f967a325e654c8
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58761008"
---
### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>HtmlTextWriter n’effectue pas correctement le rendu de l’élément `<br/>`

|   |   |
|---|---|
|Détails|À compter de la version 4.6 du .NET Framework, l’appel de <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> et <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> avec un élément <code>&lt;BR /&gt;</code> aboutit à l’insertion d’un seul <code>&lt;BR /&gt;</code> (au lieu de deux).|
|Suggestion|Si une application dépendait de la balise <code>&lt;BR /&gt;</code> supplémentaire, <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> doit être appelé une deuxième fois. Notez que ce changement de comportement affecte uniquement les applications qui ciblent .NET Framework 4.6 ou les versions ultérieures. Vous pouvez donc également cibler une version antérieure du .NET Framework pour obtenir l’ancien comportement.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

