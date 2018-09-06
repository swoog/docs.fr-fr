---
title: Collections de schémas ODBC
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43877529"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="b3b81-102">Collections de schémas ODBC</span><span class="sxs-lookup"><span data-stu-id="b3b81-102">ODBC Schema Collections</span></span>
<span data-ttu-id="b3b81-103">Cette section traite de la prise en charge des collections de schémas pour les pilotes ODBC Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="b3b81-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="b3b81-104">Pilote Microsoft SQL Server ODBC</span><span class="sxs-lookup"><span data-stu-id="b3b81-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="b3b81-105">Le pilote ODBC de Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="b3b81-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="b3b81-106">Tables</span><span class="sxs-lookup"><span data-stu-id="b3b81-106">Tables</span></span>  
  
-   <span data-ttu-id="b3b81-107">Index</span><span class="sxs-lookup"><span data-stu-id="b3b81-107">Indexes</span></span>  
  
-   <span data-ttu-id="b3b81-108">Columns</span><span class="sxs-lookup"><span data-stu-id="b3b81-108">Columns</span></span>  
  
-   <span data-ttu-id="b3b81-109">Procédures</span><span class="sxs-lookup"><span data-stu-id="b3b81-109">Procedures</span></span>  
  
-   <span data-ttu-id="b3b81-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="b3b81-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="b3b81-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="b3b81-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="b3b81-112">Vues</span><span class="sxs-lookup"><span data-stu-id="b3b81-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="b3b81-113">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="b3b81-113">Tables and Views</span></span>  
  
|<span data-ttu-id="b3b81-114">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-114">ColumnName</span></span>|<span data-ttu-id="b3b81-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="b3b81-116">TABLE_CAT</span></span>|<span data-ttu-id="b3b81-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-117">String</span></span>|  
|<span data-ttu-id="b3b81-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="b3b81-118">TABLE_SCHEM</span></span>|<span data-ttu-id="b3b81-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-119">String</span></span>|  
|<span data-ttu-id="b3b81-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-120">TABLE_NAME</span></span>|<span data-ttu-id="b3b81-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-121">String</span></span>|  
|<span data-ttu-id="b3b81-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-122">TABLE_TYPE</span></span>|<span data-ttu-id="b3b81-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-123">String</span></span>|  
|<span data-ttu-id="b3b81-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-124">REMARKS</span></span>|<span data-ttu-id="b3b81-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="b3b81-126">Index</span><span class="sxs-lookup"><span data-stu-id="b3b81-126">Indexes</span></span>  
  
|<span data-ttu-id="b3b81-127">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-127">ColumnName</span></span>|<span data-ttu-id="b3b81-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="b3b81-129">TABLE_CAT</span></span>|<span data-ttu-id="b3b81-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-130">String</span></span>|  
|<span data-ttu-id="b3b81-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="b3b81-131">TABLE_SCHEM</span></span>|<span data-ttu-id="b3b81-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-132">String</span></span>|  
|<span data-ttu-id="b3b81-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-133">TABLE_NAME</span></span>|<span data-ttu-id="b3b81-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-134">String</span></span>|  
|<span data-ttu-id="b3b81-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="b3b81-135">NON_UNIQUE</span></span>|<span data-ttu-id="b3b81-136">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-136">Int16</span></span>|  
|<span data-ttu-id="b3b81-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="b3b81-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-138">String</span></span>|  
|<span data-ttu-id="b3b81-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-139">INDEX_NAME</span></span>|<span data-ttu-id="b3b81-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-140">String</span></span>|  
|<span data-ttu-id="b3b81-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-141">TYPE</span></span>|<span data-ttu-id="b3b81-142">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-142">Int16</span></span>|  
|<span data-ttu-id="b3b81-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-144">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-144">Int16</span></span>|  
|<span data-ttu-id="b3b81-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-145">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-146">String</span></span>|  
|<span data-ttu-id="b3b81-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="b3b81-147">ASC_OR_DESC</span></span>|<span data-ttu-id="b3b81-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-148">String</span></span>|  
|<span data-ttu-id="b3b81-149">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="b3b81-149">CARDINATLITY</span></span>|<span data-ttu-id="b3b81-150">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-150">Int32</span></span>|  
|<span data-ttu-id="b3b81-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="b3b81-151">PAGES</span></span>|<span data-ttu-id="b3b81-152">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-152">Int32</span></span>|  
|<span data-ttu-id="b3b81-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-153">FILTER_CONDITION</span></span>|<span data-ttu-id="b3b81-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-154">String</span></span>|  
|<span data-ttu-id="b3b81-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="b3b81-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="b3b81-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-156">String</span></span>|  
|<span data-ttu-id="b3b81-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="b3b81-158">Byte</span><span class="sxs-lookup"><span data-stu-id="b3b81-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="b3b81-159">Columns</span><span class="sxs-lookup"><span data-stu-id="b3b81-159">Columns</span></span>  
  
