---
title: "Comment : charger du code XML à partir d'un fichier, d'une chaîne ou d'un flux (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- XML [Visual Basic], loading
- LINQ to XML [Visual Basic], loading XML from files
ms.assetid: 2b02dcec-4cca-4575-b4ad-89ceb87b984c
ms.openlocfilehash: 241f6552e46d7689b42a409ba44bc747984773ca
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647629"
---
# <a name="how-to-load-xml-from-a-file-string-or-stream-visual-basic"></a>Comment : charger du code XML à partir d'un fichier, d'une chaîne ou d'un flux (Visual Basic)
Vous pouvez créer [littéraux XML](../../../../visual-basic/language-reference/xml-literals/index.md) et les remplir avec le contenu à partir d’une source externe, comme un fichier, une chaîne ou un flux de données à l’aide de plusieurs méthodes. Ces méthodes sont illustrées dans les exemples suivants.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-load-xml-from-a-file"></a>Charger XML à partir d’un fichier  
  
-   Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> objet à partir d’un fichier, utilisez le `Load` (méthode). Cette méthode peut prendre un chemin d’accès du fichier, un flux de texte ou un flux XML comme entrée.  
  
     L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XDocument.Load%28System.String%29> méthode pour remplir un <xref:System.Xml.Linq.XDocument> objet avec les données XML à partir d’un fichier texte.  
  
     [!code-vb[VbXMLSamples#43](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_1.vb)]  
  
### <a name="to-load-xml-from-a-string"></a>Charger XML à partir d’une chaîne  
  
-   Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> de l’objet d’une chaîne, vous pouvez utiliser la `Parse` (méthode).  
  
     L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=nameWithType> méthode pour remplir un <xref:System.Xml.Linq.XDocument> objet XML à partir d’une chaîne.  
  
     [!code-vb[VbXMLSamples#47](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_2.vb)]  
  
### <a name="to-load-xml-from-a-stream"></a>Charger XML à partir d’un flux de données  
  
-   Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> de l’objet à partir d’un flux de données, vous pouvez utiliser la `Load` méthode ou la <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=nameWithType> (méthode).  
  
 L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XNode.ReadFrom%2A> méthode pour remplir un <xref:System.Xml.Linq.XDocument> objet avec les données XML à partir d’un flux XML.  
  
 [!code-vb[VbXMLSamples#46](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_3.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=nameWithType>  
 <xref:System.Xml.Linq.XElement.Load%2A?displayProperty=nameWithType>  
 <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>  
 <xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=nameWithType>  
 <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=nameWithType>  
 [Littéraux XML](../../../../visual-basic/language-reference/xml-literals/index.md)  
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)  
 [Manipulation de code XML dans Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)
