---
title: Chiffrement et déchiffrement de chaînes en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- encryption [Visual Basic], strings
- strings [Visual Basic], encrypting
- decryption [Visual Basic], strings
- strings [Visual Basic], decrypting
ms.assetid: 1f51e40a-2f88-43e2-a83e-28a0b5c0d6fd
ms.openlocfilehash: aaf8238a330ceb9e1cf4f9ff5892d1db1d951faa
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58826793"
---
# <a name="walkthrough-encrypting-and-decrypting-strings-in-visual-basic"></a>Procédure pas à pas : Chiffrement et déchiffrement de chaînes en Visual Basic
Cette procédure pas à pas vous montre comment utiliser le <xref:System.Security.Cryptography.DESCryptoServiceProvider> classe pour chiffrer et déchiffrer des chaînes à l’aide de la version du fournisseur (CSP) de services de chiffrement de Triple Data Encryption Standard (<xref:System.Security.Cryptography.TripleDES>) algorithme. La première étape consiste à créer une classe wrapper simple qui encapsule l’algorithme 3DES et stocke les données chiffrées en tant qu’une chaîne codée en base 64. Ensuite, ce wrapper est utilisé pour stocker en toute sécurité des données utilisateur privées dans un fichier texte accessible publiquement.  
  
 Vous pouvez utiliser le chiffrement pour protéger les secrets de l’utilisateur (par exemple, les mots de passe) et pour rendre les informations d’identification illisibles par les utilisateurs non autorisés. Cela peut protéger l’identité d’un utilisateur autorisé son vol, qui protège les actifs de l’utilisateur et fournit la non répudiation. Le chiffrement peut également protéger les données d’un utilisateur d’accéder à des utilisateurs non autorisés.  
  
 Pour plus d’informations, consultez [Services de cryptographie](../../../../standard/security/cryptographic-services.md).  
  
> [!IMPORTANT]
>  Les Rijndael (maintenant appelé Advanced Encryption Standard [AES]) et les algorithmes Triple Data Encryption Standard (3DES) fournissent une meilleure sécurité que DES car elles sont plus intensifs. Pour plus d’informations, consultez <xref:System.Security.Cryptography.DES> et <xref:System.Security.Cryptography.Rijndael>.  
  
### <a name="to-create-the-encryption-wrapper"></a>Pour créer le wrapper de chiffrement  
  
1.  Créer la `Simple3Des` classe pour encapsuler les méthodes de chiffrement et le déchiffrement.  
  
     [!code-vb[VbVbalrStrings#38](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#38)]  
  
2.  Ajoutez une importation de l’espace de noms de chiffrement au début du fichier qui contient le `Simple3Des` classe.  
  
     [!code-vb[VbVbalrStrings#77](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#77)]  
  
3.  Dans la `Simple3Des` classe, ajoutez un champ privé pour stocker le fournisseur de services de chiffrement 3DES.  
  
     [!code-vb[VbVbalrStrings#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#39)]  
  
4.  Ajoutez une méthode privée qui crée un tableau d’octets d’une longueur spécifiée à partir du hachage de la clé spécifiée.  
  
     [!code-vb[VbVbalrStrings#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#41)]  
  
5.  Ajoutez un constructeur pour initialiser le fournisseur de services de chiffrement 3DES.  
  
     Le `key` paramètre contrôle le `EncryptData` et `DecryptData` méthodes.  
  
     [!code-vb[VbVbalrStrings#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#40)]  
  
6.  Ajoutez une méthode publique qui chiffre une chaîne.  
  
     [!code-vb[VbVbalrStrings#42](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#42)]  
  
7.  Ajoutez une méthode publique qui déchiffre une chaîne.  
  
     [!code-vb[VbVbalrStrings#43](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#43)]  
  
     La classe wrapper peut maintenant être utilisée pour protéger les ressources de l’utilisateur. Dans cet exemple, il est utilisé pour stocker en toute sécurité des données utilisateur privées dans un fichier texte accessible publiquement.  
  
### <a name="to-test-the-encryption-wrapper"></a>Pour tester le wrapper de chiffrement  
  
1.  Dans une classe distincte, ajoutez une méthode qui utilise le wrapper `EncryptData` méthode pour chiffrer une chaîne et l’écrire à l’utilisateur du dossier Mes Documents.  
  
     [!code-vb[VbVbalrStrings#78](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#78)]  
  
2.  Ajouter une méthode qui lit la chaîne chiffrée à partir de l’utilisateur du dossier Mes Documents et déchiffre la chaîne avec le wrapper `DecryptData` (méthode).  
  
     [!code-vb[VbVbalrStrings#79](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#79)]  
  
3.  Ajoutez le code d’interface utilisateur pour appeler le `TestEncoding` et `TestDecoding` méthodes.  
  
4.  Exécutez l'application.  
  
     Lorsque vous testez l’application, notez qu’il ne sera pas déchiffrer les données si vous fournissez le mot de passe incorrect.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Security.Cryptography>
- <xref:System.Security.Cryptography.DESCryptoServiceProvider>
- <xref:System.Security.Cryptography.DES>
- <xref:System.Security.Cryptography.TripleDES>
- <xref:System.Security.Cryptography.Rijndael>
- [Cryptographic Services](../../../../standard/security/cryptographic-services.md)
