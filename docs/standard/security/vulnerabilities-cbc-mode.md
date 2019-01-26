---
title: Vulnérabilités de minutage avec déchiffrement symétrique en mode CBC à l’aide de la marge intérieure
description: Apprenez à détecter et atténuer les vulnérabilités de minutage avec déchiffrement symétrique sur le mode Cipher Block Chaining (CBC) à l’aide de la marge intérieure.
ms.date: 06/12/2018
author: blowdart
ms.author: mairaw
ms.openlocfilehash: 0f5f7d2032981d28445abe27f87a678ce2c74600
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55066172"
---
# <a name="timing-vulnerabilities-with-cbc-mode-symmetric-decryption-using-padding"></a>Vulnérabilités de minutage avec déchiffrement symétrique en mode CBC à l’aide de la marge intérieure

Microsoft est convaincu qu’il n’est plus sûr déchiffrer les données chiffrées avec le mode Cipher Block Chaining (CBC) de chiffrement symétrique lors de la marge intérieure vérifiable a été appliqué sans d’abord vérifié que l’intégrité du texte chiffré, à l’exception de très spécifique circonstances. Cette opinion est basée sur les recherches sur le chiffrement connus. 

## <a name="introduction"></a>Introduction

Une attaque d’oracle de remplissage est un type d’attaque sur les données chiffrées qui permet à un attaquant déchiffrer le contenu des données, sans connaître la clé.

Oracle fait référence à un « savoir » qui donne une personne malveillante d’informations sur si l’action qu’ils exécutent est correcte ou non. Imaginez un plateau de jeu ou une carte de jeu avec un enfant. Lorsque sa face s’allume avec un sourire volumineux, car elle pense qu’elle est sur le point d’effectuer un mouvement bon, ce qui est oracle. Vous, en tant que l’adversaire, pourrez utiliser cette oracle pour bien planifier votre prochain déplacement.

Marge intérieure est un terme de chiffrement spécifique. Certains chiffrements qui sont les algorithmes utilisés pour chiffrer vos données, travailler sur des blocs de données où chaque bloc est de taille fixe. Si les données que vous souhaitez chiffrer n’est pas la bonne taille pour remplir les blocs, vos données sont complétées jusqu'à ce que c’est le cas. Différentes formes de la marge intérieure nécessitent ce remplissage soit toujours présents, même si l’entrée d’origine était de la taille appropriée. Ainsi, la marge intérieure à toujours être supprimés lors de déchiffrement.

Assembler les deux tâches, une implémentation logicielle avec une marge intérieure d’oracle révèle si les données déchiffrées ont remplissage valide. Oracle peut être quelque chose d’aussi simple que retournant une valeur qui indique « Remplissage non valide » ou quelque chose de plus compliqué à prendre une heure sensiblement différente pour traiter un bloc valide par opposition à un bloc non valide.

Les chiffrements par bloc ont une autre propriété, appelée le mode, qui détermine la relation de données dans le premier bloc de données dans le deuxième bloc, et ainsi de suite. Un des modes plus couramment utilisées est CBC. CBC introduit un bloc aléatoire initial, connu en tant que le vecteur d’initialisation (IV) et combine le bloc précédent avec le résultat du chiffrement statique pour le rendre telles que le chiffrement du message même avec la même clé ne produire toujours la même sortie chiffrée.

Une personne malveillante peut utiliser une oracle de remplissage, en association avec la structure des données de CBC, pour envoyer des messages légèrement modifiés pour le code qui expose l’oracle et envoyer des données jusqu'à ce que l’oracle lui indiquant les données sont correctes. À partir de cette réponse, l’attaquant peut déchiffrer le message octet par octet.

Réseaux informatiques modernes sont de ce type haute qualité qu’une personne malveillante peut détecter très petite (inférieure à 0,1 ms) les différences dans l’exécution de temps sur des systèmes distants. Les applications qui sont en supposant que le déchiffrement réussi ne peut se produire lorsque les données n’a pas été falsifiées peuvent être vulnérables aux attaques à partir d’outils sont conçus pour observer les différences de déchiffrement ayant réussi ou échoué. Cette différence de minutage peut être plus importante dans certains langages ou des bibliothèques que d’autres, il est désormais croire qu’il s’agit d’une menace pratique pour tous les langages et bibliothèques lors de la réponse de l’application aux défaillances est pris en compte.

Cette attaque s’appuie sur la possibilité de modifier les données chiffrées et testez le résultat avec oracle. La seule façon d’atténuer entièrement l’attaque consiste à détecter les modifications apportées aux données chiffrées et refuse d’effectuer des actions sur celui-ci. Pour ce faire, le standard consiste à créer une signature pour les données et valider la signature avant que toutes les opérations sont effectuées. La signature doit être vérifiable, il ne peut pas être créé par l’attaquant, sinon ils seraient modifier les données chiffrées, puis calculer une nouvelle signature basée sur les données modifiées. Un type courant de la signature appropriée est appelé un code d’authentification de message de hachage à clé (HMAC). Un HMAC diffère d’une somme de contrôle dans la mesure où il prend une clé secrète, connu uniquement à la personne produisant le code HMAC et à la personne validant. Sans la possession de la clé, vous ne peuvent pas produire un code HMAC correct. Lorsque vous recevez vos données, vous prendre les données chiffrées, calculer indépendamment le HMAC à l’aide de la clé secrète vous et le partage de l’expéditeur, puis compare le HMAC ils vous avons envoyé par rapport à celle calculé. Cette comparaison doit être temps constant, sinon vous avez ajouté un autre oracle détectable, ce qui permet un autre type d’attaque.

