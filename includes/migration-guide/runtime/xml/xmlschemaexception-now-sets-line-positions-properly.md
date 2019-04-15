---
ms.openlocfilehash: a5b3e325c13d2f56532ebc6ebb5c259d565a4952
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235365"
---
### <a name="xmlschemaexception-now-sets-line-positions-properly"></a><span data-ttu-id="0bbd8-101">XmlSchemaException définit désormais les positions de ligne correctement</span><span class="sxs-lookup"><span data-stu-id="0bbd8-101">XmlSchemaException now sets line positions properly</span></span>

|   |   |
|---|---|
|<span data-ttu-id="0bbd8-102">Détails</span><span class="sxs-lookup"><span data-stu-id="0bbd8-102">Details</span></span>|<span data-ttu-id="0bbd8-103">Si la valeur <xref:System.Xml.Linq.LoadOptions.SetLineInfo> est passée à la méthode Load et qu’une erreur de validation se produit, les propriétés <xref:System.Xml.Schema.XmlSchemaException.LineNumber> et <xref:System.Xml.Schema.XmlSchemaException.LinePosition> contiennent désormais les informations de ligne.</span><span class="sxs-lookup"><span data-stu-id="0bbd8-103">If the <xref:System.Xml.Linq.LoadOptions.SetLineInfo> value is passed to the Load method and a validation error occurs, the <xref:System.Xml.Schema.XmlSchemaException.LineNumber> and <xref:System.Xml.Schema.XmlSchemaException.LinePosition> properties now contain line information.</span></span>|
|<span data-ttu-id="0bbd8-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="0bbd8-104">Suggestion</span></span>|<span data-ttu-id="0bbd8-105">Le code de gestion des exceptions qui suppose que <xref:System.Xml.Schema.XmlSchemaException.LineNumber> et <xref:System.Xml.Schema.XmlSchemaException.LinePosition> ne seront pas définies doit être modifié, car ces propriétés seront maintenant définies correctement quand SetLineInfo est utilisé lors du chargement du code XML.</span><span class="sxs-lookup"><span data-stu-id="0bbd8-105">Exception-handling code that assumes <xref:System.Xml.Schema.XmlSchemaException.LineNumber> and <xref:System.Xml.Schema.XmlSchemaException.LinePosition> will not be set should be updated since these properties will now be set properly when SetLineInfo is used while loading XML.</span></span>|
|<span data-ttu-id="0bbd8-106">Portée</span><span class="sxs-lookup"><span data-stu-id="0bbd8-106">Scope</span></span>|<span data-ttu-id="0bbd8-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0bbd8-107">Edge</span></span>|
|<span data-ttu-id="0bbd8-108">Version</span><span class="sxs-lookup"><span data-stu-id="0bbd8-108">Version</span></span>|<span data-ttu-id="0bbd8-109">4.5</span><span class="sxs-lookup"><span data-stu-id="0bbd8-109">4.5</span></span>|
|<span data-ttu-id="0bbd8-110">Type</span><span class="sxs-lookup"><span data-stu-id="0bbd8-110">Type</span></span>|<span data-ttu-id="0bbd8-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="0bbd8-111">Runtime</span></span>|
|<span data-ttu-id="0bbd8-112">API affectées</span><span class="sxs-lookup"><span data-stu-id="0bbd8-112">Affected APIs</span></span>|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|
