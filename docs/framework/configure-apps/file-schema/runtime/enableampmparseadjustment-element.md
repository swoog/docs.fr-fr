---
title: Élément <EnableAmPmParseAdjustment>
ms.date: 03/30/2017
ms.assetid: fda998a5-f538-4f8b-a18c-ee7f35e16938
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b3316184aaa624fffdd18f472a7f3a709b42045a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269209"
---
# <a name="enableampmparseadjustment-element"></a><span data-ttu-id="902ef-102">\<EnableAmPmParseAdjustment > élément</span><span class="sxs-lookup"><span data-stu-id="902ef-102">\<EnableAmPmParseAdjustment> Element</span></span>
<span data-ttu-id="902ef-103">Détermine si date et l’heure de méthodes d’analyse utilisent un ensemble de règles ajusté pour analyser des chaînes de date qui contiennent un jour, un mois, une heure et un indicateur AM/PM.</span><span class="sxs-lookup"><span data-stu-id="902ef-103">Determines whether date and time parsing methods use an adjusted set of rules to parse date strings that contain a day, month, hour, and AM/PM designator.</span></span>  
  
 <span data-ttu-id="902ef-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="902ef-104">\<configuration></span></span>  
 <span data-ttu-id="902ef-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="902ef-105">\<runtime></span></span>  
<span data-ttu-id="902ef-106">\<EnableAmPmParseAdjustment></span><span class="sxs-lookup"><span data-stu-id="902ef-106">\<EnableAmPmParseAdjustment></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="902ef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="902ef-107">Syntax</span></span>  
  
