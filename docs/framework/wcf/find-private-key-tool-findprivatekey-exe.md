---
title: Outil de recherche de clé privée (FindPrivateKey.exe)
ms.date: 09/11/2017
ms.assetid: b8846a95-3fcc-4e8c-b9c0-128d975a6307
ms.openlocfilehash: 8f156cbb2f4fad8d51e356bd4dee2d72d9397ffb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61929582"
---
# <a name="find-private-key-tool-findprivatekeyexe"></a>Outil de recherche de clé privée (FindPrivateKey.exe)

Cet outil de ligne de commande peut être utilisé pour récupérer une clé privée provenant d'un magasin de certificats. Par exemple, *FindPrivateKey.exe* peut être utilisé pour rechercher l’emplacement et le nom du fichier de clé privée associé à un certificat X.509 spécifique dans le magasin de certificats.

> [!IMPORTANT]
> L'outil FindPrivateKey est fourni à titre d'exemple WCF. Pour plus d’informations sur l’accès à l’exemple et comment le créer, consultez [FindPrivateKey](./samples/findprivatekey.md).

## <a name="syntax"></a>Syntaxe

```
FindPrivateKey<storeName> <storeLocation> [{ {-n <subjectName>} | {-t <thumbprint>} } [-f | -d | -a]]
```

## <a name="remarks"></a>Notes

Les tables suivantes décrivent les arguments et les options qui peuvent être utilisés avec l'outil de recherche de clé privée Clé (FindPrivateKey.exe).

|Argument|Description|
|--------------|-----------------|
|`storeName`|Nom du magasin de certificats|
|`storeLocation`|Emplacement du magasin de certificats|

|Option|Description|
|------------|-----------------|
|`/n <` *subjectName* `>`|Spécifie le nom du sujet du certificat.|
|`/t <` *thumbprint* `>`|Spécifie l'empreinte numérique du certificat. Utilisez Certmgr.exe pour récupérer l'empreinte numérique du certificat.|
|`/f`|Affiche le nom de fichier uniquement.|
|`/d`|Affiche le répertoire uniquement.|
|`/a`|Affiche le nom de fichier absolu.|

## <a name="examples"></a>Exemples

La commande suivante récupère la clé privée pour John Doe :

```
FindPrivateKey My CurrentUser -n "CN=John Doe"
```

La commande suivante récupère la clé privée pour l’ordinateur local :

```
FindPrivateKey My LocalMachine -t "03 33 98 63 d0 47 e7 48 71 33 62 64 76 5c 4c 9d 42 1d 6b 52" –a
```