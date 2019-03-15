---
title: '{} Échappement - Extension de balisage'
ms.date: 03/30/2017
f1_keywords:
- '{}'
helpviewer_keywords:
- XAML [XAML Services], quotation mark (")
- '{} escape sequence [XAML Services]'
- XAML [XAML Services], {} escape sequence
- XAML [XAML Services], escape sequence
- quotation mark (") [XAML Services]
- escape sequence [XAML Services]
ms.assetid: 3ce3e2ad-a868-43f9-9c98-b29561cb146e
ms.openlocfilehash: eaee0a1f92d8b7cb3810651eda21f1cc800ebf57
ms.sourcegitcommit: 5c1abeec15fbddcc7dbaa729fabc1f1f29f12045
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58018553"
---
# <a name="-escape-sequence--markup-extension"></a><span data-ttu-id="d4822-102">{} Séquence d’échappement / Extension de balisage</span><span class="sxs-lookup"><span data-stu-id="d4822-102">{} Escape Sequence / Markup Extension</span></span>
<span data-ttu-id="d4822-103">Fournit la séquence d’échappement XAML pour les valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d4822-103">Provides the XAML escape sequence for attribute values.</span></span> <span data-ttu-id="d4822-104">La séquence d’échappement autorise les valeurs suivantes dans l’attribut doit être interprété comme un littéral.</span><span class="sxs-lookup"><span data-stu-id="d4822-104">The escape sequence allows the subsequent values in the attribute to be interpreted as a literal.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="d4822-105">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="d4822-105">XAML Attribute Usage</span></span>  
  
```xml  
<object property="{} literalValue" .../>  
```  
  
## <a name="xaml-property-element-usage"></a><span data-ttu-id="d4822-106">Utilisation des éléments de propriété XAML</span><span class="sxs-lookup"><span data-stu-id="d4822-106">XAML Property Element Usage</span></span>  
  
```  
<object>  
  <object.property>  
    {} literalValue  
  </object.property>  
</object>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="d4822-107">Valeurs XAML</span><span class="sxs-lookup"><span data-stu-id="d4822-107">XAML Values</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d4822-108">*literalValue*</span><span class="sxs-lookup"><span data-stu-id="d4822-108">*literalValue*</span></span>|<span data-ttu-id="d4822-109">La chaîne littérale qui suit la séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="d4822-109">The literal string that follows the escape sequence.</span></span> <span data-ttu-id="d4822-110">En général, cette chaîne contient une accolade ouvrante ou fermante ({ou}).</span><span class="sxs-lookup"><span data-stu-id="d4822-110">Typically this string contains an open or close brace ({ or }).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d4822-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d4822-111">Remarks</span></span>  
 <span data-ttu-id="d4822-112">La séquence d’échappement ({}) est utilisé afin qu’une accolade ouvrante ({}) peut être utilisée comme un caractère littéral dans XAML.</span><span class="sxs-lookup"><span data-stu-id="d4822-112">The escape sequence ({}) is used so that an open brace ({)can be used as a literal character in XAML.</span></span>  
  
 <span data-ttu-id="d4822-113">Les lecteurs XAML utilisent généralement l’accolade ouvrante ({}) pour indiquer le point d’entrée d’une extension de balisage ; toutefois, ils vérifient d’abord le caractère suivant pour déterminer s’il s’agit d’une accolade fermante (}).</span><span class="sxs-lookup"><span data-stu-id="d4822-113">XAML readers typically use the open brace ({) to denote the entry point of a markup extension; however, they first check the next character to determine whether it is a closing brace (}).</span></span> <span data-ttu-id="d4822-114">Uniquement lorsque les deux accolades ({}) sont adjacente, sont elles considérées comme une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="d4822-114">Only when the two braces ({}) are adjacent, are they considered an escape sequence.</span></span>  
  
 <span data-ttu-id="d4822-115">Si la séquence d’échappement est rencontrée, le lecteur XAML doit traiter le reste de la chaîne sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d4822-115">If the escape sequence is encountered, the XAML reader should process the remainder of the string as a string.</span></span> <span data-ttu-id="d4822-116">Toutefois, si la séquence d’échappement est appliquée à un membre qui a un convertisseur de type, la chaîne peut subir une conversion de type lorsqu’il est interprété par un writer XAML.</span><span class="sxs-lookup"><span data-stu-id="d4822-116">However, if the escape sequence is applied to a member that has a type converter, the string might undergo type conversion when it is interpreted by a XAML writer.</span></span>  
  
 <span data-ttu-id="d4822-117">La séquence d’échappement n’est pas une extension de balisage et n’est pas stockée par une classe.</span><span class="sxs-lookup"><span data-stu-id="d4822-117">The escape sequence is not a markup extension and is not backed by a class.</span></span> <span data-ttu-id="d4822-118">Toutefois, il est une convention qui respectent les lecteurs XAML (y compris les lecteurs XAML personnalisés).</span><span class="sxs-lookup"><span data-stu-id="d4822-118">However, it is a convention that XAML readers (including custom XAML readers) should respect.</span></span>  
  
 <span data-ttu-id="d4822-119">Un guillemet (") ne peut pas être utilisé comme une séquence d’échappement de cette manière.</span><span class="sxs-lookup"><span data-stu-id="d4822-119">A quotation mark (") cannot be used as an escape sequence in this manner.</span></span> <span data-ttu-id="d4822-120">Si vous avez besoin définir un guillemet comme une valeur de propriété pour une propriété de non-contenu, utilisez la syntaxe d’élément de propriété et placez le guillemet sous forme de chaîne à l’intérieur de l’élément de propriété ou utiliser une entité de caractère XML.</span><span class="sxs-lookup"><span data-stu-id="d4822-120">If you need to set a quotation mark as a property value for a noncontent property, use property element syntax and place the quotation mark as a string inside the property element, or use an XML character entity.</span></span> <span data-ttu-id="d4822-121">Pour une propriété de contenu, le guillemet peut être l’intégralité du contenu.</span><span class="sxs-lookup"><span data-stu-id="d4822-121">For a content property, the quotation mark can be the entire content.</span></span>  
  
 <span data-ttu-id="d4822-122">La séquence d’échappement ({}) est souvent nécessaire lors de la spécification d’un type XML qui doit inclure un qualificateur d’espace de noms dans un emplacement où une extension de balisage XAML peut apparaître.</span><span class="sxs-lookup"><span data-stu-id="d4822-122">The escape sequence ({}) is frequently required when specifying an XML type that must include a namespace qualifier in a location where a XAML markup extension might appear.</span></span> <span data-ttu-id="d4822-123">Cela inclut le début d’une valeur d’attribut XAML et dans une extension de balisage, immédiatement après un signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="d4822-123">This includes the start of a XAML attribute value, and in a markup extension, immediately after an equal sign (=).</span></span> <span data-ttu-id="d4822-124">L’exemple suivant montre des séquences d’échappement pour un espace de noms XML qui apparaît au début d’une valeur d’attribut XAML.</span><span class="sxs-lookup"><span data-stu-id="d4822-124">The following example shows escape sequences for an XML namespace that appears at the start of a XAML attribute value.</span></span>  
  
 [!code-xaml[XLINQExample#StackPanelResources](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#stackpanelresources)]  
  
## <a name="see-also"></a><span data-ttu-id="d4822-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4822-125">See also</span></span>
- [<span data-ttu-id="d4822-126">Convertisseurs de types et extensions de balisage pour XAML</span><span class="sxs-lookup"><span data-stu-id="d4822-126">Type Converters and Markup Extensions for XAML</span></span>](type-converters-and-markup-extensions-for-xaml.md)
- [<span data-ttu-id="d4822-127">Entités de caractères XML et XAML</span><span class="sxs-lookup"><span data-stu-id="d4822-127">XML Character Entities and XAML</span></span>](xml-character-entities-and-xaml.md)
