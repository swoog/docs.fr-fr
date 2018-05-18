---
title: Cert2spc.exe (outil de test de certificat d'éditeur de logiciels)
ms.date: 03/30/2017
helpviewer_keywords:
- SPC
- Software Publisher Certificate Test tool
- Software Publisher Certificate
- Cert2spc.exe
- certificates, Software Publisher's Certificate
ms.assetid: be434d7d-9c0d-46e7-8392-58a9b542d11d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3c1d1944ae06ea26ce9bf7b4726e79155768d444
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="cert2spcexe-software-publisher-certificate-test-tool"></a>Cert2spc.exe (outil de test de certificat d'éditeur de logiciels)
L'outil Software Publisher Certificate Test (Test de certificat d'édition de logiciel) crée un certificat d'édition de logiciel SPC (Software Publisher's Certificate) à partir d'un ou plusieurs certificats X.509. Cert2spc.exe doit être utilisé à des fins de test uniquement. Vous pouvez vous procurer un certificat SPC valide auprès d'une autorité de certification comme VeriSign ou Thawte. Pour plus d’informations sur la création de certificats X.509, consultez [Makecert.exe (outil de création de certificat)](http://msdn.microsoft.com/library/b0343f8e-9c41-4852-a85c-f8a0c408cf0d).  
  
 Cet outil est installé automatiquement avec Visual Studio. Pour exécuter l'outil, utilisez l'invite de commandes développeur (ou l'invite de commandes Visual Studio dans Windows 7). Pour plus d'informations, consultez [Invites de commandes](../../../docs/framework/tools/developer-command-prompt-for-vs.md).  
  
 À l'invite de commandes, tapez le texte suivant :  
  
## <a name="syntax"></a>Syntaxe  
  
```  
cert2spc cert1.cer | crl1.crl [... certN.cer | crlN.crl] outputSPCfile.spc  
```  
  
#### <a name="parameters"></a>Paramètres  
  
|Argument|Description|  
|--------------|-----------------|  
|`certN.cer`|Nom d'un certificat X.509 à inclure dans le fichier SPC. Vous pouvez spécifier plusieurs noms séparés par des espaces.|  
|`crlN.crl`|Nom d'une liste de révocation de certificats à inclure dans le fichier SPC. Vous pouvez spécifier plusieurs noms séparés par des espaces.|  
|`outputSPCfile.spc`|Nom de l'objet PKCS #7 qui contiendra les certificats X.509.|  
  
|Option|Description|  
|------------|-----------------|  
|**/?**|Affiche la syntaxe et les options de commande de l'outil.|  
  
## <a name="examples"></a>Exemples  
 La commande suivante crée un fichier SPC à partir de `myCertificate.cer` et le place dans `mySPCFile.spc`.  
  
```  
cert2spc myCertificate.cer mySPCFile.spc  
```  
  
 La commande suivante crée un fichier SPC à partir de `oneCertificate.cer` et `twoCertificate.cer` et le place dans `mySPCFile.spc`.  
  
```  
cert2spc oneCertificate.cer twoCertificate.cer mySPCFile.spc  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Outils](../../../docs/framework/tools/index.md)  
 [Makecert.exe (outil de création du certificat)](http://msdn.microsoft.com/library/b0343f8e-9c41-4852-a85c-f8a0c408cf0d)  
 [Invites de commandes](../../../docs/framework/tools/developer-command-prompt-for-vs.md)
