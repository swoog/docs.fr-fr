---
title: Collections de schémas ODBC
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43750007"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="ccebe-102">Collections de schémas ODBC</span><span class="sxs-lookup"><span data-stu-id="ccebe-102">ODBC Schema Collections</span></span>
<span data-ttu-id="ccebe-103">Cette section traite de la prise en charge des collections de schémas pour les pilotes ODBC Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="ccebe-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="ccebe-104">Pilote Microsoft SQL Server ODBC</span><span class="sxs-lookup"><span data-stu-id="ccebe-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="ccebe-105">Le pilote ODBC de Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="ccebe-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="ccebe-106">Tables</span><span class="sxs-lookup"><span data-stu-id="ccebe-106">Tables</span></span>  
  
-   <span data-ttu-id="ccebe-107">Index</span><span class="sxs-lookup"><span data-stu-id="ccebe-107">Indexes</span></span>  
  
-   <span data-ttu-id="ccebe-108">Columns</span><span class="sxs-lookup"><span data-stu-id="ccebe-108">Columns</span></span>  
  
-   <span data-ttu-id="ccebe-109">Procédures</span><span class="sxs-lookup"><span data-stu-id="ccebe-109">Procedures</span></span>  
  
-   <span data-ttu-id="ccebe-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ccebe-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="ccebe-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ccebe-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="ccebe-112">Vues</span><span class="sxs-lookup"><span data-stu-id="ccebe-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="ccebe-113">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="ccebe-113">Tables and Views</span></span>  
  
|<span data-ttu-id="ccebe-114">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-114">ColumnName</span></span>|<span data-ttu-id="ccebe-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="ccebe-116">TABLE_CAT</span></span>|<span data-ttu-id="ccebe-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-117">String</span></span>|  
|<span data-ttu-id="ccebe-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ccebe-118">TABLE_SCHEM</span></span>|<span data-ttu-id="ccebe-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-119">String</span></span>|  
|<span data-ttu-id="ccebe-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-120">TABLE_NAME</span></span>|<span data-ttu-id="ccebe-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-121">String</span></span>|  
|<span data-ttu-id="ccebe-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-122">TABLE_TYPE</span></span>|<span data-ttu-id="ccebe-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-123">String</span></span>|  
|<span data-ttu-id="ccebe-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-124">REMARKS</span></span>|<span data-ttu-id="ccebe-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="ccebe-126">Index</span><span class="sxs-lookup"><span data-stu-id="ccebe-126">Indexes</span></span>  
  
|<span data-ttu-id="ccebe-127">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-127">ColumnName</span></span>|<span data-ttu-id="ccebe-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="ccebe-129">TABLE_CAT</span></span>|<span data-ttu-id="ccebe-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-130">String</span></span>|  
|<span data-ttu-id="ccebe-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ccebe-131">TABLE_SCHEM</span></span>|<span data-ttu-id="ccebe-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-132">String</span></span>|  
|<span data-ttu-id="ccebe-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-133">TABLE_NAME</span></span>|<span data-ttu-id="ccebe-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-134">String</span></span>|  
|<span data-ttu-id="ccebe-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="ccebe-135">NON_UNIQUE</span></span>|<span data-ttu-id="ccebe-136">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-136">Int16</span></span>|  
|<span data-ttu-id="ccebe-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="ccebe-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-138">String</span></span>|  
|<span data-ttu-id="ccebe-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-139">INDEX_NAME</span></span>|<span data-ttu-id="ccebe-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-140">String</span></span>|  
|<span data-ttu-id="ccebe-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-141">TYPE</span></span>|<span data-ttu-id="ccebe-142">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-142">Int16</span></span>|  
|<span data-ttu-id="ccebe-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-144">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-144">Int16</span></span>|  
|<span data-ttu-id="ccebe-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-145">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-146">String</span></span>|  
|<span data-ttu-id="ccebe-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="ccebe-147">ASC_OR_DESC</span></span>|<span data-ttu-id="ccebe-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-148">String</span></span>|  
|<span data-ttu-id="ccebe-149">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="ccebe-149">CARDINATLITY</span></span>|<span data-ttu-id="ccebe-150">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-150">Int32</span></span>|  
|<span data-ttu-id="ccebe-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="ccebe-151">PAGES</span></span>|<span data-ttu-id="ccebe-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-152">Int32</span></span>|  
|<span data-ttu-id="ccebe-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-153">FILTER_CONDITION</span></span>|<span data-ttu-id="ccebe-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-154">String</span></span>|  
|<span data-ttu-id="ccebe-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ccebe-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="ccebe-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-156">String</span></span>|  
|<span data-ttu-id="ccebe-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="ccebe-158">Byte</span><span class="sxs-lookup"><span data-stu-id="ccebe-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="ccebe-159">Columns</span><span class="sxs-lookup"><span data-stu-id="ccebe-159">Columns</span></span>  
  