|<span data-ttu-id="b3b81-160">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-160">ColumnName</span></span>|<span data-ttu-id="b3b81-161">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="b3b81-162">TABLE_CAT</span></span>|<span data-ttu-id="b3b81-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-163">String</span></span>|  
|<span data-ttu-id="b3b81-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="b3b81-164">TABLE_SCHEM</span></span>|<span data-ttu-id="b3b81-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-165">String</span></span>|  
|<span data-ttu-id="b3b81-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-166">TABLE_NAME</span></span>|<span data-ttu-id="b3b81-167">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-167">String</span></span>|  
|<span data-ttu-id="b3b81-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-168">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-169">String</span></span>|  
|<span data-ttu-id="b3b81-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-170">DATA_TYPE</span></span>|<span data-ttu-id="b3b81-171">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-171">Int16</span></span>|  
|<span data-ttu-id="b3b81-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-172">TYPE_NAME</span></span>|<span data-ttu-id="b3b81-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-173">String</span></span>|  
|<span data-ttu-id="b3b81-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="b3b81-174">COLUMN_SIZE</span></span>|<span data-ttu-id="b3b81-175">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-175">Int32</span></span>|  
|<span data-ttu-id="b3b81-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="b3b81-177">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-177">Int32</span></span>|  
|<span data-ttu-id="b3b81-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="b3b81-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="b3b81-179">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-179">Int16</span></span>|  
|<span data-ttu-id="b3b81-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="b3b81-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="b3b81-181">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-181">Int16</span></span>|  
|<span data-ttu-id="b3b81-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-182">NULLABLE</span></span>|<span data-ttu-id="b3b81-183">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-183">Int16</span></span>|  
|<span data-ttu-id="b3b81-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-184">REMARKS</span></span>|<span data-ttu-id="b3b81-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-185">String</span></span>|  
|<span data-ttu-id="b3b81-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="b3b81-186">COLUMN_DEF</span></span>|<span data-ttu-id="b3b81-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-187">String</span></span>|  
|<span data-ttu-id="b3b81-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="b3b81-189">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-189">Int16</span></span>|  
|<span data-ttu-id="b3b81-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="b3b81-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="b3b81-191">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-191">Int16</span></span>|  
|<span data-ttu-id="b3b81-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="b3b81-193">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-193">Int32</span></span>|  
|<span data-ttu-id="b3b81-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-195">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-195">Int32</span></span>|  
|<span data-ttu-id="b3b81-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-196">IS_NULLABLE</span></span>|<span data-ttu-id="b3b81-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-197">String</span></span>|  
|<span data-ttu-id="b3b81-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="b3b81-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="b3b81-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-199">String</span></span>|  
|<span data-ttu-id="b3b81-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="b3b81-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="b3b81-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-201">String</span></span>|  
|<span data-ttu-id="b3b81-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="b3b81-203">Byte</span><span class="sxs-lookup"><span data-stu-id="b3b81-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="b3b81-204">Procédures</span><span class="sxs-lookup"><span data-stu-id="b3b81-204">Procedures</span></span>  
  
