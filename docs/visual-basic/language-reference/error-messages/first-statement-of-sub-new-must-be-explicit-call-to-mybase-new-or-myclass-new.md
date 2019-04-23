---
title: "La première instruction de ce 'Sub New' doit être un appel explicite à 'MyBase.New' ou 'MyClass.New', car le '<constructorname>' dans la classe de base '<baseclassname>' de '<derivedclassname>' est marqué comme obsolète : '<errormessage>'"
ms.date: 07/20/2015
f1_keywords:
- vbc30920
- bc30920
helpviewer_keywords:
- BC30920
ms.assetid: e47dc755-4294-4368-b813-2177b7677957
ms.openlocfilehash: 89b6c241bb637f2efc6014c4640b3b463c4facfa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59313475"
---
# <a name="first-statement-of-this-sub-new-must-be-an-explicit-call-to-mybasenew-or-myclassnew-because-the-constructorname-in-the-base-class-baseclassname-of-derivedclassname-is-marked-obsolete-errormessage"></a>La première instruction de ce 'Sub New' doit être un appel explicite à 'MyBase.New' ou 'MyClass.New', car le '\<Nom_Constructeur >' dans la classe de base\<nom_classe_de_base >' de '\<nom_classe_dérivée >' est marqué comme obsolète : '\< message d’erreur >'
Un constructeur de classe n’appelle pas explicitement un constructeur de classe de base et le constructeur de classe de base implicite est marqué avec l’attribut <xref:System.ObsoleteAttribute> et la directive pour le traiter comme une erreur.  
  
 Lorsqu’un constructeur de classe dérivée n’appelle pas un constructeur de classe de base, Visual Basic essaie d’en générer un appel implicite à un constructeur de classe de base sans paramètre. S’il n’existe aucun constructeur accessible dans la classe de base qui peut être appelée sans arguments, Visual Basic ne peut pas générer un appel implicite. Dans ce cas, le constructeur requis est marqué avec le <xref:System.ObsoleteAttribute> d’attribut, Visual Basic ne peut pas l’appeler.  
  
 Vous pouvez marquer un élément de programmation comme n’étant plus utilisé en lui appliquant <xref:System.ObsoleteAttribute> . Dans ce cas, vous pouvez affecter à la propriété <xref:System.ObsoleteAttribute.IsError%2A> de l’attribut la valeur `True` ou `False`. Si vous lui affectez la valeur `True`, le compilateur traite une tentative d’utilisation de l’élément comme une erreur. Si vous lui affectez la valeur `False`ou si vous laissez la valeur par défaut `False`, le compilateur émet un avertissement en cas de tentative d’utilisation de l’élément.  
  
 **ID d’erreur :** BC30920  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Examinez le message d’erreur mentionné et prenez les mesures nécessaires.  
  
2. Incluez un appel à `MyBase.New()` ou `MyClass.New()` en tant que première instruction de `Sub New` dans la classe dérivée.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des attributs](../../../visual-basic/programming-guide/concepts/attributes/index.md)