|<span data-ttu-id="ccebe-160">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-160">ColumnName</span></span>|<span data-ttu-id="ccebe-161">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="ccebe-162">TABLE_CAT</span></span>|<span data-ttu-id="ccebe-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-163">String</span></span>|  
|<span data-ttu-id="ccebe-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ccebe-164">TABLE_SCHEM</span></span>|<span data-ttu-id="ccebe-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-165">String</span></span>|  
|<span data-ttu-id="ccebe-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-166">TABLE_NAME</span></span>|<span data-ttu-id="ccebe-167">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-167">String</span></span>|  
|<span data-ttu-id="ccebe-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-168">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-169">String</span></span>|  
|<span data-ttu-id="ccebe-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-170">DATA_TYPE</span></span>|<span data-ttu-id="ccebe-171">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-171">Int16</span></span>|  
|<span data-ttu-id="ccebe-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-172">TYPE_NAME</span></span>|<span data-ttu-id="ccebe-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-173">String</span></span>|  
|<span data-ttu-id="ccebe-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="ccebe-174">COLUMN_SIZE</span></span>|<span data-ttu-id="ccebe-175">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-175">Int32</span></span>|  
|<span data-ttu-id="ccebe-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="ccebe-177">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-177">Int32</span></span>|  
|<span data-ttu-id="ccebe-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="ccebe-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="ccebe-179">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-179">Int16</span></span>|  
|<span data-ttu-id="ccebe-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="ccebe-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="ccebe-181">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-181">Int16</span></span>|  
|<span data-ttu-id="ccebe-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-182">NULLABLE</span></span>|<span data-ttu-id="ccebe-183">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-183">Int16</span></span>|  
|<span data-ttu-id="ccebe-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-184">REMARKS</span></span>|<span data-ttu-id="ccebe-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-185">String</span></span>|  
|<span data-ttu-id="ccebe-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="ccebe-186">COLUMN_DEF</span></span>|<span data-ttu-id="ccebe-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-187">String</span></span>|  
|<span data-ttu-id="ccebe-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="ccebe-189">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-189">Int16</span></span>|  
|<span data-ttu-id="ccebe-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="ccebe-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="ccebe-191">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-191">Int16</span></span>|  
|<span data-ttu-id="ccebe-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="ccebe-193">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-193">Int32</span></span>|  
|<span data-ttu-id="ccebe-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-195">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-195">Int32</span></span>|  
|<span data-ttu-id="ccebe-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-196">IS_NULLABLE</span></span>|<span data-ttu-id="ccebe-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-197">String</span></span>|  
|<span data-ttu-id="ccebe-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ccebe-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="ccebe-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-199">String</span></span>|  
|<span data-ttu-id="ccebe-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ccebe-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="ccebe-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-201">String</span></span>|  
|<span data-ttu-id="ccebe-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="ccebe-203">Byte</span><span class="sxs-lookup"><span data-stu-id="ccebe-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="ccebe-204">Procédures</span><span class="sxs-lookup"><span data-stu-id="ccebe-204">Procedures</span></span>  
  