|<span data-ttu-id="b3b81-205">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-205">ColumnName</span></span>|<span data-ttu-id="b3b81-206">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="b3b81-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="b3b81-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-208">String</span></span>|  
|<span data-ttu-id="b3b81-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="b3b81-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="b3b81-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-210">String</span></span>|  
|<span data-ttu-id="b3b81-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="b3b81-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-212">String</span></span>|  
|<span data-ttu-id="b3b81-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="b3b81-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="b3b81-214">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-214">Int32</span></span>|  
|<span data-ttu-id="b3b81-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="b3b81-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="b3b81-216">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-216">Int32</span></span>|  
|<span data-ttu-id="b3b81-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="b3b81-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="b3b81-218">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-218">Int32</span></span>|  
|<span data-ttu-id="b3b81-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-219">REMARKS</span></span>|<span data-ttu-id="b3b81-220">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-220">String</span></span>|  
|<span data-ttu-id="b3b81-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="b3b81-222">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="b3b81-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="b3b81-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="b3b81-224">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-224">ColumnName</span></span>|<span data-ttu-id="b3b81-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="b3b81-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="b3b81-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-227">String</span></span>|  
|<span data-ttu-id="b3b81-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="b3b81-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="b3b81-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-229">String</span></span>|  
|<span data-ttu-id="b3b81-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="b3b81-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-231">String</span></span>|  
|<span data-ttu-id="b3b81-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-232">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-233">String</span></span>|  
|<span data-ttu-id="b3b81-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-234">COLUMN_TYPE</span></span>|<span data-ttu-id="b3b81-235">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-235">Int16</span></span>|  
|<span data-ttu-id="b3b81-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-236">DATA_TYPE</span></span>|<span data-ttu-id="b3b81-237">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-237">Int16</span></span>|  
|<span data-ttu-id="b3b81-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-238">TYPE_NAME</span></span>|<span data-ttu-id="b3b81-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-239">String</span></span>|  
|<span data-ttu-id="b3b81-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="b3b81-240">COLUMN_SIZE</span></span>|<span data-ttu-id="b3b81-241">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-241">Int32</span></span>|  
|<span data-ttu-id="b3b81-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="b3b81-243">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-243">Int32</span></span>|  
|<span data-ttu-id="b3b81-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="b3b81-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="b3b81-245">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-245">Int16</span></span>|  
|<span data-ttu-id="b3b81-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="b3b81-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="b3b81-247">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-247">Int16</span></span>|  
|<span data-ttu-id="b3b81-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-248">NULLABLE</span></span>|<span data-ttu-id="b3b81-249">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-249">Int16</span></span>|  
|<span data-ttu-id="b3b81-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-250">REMARKS</span></span>|<span data-ttu-id="b3b81-251">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-251">String</span></span>|  
|<span data-ttu-id="b3b81-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="b3b81-252">COLUMN_DEF</span></span>|<span data-ttu-id="b3b81-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-253">String</span></span>|  
|<span data-ttu-id="b3b81-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="b3b81-255">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-255">Int16</span></span>|  
|<span data-ttu-id="b3b81-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="b3b81-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="b3b81-257">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-257">Int16</span></span>|  
|<span data-ttu-id="b3b81-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="b3b81-259">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-259">Int32</span></span>|  
|<span data-ttu-id="b3b81-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-261">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-261">Int32</span></span>|  
|<span data-ttu-id="b3b81-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-262">IS_NULLABLE</span></span>|<span data-ttu-id="b3b81-263">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-263">String</span></span>|  
|<span data-ttu-id="b3b81-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="b3b81-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="b3b81-265">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-265">String</span></span>|  
|<span data-ttu-id="b3b81-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="b3b81-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="b3b81-267">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-267">String</span></span>|  
|<span data-ttu-id="b3b81-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="b3b81-269">Byte</span><span class="sxs-lookup"><span data-stu-id="b3b81-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="b3b81-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="b3b81-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="b3b81-271">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-271">ColumnName</span></span>|<span data-ttu-id="b3b81-272">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="b3b81-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="b3b81-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-274">String</span></span>|  
|<span data-ttu-id="b3b81-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="b3b81-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="b3b81-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-276">String</span></span>|  
|<span data-ttu-id="b3b81-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="b3b81-278">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-278">String</span></span>|  
|<span data-ttu-id="b3b81-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-279">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-280">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-280">String</span></span>|  
|<span data-ttu-id="b3b81-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-281">COLUMN_TYPE</span></span>|<span data-ttu-id="b3b81-282">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-282">Int16</span></span>|  
|<span data-ttu-id="b3b81-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-283">DATA_TYPE</span></span>|<span data-ttu-id="b3b81-284">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-284">Int16</span></span>|  
|<span data-ttu-id="b3b81-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-285">TYPE_NAME</span></span>|<span data-ttu-id="b3b81-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-286">String</span></span>|  
|<span data-ttu-id="b3b81-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="b3b81-287">COLUMN_SIZE</span></span>|<span data-ttu-id="b3b81-288">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-288">Int32</span></span>|  
|<span data-ttu-id="b3b81-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="b3b81-290">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-290">Int32</span></span>|  
|<span data-ttu-id="b3b81-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="b3b81-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="b3b81-292">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-292">Int16</span></span>|  
|<span data-ttu-id="b3b81-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="b3b81-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="b3b81-294">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-294">Int16</span></span>|  
|<span data-ttu-id="b3b81-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-295">NULLABLE</span></span>|<span data-ttu-id="b3b81-296">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-296">Int16</span></span>|  
|<span data-ttu-id="b3b81-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-297">REMARKS</span></span>|<span data-ttu-id="b3b81-298">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-298">String</span></span>|  
|<span data-ttu-id="b3b81-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="b3b81-299">COLUMN_DEF</span></span>|<span data-ttu-id="b3b81-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-300">String</span></span>|  
|<span data-ttu-id="b3b81-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="b3b81-302">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-302">Int16</span></span>|  
|<span data-ttu-id="b3b81-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="b3b81-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="b3b81-304">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-304">Int16</span></span>|  
|<span data-ttu-id="b3b81-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="b3b81-306">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-306">Int32</span></span>|  
|<span data-ttu-id="b3b81-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-308">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-308">Int32</span></span>|  
|<span data-ttu-id="b3b81-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-309">IS_NULLABLE</span></span>|<span data-ttu-id="b3b81-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-310">String</span></span>|  
|<span data-ttu-id="b3b81-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="b3b81-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="b3b81-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-312">String</span></span>|  
|<span data-ttu-id="b3b81-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="b3b81-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="b3b81-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-314">String</span></span>|  
|<span data-ttu-id="b3b81-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="b3b81-316">Byte</span><span class="sxs-lookup"><span data-stu-id="b3b81-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="b3b81-317">Pilote Microsoft Oracle ODBC</span><span class="sxs-lookup"><span data-stu-id="b3b81-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="b3b81-318">Le pilote Microsoft SQL Server Oracle ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="b3b81-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="b3b81-319">Tables</span><span class="sxs-lookup"><span data-stu-id="b3b81-319">Tables</span></span>  
  
