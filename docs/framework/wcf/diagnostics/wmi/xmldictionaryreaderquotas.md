---
title: XmlDictionaryReaderQuotas
ms.date: 03/30/2017
ms.assetid: 9b4ca8b4-0a89-4758-97ab-528a8ce18f07
ms.openlocfilehash: 78914d52a9e57fe2e48adcfc0d7b6f911a0d8b3a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33487826"
---
# <a name="xmldictionaryreaderquotas"></a><span data-ttu-id="2d1da-102">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="2d1da-102">XmlDictionaryReaderQuotas</span></span>
<span data-ttu-id="2d1da-103">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="2d1da-103">XmlDictionaryReaderQuotas</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d1da-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d1da-104">Syntax</span></span>  
  
```  
class XmlDictionaryReaderQuotas  
{  
  sint32 MaxArrayLength;  
  sint32 MaxBytesPerRead;  
  sint32 MaxDepth;  
  sint32 MaxNameTableCharCount;  
  sint32 MaxStringContentLength;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="2d1da-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d1da-105">Methods</span></span>  
 <span data-ttu-id="2d1da-106">La classe XmlDictionaryReaderQuotas ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="2d1da-106">The XmlDictionaryReaderQuotas class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="2d1da-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d1da-107">Properties</span></span>  
 <span data-ttu-id="2d1da-108">La classe XmlDictionaryReaderQuotas a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d1da-108">The XmlDictionaryReaderQuotas class has the following properties:</span></span>  
  
### <a name="maxarraylength"></a><span data-ttu-id="2d1da-109">MaxArrayLength</span><span class="sxs-lookup"><span data-stu-id="2d1da-109">MaxArrayLength</span></span>  
 <span data-ttu-id="2d1da-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="2d1da-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="2d1da-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d1da-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2d1da-112">La longueur de tableau maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="2d1da-112">The maximum allowed array length.</span></span>  
  
### <a name="maxbytesperread"></a><span data-ttu-id="2d1da-113">MaxBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="2d1da-113">MaxBytesPerRead</span></span>  
 <span data-ttu-id="2d1da-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="2d1da-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="2d1da-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d1da-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2d1da-116">Le nombre maximal d'octets autorisés retournés pour chaque lecture.</span><span class="sxs-lookup"><span data-stu-id="2d1da-116">The maximum allowed bytes returned for each read.</span></span>  
  
### <a name="maxdepth"></a><span data-ttu-id="2d1da-117">MaxDepth</span><span class="sxs-lookup"><span data-stu-id="2d1da-117">MaxDepth</span></span>  
 <span data-ttu-id="2d1da-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="2d1da-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="2d1da-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d1da-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2d1da-120">Profondeur maximale de nœud imbriqué par lecture.</span><span class="sxs-lookup"><span data-stu-id="2d1da-120">The maximum nested node depth for each read.</span></span>  
  
### <a name="maxnametablecharcount"></a><span data-ttu-id="2d1da-121">MaxNameTableCharCount</span><span class="sxs-lookup"><span data-stu-id="2d1da-121">MaxNameTableCharCount</span></span>  
 <span data-ttu-id="2d1da-122">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="2d1da-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="2d1da-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d1da-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2d1da-124">Le nombre maximal de caractères autorisés dans un nom de table.</span><span class="sxs-lookup"><span data-stu-id="2d1da-124">The maximum characters allowed in a table name.</span></span>  
  
### <a name="maxstringcontentlength"></a><span data-ttu-id="2d1da-125">MaxStringContentLength</span><span class="sxs-lookup"><span data-stu-id="2d1da-125">MaxStringContentLength</span></span>  
 <span data-ttu-id="2d1da-126">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="2d1da-126">Data type: sint32</span></span>  
  
 <span data-ttu-id="2d1da-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d1da-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2d1da-128">Nombre maximal de caractères autorisés dans un contenu d'élément XML.</span><span class="sxs-lookup"><span data-stu-id="2d1da-128">The maximum characters allowed in XML element content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d1da-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2d1da-129">Requirements</span></span>  
  
|<span data-ttu-id="2d1da-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2d1da-130">MOF</span></span>|<span data-ttu-id="2d1da-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="2d1da-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="2d1da-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d1da-132">Namespace</span></span>|<span data-ttu-id="2d1da-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="2d1da-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2d1da-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d1da-134">See Also</span></span>  
 <xref:System.Xml.XmlDictionaryReaderQuotas>  
 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>