En résumé, pour utiliser complété les chiffrements par bloc CBC en toute sécurité, vous devez les combiner avec un code HMAC (ou une autre vérification de l’intégrité des données) que vous validez à l’aide d’une comparaison de temps constant avant d’essayer de déchiffrer les données. Étant donné que tous les messages modifiés prennent le même volume de temps pour produire une réponse, l’attaque est empêchée.

## <a name="who-is-vulnerable"></a>Qui est vulnérable

Cette vulnérabilité s’applique aux applications gérées et natives qui effectuent leur propre chiffrement et le déchiffrement. Cela inclut, par exemple :

- Une application qui chiffre un cookie pour le déchiffrement ultérieure sur le serveur.
- Une application de base de données qui offre la possibilité aux utilisateurs d’insérer des données dans une table dont les colonnes sont déchiffrées.
- Une application de transfert de données qui s’appuie sur le chiffrement à l’aide d’une clé partagée pour protéger les données en transit.
- Une application qui chiffre et déchiffre les messages « interne » le tunnel TLS.

Notez qu’à l’aide de TLS seul ne peut pas protéger dans ces scénarios.

Une application vulnérable :

- Déchiffre les données à l’aide du mode de chiffrement CBC avec un mode de remplissage vérifiable, tels que PKCS #7 ou ANSI X.923.
- Exécute le déchiffrement sans avoir effectué une vérification de l’intégrité des données (via un MAC ou une signature numérique asymétrique).