-   <span data-ttu-id="b3b81-320">Columns</span><span class="sxs-lookup"><span data-stu-id="b3b81-320">Columns</span></span>  
  
-   <span data-ttu-id="b3b81-321">Procédures</span><span class="sxs-lookup"><span data-stu-id="b3b81-321">Procedures</span></span>  
  
-   <span data-ttu-id="b3b81-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="b3b81-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="b3b81-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="b3b81-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="b3b81-324">Vues</span><span class="sxs-lookup"><span data-stu-id="b3b81-324">Views</span></span>  
  
-   <span data-ttu-id="b3b81-325">Index</span><span class="sxs-lookup"><span data-stu-id="b3b81-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="b3b81-326">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="b3b81-326">Tables and Views</span></span>  
  
|<span data-ttu-id="b3b81-327">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-327">ColumnName</span></span>|<span data-ttu-id="b3b81-328">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="b3b81-330">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-330">String</span></span>|  
|<span data-ttu-id="b3b81-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3b81-331">TABLE_OWNER</span></span>|<span data-ttu-id="b3b81-332">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-332">String</span></span>|  
|<span data-ttu-id="b3b81-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-333">TABLE_NAME</span></span>|<span data-ttu-id="b3b81-334">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-334">String</span></span>|  
|<span data-ttu-id="b3b81-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-335">TABLE_TYPE</span></span>|<span data-ttu-id="b3b81-336">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-336">String</span></span>|  
|<span data-ttu-id="b3b81-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-337">REMARKS</span></span>|<span data-ttu-id="b3b81-338">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="b3b81-339">Columns</span><span class="sxs-lookup"><span data-stu-id="b3b81-339">Columns</span></span>  
  
