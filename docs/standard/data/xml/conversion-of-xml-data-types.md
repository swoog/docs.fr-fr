---
title: Conversion des types de données XML
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: a2aa99ba-8239-4818-9281-f1d72ee40bde
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cec2b85c55871c8a21a74e79cfcdd041fa063bec
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44262347"
---
# <a name="conversion-of-xml-data-types"></a>Conversion des types de données XML
La majorité des méthodes présentes dans la classe **XmlConvert** sont utilisées pour la conversion de données entre le format de chaînes et le format fortement typé. Ces méthodes sont indépendantes des paramètres régionaux. Cela signifie qu'elles ne prennent pas en compte les paramètres régionaux éventuels lors de la conversion.  
  
## <a name="reading-string-as-types"></a>Lecture de chaînes comme des types  
 L'exemple suivant lit une chaîne et la convertit en type **DateTime**.  
  
 En supposant l'entrée XML suivante :  
  
 **Entrée**  
  
```xml  
<Element>2001-02-27T11:13:23</Element>  
```  
  
 Ce code convertit la chaîne au format **DateTime** :  
  
```vb  
reader.ReadStartElement()  
Dim vDateTime As DateTime = XmlConvert.ToDateTime(reader.ReadString())  
Console.WriteLine(vDateTime)  
```  
  
```csharp  
reader.ReadStartElement();  
DateTime vDateTime = XmlConvert.ToDateTime(reader.ReadString());  
Console.WriteLine(vDateTime);  
```  
  
## <a name="writing-strings-as-types"></a>Écriture de chaînes comme des types  
 L'exemple suivant lit un type **Int32** et le convertit en chaîne.  
  
 En supposant l'entrée XML suivante :  
  
 **Entrée**  
  
```xml  
<TestInt32>-2147483648</TestInt32>  
```  
  
 Ce code convertit le type **Int32** en type **String**:  
  
```vb  
Dim vInt32 As Int32 = -2147483648  
writer.WriteElementString("TestInt32", XmlConvert.ToString(vInt32))  
```  
  
```csharp  
Int32 vInt32=-2147483648;  
writer.WriteElementString("TestInt32",XmlConvert.ToString(vInt32));  
```  
  
## <a name="see-also"></a>Voir aussi

- [Conversion de chaînes en types de données .NET Framework](../../../../docs/standard/data/xml/converting-strings-to-dotnet-data-types.md)  
- [Conversion de types .NET Framework en chaînes](../../../../docs/standard/data/xml/converting-dotnet-types-to-strings.md)