|<span data-ttu-id="ccebe-205">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-205">ColumnName</span></span>|<span data-ttu-id="ccebe-206">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="ccebe-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="ccebe-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-208">String</span></span>|  
|<span data-ttu-id="ccebe-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ccebe-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="ccebe-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-210">String</span></span>|  
|<span data-ttu-id="ccebe-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="ccebe-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-212">String</span></span>|  
|<span data-ttu-id="ccebe-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ccebe-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="ccebe-214">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-214">Int32</span></span>|  
|<span data-ttu-id="ccebe-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ccebe-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="ccebe-216">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-216">Int32</span></span>|  
|<span data-ttu-id="ccebe-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="ccebe-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="ccebe-218">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-218">Int32</span></span>|  
|<span data-ttu-id="ccebe-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-219">REMARKS</span></span>|<span data-ttu-id="ccebe-220">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-220">String</span></span>|  
|<span data-ttu-id="ccebe-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="ccebe-222">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="ccebe-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ccebe-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="ccebe-224">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-224">ColumnName</span></span>|<span data-ttu-id="ccebe-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="ccebe-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="ccebe-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-227">String</span></span>|  
|<span data-ttu-id="ccebe-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ccebe-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="ccebe-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-229">String</span></span>|  
|<span data-ttu-id="ccebe-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="ccebe-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-231">String</span></span>|  
|<span data-ttu-id="ccebe-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-232">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-233">String</span></span>|  
|<span data-ttu-id="ccebe-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-234">COLUMN_TYPE</span></span>|<span data-ttu-id="ccebe-235">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-235">Int16</span></span>|  
|<span data-ttu-id="ccebe-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-236">DATA_TYPE</span></span>|<span data-ttu-id="ccebe-237">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-237">Int16</span></span>|  
|<span data-ttu-id="ccebe-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-238">TYPE_NAME</span></span>|<span data-ttu-id="ccebe-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-239">String</span></span>|  
|<span data-ttu-id="ccebe-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="ccebe-240">COLUMN_SIZE</span></span>|<span data-ttu-id="ccebe-241">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-241">Int32</span></span>|  
|<span data-ttu-id="ccebe-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="ccebe-243">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-243">Int32</span></span>|  
|<span data-ttu-id="ccebe-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="ccebe-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="ccebe-245">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-245">Int16</span></span>|  
|<span data-ttu-id="ccebe-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="ccebe-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="ccebe-247">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-247">Int16</span></span>|  
|<span data-ttu-id="ccebe-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-248">NULLABLE</span></span>|<span data-ttu-id="ccebe-249">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-249">Int16</span></span>|  
|<span data-ttu-id="ccebe-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-250">REMARKS</span></span>|<span data-ttu-id="ccebe-251">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-251">String</span></span>|  
|<span data-ttu-id="ccebe-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="ccebe-252">COLUMN_DEF</span></span>|<span data-ttu-id="ccebe-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-253">String</span></span>|  
|<span data-ttu-id="ccebe-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="ccebe-255">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-255">Int16</span></span>|  
|<span data-ttu-id="ccebe-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="ccebe-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="ccebe-257">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-257">Int16</span></span>|  
|<span data-ttu-id="ccebe-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="ccebe-259">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-259">Int32</span></span>|  
|<span data-ttu-id="ccebe-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-261">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-261">Int32</span></span>|  
|<span data-ttu-id="ccebe-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-262">IS_NULLABLE</span></span>|<span data-ttu-id="ccebe-263">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-263">String</span></span>|  
|<span data-ttu-id="ccebe-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ccebe-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="ccebe-265">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-265">String</span></span>|  
|<span data-ttu-id="ccebe-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ccebe-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="ccebe-267">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-267">String</span></span>|  
|<span data-ttu-id="ccebe-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="ccebe-269">Byte</span><span class="sxs-lookup"><span data-stu-id="ccebe-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="ccebe-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ccebe-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="ccebe-271">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-271">ColumnName</span></span>|<span data-ttu-id="ccebe-272">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="ccebe-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="ccebe-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-274">String</span></span>|  
|<span data-ttu-id="ccebe-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ccebe-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="ccebe-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-276">String</span></span>|  
|<span data-ttu-id="ccebe-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="ccebe-278">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-278">String</span></span>|  
|<span data-ttu-id="ccebe-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-279">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-280">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-280">String</span></span>|  
|<span data-ttu-id="ccebe-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-281">COLUMN_TYPE</span></span>|<span data-ttu-id="ccebe-282">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-282">Int16</span></span>|  
|<span data-ttu-id="ccebe-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-283">DATA_TYPE</span></span>|<span data-ttu-id="ccebe-284">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-284">Int16</span></span>|  
|<span data-ttu-id="ccebe-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-285">TYPE_NAME</span></span>|<span data-ttu-id="ccebe-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-286">String</span></span>|  
|<span data-ttu-id="ccebe-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="ccebe-287">COLUMN_SIZE</span></span>|<span data-ttu-id="ccebe-288">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-288">Int32</span></span>|  
|<span data-ttu-id="ccebe-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="ccebe-290">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-290">Int32</span></span>|  
|<span data-ttu-id="ccebe-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="ccebe-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="ccebe-292">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-292">Int16</span></span>|  
|<span data-ttu-id="ccebe-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="ccebe-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="ccebe-294">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-294">Int16</span></span>|  
|<span data-ttu-id="ccebe-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-295">NULLABLE</span></span>|<span data-ttu-id="ccebe-296">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-296">Int16</span></span>|  
|<span data-ttu-id="ccebe-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-297">REMARKS</span></span>|<span data-ttu-id="ccebe-298">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-298">String</span></span>|  
|<span data-ttu-id="ccebe-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="ccebe-299">COLUMN_DEF</span></span>|<span data-ttu-id="ccebe-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-300">String</span></span>|  
|<span data-ttu-id="ccebe-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="ccebe-302">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-302">Int16</span></span>|  
|<span data-ttu-id="ccebe-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="ccebe-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="ccebe-304">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-304">Int16</span></span>|  
|<span data-ttu-id="ccebe-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="ccebe-306">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-306">Int32</span></span>|  
|<span data-ttu-id="ccebe-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-308">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-308">Int32</span></span>|  
|<span data-ttu-id="ccebe-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-309">IS_NULLABLE</span></span>|<span data-ttu-id="ccebe-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-310">String</span></span>|  
|<span data-ttu-id="ccebe-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ccebe-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="ccebe-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-312">String</span></span>|  
|<span data-ttu-id="ccebe-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ccebe-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="ccebe-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-314">String</span></span>|  
|<span data-ttu-id="ccebe-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="ccebe-316">Byte</span><span class="sxs-lookup"><span data-stu-id="ccebe-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="ccebe-317">Pilote Microsoft Oracle ODBC</span><span class="sxs-lookup"><span data-stu-id="ccebe-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="ccebe-318">Le pilote Microsoft SQL Server Oracle ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="ccebe-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="ccebe-319">Tables</span><span class="sxs-lookup"><span data-stu-id="ccebe-319">Tables</span></span>  
  
