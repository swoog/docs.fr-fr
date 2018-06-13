---
title: Des erreurs se sont produites lors de la compilation des schémas Xml du projet
ms.date: 07/20/2015
f1_keywords:
- bc36810
- vbc36810
helpviewer_keywords:
- BC36810
ms.assetid: 9323b5d2-ba14-4e49-91f1-9ad647162144
ms.openlocfilehash: 0cc565809792c619ca9903f9ef9b029b51a8aa17
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588260"
---
# <a name="errors-occurred-while-compiling-the-xml-schemas-in-the-project"></a>Des erreurs se sont produites lors de la compilation des schémas Xml du projet
Erreurs se sont produites lors de la compilation des schémas XML dans le projet. Pour cette raison, XML IntelliSense n’est pas disponible.  
  
 Il existe une erreur dans un schéma de définition de schéma XML (XSD) inclus dans le projet. Cette erreur se produit lorsque vous ajoutez un fichier de schéma (.xsd) XSD qui est en conflit avec le schéma XSD existant défini pour le projet.  
  
 **ID d’erreur :** BC36810  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Double-cliquez sur l’avertissement dans la **liste d’erreurs** fenêtre. Visual Basic vous dirige vers l’emplacement dans le fichier XSD qui est la source de l’avertissement. Corrigez l’erreur dans le schéma XSD.  
  
-   Assurez-vous que tous les requises des fichiers XSD schéma (.xsd) sont inclus dans le projet. Vous devrez peut-être cliquer sur **afficher tous les fichiers** sur la **projet** menu pour afficher votre .xsd dans les fichiers **l’Explorateur de solutions**. Cliquez sur un fichier .xsd, puis sur **inclure dans le projet** pour inclure le fichier dans votre projet.  
  
-   Si vous utilisez l’Assistant schéma XML vers, cette erreur peut se produire si vous déduisez des schémas à plusieurs fois à partir de la même source. Dans ce cas, vous pouvez supprimer les fichiers de schéma XSD existants à partir du projet, y ajouter un nouveau code XML pour le modèle d’élément de schéma, puis fournir le code XML à l’Assistant schéma de toutes les sources XML applicables pour votre projet.  
  
-   Si aucune erreur n’est identifiée dans votre schéma XSD, le compilateur XML peut-être pas suffisamment d’informations pour fournir un message d’erreur détaillé. Vous serez peut-être en mesure d’obtenir davantage d’informations sur l’erreur si vous vérifiez que les espaces de noms XML pour les fichiers .xsd inclus dans votre projet correspondent aux espaces de noms XML identifié pour le schéma XML défini dans Visual Studio.  
  
## <a name="see-also"></a>Voir aussi  
 [Liste d’erreurs, fenêtre](/visualstudio/ide/reference/error-list-window)  
 [XML](../../../visual-basic/programming-guide/language-features/xml/index.md)
