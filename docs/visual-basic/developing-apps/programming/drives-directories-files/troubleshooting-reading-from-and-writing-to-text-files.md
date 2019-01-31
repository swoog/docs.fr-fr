---
title: 'Dépannage : lecture et écriture dans des fichiers texte (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- troubleshooting file I/O
- writing text to files [Visual Basic], troubleshooting
- troubleshooting Visual Basic, text files
- I/O [Visual Basic], troubleshooting text files
- writing to files [Visual Basic], troubleshooting
- reading text files [Visual Basic], troubleshooting
ms.assetid: a8e9b44d-facb-4718-8c0f-466537171182
ms.openlocfilehash: cc0ec3c624fc4f47a0ef8594669ba120e6628e82
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54684396"
---
# <a name="troubleshooting-reading-from-and-writing-to-text-files-visual-basic"></a>Dépannage : lecture et écriture dans des fichiers texte (Visual Basic)
Cette rubrique aborde les problèmes courants rencontrés lors de l’utilisation de fichiers texte et propose une approche pour chacun d’entre eux.  
  
## <a name="common-problems"></a>Problèmes courants  
 Les problèmes les plus fréquemment rencontrés lors de l’utilisation de fichiers texte incluent les exceptions de sécurité, les encodages de fichiers ou les chemins non valides.  
  
### <a name="security-exceptions"></a>Exceptions de sécurité  
 Une <xref:System.Security.SecurityException> est levée quand une erreur de sécurité se produit. Cela est souvent dû au fait que l’utilisateur n’a pas les autorisations nécessaires, ce qui peut être résolu par l’ajout d’autorisations ou l’utilisation des fichiers dans un stockage isolé.  
  
### <a name="file-encodings"></a>Encodages de fichiers  
 Les encodages de fichiers, également appelés codages de caractères, spécifient comment représenter les caractères lors du traitement du texte. Les caractères inattendus d’un fichier texte peuvent résulter d’un encodage incorrect. Pour la plupart des fichiers, un encodage peut être préférable à un autre en fonction des caractères de langue qu’il peut ou non gérer, bien qu’Unicode soit généralement préféré. Pour plus d’informations, consultez [Encodages de fichiers](../../../../visual-basic/developing-apps/programming/drives-directories-files/file-encodings.md) et <xref:System.Text.Encoding>.  
  
### <a name="incorrect-paths"></a>Chemins incorrects  
 Lors de l’analyse des chemins, notamment des chemins relatifs, il est facile de fournir des données incorrectes. Vous pouvez résoudre de nombreux problèmes en vous assurant de fournir le chemin correct. Pour plus d'informations, voir [Procédure : analyser des chemins](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- [Lecture à partir de fichiers](../../../../visual-basic/developing-apps/programming/drives-directories-files/reading-from-files.md)
- [Écriture dans des fichiers](../../../../visual-basic/developing-apps/programming/drives-directories-files/writing-to-files.md)
- [Analyse des fichiers texte avec l’objet TextFieldParser](../../../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)
