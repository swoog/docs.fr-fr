---
title: "'<interfacename>. <membername>'est déjà implémenté par la classe de base'<baseclassname>'. Réimplémentation de <type> supposé"
ms.date: 07/20/2015
f1_keywords:
- vbc42015
- bc42015
helpviewer_keywords:
- BC42015
ms.assetid: 658c070a-113e-4bd8-b294-12c243191160
ms.openlocfilehash: 5d5d9f21069c7b9aa54940525b7678bc3987b77c
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264149"
---
# <a name="interfacenamemembername-is-already-implemented-by-the-base-class-baseclassname-re-implementation-of-type-assumed"></a>'\<nom_interface >. \<nom_membre >' est déjà implémenté par la classe de base\<nom_classe_de_base >'. Réimplémentation de \<type > supposé
Une propriété, une procédure ou un événement dans une classe dérivée utilise une `Implements` clause qui spécifie un membre d’interface qui est déjà implémenté dans la classe de base.  
  
 Une classe dérivée peut réimplémenter un membre d’interface qui est implémenté par sa classe de base. La substitution de l’implémentation de la classe de base est une procédure différente. Pour plus d’informations, consultez [Implements](../../../visual-basic/language-reference/statements/implements-clause.md).  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC42015  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Si vous comptez réimplémenter le membre d’interface, aucune mesure n’est nécessaire. Code de votre classe dérivée accède au membre réimplémenté, sauf si vous utilisez le `MyBase` mot clé pour accéder à l’implémentation de classe de base.  
  
-   Si vous ne comptez pas réimplémenter le membre d’interface, supprimez la clause `Implements` de la déclaration de la propriété, de la procédure ou de l’événement.  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