|<span data-ttu-id="b3b81-340">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-340">ColumnName</span></span>|<span data-ttu-id="b3b81-341">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="b3b81-343">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-343">String</span></span>|  
|<span data-ttu-id="b3b81-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3b81-344">TABLE_OWNER</span></span>|<span data-ttu-id="b3b81-345">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-345">String</span></span>|  
|<span data-ttu-id="b3b81-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-346">TABLE_NAME</span></span>|<span data-ttu-id="b3b81-347">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-347">String</span></span>|  
|<span data-ttu-id="b3b81-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-348">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-349">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-349">String</span></span>|  
|<span data-ttu-id="b3b81-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-350">DATA_TYPE</span></span>|<span data-ttu-id="b3b81-351">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-351">Int16</span></span>|  
|<span data-ttu-id="b3b81-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-352">TYPE_NAME</span></span>|<span data-ttu-id="b3b81-353">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-353">String</span></span>|  
|<span data-ttu-id="b3b81-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="b3b81-354">PRECISION</span></span>|<span data-ttu-id="b3b81-355">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-355">Int32</span></span>|  
|<span data-ttu-id="b3b81-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-356">LENGTH</span></span>|<span data-ttu-id="b3b81-357">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-357">Int32</span></span>|  
|<span data-ttu-id="b3b81-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="b3b81-358">SCALE</span></span>|<span data-ttu-id="b3b81-359">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-359">Int16</span></span>|  
|<span data-ttu-id="b3b81-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="b3b81-360">RADIX</span></span>|<span data-ttu-id="b3b81-361">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-361">Int16</span></span>|  
|<span data-ttu-id="b3b81-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-362">NULLABLE</span></span>|<span data-ttu-id="b3b81-363">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-363">Int16</span></span>|  
|<span data-ttu-id="b3b81-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-364">REMARKS</span></span>|<span data-ttu-id="b3b81-365">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-365">String</span></span>|  
|<span data-ttu-id="b3b81-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-367">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="b3b81-368">Procédures</span><span class="sxs-lookup"><span data-stu-id="b3b81-368">Procedures</span></span>  
  