-   <span data-ttu-id="ccebe-320">Columns</span><span class="sxs-lookup"><span data-stu-id="ccebe-320">Columns</span></span>  
  
-   <span data-ttu-id="ccebe-321">Procédures</span><span class="sxs-lookup"><span data-stu-id="ccebe-321">Procedures</span></span>  
  
-   <span data-ttu-id="ccebe-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ccebe-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="ccebe-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ccebe-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="ccebe-324">Vues</span><span class="sxs-lookup"><span data-stu-id="ccebe-324">Views</span></span>  
  
-   <span data-ttu-id="ccebe-325">Index</span><span class="sxs-lookup"><span data-stu-id="ccebe-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="ccebe-326">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="ccebe-326">Tables and Views</span></span>  
  
|<span data-ttu-id="ccebe-327">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-327">ColumnName</span></span>|<span data-ttu-id="ccebe-328">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="ccebe-330">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-330">String</span></span>|  
|<span data-ttu-id="ccebe-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccebe-331">TABLE_OWNER</span></span>|<span data-ttu-id="ccebe-332">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-332">String</span></span>|  
|<span data-ttu-id="ccebe-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-333">TABLE_NAME</span></span>|<span data-ttu-id="ccebe-334">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-334">String</span></span>|  
|<span data-ttu-id="ccebe-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-335">TABLE_TYPE</span></span>|<span data-ttu-id="ccebe-336">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-336">String</span></span>|  
|<span data-ttu-id="ccebe-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-337">REMARKS</span></span>|<span data-ttu-id="ccebe-338">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="ccebe-339">Columns</span><span class="sxs-lookup"><span data-stu-id="ccebe-339">Columns</span></span>  
  
