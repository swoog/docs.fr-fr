---
title: 'Procédure : Créer une Documentation XML en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- XML comments
- XML documentation [Visual Basic], creating
ms.assetid: 27b5b06c-09b9-496a-8245-f9542d846230
ms.openlocfilehash: d67724aad6cd3e7af30531328d85e89937390dd1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54551369"
---
# <a name="how-to-create-xml-documentation-in-visual-basic"></a><span data-ttu-id="b399e-102">Procédure : Créer une Documentation XML en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b399e-102">How to: Create XML Documentation in Visual Basic</span></span>
<span data-ttu-id="b399e-103">Cet exemple montre comment ajouter des commentaires de documentation XML à votre code.</span><span class="sxs-lookup"><span data-stu-id="b399e-103">This example shows how to add XML documentation comments to your code.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-xml-documentation-for-a-type-or-member"></a><span data-ttu-id="b399e-104">Pour créer une documentation XML pour un type ou membre</span><span class="sxs-lookup"><span data-stu-id="b399e-104">To create XML documentation for a type or member</span></span>  
  
1.  <span data-ttu-id="b399e-105">Dans le **éditeur de Code**, positionnez votre curseur sur la ligne au-dessus du type ou le membre pour lequel vous souhaitez créer la documentation.</span><span class="sxs-lookup"><span data-stu-id="b399e-105">In the **Code Editor**, position your cursor on the line above the type or member for which you want to create documentation.</span></span>  
  
2.  <span data-ttu-id="b399e-106">Type `'''` (trois guillemets simples).</span><span class="sxs-lookup"><span data-stu-id="b399e-106">Type `'''` (three single-quotation marks).</span></span>  
  
     <span data-ttu-id="b399e-107">Une structure XML pour le type ou le membre est ajoutée dans le **éditeur de Code**.</span><span class="sxs-lookup"><span data-stu-id="b399e-107">An XML skeleton for the type or member is added in the **Code Editor**.</span></span>  
  
3.  <span data-ttu-id="b399e-108">Ajouter des informations descriptives entre les balises appropriées.</span><span class="sxs-lookup"><span data-stu-id="b399e-108">Add descriptive information between the appropriate tags.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="b399e-109">Si vous ajoutez des lignes supplémentaires dans le bloc de documentation XML, chaque ligne doit commencer par `'''`.</span><span class="sxs-lookup"><span data-stu-id="b399e-109">If you add additional lines within the XML documentation block, each line must begin with `'''`.</span></span>  
  
4.  <span data-ttu-id="b399e-110">Ajouter du code qui utilise le type ou le membre avec les nouveaux commentaires de documentation XML.</span><span class="sxs-lookup"><span data-stu-id="b399e-110">Add additional code that uses the type or member with the new XML documentation comments.</span></span>  
  
     <span data-ttu-id="b399e-111">IntelliSense affiche le texte à partir de la \<Résumé > balise pour le type ou membre.</span><span class="sxs-lookup"><span data-stu-id="b399e-111">IntelliSense displays the text from the \<summary> tag for the type or member.</span></span>  
  
5.  <span data-ttu-id="b399e-112">Compilez le code pour générer un fichier XML contenant les commentaires de documentation.</span><span class="sxs-lookup"><span data-stu-id="b399e-112">Compile the code to generate an XML file containing the documentation comments.</span></span> <span data-ttu-id="b399e-113">Pour plus d’informations, consultez [/doc](../../../visual-basic/reference/command-line-compiler/doc.md).</span><span class="sxs-lookup"><span data-stu-id="b399e-113">For more information, see [/doc](../../../visual-basic/reference/command-line-compiler/doc.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b399e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b399e-114">See also</span></span>
- [<span data-ttu-id="b399e-115">Documentation de votre code avec le langage XML</span><span class="sxs-lookup"><span data-stu-id="b399e-115">Documenting Your Code with XML</span></span>](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)
- [<span data-ttu-id="b399e-116">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="b399e-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
- [<span data-ttu-id="b399e-117">/doc</span><span class="sxs-lookup"><span data-stu-id="b399e-117">/doc</span></span>](../../../visual-basic/reference/command-line-compiler/doc.md)
