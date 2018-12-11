---
title: XmlDictionaryReaderQuotas
ms.date: 03/30/2017
ms.assetid: 9b4ca8b4-0a89-4758-97ab-528a8ce18f07
ms.openlocfilehash: 9bc519509b00383be333ac605688950d2709117c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153135"
---
# <a name="xmldictionaryreaderquotas"></a><span data-ttu-id="7498d-102">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="7498d-102">XmlDictionaryReaderQuotas</span></span>
<span data-ttu-id="7498d-103">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="7498d-103">XmlDictionaryReaderQuotas</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7498d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7498d-104">Syntax</span></span>  
  
```csharp
class XmlDictionaryReaderQuotas  
{  
  sint32 MaxArrayLength;  
  sint32 MaxBytesPerRead;  
  sint32 MaxDepth;  
  sint32 MaxNameTableCharCount;  
  sint32 MaxStringContentLength;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="7498d-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7498d-105">Methods</span></span>  
 <span data-ttu-id="7498d-106">La classe XmlDictionaryReaderQuotas ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="7498d-106">The XmlDictionaryReaderQuotas class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="7498d-107">Properties</span><span class="sxs-lookup"><span data-stu-id="7498d-107">Properties</span></span>  
 <span data-ttu-id="7498d-108">La classe XmlDictionaryReaderQuotas a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="7498d-108">The XmlDictionaryReaderQuotas class has the following properties:</span></span>  
  
### <a name="maxarraylength"></a><span data-ttu-id="7498d-109">MaxArrayLength</span><span class="sxs-lookup"><span data-stu-id="7498d-109">MaxArrayLength</span></span>  
 <span data-ttu-id="7498d-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="7498d-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="7498d-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7498d-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7498d-112">La longueur de tableau maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="7498d-112">The maximum allowed array length.</span></span>  
  
### <a name="maxbytesperread"></a><span data-ttu-id="7498d-113">MaxBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="7498d-113">MaxBytesPerRead</span></span>  
 <span data-ttu-id="7498d-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="7498d-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="7498d-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7498d-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7498d-116">Le nombre maximal d'octets autorisés retournés pour chaque lecture.</span><span class="sxs-lookup"><span data-stu-id="7498d-116">The maximum allowed bytes returned for each read.</span></span>  
  
### <a name="maxdepth"></a><span data-ttu-id="7498d-117">MaxDepth</span><span class="sxs-lookup"><span data-stu-id="7498d-117">MaxDepth</span></span>  
 <span data-ttu-id="7498d-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="7498d-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="7498d-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7498d-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7498d-120">Profondeur maximale de nœud imbriqué par lecture.</span><span class="sxs-lookup"><span data-stu-id="7498d-120">The maximum nested node depth for each read.</span></span>  
  
### <a name="maxnametablecharcount"></a><span data-ttu-id="7498d-121">MaxNameTableCharCount</span><span class="sxs-lookup"><span data-stu-id="7498d-121">MaxNameTableCharCount</span></span>  
 <span data-ttu-id="7498d-122">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="7498d-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="7498d-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7498d-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7498d-124">Le nombre maximal de caractères autorisés dans un nom de table.</span><span class="sxs-lookup"><span data-stu-id="7498d-124">The maximum characters allowed in a table name.</span></span>  
  
### <a name="maxstringcontentlength"></a><span data-ttu-id="7498d-125">MaxStringContentLength</span><span class="sxs-lookup"><span data-stu-id="7498d-125">MaxStringContentLength</span></span>  
 <span data-ttu-id="7498d-126">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="7498d-126">Data type: sint32</span></span>  
  
 <span data-ttu-id="7498d-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="7498d-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7498d-128">Nombre maximal de caractères autorisés dans un contenu d'élément XML.</span><span class="sxs-lookup"><span data-stu-id="7498d-128">The maximum characters allowed in XML element content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7498d-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7498d-129">Requirements</span></span>  
  
|<span data-ttu-id="7498d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7498d-130">MOF</span></span>|<span data-ttu-id="7498d-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="7498d-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="7498d-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7498d-132">Namespace</span></span>|<span data-ttu-id="7498d-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="7498d-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7498d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7498d-134">See Also</span></span>  
 <xref:System.Xml.XmlDictionaryReaderQuotas>  
 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>