|<span data-ttu-id="b3b81-369">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-369">ColumnName</span></span>|<span data-ttu-id="b3b81-370">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="b3b81-372">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-372">String</span></span>|  
|<span data-ttu-id="b3b81-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3b81-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="b3b81-374">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-374">String</span></span>|  
|<span data-ttu-id="b3b81-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="b3b81-376">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-376">String</span></span>|  
|<span data-ttu-id="b3b81-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="b3b81-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="b3b81-378">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-378">Int16</span></span>|  
|<span data-ttu-id="b3b81-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="b3b81-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="b3b81-380">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-380">Int16</span></span>|  
|<span data-ttu-id="b3b81-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="b3b81-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="b3b81-382">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-382">Int16</span></span>|  
|<span data-ttu-id="b3b81-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-383">REMARKS</span></span>|<span data-ttu-id="b3b81-384">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-384">String</span></span>|  
|<span data-ttu-id="b3b81-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="b3b81-386">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="b3b81-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="b3b81-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="b3b81-388">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-388">ColumnName</span></span>|<span data-ttu-id="b3b81-389">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="b3b81-391">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-391">String</span></span>|  
|<span data-ttu-id="b3b81-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3b81-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="b3b81-393">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-393">String</span></span>|  
|<span data-ttu-id="b3b81-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="b3b81-395">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-395">String</span></span>|  
|<span data-ttu-id="b3b81-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-396">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-397">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-397">String</span></span>|  
|<span data-ttu-id="b3b81-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-398">COLUMN_TYPE</span></span>|<span data-ttu-id="b3b81-399">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-399">Int16</span></span>|  
|<span data-ttu-id="b3b81-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-400">DATA_TYPE</span></span>|<span data-ttu-id="b3b81-401">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-401">Int16</span></span>|  
|<span data-ttu-id="b3b81-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-402">TYPE_NAME</span></span>|<span data-ttu-id="b3b81-403">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-403">String</span></span>|  
|<span data-ttu-id="b3b81-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="b3b81-404">PRECISION</span></span>|<span data-ttu-id="b3b81-405">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-405">Int32</span></span>|  
|<span data-ttu-id="b3b81-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-406">LENGTH</span></span>|<span data-ttu-id="b3b81-407">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-407">Int32</span></span>|  
|<span data-ttu-id="b3b81-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="b3b81-408">SCALE</span></span>|<span data-ttu-id="b3b81-409">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-409">Int16</span></span>|  
|<span data-ttu-id="b3b81-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="b3b81-410">RADIX</span></span>|<span data-ttu-id="b3b81-411">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-411">Int16</span></span>|  
|<span data-ttu-id="b3b81-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-412">NULLABLE</span></span>|<span data-ttu-id="b3b81-413">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-413">Int16</span></span>|  
|<span data-ttu-id="b3b81-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-414">REMARKS</span></span>|<span data-ttu-id="b3b81-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-415">String</span></span>|  
|<span data-ttu-id="b3b81-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="b3b81-416">OVERLOAD</span></span>|<span data-ttu-id="b3b81-417">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-417">Int32</span></span>|  
|<span data-ttu-id="b3b81-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-419">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="b3b81-420">Pilote Microsoft Jet ODBC</span><span class="sxs-lookup"><span data-stu-id="b3b81-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="b3b81-421">Le pilote Microsoft Jet ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="b3b81-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="b3b81-422">Tables</span><span class="sxs-lookup"><span data-stu-id="b3b81-422">Tables</span></span>  
  
-   <span data-ttu-id="b3b81-423">Index</span><span class="sxs-lookup"><span data-stu-id="b3b81-423">Indexes</span></span>  
  
-   <span data-ttu-id="b3b81-424">Columns</span><span class="sxs-lookup"><span data-stu-id="b3b81-424">Columns</span></span>  
  
-   <span data-ttu-id="b3b81-425">Procédures</span><span class="sxs-lookup"><span data-stu-id="b3b81-425">Procedures</span></span>  
  
-   <span data-ttu-id="b3b81-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="b3b81-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="b3b81-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="b3b81-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="b3b81-428">Vues</span><span class="sxs-lookup"><span data-stu-id="b3b81-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="b3b81-429">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="b3b81-429">Tables and Views</span></span>  
  
|<span data-ttu-id="b3b81-430">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-430">ColumnName</span></span>|<span data-ttu-id="b3b81-431">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="b3b81-433">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-433">String</span></span>|  
|<span data-ttu-id="b3b81-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3b81-434">TABLE_OWNER</span></span>|<span data-ttu-id="b3b81-435">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-435">String</span></span>|  
|<span data-ttu-id="b3b81-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-436">TABLE_NAME</span></span>|<span data-ttu-id="b3b81-437">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-437">String</span></span>|  
|<span data-ttu-id="b3b81-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-438">TABLE_TYPE</span></span>|<span data-ttu-id="b3b81-439">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-439">String</span></span>|  
|<span data-ttu-id="b3b81-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-440">REMARKS</span></span>|<span data-ttu-id="b3b81-441">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="b3b81-442">Columns</span><span class="sxs-lookup"><span data-stu-id="b3b81-442">Columns</span></span>  
  
