---
title: <param> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- param XML tag
- <param> XML tag
ms.assetid: 4e32e86f-f6f3-4301-b7fc-2f321fb54368
ms.openlocfilehash: 476b3f4f6b85908897e15f73bc23d2b060e337c3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283645"
---
# <a name="param-visual-basic"></a>\<param > (Visual Basic)
Définit un nom de paramètre et une description.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `name`  
 Nom d’un paramètre de méthode. Mettez le nom entre guillemets doubles (" ").  
  
 `description`  
 Description du paramètre.  
  
## <a name="remarks"></a>Notes  
 Le `<param>` balise doit être utilisée dans le commentaire pour une déclaration de méthode pour décrire un des paramètres pour la méthode.  
  
 Le texte pour le `<param>` balise apparaît dans les emplacements suivants :  
  
-   Informations sur les paramètres d’IntelliSense. Pour plus d’informations, consultez [Utilisation d’IntelliSense](/visualstudio/ide/using-intellisense).  
  
-   Explorateur d’objets. Pour plus d’informations, consultez [Affichage de la structure du code](/visualstudio/ide/viewing-the-structure-of-code).  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<param>` balises pour décrire le `id` paramètre.  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/param_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
