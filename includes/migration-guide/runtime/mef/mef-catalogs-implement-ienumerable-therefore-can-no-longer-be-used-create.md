---
ms.openlocfilehash: 4cc91e7c6054fdb8e96cecf7120df5b9f25de56c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235288"
---
### <a name="mef-catalogs-implement-ienumerable-and-therefore-can-no-longer-be-used-to-create-a-serializer"></a><span data-ttu-id="74bac-101">Les catalogues MEF implémentent IEnumerable et ne peuvent donc plus être utilisés pour créer un sérialiseur</span><span class="sxs-lookup"><span data-stu-id="74bac-101">MEF catalogs implement IEnumerable and therefore can no longer be used to create a serializer</span></span>

|   |   |
|---|---|
|<span data-ttu-id="74bac-102">Détails</span><span class="sxs-lookup"><span data-stu-id="74bac-102">Details</span></span>|<span data-ttu-id="74bac-103">À compter de .NET Framework 4.5, les catalogues MEF implémentent IEnumerable et ne peuvent donc plus être utilisés pour créer un sérialiseur (objet <xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>).</span><span class="sxs-lookup"><span data-stu-id="74bac-103">Starting with the .NET Framework 4.5, MEF catalogs implement IEnumerable and therefore can no longer be used to create a serializer (<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name> object).</span></span> <span data-ttu-id="74bac-104">La tentative de sérialisation d'un catalogue MEF lève une exception.</span><span class="sxs-lookup"><span data-stu-id="74bac-104">Trying to serialize a MEF catalog throws an exception.</span></span>|
|<span data-ttu-id="74bac-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="74bac-105">Suggestion</span></span>|<span data-ttu-id="74bac-106">Ne peut plus utiliser un catalogue MEF pour créer un sérialiseur</span><span class="sxs-lookup"><span data-stu-id="74bac-106">Can no longer use MEF to create a serializer</span></span>|
|<span data-ttu-id="74bac-107">Portée</span><span class="sxs-lookup"><span data-stu-id="74bac-107">Scope</span></span>|<span data-ttu-id="74bac-108">Majeur</span><span class="sxs-lookup"><span data-stu-id="74bac-108">Major</span></span>|
|<span data-ttu-id="74bac-109">Version</span><span class="sxs-lookup"><span data-stu-id="74bac-109">Version</span></span>|<span data-ttu-id="74bac-110">4.5</span><span class="sxs-lookup"><span data-stu-id="74bac-110">4.5</span></span>|
|<span data-ttu-id="74bac-111">Type</span><span class="sxs-lookup"><span data-stu-id="74bac-111">Type</span></span>|<span data-ttu-id="74bac-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="74bac-112">Runtime</span></span>|