|<span data-ttu-id="ccebe-340">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-340">ColumnName</span></span>|<span data-ttu-id="ccebe-341">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="ccebe-343">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-343">String</span></span>|  
|<span data-ttu-id="ccebe-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccebe-344">TABLE_OWNER</span></span>|<span data-ttu-id="ccebe-345">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-345">String</span></span>|  
|<span data-ttu-id="ccebe-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-346">TABLE_NAME</span></span>|<span data-ttu-id="ccebe-347">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-347">String</span></span>|  
|<span data-ttu-id="ccebe-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-348">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-349">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-349">String</span></span>|  
|<span data-ttu-id="ccebe-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-350">DATA_TYPE</span></span>|<span data-ttu-id="ccebe-351">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-351">Int16</span></span>|  
|<span data-ttu-id="ccebe-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-352">TYPE_NAME</span></span>|<span data-ttu-id="ccebe-353">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-353">String</span></span>|  
|<span data-ttu-id="ccebe-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="ccebe-354">PRECISION</span></span>|<span data-ttu-id="ccebe-355">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-355">Int32</span></span>|  
|<span data-ttu-id="ccebe-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-356">LENGTH</span></span>|<span data-ttu-id="ccebe-357">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-357">Int32</span></span>|  
|<span data-ttu-id="ccebe-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="ccebe-358">SCALE</span></span>|<span data-ttu-id="ccebe-359">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-359">Int16</span></span>|  
|<span data-ttu-id="ccebe-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="ccebe-360">RADIX</span></span>|<span data-ttu-id="ccebe-361">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-361">Int16</span></span>|  
|<span data-ttu-id="ccebe-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-362">NULLABLE</span></span>|<span data-ttu-id="ccebe-363">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-363">Int16</span></span>|  
|<span data-ttu-id="ccebe-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-364">REMARKS</span></span>|<span data-ttu-id="ccebe-365">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-365">String</span></span>|  
|<span data-ttu-id="ccebe-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-367">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="ccebe-368">Procédures</span><span class="sxs-lookup"><span data-stu-id="ccebe-368">Procedures</span></span>  
  
