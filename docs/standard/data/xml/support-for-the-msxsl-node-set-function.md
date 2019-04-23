---
title: Prise en charge de la fonction msxsl:node-set()
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: d0cbf517-d9f6-4097-9851-4fa62903decd
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a37220816ab320340b2dd5c048cc4ff2ad9724a3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59330231"
---
# <a name="support-for-the-msxslnode-set-function"></a><span data-ttu-id="92518-102">Prise en charge de la fonction msxsl:node-set()</span><span class="sxs-lookup"><span data-stu-id="92518-102">Support for the msxsl:node-set() Function</span></span>
<span data-ttu-id="92518-103">La fonction `msxsl:node-set` vous permet de convertir un fragment d’arborescence résultat en une collection de nœuds.</span><span class="sxs-lookup"><span data-stu-id="92518-103">The `msxsl:node-set` function enables you to convert a result tree fragment into a node set.</span></span> <span data-ttu-id="92518-104">La collection de nœuds obtenue contient toujours un seul nœud et représente le nœud racine de l'arborescence.</span><span class="sxs-lookup"><span data-stu-id="92518-104">The resulting node set always contains a single node and is the root node of the tree.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="92518-105">La classe <xref:System.Xml.Xsl.XslTransform> est obsolète dans le [!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)].</span><span class="sxs-lookup"><span data-stu-id="92518-105">The <xref:System.Xml.Xsl.XslTransform> class is obsolete in the [!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)].</span></span> <span data-ttu-id="92518-106">Vous pouvez effectuer des transformations XSLT (Extensible Stylesheet Language Transformation) à l'aide de la classe <xref:System.Xml.Xsl.XslCompiledTransform>.</span><span class="sxs-lookup"><span data-stu-id="92518-106">You can perform Extensible Stylesheet Language for Transformations (XSLT) transformations using the <xref:System.Xml.Xsl.XslCompiledTransform> class.</span></span> <span data-ttu-id="92518-107">Pour plus d'informations, consultez [Utilisation de la classe XslCompiledTransform](../../../../docs/standard/data/xml/using-the-xslcompiledtransform-class.md) et [Migration depuis la classe XslTransform](../../../../docs/standard/data/xml/migrating-from-the-xsltransform-class.md).</span><span class="sxs-lookup"><span data-stu-id="92518-107">See [Using the XslCompiledTransform Class](../../../../docs/standard/data/xml/using-the-xslcompiledtransform-class.md) and [Migrating From the XslTransform Class](../../../../docs/standard/data/xml/migrating-from-the-xsltransform-class.md) for more information.</span></span>  
  
 <span data-ttu-id="92518-108">La fonction `msxsl:node-set` vous permet de convertir un fragment d’arborescence résultat en une collection de nœuds.</span><span class="sxs-lookup"><span data-stu-id="92518-108">The `msxsl:node-set` function enables you to convert a result tree fragment into a node set.</span></span> <span data-ttu-id="92518-109">La collection de nœuds obtenue contient toujours un seul nœud et représente le nœud racine de l'arborescence.</span><span class="sxs-lookup"><span data-stu-id="92518-109">The resulting node set always contains a single node and is the root node of the tree.</span></span>  
  
## <a name="example"></a><span data-ttu-id="92518-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="92518-110">Example</span></span>  
 <span data-ttu-id="92518-111">Dans l'exemple suivant, `$var` est une variable qui est une arborescence de nœuds dans la feuille de style.</span><span class="sxs-lookup"><span data-stu-id="92518-111">In the following example, `$var` is a variable that is a node tree in the style sheet.</span></span> <span data-ttu-id="92518-112">L'instruction for-each associée à la fonction `node-set` permet à l'utilisateur d'itérer sur cette arborescence de nœuds comme une collection de nœuds.</span><span class="sxs-lookup"><span data-stu-id="92518-112">The for-each statement combined with the `node-set` function allows the user to iterate over this node tree as a node set.</span></span>  
  
## <a name="nodesetxsl"></a><span data-ttu-id="92518-113">nodeset.xsl</span><span class="sxs-lookup"><span data-stu-id="92518-113">nodeset.xsl</span></span>  
  
```xml  
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform"  
                xmlns:msxsl="urn:schemas-microsoft-com:xslt"  
                xmlns:user="http://www.contoso.com"  
                version="1.0">  
    <xsl:variable name="books">  
        <book author="Michael Howard">Writing Secure Code</book>  
        <book author="Michael Kay">XSLT Reference</book>  
    </xsl:variable>  
  
    <xsl:template match="/">  
        <authors>  
            <xsl:for-each select="msxsl:node-set($books)/book">   
                <author><xsl:value-of select="@author"/></author>  
            </xsl:for-each>  
        </authors>  
    </xsl:template>  
</xsl:stylesheet>  
```  
  
## <a name="output"></a><span data-ttu-id="92518-114">Sortie</span><span class="sxs-lookup"><span data-stu-id="92518-114">Output</span></span>  
 <span data-ttu-id="92518-115">La sortie de la transformation est :</span><span class="sxs-lookup"><span data-stu-id="92518-115">The output of the transformation is</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<authors><author>Michael Howard</author><author>Michael Kay</author></authors>  
```  
  
## <a name="see-also"></a><span data-ttu-id="92518-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92518-116">See also</span></span>

- [<span data-ttu-id="92518-117">Implémentation du processeur XSLT par la classe XslTransform</span><span class="sxs-lookup"><span data-stu-id="92518-117">XslTransform Class Implements the XSLT Processor</span></span>](../../../../docs/standard/data/xml/xsltransform-class-implements-the-xslt-processor.md)
