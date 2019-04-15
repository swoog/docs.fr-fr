---
ms.openlocfilehash: b4e062fe3a00b76da144e706841f87b2a95888e5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234712"
---
### <a name="encoderparameter-ctor-is-obsolete"></a><span data-ttu-id="6d685-101">Le constructeur EncoderParameter est obsolète</span><span class="sxs-lookup"><span data-stu-id="6d685-101">EncoderParameter ctor is obsolete</span></span>

|   |   |
|---|---|
|<span data-ttu-id="6d685-102">Détails</span><span class="sxs-lookup"><span data-stu-id="6d685-102">Details</span></span>|<span data-ttu-id="6d685-103">Le constructeur <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> est désormais obsolète et génère des avertissements quand il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6d685-103">The <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> constructor is obsolete now and will introduce build warnings if used.</span></span>|
|<span data-ttu-id="6d685-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="6d685-104">Suggestion</span></span>|<span data-ttu-id="6d685-105">Même si le constructeur <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> continue de fonctionner, le constructeur suivant doit être utilisé à sa place pour éviter l’avertissement de génération indiquant qu’il est obsolète durant la recompilation du code avec les outils .NET Framework 4.5 : <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>.</span><span class="sxs-lookup"><span data-stu-id="6d685-105">Although the <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>constructor will continue to work, the following constructor should be used instead to avoid the obsolete build warning when re-compiling code with .NET Framework  4.5 tools: <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>.</span></span>|
|<span data-ttu-id="6d685-106">Portée</span><span class="sxs-lookup"><span data-stu-id="6d685-106">Scope</span></span>|<span data-ttu-id="6d685-107">Mineur</span><span class="sxs-lookup"><span data-stu-id="6d685-107">Minor</span></span>|
|<span data-ttu-id="6d685-108">Version</span><span class="sxs-lookup"><span data-stu-id="6d685-108">Version</span></span>|<span data-ttu-id="6d685-109">4.5</span><span class="sxs-lookup"><span data-stu-id="6d685-109">4.5</span></span>|
|<span data-ttu-id="6d685-110">Type</span><span class="sxs-lookup"><span data-stu-id="6d685-110">Type</span></span>|<span data-ttu-id="6d685-111">Reciblage</span><span class="sxs-lookup"><span data-stu-id="6d685-111">Retargeting</span></span>|
|<span data-ttu-id="6d685-112">API affectées</span><span class="sxs-lookup"><span data-stu-id="6d685-112">Affected APIs</span></span>|<ul><li><xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|