|<span data-ttu-id="ccebe-369">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-369">ColumnName</span></span>|<span data-ttu-id="ccebe-370">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="ccebe-372">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-372">String</span></span>|  
|<span data-ttu-id="ccebe-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccebe-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="ccebe-374">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-374">String</span></span>|  
|<span data-ttu-id="ccebe-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="ccebe-376">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-376">String</span></span>|  
|<span data-ttu-id="ccebe-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ccebe-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="ccebe-378">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-378">Int16</span></span>|  
|<span data-ttu-id="ccebe-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ccebe-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="ccebe-380">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-380">Int16</span></span>|  
|<span data-ttu-id="ccebe-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="ccebe-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="ccebe-382">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-382">Int16</span></span>|  
|<span data-ttu-id="ccebe-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-383">REMARKS</span></span>|<span data-ttu-id="ccebe-384">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-384">String</span></span>|  
|<span data-ttu-id="ccebe-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="ccebe-386">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="ccebe-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ccebe-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="ccebe-388">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-388">ColumnName</span></span>|<span data-ttu-id="ccebe-389">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="ccebe-391">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-391">String</span></span>|  
|<span data-ttu-id="ccebe-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccebe-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="ccebe-393">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-393">String</span></span>|  
|<span data-ttu-id="ccebe-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="ccebe-395">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-395">String</span></span>|  
|<span data-ttu-id="ccebe-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-396">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-397">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-397">String</span></span>|  
|<span data-ttu-id="ccebe-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-398">COLUMN_TYPE</span></span>|<span data-ttu-id="ccebe-399">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-399">Int16</span></span>|  
|<span data-ttu-id="ccebe-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-400">DATA_TYPE</span></span>|<span data-ttu-id="ccebe-401">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-401">Int16</span></span>|  
|<span data-ttu-id="ccebe-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-402">TYPE_NAME</span></span>|<span data-ttu-id="ccebe-403">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-403">String</span></span>|  
|<span data-ttu-id="ccebe-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="ccebe-404">PRECISION</span></span>|<span data-ttu-id="ccebe-405">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-405">Int32</span></span>|  
|<span data-ttu-id="ccebe-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-406">LENGTH</span></span>|<span data-ttu-id="ccebe-407">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-407">Int32</span></span>|  
|<span data-ttu-id="ccebe-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="ccebe-408">SCALE</span></span>|<span data-ttu-id="ccebe-409">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-409">Int16</span></span>|  
|<span data-ttu-id="ccebe-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="ccebe-410">RADIX</span></span>|<span data-ttu-id="ccebe-411">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-411">Int16</span></span>|  
|<span data-ttu-id="ccebe-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-412">NULLABLE</span></span>|<span data-ttu-id="ccebe-413">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-413">Int16</span></span>|  
|<span data-ttu-id="ccebe-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-414">REMARKS</span></span>|<span data-ttu-id="ccebe-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-415">String</span></span>|  
|<span data-ttu-id="ccebe-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="ccebe-416">OVERLOAD</span></span>|<span data-ttu-id="ccebe-417">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-417">Int32</span></span>|  
|<span data-ttu-id="ccebe-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-419">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="ccebe-420">Pilote Microsoft Jet ODBC</span><span class="sxs-lookup"><span data-stu-id="ccebe-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="ccebe-421">Le pilote Microsoft Jet ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="ccebe-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="ccebe-422">Tables</span><span class="sxs-lookup"><span data-stu-id="ccebe-422">Tables</span></span>  
  
-   <span data-ttu-id="ccebe-423">Index</span><span class="sxs-lookup"><span data-stu-id="ccebe-423">Indexes</span></span>  
  
-   <span data-ttu-id="ccebe-424">Columns</span><span class="sxs-lookup"><span data-stu-id="ccebe-424">Columns</span></span>  
  
-   <span data-ttu-id="ccebe-425">Procédures</span><span class="sxs-lookup"><span data-stu-id="ccebe-425">Procedures</span></span>  
  
-   <span data-ttu-id="ccebe-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ccebe-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="ccebe-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ccebe-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="ccebe-428">Vues</span><span class="sxs-lookup"><span data-stu-id="ccebe-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="ccebe-429">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="ccebe-429">Tables and Views</span></span>  
  
|<span data-ttu-id="ccebe-430">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-430">ColumnName</span></span>|<span data-ttu-id="ccebe-431">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="ccebe-433">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-433">String</span></span>|  
|<span data-ttu-id="ccebe-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccebe-434">TABLE_OWNER</span></span>|<span data-ttu-id="ccebe-435">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-435">String</span></span>|  
|<span data-ttu-id="ccebe-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-436">TABLE_NAME</span></span>|<span data-ttu-id="ccebe-437">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-437">String</span></span>|  
|<span data-ttu-id="ccebe-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-438">TABLE_TYPE</span></span>|<span data-ttu-id="ccebe-439">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-439">String</span></span>|  
|<span data-ttu-id="ccebe-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-440">REMARKS</span></span>|<span data-ttu-id="ccebe-441">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="ccebe-442">Columns</span><span class="sxs-lookup"><span data-stu-id="ccebe-442">Columns</span></span>  
  
