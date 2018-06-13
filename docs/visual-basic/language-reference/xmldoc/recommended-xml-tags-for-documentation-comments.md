---
title: Étiquettes XML recommandées pour les commentaires de documentation (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlDocComment
helpviewer_keywords:
- tags, XML
- XML comments, recommended tags [Visual Basic]
- comments, recommended XML tags
ms.assetid: 294e0736-ff1e-498e-af83-6db71ed41a72
ms.openlocfilehash: 8f27a892117980e89fa7143b7e49551b9e8703f6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33604419"
---
# <a name="recommended-xml-tags-for-documentation-comments-visual-basic"></a><span data-ttu-id="cc4b7-102">Étiquettes XML recommandées pour les commentaires de documentation (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cc4b7-102">Recommended XML Tags for Documentation Comments (Visual Basic)</span></span>
<span data-ttu-id="cc4b7-103">Le compilateur Visual Basic peut traiter les commentaires de documentation dans votre code dans un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-103">The Visual Basic compiler can process documentation comments in your code to an XML file.</span></span> <span data-ttu-id="cc4b7-104">Vous pouvez utiliser des outils supplémentaires pour traiter le fichier XML dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-104">You can use additional tools to process the XML file into documentation.</span></span>  
  
 <span data-ttu-id="cc4b7-105">Commentaires XML sont autorisés sur les constructions de code tels que les types et membres de type.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-105">XML comments are allowed on code constructs such as types and type members.</span></span> <span data-ttu-id="cc4b7-106">Pour les types partiels, qu’une partie du type peut avoir des commentaires XML, bien qu’il n’existe aucune restriction sur le commentaire de ses membres.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-106">For partial types, only one part of the type can have XML comments, although there is no restriction on commenting its members.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cc4b7-107">Commentaires de documentation ne peut pas être appliqués aux espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-107">Documentation comments cannot be applied to namespaces.</span></span> <span data-ttu-id="cc4b7-108">La raison est qu’un espace de noms peut s’étendre sur plusieurs assemblys, et non tous les assemblys doit être chargé en même temps.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-108">The reason is that one namespace can span several assemblies, and not all assemblies have to be loaded at the same time.</span></span>  
  
 <span data-ttu-id="cc4b7-109">Le compilateur traite toute balise XML valid.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-109">The compiler processes any tag that is valid XML.</span></span> <span data-ttu-id="cc4b7-110">Les balises suivantes fournissent des fonctionnalités couramment utilisées dans la documentation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-110">The following tags provide commonly used functionality in user documentation.</span></span>  
  
||||  
|---|---|---|  
|[<span data-ttu-id="cc4b7-111">\<c></span><span class="sxs-lookup"><span data-stu-id="cc4b7-111">\<c></span></span>](../../../visual-basic/language-reference/xmldoc/c.md)|[<span data-ttu-id="cc4b7-112">\<code></span><span class="sxs-lookup"><span data-stu-id="cc4b7-112">\<code></span></span>](../../../visual-basic/language-reference/xmldoc/code.md)|[<span data-ttu-id="cc4b7-113">\<example></span><span class="sxs-lookup"><span data-stu-id="cc4b7-113">\<example></span></span>](../../../visual-basic/language-reference/xmldoc/example.md)|  
|<span data-ttu-id="cc4b7-114">[\<exception >](../../../visual-basic/language-reference/xmldoc/exception.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="cc4b7-114">[\<exception>](../../../visual-basic/language-reference/xmldoc/exception.md) <sup>1</sup></span></span>|<span data-ttu-id="cc4b7-115">[\<Inclure >](../../../visual-basic/language-reference/xmldoc/include.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="cc4b7-115">[\<include>](../../../visual-basic/language-reference/xmldoc/include.md) <sup>1</sup></span></span>|[<span data-ttu-id="cc4b7-116">\<list></span><span class="sxs-lookup"><span data-stu-id="cc4b7-116">\<list></span></span>](../../../visual-basic/language-reference/xmldoc/list.md)|  
|[<span data-ttu-id="cc4b7-117">\<para></span><span class="sxs-lookup"><span data-stu-id="cc4b7-117">\<para></span></span>](../../../visual-basic/language-reference/xmldoc/para.md)|<span data-ttu-id="cc4b7-118">[\<param >](../../../visual-basic/language-reference/xmldoc/param.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="cc4b7-118">[\<param>](../../../visual-basic/language-reference/xmldoc/param.md) <sup>1</sup></span></span>|[<span data-ttu-id="cc4b7-119">\<paramref></span><span class="sxs-lookup"><span data-stu-id="cc4b7-119">\<paramref></span></span>](../../../visual-basic/language-reference/xmldoc/paramref.md)|  
|<span data-ttu-id="cc4b7-120">[\<autorisation >](../../../visual-basic/language-reference/xmldoc/permission.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="cc4b7-120">[\<permission>](../../../visual-basic/language-reference/xmldoc/permission.md) <sup>1</sup></span></span>|[<span data-ttu-id="cc4b7-121">\<remarks></span><span class="sxs-lookup"><span data-stu-id="cc4b7-121">\<remarks></span></span>](../../../visual-basic/language-reference/xmldoc/remarks.md)|[<span data-ttu-id="cc4b7-122">\<returns></span><span class="sxs-lookup"><span data-stu-id="cc4b7-122">\<returns></span></span>](../../../visual-basic/language-reference/xmldoc/returns.md)|  
|<span data-ttu-id="cc4b7-123">[\<consultez >](../../../visual-basic/language-reference/xmldoc/see.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="cc4b7-123">[\<see>](../../../visual-basic/language-reference/xmldoc/see.md) <sup>1</sup></span></span>|<span data-ttu-id="cc4b7-124">[\<seealso >](../../../visual-basic/language-reference/xmldoc/seealso.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="cc4b7-124">[\<seealso>](../../../visual-basic/language-reference/xmldoc/seealso.md) <sup>1</sup></span></span>|[<span data-ttu-id="cc4b7-125">\<summary></span><span class="sxs-lookup"><span data-stu-id="cc4b7-125">\<summary></span></span>](../../../visual-basic/language-reference/xmldoc/summary.md)|  
|<span data-ttu-id="cc4b7-126">[\<typeparam >](../../../visual-basic/language-reference/xmldoc/typeparam.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="cc4b7-126">[\<typeparam>](../../../visual-basic/language-reference/xmldoc/typeparam.md) <sup>1</sup></span></span>|[<span data-ttu-id="cc4b7-127">\<value></span><span class="sxs-lookup"><span data-stu-id="cc4b7-127">\<value></span></span>](../../../visual-basic/language-reference/xmldoc/value.md)||  
  
 <span data-ttu-id="cc4b7-128">(<sup>1</sup> le compilateur vérifie la syntaxe.)</span><span class="sxs-lookup"><span data-stu-id="cc4b7-128">(<sup>1</sup> The compiler verifies syntax.)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cc4b7-129">Si vous souhaitez des crochets pointus pour apparaître dans le texte d’un commentaire de documentation, utilisez `<` et `>`.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-129">If you want angle brackets to appear in the text of a documentation comment, use `<` and `>`.</span></span> <span data-ttu-id="cc4b7-130">Par exemple, la chaîne `"<text in angle brackets>"` apparaît sous la forme `<text in angle``brackets>`.</span><span class="sxs-lookup"><span data-stu-id="cc4b7-130">For example, the string `"<text in angle brackets>"` will appear as `<text in angle``brackets>`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc4b7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc4b7-131">See Also</span></span>  
 [<span data-ttu-id="cc4b7-132">Documentation de votre code avec le langage XML</span><span class="sxs-lookup"><span data-stu-id="cc4b7-132">Documenting Your Code with XML</span></span>](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)  
 [<span data-ttu-id="cc4b7-133">/doc</span><span class="sxs-lookup"><span data-stu-id="cc4b7-133">/doc</span></span>](../../../visual-basic/reference/command-line-compiler/doc.md)  
 [<span data-ttu-id="cc4b7-134">Guide pratique : créer une documentation XML</span><span class="sxs-lookup"><span data-stu-id="cc4b7-134">How to: Create XML Documentation</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)
