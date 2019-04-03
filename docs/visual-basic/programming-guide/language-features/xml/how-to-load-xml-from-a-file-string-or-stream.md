---
title: 'Procédure : Charger XML à partir d’un fichier, une chaîne ou un Stream (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- XML [Visual Basic], loading
- LINQ to XML [Visual Basic], loading XML from files
ms.assetid: 2b02dcec-4cca-4575-b4ad-89ceb87b984c
ms.openlocfilehash: 2b9da2062068ef25c5df97ef19b1502999ea78ed
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58832136"
---
# <a name="how-to-load-xml-from-a-file-string-or-stream-visual-basic"></a><span data-ttu-id="2cde2-102">Procédure : Charger XML à partir d’un fichier, une chaîne ou un Stream (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2cde2-102">How to: Load XML from a File, String, or Stream (Visual Basic)</span></span>
<span data-ttu-id="2cde2-103">Vous pouvez créer [littéraux XML](../../../../visual-basic/language-reference/xml-literals/index.md) et les remplir avec le contenu d’une source externe, comme un fichier, une chaîne ou un flux de données à l’aide de plusieurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="2cde2-103">You can create [XML Literals](../../../../visual-basic/language-reference/xml-literals/index.md) and populate them with the contents from an external source such as a file, a string, or a stream by using several methods.</span></span> <span data-ttu-id="2cde2-104">Ces méthodes sont illustrées dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="2cde2-104">These methods are shown in the following examples.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-load-xml-from-a-file"></a><span data-ttu-id="2cde2-105">Charger XML à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="2cde2-105">To load XML from a file</span></span>  
  
-   <span data-ttu-id="2cde2-106">Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> objet à partir d’un fichier, utilisez le `Load` (méthode).</span><span class="sxs-lookup"><span data-stu-id="2cde2-106">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a file, use the `Load` method.</span></span> <span data-ttu-id="2cde2-107">Cette méthode peut prendre un chemin d’accès du fichier, un flux de texte ou un flux de données XML en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="2cde2-107">This method can take a file path, text stream, or XML stream as input.</span></span>  
  
     <span data-ttu-id="2cde2-108">L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XDocument.Load%28System.String%29> méthode pour remplir un <xref:System.Xml.Linq.XDocument> objet XML à partir d’un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="2cde2-108">The following code example shows the use of the <xref:System.Xml.Linq.XDocument.Load%28System.String%29> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from a text file.</span></span>  
  
     [!code-vb[VbXMLSamples#43](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples15.vb#43)]  
  
### <a name="to-load-xml-from-a-string"></a><span data-ttu-id="2cde2-109">Charger XML à partir d’une chaîne</span><span class="sxs-lookup"><span data-stu-id="2cde2-109">To load XML from a string</span></span>  
  
-   <span data-ttu-id="2cde2-110">Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> de l’objet d’une chaîne, vous pouvez utiliser le `Parse` (méthode).</span><span class="sxs-lookup"><span data-stu-id="2cde2-110">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a string, you can use the `Parse` method.</span></span>  
  
     <span data-ttu-id="2cde2-111">L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=nameWithType> méthode pour remplir un <xref:System.Xml.Linq.XDocument> objet avec le code XML à partir d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="2cde2-111">The following code example shows the use of the <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=nameWithType> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from a string.</span></span>  
  
     [!code-vb[VbXMLSamples#47](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples15.vb#47)]  
  
### <a name="to-load-xml-from-a-stream"></a><span data-ttu-id="2cde2-112">Charger XML à partir d’un flux de données</span><span class="sxs-lookup"><span data-stu-id="2cde2-112">To load XML from a stream</span></span>  
  
-   <span data-ttu-id="2cde2-113">Pour remplir un littéral XML tel qu’un <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> de l’objet à partir d’un flux, vous pouvez utiliser la `Load` méthode ou le <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="2cde2-113">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a stream, you can use the `Load` method or the <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="2cde2-114">L’exemple de code suivant illustre l’utilisation de la <xref:System.Xml.Linq.XNode.ReadFrom%2A> méthode pour remplir un <xref:System.Xml.Linq.XDocument> objet XML à partir d’un flux XML.</span><span class="sxs-lookup"><span data-stu-id="2cde2-114">The following code example shows the use of the <xref:System.Xml.Linq.XNode.ReadFrom%2A> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from an XML stream.</span></span>  
  
 [!code-vb[VbXMLSamples#46](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples15.vb#46)]  
  
## <a name="see-also"></a><span data-ttu-id="2cde2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cde2-115">See also</span></span>

- <xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=nameWithType>
- <xref:System.Xml.Linq.XElement.Load%2A?displayProperty=nameWithType>
- <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>
- <xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=nameWithType>
- <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=nameWithType>
- [<span data-ttu-id="2cde2-116">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="2cde2-116">XML Literals</span></span>](../../../../visual-basic/language-reference/xml-literals/index.md)
- [<span data-ttu-id="2cde2-117">XML</span><span class="sxs-lookup"><span data-stu-id="2cde2-117">XML</span></span>](../../../../visual-basic/programming-guide/language-features/xml/index.md)
- [<span data-ttu-id="2cde2-118">Manipulation de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2cde2-118">Manipulating XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)