|<span data-ttu-id="ccebe-443">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-443">ColumnName</span></span>|<span data-ttu-id="ccebe-444">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="ccebe-446">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-446">String</span></span>|  
|<span data-ttu-id="ccebe-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccebe-447">TABLE_OWNER</span></span>|<span data-ttu-id="ccebe-448">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-448">String</span></span>|  
|<span data-ttu-id="ccebe-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-449">TABLE_NAME</span></span>|<span data-ttu-id="ccebe-450">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-450">String</span></span>|  
|<span data-ttu-id="ccebe-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-451">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-452">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-452">String</span></span>|  
|<span data-ttu-id="ccebe-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-453">DATA_TYPE</span></span>|<span data-ttu-id="ccebe-454">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-454">Int16</span></span>|  
|<span data-ttu-id="ccebe-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-455">TYPE_NAME</span></span>|<span data-ttu-id="ccebe-456">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-456">String</span></span>|  
|<span data-ttu-id="ccebe-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="ccebe-457">PRECISION</span></span>|<span data-ttu-id="ccebe-458">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-458">Int32</span></span>|  
|<span data-ttu-id="ccebe-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-459">LENGTH</span></span>|<span data-ttu-id="ccebe-460">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-460">Int32</span></span>|  
|<span data-ttu-id="ccebe-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="ccebe-461">SCALE</span></span>|<span data-ttu-id="ccebe-462">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-462">Int16</span></span>|  
|<span data-ttu-id="ccebe-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="ccebe-463">RADIX</span></span>|<span data-ttu-id="ccebe-464">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-464">Int16</span></span>|  
|<span data-ttu-id="ccebe-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-465">NULLABLE</span></span>|<span data-ttu-id="ccebe-466">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-466">Int16</span></span>|  
|<span data-ttu-id="ccebe-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-467">REMARKS</span></span>|<span data-ttu-id="ccebe-468">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-468">String</span></span>|  
|<span data-ttu-id="ccebe-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-470">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="ccebe-471">Procédures</span><span class="sxs-lookup"><span data-stu-id="ccebe-471">Procedures</span></span>  
  