```xml  
<EnableAmPmParseAdjustment enabled="0"|"1" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="902ef-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="902ef-108">Attributes and Elements</span></span>  
 <span data-ttu-id="902ef-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="902ef-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="902ef-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="902ef-110">Attributes</span></span>  
  
|<span data-ttu-id="902ef-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="902ef-111">Attribute</span></span>|<span data-ttu-id="902ef-112">Description</span><span class="sxs-lookup"><span data-stu-id="902ef-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="902ef-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="902ef-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="902ef-114">Spécifie si date et l’heure de méthodes d’analyse utilisent un ensemble de règles ajusté pour analyser des chaînes de date qui contiennent uniquement un jour, mois, les heures et indicateur AM/PM.</span><span class="sxs-lookup"><span data-stu-id="902ef-114">Specifies whether date and time parsing methods use an adjusted set of rules to parse date strings that contain only a day, month, hour, and AM/PM designator.</span></span>|  
  
### <a name="enabled-attribute"></a><span data-ttu-id="902ef-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="902ef-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="902ef-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="902ef-116">Value</span></span>|<span data-ttu-id="902ef-117">Description</span><span class="sxs-lookup"><span data-stu-id="902ef-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="902ef-118">0</span><span class="sxs-lookup"><span data-stu-id="902ef-118">0</span></span>|<span data-ttu-id="902ef-119">Date et heure de méthodes d’analyse n’utilisent pas de règles ajustés pour analyser les chaînes de date qui contiennent uniquement un jour, mois, les heures et indicateur AM/PM.</span><span class="sxs-lookup"><span data-stu-id="902ef-119">Date and time parsing methods do not use adjusted rules for parsing date strings that contain only a day, month, hour, and AM/PM designator.</span></span>|  
|<span data-ttu-id="902ef-120">1</span><span class="sxs-lookup"><span data-stu-id="902ef-120">1</span></span>|<span data-ttu-id="902ef-121">Date et heure de méthodes d’analyse utilisent règles ajustés pour analyser les chaînes de date qui contiennent uniquement un jour, mois, les heures et indicateur AM/PM.</span><span class="sxs-lookup"><span data-stu-id="902ef-121">Date and time parsing methods use adjusted rules for parsing date strings that contain only a day, month, hour, and AM/PM designator.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="902ef-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="902ef-122">Child Elements</span></span>  
 <span data-ttu-id="902ef-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="902ef-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="902ef-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="902ef-124">Parent Elements</span></span>  
  
|<span data-ttu-id="902ef-125">Élément</span><span class="sxs-lookup"><span data-stu-id="902ef-125">Element</span></span>|<span data-ttu-id="902ef-126">Description</span><span class="sxs-lookup"><span data-stu-id="902ef-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="902ef-127">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="902ef-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="902ef-128">Contient des informations sur les options d'initialisation du runtime.</span><span class="sxs-lookup"><span data-stu-id="902ef-128">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="902ef-129">Notes</span><span class="sxs-lookup"><span data-stu-id="902ef-129">Remarks</span></span>  
 <span data-ttu-id="902ef-130">Le `<EnableAmPmParseAdjustment>` élément contrôle comment les méthodes suivantes analysent une chaîne de date qui contient un numéro du jour et le mois, suivie d’une heure et un indicateur AM/PM (par exemple, « 4/10 6 h ») :</span><span class="sxs-lookup"><span data-stu-id="902ef-130">The `<EnableAmPmParseAdjustment>` element controls how the following methods parse a date string that contains a numeric day and month followed by an hour and an AM/PM designator (such as "4/10 6 AM"):</span></span>  
  
-   <xref:System.DateTime.Parse%2A?displayProperty=nameWithType>  
  
-   <xref:System.DateTimeOffset.Parse%2A?displayProperty=nameWithType>  
  
-   <xref:System.DateTime.TryParse%2A?displayProperty=nameWithType>  
  
-   <xref:System.DateTimeOffset.TryParse%2A?displayProperty=nameWithType>  
  
-   <xref:System.Convert.ToDateTime%2A?displayProperty=nameWithType>  
  
 <span data-ttu-id="902ef-131">Aucune des autres modèles ne sont affectés.</span><span class="sxs-lookup"><span data-stu-id="902ef-131">No other patterns are affected.</span></span>  
  
 <span data-ttu-id="902ef-132">Le `<EnableAmPmParseAdjustment>` élément n’a aucun effet le <xref:System.DateTime.ParseExact%2A?displayProperty=nameWithType>, <xref:System.DateTime.TryParseExact%2A?displayProperty=nameWithType>, <xref:System.DateTimeOffset.ParseExact%2A?displayProperty=nameWithType>, et <xref:System.DateTimeOffset.TryParseExact%2A?displayProperty=nameWithType> méthodes.</span><span class="sxs-lookup"><span data-stu-id="902ef-132">The `<EnableAmPmParseAdjustment>` element has no effect on the  <xref:System.DateTime.ParseExact%2A?displayProperty=nameWithType>,  <xref:System.DateTime.TryParseExact%2A?displayProperty=nameWithType>, <xref:System.DateTimeOffset.ParseExact%2A?displayProperty=nameWithType>, and <xref:System.DateTimeOffset.TryParseExact%2A?displayProperty=nameWithType> methods.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="902ef-133">Dans .NET Core et .NET Native, les règles d’analyse ajustées AM/PM sont activés par défaut.</span><span class="sxs-lookup"><span data-stu-id="902ef-133">In .NET Core and .NET Native, the adjusted AM/PM parsing rules are enabled by default.</span></span>  
  
 <span data-ttu-id="902ef-134">Si la règle d’ajustement analyse n’est pas activée, le premier chiffre de la chaîne est interprété comme l’heure de l’horloge de 12 heures, et le reste de la chaîne à l’exception de l’indicateur AM/PM est ignoré.</span><span class="sxs-lookup"><span data-stu-id="902ef-134">If the parsing adjustment rule is not enabled, the first digit of the string is interpreted as the hour of the 12-hour clock, and the remainder of the string except for the AM/PM designator is ignored.</span></span> <span data-ttu-id="902ef-135">La date et l’heure retournée par la méthode d’analyse se compose de la date actuelle et l’heure de la journée extraite à partir de la chaîne de date.</span><span class="sxs-lookup"><span data-stu-id="902ef-135">The date and time returned by the parsing method consists of the current date and the hour of the day extracted from the date string.</span></span>  
  
 <span data-ttu-id="902ef-136">Si la règle d’ajustement analyse est activée, la méthode d’analyse interpréter le jour et le mois comme appartenant à l’année en cours et interpréter le temps que l’heure de l’horloge de 12 heures.</span><span class="sxs-lookup"><span data-stu-id="902ef-136">If the parsing adjustment rule is enabled, parsing method interpret the day and month as belonging to the current year, and interpret the time as the hour of the 12-hour clock.</span></span>  
  
 <span data-ttu-id="902ef-137">Le tableau suivant illustre la différence entre la <xref:System.DateTime> valeur lorsque le <xref:System.DateTime.Parse%28System.String%29?displayProperty=nameWithType> méthode est utilisée pour analyser la chaîne « « 4/10 de 6 h » avec le `<EnableAmPmParseAdjustment>` l’élément `enabled` propriété la valeur « 0 » ou « 1 ».</span><span class="sxs-lookup"><span data-stu-id="902ef-137">The following table illustrates the difference in the <xref:System.DateTime> value when the <xref:System.DateTime.Parse%28System.String%29?displayProperty=nameWithType> method is used to parse the string ""4/10 6 AM" with the `<EnableAmPmParseAdjustment>` element's `enabled` property  set to "0" or "1".</span></span> <span data-ttu-id="902ef-138">Il suppose que la date du jour est le 5 janvier 2017 et affiche la date comme si elle est mise en forme à l’aide de la chaîne de format « G » de la culture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="902ef-138">It assumes that today's date is January 5, 2017, and displays the date as if it is formatted using the specified culture's "G" format string.</span></span>  
  
|<span data-ttu-id="902ef-139">Nom de culture</span><span class="sxs-lookup"><span data-stu-id="902ef-139">Culture name</span></span>|<span data-ttu-id="902ef-140">enabled="0"</span><span class="sxs-lookup"><span data-stu-id="902ef-140">enabled="0"</span></span>|<span data-ttu-id="902ef-141">enabled="1"</span><span class="sxs-lookup"><span data-stu-id="902ef-141">enabled="1"</span></span>|  
|------------------|------------------|------------------|  
|<span data-ttu-id="902ef-142">fr-FR</span><span class="sxs-lookup"><span data-stu-id="902ef-142">en-US</span></span>|<span data-ttu-id="902ef-143">1/5/2017 4:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="902ef-143">1/5/2017 4:00:00 AM</span></span>|<span data-ttu-id="902ef-144">4/10/2017 6:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="902ef-144">4/10/2017 6:00:00 AM</span></span>|  
|<span data-ttu-id="902ef-145">en-GB</span><span class="sxs-lookup"><span data-stu-id="902ef-145">en-GB</span></span>|<span data-ttu-id="902ef-146">5/1/2017 6:00:00</span><span class="sxs-lookup"><span data-stu-id="902ef-146">5/1/2017 6:00:00</span></span>|<span data-ttu-id="902ef-147">10/4/2017 6:00:00</span><span class="sxs-lookup"><span data-stu-id="902ef-147">10/4/2017 6:00:00</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="902ef-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="902ef-148">See also</span></span>
- [<span data-ttu-id="902ef-149">\<runtime > élément</span><span class="sxs-lookup"><span data-stu-id="902ef-149">\<runtime> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md)
- [<span data-ttu-id="902ef-150">\<configuration>, élément</span><span class="sxs-lookup"><span data-stu-id="902ef-150">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)
