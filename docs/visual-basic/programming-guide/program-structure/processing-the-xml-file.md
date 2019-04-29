---
title: Traitement du fichier XML (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- XML comments [Visual Basic], parsing [Visual Basic]
ms.assetid: 78a15cd0-7708-4e79-85d1-c154b7a14a8c
ms.openlocfilehash: a10255be140c7c86a435cca98cec5df7df82ffee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61955491"
---
# <a name="processing-the-xml-file-visual-basic"></a>Traitement du fichier XML (Visual Basic)
Le compilateur génère une chaîne d’ID pour chaque construction de votre code qui est marquée pour générer la documentation. (Pour plus d’informations sur la façon de baliser votre code, consultez [balises de commentaire XML](../../../visual-basic/language-reference/xmldoc/index.md).) La chaîne d’ID identifie de façon unique la construction. Les programmes qui traitent le fichier XML peuvent utiliser la chaîne d’ID pour identifier le correspondantes [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] élément de métadonnées/réflexion.  
  
 Le fichier XML n’est pas une représentation hiérarchique de votre code. Il est une liste plate avec un ID généré pour chaque élément.  
  
 Le compilateur respecte les règles suivantes quand il génère les chaînes d’ID :  
  
- La chaîne ne contient aucun espace blanc.  
  
- La première partie de la chaîne d’ID identifie le type du membre, avec un caractère unique suivi de deux-points. Les types de membre suivants sont utilisés.  
  
|Caractère|Description|  
|---|---|  
|N|namespace<br /><br /> Impossible d’ajouter des commentaires de documentation à un espace de noms, mais vous pouvez faire des références CREF à ceux-ci, si pris en charge.|  
|T|type: `Class`, `Module`, `Interface`, `Structure`, `Enum`, `Delegate`|  
|F|champ : `Dim`|  
|P|propriété : `Property` (y compris les propriétés par défaut)|  
|M|méthode : `Sub`, `Function`, `Declare`, `Operator`|  
|E|événement : `Event`|  
|!|chaîne d’erreur<br /><br /> Le reste de la chaîne fournit des informations sur l’erreur. Le compilateur Visual Basic génère des informations d’erreur pour les liens qui ne peut pas être résolus.|  
  
- La deuxième partie de la `String` est le nom qualifié complet de l’élément, en commençant à la racine de l’espace de noms. Le nom de l’élément, ses types englobants et l’espace de noms sont séparés par des points. Si le nom de l’élément lui-même comporte des points, ils sont remplacés par le signe dièse (#). Il est supposé qu’aucun élément n’a un signe dièse directement dans son nom. Par exemple, le nom qualifié complet de le `String` constructeur serait `System.String.#ctor`.  
  
- Pour les propriétés et méthodes, si la méthode a des arguments, la liste d’arguments entre parenthèses suit. S’il n’y a pas d’arguments, aucune parenthèse n’est présente. Les arguments sont séparés par des virgules. L’encodage de chaque argument correspond directement à son encodage dans une [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] signature.  
  
## <a name="example"></a>Exemple  
 Le code suivant montre comment les chaînes d’ID pour une classe et ses membres sont générés.  
  
 [!code-vb[VbVbcnXmlDocComments#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#10)]  
  
## <a name="see-also"></a>Voir aussi

- [/doc](../../../visual-basic/reference/command-line-compiler/doc.md)
- [Guide pratique pour Créer une Documentation XML](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)
