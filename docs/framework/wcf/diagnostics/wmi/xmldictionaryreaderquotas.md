---
title: XmlDictionaryReaderQuotas
ms.date: 03/30/2017
ms.assetid: 9b4ca8b4-0a89-4758-97ab-528a8ce18f07
ms.openlocfilehash: f1c12a0a60397a84d4e9ff0241c4182b4511af5c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61858427"
---
# <a name="xmldictionaryreaderquotas"></a><span data-ttu-id="e85a5-102">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="e85a5-102">XmlDictionaryReaderQuotas</span></span>
<span data-ttu-id="e85a5-103">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="e85a5-103">XmlDictionaryReaderQuotas</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e85a5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e85a5-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="e85a5-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e85a5-105">Methods</span></span>  
 <span data-ttu-id="e85a5-106">La classe XmlDictionaryReaderQuotas ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="e85a5-106">The XmlDictionaryReaderQuotas class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="e85a5-107">Properties</span><span class="sxs-lookup"><span data-stu-id="e85a5-107">Properties</span></span>  
 <span data-ttu-id="e85a5-108">La classe XmlDictionaryReaderQuotas a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e85a5-108">The XmlDictionaryReaderQuotas class has the following properties:</span></span>  
  
### <a name="maxarraylength"></a><span data-ttu-id="e85a5-109">MaxArrayLength</span><span class="sxs-lookup"><span data-stu-id="e85a5-109">MaxArrayLength</span></span>  
 <span data-ttu-id="e85a5-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="e85a5-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="e85a5-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e85a5-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e85a5-112">La longueur de tableau maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="e85a5-112">The maximum allowed array length.</span></span>  
  
### <a name="maxbytesperread"></a><span data-ttu-id="e85a5-113">MaxBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="e85a5-113">MaxBytesPerRead</span></span>  
 <span data-ttu-id="e85a5-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="e85a5-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="e85a5-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e85a5-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e85a5-116">Le nombre maximal d'octets autorisés retournés pour chaque lecture.</span><span class="sxs-lookup"><span data-stu-id="e85a5-116">The maximum allowed bytes returned for each read.</span></span>  
  
### <a name="maxdepth"></a><span data-ttu-id="e85a5-117">MaxDepth</span><span class="sxs-lookup"><span data-stu-id="e85a5-117">MaxDepth</span></span>  
 <span data-ttu-id="e85a5-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="e85a5-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="e85a5-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e85a5-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e85a5-120">Profondeur maximale de nœud imbriqué par lecture.</span><span class="sxs-lookup"><span data-stu-id="e85a5-120">The maximum nested node depth for each read.</span></span>  
  
### <a name="maxnametablecharcount"></a><span data-ttu-id="e85a5-121">MaxNameTableCharCount</span><span class="sxs-lookup"><span data-stu-id="e85a5-121">MaxNameTableCharCount</span></span>  
 <span data-ttu-id="e85a5-122">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="e85a5-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="e85a5-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e85a5-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e85a5-124">Le nombre maximal de caractères autorisés dans un nom de table.</span><span class="sxs-lookup"><span data-stu-id="e85a5-124">The maximum characters allowed in a table name.</span></span>  
  
### <a name="maxstringcontentlength"></a><span data-ttu-id="e85a5-125">MaxStringContentLength</span><span class="sxs-lookup"><span data-stu-id="e85a5-125">MaxStringContentLength</span></span>  
 <span data-ttu-id="e85a5-126">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="e85a5-126">Data type: sint32</span></span>  
  
 <span data-ttu-id="e85a5-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e85a5-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e85a5-128">Nombre maximal de caractères autorisés dans un contenu d'élément XML.</span><span class="sxs-lookup"><span data-stu-id="e85a5-128">The maximum characters allowed in XML element content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e85a5-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e85a5-129">Requirements</span></span>  
  
|<span data-ttu-id="e85a5-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e85a5-130">MOF</span></span>|<span data-ttu-id="e85a5-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="e85a5-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="e85a5-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e85a5-132">Namespace</span></span>|<span data-ttu-id="e85a5-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="e85a5-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e85a5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e85a5-134">See also</span></span>

- <xref:System.Xml.XmlDictionaryReaderQuotas>
- <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>