|<span data-ttu-id="b3b81-443">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-443">ColumnName</span></span>|<span data-ttu-id="b3b81-444">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="b3b81-446">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-446">String</span></span>|  
|<span data-ttu-id="b3b81-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3b81-447">TABLE_OWNER</span></span>|<span data-ttu-id="b3b81-448">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-448">String</span></span>|  
|<span data-ttu-id="b3b81-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-449">TABLE_NAME</span></span>|<span data-ttu-id="b3b81-450">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-450">String</span></span>|  
|<span data-ttu-id="b3b81-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-451">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-452">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-452">String</span></span>|  
|<span data-ttu-id="b3b81-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-453">DATA_TYPE</span></span>|<span data-ttu-id="b3b81-454">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-454">Int16</span></span>|  
|<span data-ttu-id="b3b81-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-455">TYPE_NAME</span></span>|<span data-ttu-id="b3b81-456">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-456">String</span></span>|  
|<span data-ttu-id="b3b81-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="b3b81-457">PRECISION</span></span>|<span data-ttu-id="b3b81-458">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-458">Int32</span></span>|  
|<span data-ttu-id="b3b81-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-459">LENGTH</span></span>|<span data-ttu-id="b3b81-460">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-460">Int32</span></span>|  
|<span data-ttu-id="b3b81-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="b3b81-461">SCALE</span></span>|<span data-ttu-id="b3b81-462">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-462">Int16</span></span>|  
|<span data-ttu-id="b3b81-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="b3b81-463">RADIX</span></span>|<span data-ttu-id="b3b81-464">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-464">Int16</span></span>|  
|<span data-ttu-id="b3b81-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-465">NULLABLE</span></span>|<span data-ttu-id="b3b81-466">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-466">Int16</span></span>|  
|<span data-ttu-id="b3b81-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-467">REMARKS</span></span>|<span data-ttu-id="b3b81-468">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-468">String</span></span>|  
|<span data-ttu-id="b3b81-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-470">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="b3b81-471">Procédures</span><span class="sxs-lookup"><span data-stu-id="b3b81-471">Procedures</span></span>  
  
