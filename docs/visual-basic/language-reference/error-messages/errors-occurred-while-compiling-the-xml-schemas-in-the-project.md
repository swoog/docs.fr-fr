---
title: Des erreurs se sont produites lors de la compilation des schémas Xml du projet
ms.date: 07/20/2015
f1_keywords:
- bc36810
- vbc36810
helpviewer_keywords:
- BC36810
ms.assetid: 9323b5d2-ba14-4e49-91f1-9ad647162144
ms.openlocfilehash: 337fc1fb4dfc83c9b4814d3e45eb0cbe0758f7ce
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61803277"
---
# <a name="errors-occurred-while-compiling-the-xml-schemas-in-the-project"></a>Des erreurs se sont produites lors de la compilation des schémas Xml du projet
Erreurs se sont produites lors de la compilation des schémas XML dans le projet. Pour cette raison, XML IntelliSense n’est pas disponible.  
  
 Il existe une erreur dans un schéma de définition de schéma XML (XSD) inclus dans le projet. Cette erreur se produit lorsque vous ajoutez un fichier de schéma (.xsd) XSD qui est en conflit avec le schéma XSD existant défini pour le projet.  
  
 **ID d’erreur :** BC36810  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Double-cliquez sur l’avertissement dans le **liste d’erreurs** fenêtre. Visual Basic vous dirigera vers l’emplacement dans le fichier XSD qui est la source de l’avertissement. Corrigez l’erreur dans le schéma XSD.  
  
- Assurez-vous que tous les requis de fichiers de schéma (.xsd) XSD sont inclus dans le projet. Vous devrez peut-être cliquer sur **afficher tous les fichiers** sur le **projet** menu pour afficher votre .xsd fichiers **l’Explorateur de solutions**. Cliquez sur un fichier .xsd, puis cliquez sur **inclure dans le projet** pour inclure le fichier dans votre projet.  
  
- Si vous utilisez l’Assistant XML vers schéma, cette erreur peut se produire si vous déduisez des schémas à plusieurs fois à partir de la même source. Dans ce cas, vous pouvez supprimer les fichiers de schéma XSD existants à partir du projet, y ajouter un nouveau code XML pour le modèle d’élément de schéma et fournissez le code XML à l’Assistant schéma avec toutes les sources XML applicables pour votre projet.  
  
- Si aucune erreur n’est identifiée dans votre schéma XSD, le compilateur XML peut-être pas suffisamment d’informations pour fournir un message d’erreur détaillé. Vous serez peut-être en mesure d’obtenir des informations d’erreur plus détaillées Si vous vous assurez que les espaces de noms XML pour les fichiers .xsd inclus dans votre projet correspondent aux espaces de noms XML identifiés pour le schéma XML défini dans Visual Studio.  
  
## <a name="see-also"></a>Voir aussi

- [Liste d’erreurs, fenêtre](/visualstudio/ide/reference/error-list-window)
- [XML](../../../visual-basic/programming-guide/language-features/xml/index.md)
