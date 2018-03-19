---
title: "Remarques pour l'implémentation de la prise en charge du type XML"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 26b071f3-1261-47ef-8690-0717f5cd93c1
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 8c2706782ed1242ecdb5af1fdfab7a3f24e19236
ms.sourcegitcommit: 15316053918995cc1380163a7d7e7edd5c44e6d7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2018
---
# <a name="xml-type-support-implementation-notes"></a>Remarques pour l'implémentation de la prise en charge du type XML
Cette rubrique décrit certains détails de l'implémentation que vous souhaitez connaître.  
  
## <a name="list-mappings"></a>Mappages de liste  
 Les types <xref:System.Collections.IList>, <xref:System.Collections.ICollection>, <xref:System.Collections.IEnumerable>, **Type[]** et <xref:System.String> permettent de représenter des types de liste du langage XSD (XML Schema Definition).  
  
## <a name="union-mappings"></a>Mappages d'union  
 Les types d'union sont représentées à l'aide du type <xref:System.Xml.Schema.XmlAtomicValue> ou <xref:System.String>. Le type de source ou de destination doit donc toujours être un objet <xref:System.String> ou <xref:System.Xml.Schema.XmlAtomicValue>.  
  
 Si l'objet <xref:System.Xml.Schema.XmlSchemaDatatype> représente un type de liste, l'objet convertit la valeur de la chaîne d'entrée en une liste d'au moins un objet. Si l'objet <xref:System.Xml.Schema.XmlSchemaDatatype> représente un type d'union, il essaye ensuite d'analyser la valeur d'entrée comme un type de membre de l'union. Si la tentative d'analyse échoue, une tentative de conversion avec le membre suivant de l'union est effectuée jusqu'à ce que la conversion soit réussie ou qu'il n'y ait plus de types de membre pour essayer la conversion. Dans ce cas, une exception est levée.  
  
## <a name="differences-between-clr-and-xml-data-types"></a>Différences entre les types de données CLR et XML  
 Voici la description de certaines incompatibilités qui peuvent se produire entre les types de données CLR et XML et concernant la manière de les traiter.  
  
> [!NOTE]
>  Le `xs` préfixe est mappé à la http://www.w3.org/2001/XMLSchema et l’URI d’espace de noms.  
  
### <a name="systemtimespan-and-xsduration"></a>System.TimeSpan et xs:duration  
 Le type `xs:duration` est partiellement trié en ce sens que certaines valeurs de durée sont différentes mais équivalentes. Cela signifie que pour la valeur de type `xs:duration`, la valeur de 1 mois (P1M) est inférieure à 32 jours (P32D), supérieure à 27 jours (P27D) et équivalente à 28, 29 ou 30 jours.  
  
 La classe <xref:System.TimeSpan> ne prend pas en charge ce tri partiel. Par contre, elle détermine un nombre spécifique de jours pour un an et pour un mois, respectivement 365 jours et 30 jours.  
  
 Pour plus d’informations sur la `xs:duration` de type, consultez le W3C XML Schema Part 2 : Datatypes Recommendation à http://www.w3.org/TR/xmlschema-2/.  
  
### <a name="xstime-gregorian-date-types-and-systemdatetime"></a>xs:time, types de dates grégoriennes et System.DateTime  
 Lorsqu'une valeur `xs:time` est mappée à un objet <xref:System.DateTime>, le champ <xref:System.DateTime.MinValue> permet d'initialiser les propriétés de date de l'objet <xref:System.DateTime> (telles que <xref:System.DateTime.Year%2A>, <xref:System.DateTime.Month%2A> et <xref:System.DateTime.Day%2A>) à la valeur <xref:System.DateTime> la plus petite possible.  
  
 De même, des instances de `xs:gMonth`, `xs:gDay`, `xs:gYear`, `xs:gYearMonth` et `xs:gMonthDay` sont également mappées à un objet <xref:System.DateTime>. Les propriétés inutilisées de l'objet <xref:System.DateTime> sont initialisées sur celles de <xref:System.DateTime.MinValue>.  
  
> [!NOTE]
>  Vous ne pouvez pas compter sur la valeur <xref:System.DateTime.Year%2A?displayProperty=nameWithType> lorsque le contenu est de type `xs:gMonthDay`. La valeur <xref:System.DateTime.Year%2A?displayProperty=nameWithType> est toujours définie sur 1904 dans ce cas.  
  
### <a name="xsanyuri-and-systemuri"></a>xs:anyURI et System.Uri  
 Lorsqu'une instance de `xs:anyURI` qui représente un URI relatif est mappée à un objet <xref:System.Uri>, l'objet <xref:System.Uri> n'a pas d'URI de base.  
  
## <a name="see-also"></a>Voir aussi  
 [Prise en charge du type dans les classes System.Xml](../../../../docs/standard/data/xml/type-support-in-the-system-xml-classes.md)