|<span data-ttu-id="b3b81-472">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-472">ColumnName</span></span>|<span data-ttu-id="b3b81-473">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="b3b81-475">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-475">String</span></span>|  
|<span data-ttu-id="b3b81-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3b81-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="b3b81-477">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-477">String</span></span>|  
|<span data-ttu-id="b3b81-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="b3b81-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-479">String</span></span>|  
|<span data-ttu-id="b3b81-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="b3b81-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="b3b81-481">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-481">Int16</span></span>|  
|<span data-ttu-id="b3b81-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="b3b81-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="b3b81-483">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-483">Int16</span></span>|  
|<span data-ttu-id="b3b81-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="b3b81-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="b3b81-485">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-485">Int16</span></span>|  
|<span data-ttu-id="b3b81-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-486">REMARKS</span></span>|<span data-ttu-id="b3b81-487">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-487">String</span></span>|  
|<span data-ttu-id="b3b81-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="b3b81-489">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="b3b81-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="b3b81-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="b3b81-491">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-491">ColumnName</span></span>|<span data-ttu-id="b3b81-492">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="b3b81-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="b3b81-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-494">String</span></span>|  
|<span data-ttu-id="b3b81-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3b81-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="b3b81-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-496">String</span></span>|  
|<span data-ttu-id="b3b81-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="b3b81-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-498">String</span></span>|  
|<span data-ttu-id="b3b81-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-499">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-500">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-500">String</span></span>|  
|<span data-ttu-id="b3b81-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-501">COLUMN_TYPE</span></span>|<span data-ttu-id="b3b81-502">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-502">Int16</span></span>|  
|<span data-ttu-id="b3b81-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-503">DATA_TYPE</span></span>|<span data-ttu-id="b3b81-504">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-504">Int16</span></span>|  
|<span data-ttu-id="b3b81-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-505">TYPE_NAME</span></span>|<span data-ttu-id="b3b81-506">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-506">String</span></span>|  
|<span data-ttu-id="b3b81-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="b3b81-507">PRECISION</span></span>|<span data-ttu-id="b3b81-508">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-508">Int32</span></span>|  
|<span data-ttu-id="b3b81-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-509">LENGTH</span></span>|<span data-ttu-id="b3b81-510">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-510">Int32</span></span>|  
|<span data-ttu-id="b3b81-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="b3b81-511">SCALE</span></span>|<span data-ttu-id="b3b81-512">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-512">Int16</span></span>|  
|<span data-ttu-id="b3b81-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="b3b81-513">RADIX</span></span>|<span data-ttu-id="b3b81-514">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-514">Int16</span></span>|  
|<span data-ttu-id="b3b81-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-515">NULLABLE</span></span>|<span data-ttu-id="b3b81-516">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-516">Int16</span></span>|  
|<span data-ttu-id="b3b81-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-517">REMARKS</span></span>|<span data-ttu-id="b3b81-518">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-518">String</span></span>|  
|<span data-ttu-id="b3b81-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="b3b81-519">OVERLOAD</span></span>|<span data-ttu-id="b3b81-520">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-520">Int32</span></span>|  
|<span data-ttu-id="b3b81-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-522">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="b3b81-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="b3b81-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="b3b81-524">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3b81-524">ColumnName</span></span>|<span data-ttu-id="b3b81-525">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3b81-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="b3b81-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="b3b81-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="b3b81-527">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-527">String</span></span>|  
|<span data-ttu-id="b3b81-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="b3b81-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="b3b81-529">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-529">String</span></span>|  
|<span data-ttu-id="b3b81-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="b3b81-531">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-531">String</span></span>|  
|<span data-ttu-id="b3b81-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-532">COLUMN_NAME</span></span>|<span data-ttu-id="b3b81-533">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-533">String</span></span>|  
|<span data-ttu-id="b3b81-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-534">COLUMN_TYPE</span></span>|<span data-ttu-id="b3b81-535">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-535">Int16</span></span>|  
|<span data-ttu-id="b3b81-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-536">DATA_TYPE</span></span>|<span data-ttu-id="b3b81-537">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-537">Int16</span></span>|  
|<span data-ttu-id="b3b81-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="b3b81-538">TYPE_NAME</span></span>|<span data-ttu-id="b3b81-539">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-539">String</span></span>|  
|<span data-ttu-id="b3b81-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="b3b81-540">COLUMN_SIZE</span></span>|<span data-ttu-id="b3b81-541">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-541">Int32</span></span>|  
|<span data-ttu-id="b3b81-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="b3b81-543">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-543">Int32</span></span>|  
|<span data-ttu-id="b3b81-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="b3b81-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="b3b81-545">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-545">Int16</span></span>|  
|<span data-ttu-id="b3b81-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="b3b81-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="b3b81-547">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-547">Int16</span></span>|  
|<span data-ttu-id="b3b81-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-548">NULLABLE</span></span>|<span data-ttu-id="b3b81-549">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-549">Int16</span></span>|  
|<span data-ttu-id="b3b81-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="b3b81-550">REMARKS</span></span>|<span data-ttu-id="b3b81-551">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-551">String</span></span>|  
|<span data-ttu-id="b3b81-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="b3b81-552">COLUMN_DEF</span></span>|<span data-ttu-id="b3b81-553">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-553">String</span></span>|  
|<span data-ttu-id="b3b81-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3b81-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="b3b81-555">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-555">Int16</span></span>|  
|<span data-ttu-id="b3b81-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="b3b81-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="b3b81-557">Int16</span><span class="sxs-lookup"><span data-stu-id="b3b81-557">Int16</span></span>|  
|<span data-ttu-id="b3b81-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="b3b81-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="b3b81-559">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-559">Int32</span></span>|  
|<span data-ttu-id="b3b81-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="b3b81-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="b3b81-561">Int32</span><span class="sxs-lookup"><span data-stu-id="b3b81-561">Int32</span></span>|  
|<span data-ttu-id="b3b81-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="b3b81-562">IS_NULLABLE</span></span>|<span data-ttu-id="b3b81-563">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b3b81-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b3b81-564">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3b81-564">See Also</span></span>  
 [<span data-ttu-id="b3b81-565">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="b3b81-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
