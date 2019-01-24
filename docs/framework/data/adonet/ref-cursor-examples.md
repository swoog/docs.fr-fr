---
title: Exemples REF CURSOR
ms.date: 03/30/2017
ms.assetid: c257da03-c6c9-4cf8-b591-b7740a962c40
ms.openlocfilehash: 00e1cd1b9c13514979ee22b32996d35e1bd1c3e2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54615346"
---
# <a name="ref-cursor-examples"></a>Exemples REF CURSOR
Les exemples de REF CURSOR comprennent les trois exemples Microsoft Visual Basic suivants qui illustrent l'utilisation des REF CURSOR.  
  
|Exemple|Description|  
|------------|-----------------|  
|[Paramètres REF CURSOR dans un OracleDataReader](../../../../docs/framework/data/adonet/ref-cursor-parameters-in-an-oracledatareader.md)|Cet exemple exécute une procédure stockée PL/SQL qui retourne un paramètre REF CURSOR et lit la valeur comme un <xref:System.Data.OracleClient.OracleDataReader>.|  
|[Récupération de données à partir de plusieurs REF CURSOR à l’aide d’un OracleDataReader](../../../../docs/framework/data/adonet/retrieving-data-from-multiple-ref-cursors.md)|Cet exemple exécute une procédure stockée PL/SQL qui retourne deux paramètres REF CURSOR et lit les valeurs en utilisant un **OracleDataReader**.|  
|[Remplissage d’un DataSet à l’aide d’un ou de plusieurs REF CURSOR](../../../../docs/framework/data/adonet/filling-a-dataset-using-one-or-more-ref-cursors.md)|Cet exemple exécute une procédure stockée PL/SQL qui retourne deux paramètres REF CURSOR et remplit un <xref:System.Data.DataSet> avec les lignes qui sont retournées.|  
  
 Pour utiliser ces exemples, il se peut que vous deviez créer les tables Oracle et vous devez créer un package PL/SQL et un corps de package.  
  
## <a name="creating-the-oracle-tables"></a>Création des tables Oracle  
 Ces exemples utilisent des tables définies dans le schéma Oracle Scott/Tiger. Le schéma Oracle Scott/Tiger est fourni avec la plupart des installations Oracle. Si ce schéma n'existe pas, vous pouvez utiliser le fichier de commandes SQL dans {OracleHome}\rdbms\admin\scott.sql pour créer les tables et les index utilisés par ces exemples.  
  
## <a name="creating-the-oracle-package-and-package-body"></a>Création du package Oracle et du corps de package  
 Ces exemples requièrent le package et le corps de package PL/SQL suivants sur votre serveur Créez le package Oracle suivant sur le serveur Oracle.  
  
```sql
CREATE OR REPLACE PACKAGE CURSPKG AS   
    TYPE T_CURSOR IS REF CURSOR;   
    PROCEDURE OPEN_ONE_CURSOR (N_EMPNO IN NUMBER,   
                               IO_CURSOR IN OUT T_CURSOR);   
    PROCEDURE OPEN_TWO_CURSORS (EMPCURSOR OUT T_CURSOR,   
                                DEPTCURSOR OUT T_CURSOR);  
END CURSPKG;  
/   
```  
  
 Créez le corps du package Oracle suivant sur le serveur Oracle.  
  
```sql
CREATE OR REPLACE PACKAGE BODY CURSPKG AS  
    PROCEDURE OPEN_ONE_CURSOR (N_EMPNO IN NUMBER,  
                               IO_CURSOR IN OUT T_CURSOR)  
    IS   
        V_CURSOR T_CURSOR;   
    BEGIN   
        IF N_EMPNO <> 0   
        THEN  
             OPEN V_CURSOR FOR   
             SELECT EMP.EMPNO, EMP.ENAME, DEPT.DEPTNO, DEPT.DNAME   
                  FROM EMP, DEPT   
                  WHERE EMP.DEPTNO = DEPT.DEPTNO   
                  AND EMP.EMPNO = N_EMPNO;  
  
        ELSE   
             OPEN V_CURSOR FOR   
             SELECT EMP.EMPNO, EMP.ENAME, DEPT.DEPTNO, DEPT.DNAME   
                  FROM EMP, DEPT   
                  WHERE EMP.DEPTNO = DEPT.DEPTNO;  
  
        END IF;  
        IO_CURSOR := V_CURSOR;   
    END OPEN_ONE_CURSOR;   
  
    PROCEDURE OPEN_TWO_CURSORS (EMPCURSOR OUT T_CURSOR,  
                                DEPTCURSOR OUT T_CURSOR)  
    IS   
        V_CURSOR1 T_CURSOR;   
        V_CURSOR2 T_CURSOR;   
    BEGIN   
        OPEN V_CURSOR1 FOR SELECT * FROM EMP;  
        OPEN V_CURSOR2 FOR SELECT * FROM DEPT;  
        EMPCURSOR  := V_CURSOR1;   
        DEPTCURSOR := V_CURSOR2;   
    END OPEN_TWO_CURSORS;   
END CURSPKG;  
/  
```  
  
## <a name="see-also"></a>Voir aussi
- [REF CURSOR Oracle](../../../../docs/framework/data/adonet/oracle-ref-cursors.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
