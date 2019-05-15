---
title: Le fichier spécifié dans FileName n’est pas un fichier XML valide
ms.date: 07/20/2015
ms.assetid: c4c30bf3-e0ad-4bc8-89e0-2c3e49e9793b
ms.openlocfilehash: 1615722d19e1a24ee4e72bc702dbce3fe30411a4
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592895"
---
# <a name="file-specified-in-filename-is-not-a-valid-xml-file"></a>Le fichier spécifié dans FileName n’est pas un fichier XML valide

Le nom de fichier fourni n’est pas un fichier XML valide. Pour spécifier la structure et le contenu autorisés d’un document XML, vous pouvez utiliser une définition de type de document (DTD), un schéma Microsoft XML-Data Reduced (XDR) ou un schéma de langage de définition de schéma XML (XSD). Schémas XSD sont la meilleure façon de spécifier des grammaires XML dans le .NET Framework.

> [!NOTE]
> Dans certaines versions antérieures de Visual Studio, le **Concepteur XML** est le concepteur pour le schéma XML et les datasets typés. Vous pouvez toujours utiliser le **Concepteur XML** pour créer et modifier des fichiers de schéma XML. Toutefois, dans Visual Studio 2012, le concepteur pour créer et modifier des datasets typés est la **Concepteur de Dataset**. Pour plus d’informations, consultez [création et modification de données typés](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/314t4see(v=vs.120)).

## <a name="to-correct-this-error"></a>Pour corriger cette erreur

- Vérifiez que le nom du fichier que vous fournissez est correct.

- Vérifiez que le fichier spécifié contient le code XML valide. Pour cela, chargez le fichier XML à vérifier dans le **Concepteur XML**. Dans le menu **XML** , cliquez sur **Valider le XML**. Les erreurs sont répertoriées dans la **Liste des tâches**.

- Si le fichier XML comprend un schéma XML associé, vérifiez que les éléments apparaissent dans la structure définie et que le contenu de chaque élément est conforme aux types de données déclarés qui sont spécifiés dans le schéma.

## <a name="see-also"></a>Voir aussi

- <xref:System.Xml>
- [Guide pratique pour analyser des chemins](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)
