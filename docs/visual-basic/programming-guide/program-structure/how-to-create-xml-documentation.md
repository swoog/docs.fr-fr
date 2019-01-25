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
# <a name="how-to-create-xml-documentation-in-visual-basic"></a>Procédure : Créer une Documentation XML en Visual Basic
Cet exemple montre comment ajouter des commentaires de documentation XML à votre code.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-xml-documentation-for-a-type-or-member"></a>Pour créer une documentation XML pour un type ou membre  
  
1.  Dans le **éditeur de Code**, positionnez votre curseur sur la ligne au-dessus du type ou le membre pour lequel vous souhaitez créer la documentation.  
  
2.  Type `'''` (trois guillemets simples).  
  
     Une structure XML pour le type ou le membre est ajoutée dans le **éditeur de Code**.  
  
3.  Ajouter des informations descriptives entre les balises appropriées.  
  
    > [!NOTE]
    >  Si vous ajoutez des lignes supplémentaires dans le bloc de documentation XML, chaque ligne doit commencer par `'''`.  
  
4.  Ajouter du code qui utilise le type ou le membre avec les nouveaux commentaires de documentation XML.  
  
     IntelliSense affiche le texte à partir de la \<Résumé > balise pour le type ou membre.  
  
5.  Compilez le code pour générer un fichier XML contenant les commentaires de documentation. Pour plus d’informations, consultez [/doc](../../../visual-basic/reference/command-line-compiler/doc.md).  
  
## <a name="see-also"></a>Voir aussi
- [Documentation de votre code avec le langage XML](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
- [/doc](../../../visual-basic/reference/command-line-compiler/doc.md)