Cela s’applique également aux applications reposant sur les abstractions par-dessus ces primitives, telles que la structure de EnvelopedData Cryptographic Message Syntax (PKCS #7/CMS).

## <a name="related-areas-of-concern"></a>Domaines de préoccupation connexes

Research a conduit Microsoft à se préoccuper davantage de messages de CBC sont complétées par ISO 10126-équivalent de remplissage lorsque le message a une structure de pied de page connu ou prévisibles. Par exemple, le contenu préparé conformément aux règles de W3C XML Encryption Syntax et de la recommandation de traitement (xmlenc, EncryptedXml). Tandis que les recommandations du W3C pour signer le message, puis chiffrer a été considérée comme appropriée en temps, Microsoft recommande toujours fait encrypt-then-sign.

Les développeurs d’applications doivent toujours être conscients de la vérification de la mise en application d’une clé de signature asymétrique, car il n’existe aucune relation d’approbation inhérente entre une clé asymétrique et un message arbitraire.

## <a name="details"></a>Détails

Historiquement, il a été consensus qu’il est important de chiffrer et authentifier des données importantes, à l’aide de moyens par exemple, les signatures HMAC ou RSA. Toutefois, il a été moins des conseils éclairés concernant la procédure pour séquencer les opérations de chiffrement et d’authentification. En raison de la vulnérabilité décrites dans cet article, les conseils de Microsoft est désormais à toujours utiliser le paradigme « encrypt-then-sign ». Autrement dit, tout d’abord chiffrer des données à l’aide d’une clé symétrique, puis un MAC ou signature asymétrique de calcul sur le texte chiffré (données chiffrées). Lors du déchiffrage des données, effectuer l’inverse. Tout d’abord, vérifiez le MAC ou la signature du texte chiffré, puis le déchiffrer.

Une classe de vulnérabilités appelé « remplissage oracle attaques » ont été identifiés existe depuis plus de 10 ans. Ces vulnérabilités permettent à une personne malveillante de déchiffrer les données chiffrées par bloc symétriques algorithmes, tels que AES et 3DES, à l’aide de tentatives de ne plus de 4 096 par bloc de données. Assurez-vous de supprimer ces vulnérabilités utilisation du fait que les chiffrements par bloc les plus fréquemment utilisés avec des données de remplissage vérifiable à la fin. Il a été trouvé si une personne malveillante peut falsifier le texte chiffré et déterminer si les risques de falsification a entraîné une erreur dans le format de la marge intérieure à la fin, l’attaquant peut déchiffrer les données.

Initialement, les attaques pratiques étaient basés sur les services qui retournent les codes d’erreur différents en fonction de remplissage intervenue valide, telle que la vulnérabilité ASP.NET [MS10-070](/security-updates/SecurityBulletins/2010/ms10-070). Toutefois, Microsoft estime maintenant qu’il est pratique de mener des attaques similaires à l’aide uniquement les différences de minutage entre le traitement de remplissage valide et non valide.

Condition que le schéma de chiffrement utilise une signature et que la vérification de signature est effectuée avec un runtime fixe pour une longueur donnée de données (quel que soit le contenu), l’intégrité des données peut être vérifiée sans émettre de toutes les informations à un attaquant via un [canal latéral](https://en.wikipedia.org/wiki/Side-channel_attack). Étant donné que la vérification d’intégrité rejette les messages falsifiés, la menace d’oracle de remplissage est atténuée.

## <a name="guidance"></a>Conseils

Tout d’abord, Microsoft recommande que les données ayant la confidentialité doivent être transmises sur sécurité TLS (Transport Layer), le successeur de couche SSL (Secure Sockets).

Ensuite, analysez votre application :

- Comprendre et avec précision quelles chiffrement que vous effectuez le chiffrement est fourni par les plateformes et les API que vous utilisez.
- Être certain que chaque utilisation au niveau de chaque couche de symétrique [algorithme de chiffrement par bloc](https://en.wikipedia.org/wiki/Block_cipher#Notable_block_ciphers), tel que AES et 3DES, en mode CBC incorporer l’utilisation d’une vérification de l’intégrité des données à la clé de secret (une signature asymétrique, un code HMAC, ou pour modifier le mode de chiffrement à un [authentifié chiffrement](https://en.wikipedia.org/wiki/Authenticated_encryption) mode (AE) telles que GCM ou CCM).

En fonction de la recherche en cours, il est de croire que lorsque les étapes de l’authentification et le chiffrement sont effectuées indépendamment pour les modes non AE de chiffrement, l’authentification le texte chiffré (encrypt-then-sign) est la meilleure option générale. Toutefois, il n’existe aucune réponse correcte uniformisée au chiffrement et cette généralisation n’est pas aussi bonne qualité qu’orienté conseils à partir d’un cryptographe Professionnel.

Les applications qui ne peuvent pas modifier leur format de messagerie mais effectuer un déchiffrement CBC non authentifié sont invitées à tentez d’incorporer des solutions d’atténuation telles que :

- Déchiffrer sans autoriser le déchiffreur vérifier ou supprimer le remplissage :
  - Tout remplissage a été appliqué doit toujours être supprimés ou ignorés, que vous déplacez le fardeau dans votre application.
  - L’avantage est que la vérification de la marge intérieure et la suppression peuvent être incorporés dans une autre logique de vérification de données application. Si la vérification de la marge intérieure et la vérification des données peuvent être effectuées en temps constant, la menace est réduite.
  - Étant donné que l’interprétation de la marge intérieure change la longueur du message perçue, il peut toujours être émises à partir de cette approche des informations de minutage.
- Modifiez le mode de remplissage de déchiffrement ISO10126 :
  - Remplissage de déchiffrement ISO10126 est compatible avec remplissage de chiffrement PKCS7 et remplissage ANSIX923.
  - Modification du mode réduit les connaissances d’oracle de remplissage à 1 octet au lieu de l’intégralité du bloc. Toutefois, si le contenu a un pied de page bien connu, tels que d’un élément XML, de fermeture attaques connexes peuvent continuer attaquer le reste du message.
  - Cela n’empêche également pas récupération en texte clair dans les situations où l’attaquant peut forcer le même texte en clair à chiffrer plusieurs fois avec un décalage de message différent.
- L’évaluation d’un appel de déchiffrement à mouiller le signal de minutage de la grille :
  - Le calcul de la durée de conservation doit avoir un minimum dépassant la quantité maximale de temps que l’opération de déchiffrement serait nécessaire pour n’importe quel segment de données qui contient le remplissage.
  - Calculs de temps doivent être effectuées selon les instructions de [l’acquisition des horodatages haute résolution](https://msdn.microsoft.com/library/windows/desktop/dn55340.aspx), ne pas à l’aide <xref:System.Environment.TickCount?displayProperty=nameWithType> (susceptibles d’être roll-over/dépassement de capacité) ou la soustraction de deux horodatages système (susceptibles d’être modifiés de NTP erreurs).
  - Calculs de temps doivent être qui inclut l’opération de déchiffrement, y compris toutes les exceptions potentielles dans géré ou des applications C++, pas seulement complétées à la fin.
  - Si la réussite ou l’échec a encore été déterminé, la porte de minutage doit renvoient une erreur lorsqu’il arrive à expiration.
- Les services qui effectuent de déchiffrement non authentifié doivent avoir en place pour détecter qu’un flux de messages « non valides » est venue par le biais du contrôle.
  - N’oubliez pas que ce signal comporte des faux positifs (données endommagées légitimement) et faux négatifs (répartir l’attaque sur une période suffisamment longue pour échapper à la détection).

## <a name="finding-vulnerable-code---native-applications"></a>Recherche de code vulnérable - applications natives

Pour les programmes basées sur la cryptographie de Windows : Bibliothèque de génération (CNG) suivante :

- L’appel de déchiffrement concerne [BCryptDecrypt](/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt), en spécifiant le `BCRYPT_BLOCK_PADDING` indicateur.
- Le handle de clé a été initialisé en appelant [BCryptSetProperty](/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty) avec [BCRYPT_CHAINING_MODE](https://msdn.microsoft.com/library/windows/desktop/aa376211.aspx#BCRYPT_CHAINING_MODE) défini sur `BCRYPT_CHAIN_MODE_CBC`.
  - Dans la mesure où `BCRYPT_CHAIN_MODE_CBC` est la valeur par défaut, affectée code a ne peut-être pas attribué la valeur de `BCRYPT_CHAINING_MODE`.

Pour les programmes développés à l’API de chiffrement Windows plus anciens :

- L’appel de déchiffrement concerne [CryptDecrypt](/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecrypt) avec `Final=TRUE`.
- Le handle de clé a été initialisé en appelant [CryptSetKeyParam](/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam) avec [KP_MODE](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam) défini sur `CRYPT_MODE_CBC`.
  - Dans la mesure où `CRYPT_MODE_CBC` est la valeur par défaut, affectée code a ne peut-être pas attribué la valeur de `KP_MODE`.

## <a name="finding-vulnerable-code---managed-applications"></a>Code vulnérable recherche - applications managées

- L’appel de déchiffrement concerne le <xref:System.Security.Cryptography.SymmetricAlgorithm.CreateDecryptor> ou <xref:System.Security.Cryptography.SymmetricAlgorithm.CreateDecryptor(System.Byte[],System.Byte[])> méthodes sur <xref:System.Security.Cryptography.SymmetricAlgorithm?displayProperty=nameWithType>.
  - Cela inclut les types dérivés suivants dans le .NET, mais peut également inclure les types de fournisseurs tiers :
    - <xref:System.Security.Cryptography.Aes>
    - <xref:System.Security.Cryptography.AesCng>
    - <xref:System.Security.Cryptography.AesCryptoServiceProvider>
    - <xref:System.Security.Cryptography.AesManaged>
    - <xref:System.Security.Cryptography.DES>
    - <xref:System.Security.Cryptography.DESCryptoServiceProvider>
    - <xref:System.Security.Cryptography.RC2>
    - <xref:System.Security.Cryptography.RC2CryptoServiceProvider>
    - <xref:System.Security.Cryptography.Rijndael>
    - <xref:System.Security.Cryptography.RijndaelManaged>
    - <xref:System.Security.Cryptography.TripleDES>
    - <xref:System.Security.Cryptography.TripleDESCng>
    - <xref:System.Security.Cryptography.TripleDESCryptoServiceProvider>
- Le <xref:System.Security.Cryptography.SymmetricAlgorithm.Padding?displayProperty=nameWithType> propriété a été définie sur <xref:System.Security.Cryptography.PaddingMode.PKCS7?displayProperty=nameWithType>, <xref:System.Security.Cryptography.PaddingMode.ANSIX923?displayProperty=nameWithType>, ou <xref:System.Security.Cryptography.PaddingMode.ISO10126?displayProperty=nameWithType>.
  - Dans la mesure où <xref:System.Security.Cryptography.PaddingMode.PKCS7?displayProperty=nameWithType> est la valeur par défaut, affectée code ne peut jamais avoir attribué la <xref:System.Security.Cryptography.SymmetricAlgorithm.Padding?displayProperty=nameWithType> propriété.
- Le <xref:System.Security.Cryptography.SymmetricAlgorithm.Mode?displayProperty=nameWithType> a la valeur de propriété <xref:System.Security.Cryptography.CipherMode.CBC?displayProperty=nameWithType>
  - Dans la mesure où <xref:System.Security.Cryptography.CipherMode.CBC?displayProperty=nameWithType> est la valeur par défaut, affectée code ne peut jamais avoir attribué la <xref:System.Security.Cryptography.SymmetricAlgorithm.Mode?displayProperty=nameWithType> propriété.

## <a name="finding-vulnerable-code---cryptographic-message-syntax"></a>Recherche de code vulnérable - syntaxe de message de chiffrement

Un message CMS EnvelopedData non authentifié dont le contenu chiffré utilise le mode CBC AES (2.16.840.1.101.3.4.1.2, 2.16.840.1.101.3.4.1.22, 2.16.840.1.101.3.4.1.42), DES (1.3.14.3.2.7), 3DES (1.2.840.113549.3.7) ou RC2 (1.2.840.113549.3.2) est vulnérable, ainsi que des messages à l’aide de n’importe quel autres algorithmes de chiffrement par bloc en mode CBC.

Tandis que les chiffrements de flux ne sont pas sensibles à cette vulnérabilité, Microsoft vous recommande de toujours authentifier les données au fil de l’inspection de la valeur ContentEncryptionAlgorithm.

Pour les applications managées, un EnvelopedData CMS blob peut être détecté comme n’importe quelle valeur passée à <xref:System.Security.Cryptography.Pkcs.EnvelopedCms.Decode(System.Byte[])?displayProperty=fullName>.

Pour les applications natives, un objet blob CMS EnvelopedData peut être détecté en tant que la valeur fournie pour un handle CMS via [CryptMsgUpdate](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate) dont résultant [CMSG_TYPE_PARAM](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam) est `CMSG_ENVELOPED` et/ou le handle CMS est envoyées ultérieurement un `CMSG_CTRL_DECRYPT` instruction via [CryptMsgControl](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol).

## <a name="vulnerable-code-example---managed"></a>Exemple de code vulnérable - géré

Cette méthode lit un cookie et la déchiffre et aucune vérification de l’intégrité des données est visible. Par conséquent, le contenu d’un cookie qui est lu par cette méthode peut être attaqué par l’utilisateur qui les ont reçues, ou par n’importe quel agresseur a obtenu la valeur du cookie chiffré.

```csharp
private byte[] DecryptCookie(string cookieName)
{
    HttpCookie cookie = Request.Cookies[cookieName];

    if (cookie == null)
    {
        return null;
    }

    using (ICryptoTransform decryptor = _aes.CreateDecryptor())
    using (MemoryStream memoryStream = new MemoryStream())
    using (CryptoStream cryptoStream =
        new CryptoStream(memoryStream, decryptor, CryptoStreamMode.Write))
    {
        byte[] readCookie = Convert.FromBase64String(cookie.Value);
        cryptoStream.Write(readCookie, 0, readCookie.Length);
        cryptoStream.FlushFinalBlock();
        return memoryStream.ToArray();
    }
}
```

## <a name="example-code-following-recommended-practices---managed"></a>Exemple suivant de code recommandées - géré

L’exemple de code suivant utilise un format de message non standard de

`cipher_algorithm_id || hmac_algorithm_id || hmac_tag || iv || ciphertext`

où les `cipher_algorithm_id` et `hmac_algorithm_id` identificateurs d’algorithme sont des représentations de (non standard) local de l’application de ces algorithmes. Ces identificateurs peuvent être judicieux dans d’autres parties de votre protocole de messagerie existant et non comme un flux d’octets concaténée strict.

Cet exemple utilise également une clé principale unique pour dériver une clé de chiffrement et une clé HMAC. Ceci est fourni à la fois comme une commodité pour l’activation d’une application indexé séparément dans une application de clés en double et à encourager la conservation des valeurs d’autre que les deux clés. Elle garantit davantage que la clé HMAC et la clé de chiffrement ne peut pas tirer parti de synchronisation.

Cet exemple n’accepte pas un <xref:System.IO.Stream> pour le chiffrement ou déchiffrement. Une étape du fait de format de données actuelle chiffrer difficile, car le `hmac_tag` valeur précède le texte chiffré. Toutefois, ce format a été choisi, car il conserve tous les éléments de taille fixe au début pour conserver la plus simple de l’analyseur. Avec ce format de données, une seule passe decrypt est possible, même si un implémenteur est imminente pour appeler GetHashAndReset et vérifier le résultat avant d’appeler TransformFinalBlock. Si le chiffrement de diffusion en continu est important, un autre mode AE peut être requis.

```csharp
// ==++==
//
//   Copyright (c) Microsoft Corporation.  All rights reserved.
//
//   Shared under the terms of the Microsoft Public License,
//   https://opensource.org/licenses/MS-PL
//
// ==--==

using System;
using System.Diagnostics;
using System.IO;
using System.Runtime.CompilerServices;
using System.Security.Cryptography;

namespace Microsoft.Examples.Cryptography
{
    public enum AeCipher : byte
    {
        Unknown,
        Aes256CbcPkcs7,
    }

    public enum AeMac : byte
    {
        Unknown,
        HMACSHA256,
        HMACSHA384,
    }

    /// <summary>
    /// Provides extension methods to make HashAlgorithm look like .NET Core's
    /// IncrementalHash
    /// </summary>
    internal static class IncrementalHashExtensions
    {
        public static void AppendData(this HashAlgorithm hash, byte[] data)
        {
            hash.TransformBlock(data, 0, data.Length, null, 0);
        }

        public static void AppendData(
            this HashAlgorithm hash,
            byte[] data,
            int offset,
            int length)
        {
            hash.TransformBlock(data, offset, length, null, 0);
        }

        public static byte[] GetHashAndReset(this HashAlgorithm hash)
        {
            hash.TransformFinalBlock(Array.Empty<byte>(), 0, 0);
            return hash.Hash;
        }
    }

    public static partial class AuthenticatedEncryption
    {
        /// <summary>
        /// Use <paramref name="masterKey"/> to derive two keys (one cipher, one HMAC)
        /// to provide authenticated encryption for <paramref name="message"/>.
        /// </summary>
        /// <param name="masterKey">The master key from which other keys derive.</param>
        /// <param name="message">The message to encrypt</param>
        /// <returns>
        /// A concatenation of
        /// [cipher algorithm+chainmode+padding][mac algorithm][authtag][IV][ciphertext],
        /// suitable to be passed to <see cref="Decrypt"/>.
        /// </returns>
        /// <remarks>
        /// <paramref name="masterKey"/> should be a 128-bit (or bigger) value generated
        /// by a secure random number generator, such as the one returned from
        /// <see cref="RandomNumberGenerator.Create()"/>.
        /// This implementation chooses to block deficient inputs by length, but does not
        /// make any attempt at discerning the randomness of the key.
        ///
        /// If the master key is being input by a prompt (like a password/passphrase)
        /// then it should be properly turned into keying material via a Key Derivation
        /// Function like PBKDF2, represented by Rfc2898DeriveBytes. A 'password' should
        /// never be simply turned to bytes via an Encoding class and used as a key.
        /// </remarks>
        public static byte[] Encrypt(byte[] masterKey, byte[] message)
        {
            if (masterKey == null)
                throw new ArgumentNullException(nameof(masterKey));
            if (masterKey.Length < 16)
                throw new ArgumentOutOfRangeException(
                    nameof(masterKey),
                    "Master Key must be at least 128 bits (16 bytes)");
            if (message == null)
                throw new ArgumentNullException(nameof(message));

            // First, choose an encryption scheme.
            AeCipher aeCipher = AeCipher.Aes256CbcPkcs7;

            // Second, choose an authentication (message integrity) scheme.
            //
            // In this example we use the master key length to change from HMACSHA256 to
            // HMACSHA384, but that is completely arbitrary. This mostly represents a
            // "cryptographic needs change over time" scenario.
            AeMac aeMac = masterKey.Length < 48 ? AeMac.HMACSHA256 : AeMac.HMACSHA384;

            // It's good to be able to identify what choices were made when a message was
            // encrypted, so that the message can later be decrypted. This allows for
            // future versions to add support for new encryption schemes, but still be
            // able to read old data. A practice known as "cryptographic agility".
            //
            // This is similar in practice to PKCS#7 messaging, but this uses a
            // private-scoped byte rather than a public-scoped Object IDentifier (OID).
            // Please note that the scheme in this example adheres to no particular
            // standard, and is unlikely to survive to a more complete implementation in
            // the .NET Framework.
            //
            // You may be well-served by prepending a version number byte to this
            // message, but may want to avoid the value 0x30 (the leading byte value for
            // DER-encoded structures such as X.509 certificates and PKCS#7 messages).
            byte[] algorithmChoices = { (byte)aeCipher, (byte)aeMac };
            byte[] iv;
            byte[] cipherText;
            byte[] tag;

            // Using our algorithm choices, open an HMAC (as an authentication tag
            // generator) and a SymmetricAlgorithm which use different keys each derived
            // from the same master key.
            //
            // A custom implementation may very well have distinctly managed secret keys
            // for the MAC and cipher, this example merely demonstrates the master to
            // derived key methodology to encourage key separation from the MAC and
            // cipher keys.
            using (HMAC tagGenerator = GetMac(aeMac, masterKey))
            {
                using (SymmetricAlgorithm cipher = GetCipher(aeCipher, masterKey))
                using (ICryptoTransform encryptor = cipher.CreateEncryptor())
                {
                    // Since no IV was provided, a random one has been generated
                    // during the call to CreateEncryptor.
                    //
                    // But note that it only does the auto-generation once. If the cipher
                    // object were used again, a call to GenerateIV would have been
                    // required.
                    iv = cipher.IV;

                    cipherText = Transform(encryptor, message, 0, message.Length);
                }

                // The IV and ciphertest both need to be included in the MAC to prevent
                // tampering.
                //
                // By including the algorithm identifiers, we have technically moved from
                // simple Authenticated Encryption (AE) to Authenticated Encryption with
                // Additional Data (AEAD). By including the algorithm identifiers in the
                // MAC, it becomes harder for an attacker to change them as an attempt to
                // perform a downgrade attack.
                //
                // If you've added a data format version field, it can also be included
                // in the MAC to further inhibit an attacker's options for confusing the
                // data processor into believing the tampered message is valid.
                tagGenerator.AppendData(algorithmChoices);
                tagGenerator.AppendData(iv);
                tagGenerator.AppendData(cipherText);
                tag = tagGenerator.GetHashAndReset();
            }

            // Build the final result as the concatenation of everything except the keys.
            int totalLength =
                algorithmChoices.Length +
                tag.Length +
                iv.Length +
                cipherText.Length;

            byte[] output = new byte[totalLength];
            int outputOffset = 0;

            Append(algorithmChoices, output, ref outputOffset);
            Append(tag, output, ref outputOffset);
            Append(iv, output, ref outputOffset);
            Append(cipherText, output, ref outputOffset);

            Debug.Assert(outputOffset == output.Length);
            return output;
        }

        /// <summary>
        /// Reads a message produced by <see cref="Encrypt"/> after verifying it hasn't
        /// been tampered with.
        /// </summary>
        /// <param name="masterKey">The master key from which other keys derive.</param>
        /// <param name="cipherText">
        /// The output of <see cref="Encrypt"/>: a concatenation of a cipher ID, mac ID,
        /// authTag, IV, and cipherText.
        /// </param>
        /// <returns>The decrypted content.</returns>
        /// <exception cref="ArgumentNullException">
        /// <paramref name="masterKey"/> is <c>null</c>.
        /// </exception>
        /// <exception cref="ArgumentNullException">
        /// <paramref name="cipherText"/> is <c>null</c>.
        /// </exception>
        /// <exception cref="CryptographicException">
        /// <paramref name="cipherText"/> identifies unknown algorithms, is not long
        /// enough, fails a data integrity check, or fails to decrypt.
        /// </exception>
        /// <remarks>
        /// <paramref name="masterKey"/> should be a 128-bit (or larger) value
        /// generated by a secure random number generator, such as the one returned from
        /// <see cref="RandomNumberGenerator.Create()"/>. This implementation chooses to
        /// block deficient inputs by length, but doesn't make any attempt at
        /// discerning the randomness of the key.
        ///
        /// If the master key is being input by a prompt (like a password/passphrase),
        /// then it should be properly turned into keying material via a Key Derivation
        /// Function like PBKDF2, represented by Rfc2898DeriveBytes. A 'password' should
        /// never be simply turned to bytes via an Encoding class and used as a key.
        /// </remarks>
        public static byte[] Decrypt(byte[] masterKey, byte[] cipherText)
        {
            // This example continues the .NET practice of throwing exceptions for
            // failures. If you consider message tampering to be normal (and thus
            // "not exceptional") behavior, you may like the signature
            // bool Decrypt(byte[] messageKey, byte[] cipherText, out byte[] message)
            // better.
            if (masterKey == null)
                throw new ArgumentNullException(nameof(masterKey));
            if (masterKey.Length < 16)
                throw new ArgumentOutOfRangeException(
                    nameof(masterKey),
                    "Master Key must be at least 128 bits (16 bytes)");
            if (cipherText == null)
                throw new ArgumentNullException(nameof(cipherText));

            // The format of this message is assumed to be public, so there's no harm in
            // saying ahead of time that the message makes no sense.
            if (cipherText.Length < 2)
            {
                throw new CryptographicException();
            }

            // Use the message algorithm headers to determine what cipher algorithm and
            // MAC algorithm are going to be used. Since the same Key Derivation
            // Functions (KDFs) are being used in Decrypt as Encrypt, the keys are also
            // the same.
            AeCipher aeCipher = (AeCipher)cipherText[0];
            AeMac aeMac = (AeMac)cipherText[1];

            using (SymmetricAlgorithm cipher = GetCipher(aeCipher, masterKey))
            using (HMAC tagGenerator = GetMac(aeMac, masterKey))
            {
                int blockSizeInBytes = cipher.BlockSize / 8;
                int tagSizeInBytes = tagGenerator.HashSize / 8;
                int headerSizeInBytes = 2;
                int tagOffset = headerSizeInBytes;
                int ivOffset = tagOffset + tagSizeInBytes;
                int cipherTextOffset = ivOffset + blockSizeInBytes;
                int cipherTextLength = cipherText.Length - cipherTextOffset;
                int minLen = cipherTextOffset + blockSizeInBytes;

                // Again, the minimum length is still assumed to be public knowledge,
                // nothing has leaked out yet. The minimum length couldn't just be calculated
                // without reading the header.
                if (cipherText.Length < minLen)
                {
                    throw new CryptographicException();
                }

                // It's very important that the MAC be calculated and verified before
                // proceeding to decrypt the ciphertext, as this prevents any sort of
                // information leaking out to an attacker.
                //
                // Don't include the tag in the calculation, though.

                // First, everything before the tag (the cipher and MAC algorithm ids)
                tagGenerator.AppendData(cipherText, 0, tagOffset);

                // Skip the data before the tag and the tag, then read everything that
                // remains.
                tagGenerator.AppendData(
                    cipherText,
                    tagOffset + tagSizeInBytes,
                    cipherText.Length - tagSizeInBytes - tagOffset);

                byte[] generatedTag = tagGenerator.GetHashAndReset();

                // The time it took to get to this point has so far been a function only
                // of the length of the data, or of non-encrypted values (e.g. it could
                // take longer to prepare the *key* for the HMACSHA384 MAC than the
                // HMACSHA256 MAC, but the algorithm choice wasn't a secret).
                //
                // If the verification of the authentication tag aborts as soon as a
                // difference is found in the byte arrays then your program may be
                // acting as a timing oracle which helps an attacker to brute-force the
                // right answer for the MAC. So, it's very important that every possible
                // "no" (2^256-1 of them for HMACSHA256) be evaluated in as close to the
                // same amount of time as possible. For this, we call CryptographicEquals
                if (!CryptographicEquals(
                    generatedTag,
                    0,
                    cipherText,
                    tagOffset,
                    tagSizeInBytes))
                {
                    // Assuming every tampered message (of the same length) took the same
                    // amount of time to process, we can now safely say
                    // "this data makes no sense" without giving anything away.
                    throw new CryptographicException();
                }

                // Restore the IV into the symmetricAlgorithm instance.
                byte[] iv = new byte[blockSizeInBytes];
                Buffer.BlockCopy(cipherText, ivOffset, iv, 0, iv.Length);
                cipher.IV = iv;

                using (ICryptoTransform decryptor = cipher.CreateDecryptor())
                {
                    return Transform(
                        decryptor,
                        cipherText,
                        cipherTextOffset,
                        cipherTextLength);
                }
            }
        }

        private static byte[] Transform(
            ICryptoTransform transform,
            byte[] input,
            int inputOffset,
            int inputLength)
        {
            // Many of the implementations of ICryptoTransform report true for
            // CanTransformMultipleBlocks, and when the entire message is available in
            // one shot this saves on the allocation of the CryptoStream and the
            // intermediate structures it needs to properly chunk the message into blocks
            // (since the underlying stream won't always return the number of bytes
            // needed).
            if (transform.CanTransformMultipleBlocks)
            {
                return transform.TransformFinalBlock(input, inputOffset, inputLength);
            }

            // If our transform couldn't do multiple blocks at once, let CryptoStream
            // handle the chunking.
            using (MemoryStream messageStream = new MemoryStream())
            using (CryptoStream cryptoStream =
                new CryptoStream(messageStream, transform, CryptoStreamMode.Write))
            {
                cryptoStream.Write(input, inputOffset, inputLength);
                cryptoStream.FlushFinalBlock();
                return messageStream.ToArray();
            }
        }

        /// <summary>
        /// Open a properly configured <see cref="SymmetricAlgorithm"/> conforming to the
        /// scheme identified by <paramref name="aeCipher"/>.
        /// </summary>
        /// <param name="aeCipher">The cipher mode to open.</param>
        /// <param name="masterKey">The master key from which other keys derive.</param>
        /// <returns>
        /// A SymmetricAlgorithm object with the right key, cipher mode, and padding
        /// mode; or <c>null</c> on unknown algorithms.
        /// </returns>
        private static SymmetricAlgorithm GetCipher(AeCipher aeCipher, byte[] masterKey)
        {
            SymmetricAlgorithm symmetricAlgorithm;

            switch (aeCipher)
            {
                case AeCipher.Aes256CbcPkcs7:
                    symmetricAlgorithm = Aes.Create();
                    // While 256-bit, CBC, and PKCS7 are all the default values for these
                    // properties, being explicit helps comprehension more than it hurts
                    // performance.
                    symmetricAlgorithm.KeySize = 256;
                    symmetricAlgorithm.Mode = CipherMode.CBC;
                    symmetricAlgorithm.Padding = PaddingMode.PKCS7;
                    break;
                default:
                    // An algorithm we don't understand
                    throw new CryptographicException();
            }

            // Instead of using the master key directly, derive a key for our chosen
            // HMAC algorithm based upon the master key.
            //
            // Since none of the symmetric encryption algorithms currently in .NET
            // support key sizes greater than 256-bit, we can use HMACSHA256 with
            // NIST SP 800-108 5.1 (Counter Mode KDF) to derive a value that is
            // no smaller than the key size, then Array.Resize to trim it down as
            // needed.

            using (HMAC hmac = new HMACSHA256(masterKey))
            {
                // i=1, Label=ASCII(cipher)
                byte[] cipherKey = hmac.ComputeHash(
                    new byte[] { 1, 99, 105, 112, 104, 101, 114 });

                // Resize the array to the desired keysize. KeySize is in bits,
                // and Array.Resize wants the length in bytes.
                Array.Resize(ref cipherKey, symmetricAlgorithm.KeySize / 8);

                symmetricAlgorithm.Key = cipherKey;
            }

            return symmetricAlgorithm;
        }

        /// <summary>
        /// Open a properly configured <see cref="HMAC"/> conforming to the scheme
        /// identified by <paramref name="aeMac"/>.
        /// </summary>
        /// <param name="aeMac">The message authentication mode to open.</param>
        /// <param name="masterKey">The master key from which other keys derive.</param>
        /// <returns>
        /// An HMAC object with the proper key, or <c>null</c> on unknown algorithms.
        /// </returns>
        private static HMAC GetMac(AeMac aeMac, byte[] masterKey)
        {
            HMAC hmac;

            switch (aeMac)
            {
                case AeMac.HMACSHA256:
                    hmac = new HMACSHA256();
                    break;
                case AeMac.HMACSHA384:
                    hmac = new HMACSHA384();
                    break;
                default:
                    // An algorithm we don't understand
                    throw new CryptographicException();
            }

            // Instead of using the master key directly, derive a key for our chosen
            // HMAC algorithm based upon the master key.
            // Since the output size of the HMAC is the same as the ideal key size for
            // the HMAC, we can use the master key over a fixed input once to perform
            // NIST SP 800-108 5.1 (Counter Mode KDF):
            hmac.Key = masterKey;

            // i=1, Context=ASCII(MAC)
            byte[] newKey = hmac.ComputeHash(new byte[] { 1, 77, 65, 67 });

            hmac.Key = newKey;
            return hmac;
        }

        // A simple helper method to ensure that the offset (writePos) always moves
        // forward with new data.
        private static void Append(byte[] newData, byte[] combinedData, ref int writePos)
        {
            Buffer.BlockCopy(newData, 0, combinedData, writePos, newData.Length);
            writePos += newData.Length;
        }

        /// <summary>
        /// Compare the contents of two arrays in an amount of time which is only
        /// dependent on <paramref name="length"/>.
        /// </summary>
        /// <param name="a">An array to compare to <paramref name="b"/>.</param>
        /// <param name="aOffset">
        /// The starting position within <paramref name="a"/> for comparison.
        /// </param>
        /// <param name="b">An array to compare to <paramref name="a"/>.</param>
        /// <param name="bOffset">
        /// The starting position within <paramref name="b"/> for comparison.
        /// </param>
        /// <param name="length">
        /// The number of bytes to compare between <paramref name="a"/> and
        /// <paramref name="b"/>.</param>
        /// <returns>
        /// <c>true</c> if both <paramref name="a"/> and <paramref name="b"/> have
        /// sufficient length for the comparison and all of the applicable values are the
        /// same in both arrays; <c>false</c> otherwise.
        /// </returns>
        /// <remarks>
        /// An "insufficient data" <c>false</c> response can happen early, but otherwise
        /// a <c>true</c> or <c>false</c> response take the same amount of time.
        /// </remarks>
        [MethodImpl(MethodImplOptions.NoInlining | MethodImplOptions.NoOptimization)]
        private static bool CryptographicEquals(
            byte[] a,
            int aOffset,
            byte[] b,
            int bOffset,
            int length)
        {
            Debug.Assert(a != null);
            Debug.Assert(b != null);
            Debug.Assert(length >= 0);

            int result = 0;

            if (a.Length - aOffset < length || b.Length - bOffset < length)
            {
                return false;
            }

            unchecked
            {
                for (int i = 0; i < length; i++)
                {
                    // Bitwise-OR of subtraction has been found to have the most
                    // stable execution time.
                    //
                    // This cannot overflow because bytes are 1 byte in length, and
                    // result is 4 bytes.
                    // The OR propagates all set bytes, so the differences are only
                    // present in the lowest byte.
                    result = result | (a[i + aOffset] - b[i + bOffset]);
                }
            }

            return result == 0;
        }
    }
}
```
