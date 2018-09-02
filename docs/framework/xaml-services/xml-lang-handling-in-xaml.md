---
title: Gestion de xml:lang en XAML
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [XAML Services], xml:lang attribute
- xml:lang attribute [XAML Services]
- RFC 3066 standard [XAML Services]
- standards [XAML Services], RFC 3066
ms.assetid: 7aac0078-a1c5-41f8-b8b0-975510d9dca0
ms.openlocfilehash: 025e4b2865fe3938e5f1454f87e90bae7a85bcfd
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43399661"
---
# <a name="xmllang-handling-in-xaml"></a>Gestion de xml:lang en XAML
L’attribut `xml:lang` est un attribut [!INCLUDE[TLA2#tla_xml](../../../includes/tla2sharptla-xml-md.md)]qui déclare les informations de langue et de culture pour un élément dans XML. Cette même signification de l’attribut persiste en XAML. Toutefois, certaines considérations supplémentaires s’appliquent.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xaml  
<object xml:lang="rfc3066lang" />  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|*rfc3066lang*|Chaîne qui est dérivée de la [RFC 3066](https://go.microsoft.com/fwlink/?LinkId=132454) standard et identifie une langue ou une langue-région. Dans le dernier cas, la langue et la région sont séparées par un tiret. Pour plus d’informations sur les valeurs et le format, consultez <xref:System.Windows.Markup.XmlLanguage> .|  
  
## <a name="remarks"></a>Notes  
 La définition de l’attribut `xml:lang` en [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] est dérivée de `xml:lang` , défini comme un « attribut spécial » par le [!INCLUDE[TLA#tla_w3c](../../../includes/tlasharptla-w3c-md.md)] pour [!INCLUDE[TLA2#tla_xml](../../../includes/tla2sharptla-xml-md.md)]. Les informations de langue et de culture peuvent être traitées de différentes façons par les éléments, selon leurs implémentations. Toutefois, il n’existe aucun traitement [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] par défaut de l’attribut `xml:lang` .  
  
 La valeur par défaut de l’attribut `xml:lang` est une chaîne vide au niveau de l’attribut.  
  
 Les effets et la valeur de l’attribut `xml:lang` sont généralement transmis aux éléments enfants, quand ils sont interprétés par des systèmes qui agissent sur les valeurs `xml:lang` .  
  
 Lorsqu’elle est interprétée par les writers XAML des services XAML du .NET Framework, une valeur `xml:lang` peut créer des objets <xref:System.Windows.Markup.XmlLanguage> ou <xref:System.Globalization.CultureInfo> dans la représentation d’objet sous-jacente. Toutefois, ce comportement varie selon que la valeur spécifiée pour `xml:lang` est ou non une construction valide pour ces classes.  
  
 Les infrastructures peuvent créer des associations entre les propriétés définies par l’infrastructure et la signification de `xml:lang` dans XML en appliquant <xref:System.Windows.Markup.XmlLangPropertyAttribute> à la propriété.  
  
## <a name="wpf-usage-nodes"></a>Nœuds d’utilisation WPF  
 Pour les éléments qui sont des classes dérivées de <xref:System.Windows.FrameworkElement> ou <xref:System.Windows.FrameworkContentElement>, vous pouvez utiliser la propriété de dépendance <xref:System.Windows.FrameworkElement.Language%2A> équivalente à la place de l’attribut `xml:lang` . Par défaut, la propriété <xref:System.Windows.FrameworkElement.Language%2A> utilise « en-US » si elle n’est pas définie autrement via la propriété ou via le traitement de l’attribut `xml:lang` .  
  
## <a name="see-also"></a>Voir aussi  
 [Globalisation pour WPF](../../../docs/framework/wpf/advanced/globalization-for-wpf.md)