|<span data-ttu-id="ccebe-472">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-472">ColumnName</span></span>|<span data-ttu-id="ccebe-473">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="ccebe-475">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-475">String</span></span>|  
|<span data-ttu-id="ccebe-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccebe-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="ccebe-477">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-477">String</span></span>|  
|<span data-ttu-id="ccebe-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="ccebe-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-479">String</span></span>|  
|<span data-ttu-id="ccebe-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ccebe-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="ccebe-481">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-481">Int16</span></span>|  
|<span data-ttu-id="ccebe-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ccebe-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="ccebe-483">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-483">Int16</span></span>|  
|<span data-ttu-id="ccebe-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="ccebe-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="ccebe-485">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-485">Int16</span></span>|  
|<span data-ttu-id="ccebe-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-486">REMARKS</span></span>|<span data-ttu-id="ccebe-487">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-487">String</span></span>|  
|<span data-ttu-id="ccebe-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="ccebe-489">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="ccebe-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ccebe-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="ccebe-491">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-491">ColumnName</span></span>|<span data-ttu-id="ccebe-492">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ccebe-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="ccebe-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-494">String</span></span>|  
|<span data-ttu-id="ccebe-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccebe-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="ccebe-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-496">String</span></span>|  
|<span data-ttu-id="ccebe-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="ccebe-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-498">String</span></span>|  
|<span data-ttu-id="ccebe-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-499">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-500">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-500">String</span></span>|  
|<span data-ttu-id="ccebe-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-501">COLUMN_TYPE</span></span>|<span data-ttu-id="ccebe-502">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-502">Int16</span></span>|  
|<span data-ttu-id="ccebe-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-503">DATA_TYPE</span></span>|<span data-ttu-id="ccebe-504">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-504">Int16</span></span>|  
|<span data-ttu-id="ccebe-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-505">TYPE_NAME</span></span>|<span data-ttu-id="ccebe-506">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-506">String</span></span>|  
|<span data-ttu-id="ccebe-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="ccebe-507">PRECISION</span></span>|<span data-ttu-id="ccebe-508">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-508">Int32</span></span>|  
|<span data-ttu-id="ccebe-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-509">LENGTH</span></span>|<span data-ttu-id="ccebe-510">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-510">Int32</span></span>|  
|<span data-ttu-id="ccebe-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="ccebe-511">SCALE</span></span>|<span data-ttu-id="ccebe-512">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-512">Int16</span></span>|  
|<span data-ttu-id="ccebe-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="ccebe-513">RADIX</span></span>|<span data-ttu-id="ccebe-514">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-514">Int16</span></span>|  
|<span data-ttu-id="ccebe-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-515">NULLABLE</span></span>|<span data-ttu-id="ccebe-516">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-516">Int16</span></span>|  
|<span data-ttu-id="ccebe-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-517">REMARKS</span></span>|<span data-ttu-id="ccebe-518">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-518">String</span></span>|  
|<span data-ttu-id="ccebe-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="ccebe-519">OVERLOAD</span></span>|<span data-ttu-id="ccebe-520">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-520">Int32</span></span>|  
|<span data-ttu-id="ccebe-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-522">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="ccebe-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ccebe-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="ccebe-524">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ccebe-524">ColumnName</span></span>|<span data-ttu-id="ccebe-525">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccebe-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="ccebe-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="ccebe-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="ccebe-527">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-527">String</span></span>|  
|<span data-ttu-id="ccebe-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ccebe-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="ccebe-529">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-529">String</span></span>|  
|<span data-ttu-id="ccebe-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="ccebe-531">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-531">String</span></span>|  
|<span data-ttu-id="ccebe-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-532">COLUMN_NAME</span></span>|<span data-ttu-id="ccebe-533">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-533">String</span></span>|  
|<span data-ttu-id="ccebe-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-534">COLUMN_TYPE</span></span>|<span data-ttu-id="ccebe-535">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-535">Int16</span></span>|  
|<span data-ttu-id="ccebe-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-536">DATA_TYPE</span></span>|<span data-ttu-id="ccebe-537">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-537">Int16</span></span>|  
|<span data-ttu-id="ccebe-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ccebe-538">TYPE_NAME</span></span>|<span data-ttu-id="ccebe-539">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-539">String</span></span>|  
|<span data-ttu-id="ccebe-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="ccebe-540">COLUMN_SIZE</span></span>|<span data-ttu-id="ccebe-541">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-541">Int32</span></span>|  
|<span data-ttu-id="ccebe-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="ccebe-543">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-543">Int32</span></span>|  
|<span data-ttu-id="ccebe-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="ccebe-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="ccebe-545">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-545">Int16</span></span>|  
|<span data-ttu-id="ccebe-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="ccebe-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="ccebe-547">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-547">Int16</span></span>|  
|<span data-ttu-id="ccebe-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-548">NULLABLE</span></span>|<span data-ttu-id="ccebe-549">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-549">Int16</span></span>|  
|<span data-ttu-id="ccebe-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ccebe-550">REMARKS</span></span>|<span data-ttu-id="ccebe-551">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-551">String</span></span>|  
|<span data-ttu-id="ccebe-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="ccebe-552">COLUMN_DEF</span></span>|<span data-ttu-id="ccebe-553">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-553">String</span></span>|  
|<span data-ttu-id="ccebe-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ccebe-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="ccebe-555">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-555">Int16</span></span>|  
|<span data-ttu-id="ccebe-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="ccebe-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="ccebe-557">Int16</span><span class="sxs-lookup"><span data-stu-id="ccebe-557">Int16</span></span>|  
|<span data-ttu-id="ccebe-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ccebe-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="ccebe-559">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-559">Int32</span></span>|  
|<span data-ttu-id="ccebe-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ccebe-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="ccebe-561">Int32</span><span class="sxs-lookup"><span data-stu-id="ccebe-561">Int32</span></span>|  
|<span data-ttu-id="ccebe-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ccebe-562">IS_NULLABLE</span></span>|<span data-ttu-id="ccebe-563">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ccebe-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ccebe-564">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccebe-564">See Also</span></span>  
 [<span data-ttu-id="ccebe-565">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="ccebe-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
