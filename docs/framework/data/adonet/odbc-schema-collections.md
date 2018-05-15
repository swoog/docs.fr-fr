---
title: Collections de schémas ODBC
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: 36d0859b897bfcea33803c219ade14722ed90421
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="3048a-102">Collections de schémas ODBC</span><span class="sxs-lookup"><span data-stu-id="3048a-102">ODBC Schema Collections</span></span>
<span data-ttu-id="3048a-103">Cette section traite de la prise en charge des collections de schémas pour les pilotes ODBC Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="3048a-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="3048a-104">Pilote Microsoft SQL Server ODBC</span><span class="sxs-lookup"><span data-stu-id="3048a-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="3048a-105">Le pilote ODBC de Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="3048a-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="3048a-106">Tables</span><span class="sxs-lookup"><span data-stu-id="3048a-106">Tables</span></span>  
  
-   <span data-ttu-id="3048a-107">Index</span><span class="sxs-lookup"><span data-stu-id="3048a-107">Indexes</span></span>  
  
-   <span data-ttu-id="3048a-108">Columns</span><span class="sxs-lookup"><span data-stu-id="3048a-108">Columns</span></span>  
  
-   <span data-ttu-id="3048a-109">Procédures</span><span class="sxs-lookup"><span data-stu-id="3048a-109">Procedures</span></span>  
  
-   <span data-ttu-id="3048a-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="3048a-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="3048a-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="3048a-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="3048a-112">Vues</span><span class="sxs-lookup"><span data-stu-id="3048a-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="3048a-113">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="3048a-113">Tables and Views</span></span>  
  
|<span data-ttu-id="3048a-114">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-114">ColumnName</span></span>|<span data-ttu-id="3048a-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="3048a-116">TABLE_CAT</span></span>|<span data-ttu-id="3048a-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-117">String</span></span>|  
|<span data-ttu-id="3048a-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="3048a-118">TABLE_SCHEM</span></span>|<span data-ttu-id="3048a-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-119">String</span></span>|  
|<span data-ttu-id="3048a-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-120">TABLE_NAME</span></span>|<span data-ttu-id="3048a-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-121">String</span></span>|  
|<span data-ttu-id="3048a-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-122">TABLE_TYPE</span></span>|<span data-ttu-id="3048a-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-123">String</span></span>|  
|<span data-ttu-id="3048a-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-124">REMARKS</span></span>|<span data-ttu-id="3048a-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="3048a-126">Index</span><span class="sxs-lookup"><span data-stu-id="3048a-126">Indexes</span></span>  
  
|<span data-ttu-id="3048a-127">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-127">ColumnName</span></span>|<span data-ttu-id="3048a-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="3048a-129">TABLE_CAT</span></span>|<span data-ttu-id="3048a-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-130">String</span></span>|  
|<span data-ttu-id="3048a-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="3048a-131">TABLE_SCHEM</span></span>|<span data-ttu-id="3048a-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-132">String</span></span>|  
|<span data-ttu-id="3048a-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-133">TABLE_NAME</span></span>|<span data-ttu-id="3048a-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-134">String</span></span>|  
|<span data-ttu-id="3048a-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="3048a-135">NON_UNIQUE</span></span>|<span data-ttu-id="3048a-136">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-136">Int16</span></span>|  
|<span data-ttu-id="3048a-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="3048a-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-138">String</span></span>|  
|<span data-ttu-id="3048a-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-139">INDEX_NAME</span></span>|<span data-ttu-id="3048a-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-140">String</span></span>|  
|<span data-ttu-id="3048a-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-141">TYPE</span></span>|<span data-ttu-id="3048a-142">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-142">Int16</span></span>|  
|<span data-ttu-id="3048a-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-144">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-144">Int16</span></span>|  
|<span data-ttu-id="3048a-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-145">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-146">String</span></span>|  
|<span data-ttu-id="3048a-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="3048a-147">ASC_OR_DESC</span></span>|<span data-ttu-id="3048a-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-148">String</span></span>|  
|<span data-ttu-id="3048a-149">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="3048a-149">CARDINATLITY</span></span>|<span data-ttu-id="3048a-150">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-150">Int32</span></span>|  
|<span data-ttu-id="3048a-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="3048a-151">PAGES</span></span>|<span data-ttu-id="3048a-152">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-152">Int32</span></span>|  
|<span data-ttu-id="3048a-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="3048a-153">FILTER_CONDITION</span></span>|<span data-ttu-id="3048a-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-154">String</span></span>|  
|<span data-ttu-id="3048a-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3048a-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="3048a-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-156">String</span></span>|  
|<span data-ttu-id="3048a-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="3048a-158">Byte</span><span class="sxs-lookup"><span data-stu-id="3048a-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="3048a-159">Columns</span><span class="sxs-lookup"><span data-stu-id="3048a-159">Columns</span></span>  
  
|<span data-ttu-id="3048a-160">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-160">ColumnName</span></span>|<span data-ttu-id="3048a-161">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="3048a-162">TABLE_CAT</span></span>|<span data-ttu-id="3048a-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-163">String</span></span>|  
|<span data-ttu-id="3048a-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="3048a-164">TABLE_SCHEM</span></span>|<span data-ttu-id="3048a-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-165">String</span></span>|  
|<span data-ttu-id="3048a-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-166">TABLE_NAME</span></span>|<span data-ttu-id="3048a-167">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-167">String</span></span>|  
|<span data-ttu-id="3048a-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-168">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-169">String</span></span>|  
|<span data-ttu-id="3048a-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-170">DATA_TYPE</span></span>|<span data-ttu-id="3048a-171">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-171">Int16</span></span>|  
|<span data-ttu-id="3048a-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-172">TYPE_NAME</span></span>|<span data-ttu-id="3048a-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-173">String</span></span>|  
|<span data-ttu-id="3048a-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="3048a-174">COLUMN_SIZE</span></span>|<span data-ttu-id="3048a-175">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-175">Int32</span></span>|  
|<span data-ttu-id="3048a-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="3048a-177">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-177">Int32</span></span>|  
|<span data-ttu-id="3048a-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="3048a-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="3048a-179">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-179">Int16</span></span>|  
|<span data-ttu-id="3048a-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="3048a-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="3048a-181">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-181">Int16</span></span>|  
|<span data-ttu-id="3048a-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-182">NULLABLE</span></span>|<span data-ttu-id="3048a-183">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-183">Int16</span></span>|  
|<span data-ttu-id="3048a-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-184">REMARKS</span></span>|<span data-ttu-id="3048a-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-185">String</span></span>|  
|<span data-ttu-id="3048a-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="3048a-186">COLUMN_DEF</span></span>|<span data-ttu-id="3048a-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-187">String</span></span>|  
|<span data-ttu-id="3048a-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="3048a-189">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-189">Int16</span></span>|  
|<span data-ttu-id="3048a-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="3048a-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="3048a-191">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-191">Int16</span></span>|  
|<span data-ttu-id="3048a-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="3048a-193">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-193">Int32</span></span>|  
|<span data-ttu-id="3048a-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-195">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-195">Int32</span></span>|  
|<span data-ttu-id="3048a-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-196">IS_NULLABLE</span></span>|<span data-ttu-id="3048a-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-197">String</span></span>|  
|<span data-ttu-id="3048a-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3048a-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="3048a-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-199">String</span></span>|  
|<span data-ttu-id="3048a-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3048a-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="3048a-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-201">String</span></span>|  
|<span data-ttu-id="3048a-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="3048a-203">Byte</span><span class="sxs-lookup"><span data-stu-id="3048a-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="3048a-204">Procédures</span><span class="sxs-lookup"><span data-stu-id="3048a-204">Procedures</span></span>  
  
|<span data-ttu-id="3048a-205">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-205">ColumnName</span></span>|<span data-ttu-id="3048a-206">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="3048a-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="3048a-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-208">String</span></span>|  
|<span data-ttu-id="3048a-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="3048a-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="3048a-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-210">String</span></span>|  
|<span data-ttu-id="3048a-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="3048a-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-212">String</span></span>|  
|<span data-ttu-id="3048a-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="3048a-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="3048a-214">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-214">Int32</span></span>|  
|<span data-ttu-id="3048a-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="3048a-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="3048a-216">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-216">Int32</span></span>|  
|<span data-ttu-id="3048a-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="3048a-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="3048a-218">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-218">Int32</span></span>|  
|<span data-ttu-id="3048a-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-219">REMARKS</span></span>|<span data-ttu-id="3048a-220">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-220">String</span></span>|  
|<span data-ttu-id="3048a-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="3048a-222">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="3048a-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="3048a-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="3048a-224">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-224">ColumnName</span></span>|<span data-ttu-id="3048a-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="3048a-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="3048a-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-227">String</span></span>|  
|<span data-ttu-id="3048a-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="3048a-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="3048a-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-229">String</span></span>|  
|<span data-ttu-id="3048a-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="3048a-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-231">String</span></span>|  
|<span data-ttu-id="3048a-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-232">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-233">String</span></span>|  
|<span data-ttu-id="3048a-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-234">COLUMN_TYPE</span></span>|<span data-ttu-id="3048a-235">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-235">Int16</span></span>|  
|<span data-ttu-id="3048a-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-236">DATA_TYPE</span></span>|<span data-ttu-id="3048a-237">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-237">Int16</span></span>|  
|<span data-ttu-id="3048a-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-238">TYPE_NAME</span></span>|<span data-ttu-id="3048a-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-239">String</span></span>|  
|<span data-ttu-id="3048a-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="3048a-240">COLUMN_SIZE</span></span>|<span data-ttu-id="3048a-241">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-241">Int32</span></span>|  
|<span data-ttu-id="3048a-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="3048a-243">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-243">Int32</span></span>|  
|<span data-ttu-id="3048a-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="3048a-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="3048a-245">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-245">Int16</span></span>|  
|<span data-ttu-id="3048a-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="3048a-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="3048a-247">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-247">Int16</span></span>|  
|<span data-ttu-id="3048a-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-248">NULLABLE</span></span>|<span data-ttu-id="3048a-249">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-249">Int16</span></span>|  
|<span data-ttu-id="3048a-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-250">REMARKS</span></span>|<span data-ttu-id="3048a-251">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-251">String</span></span>|  
|<span data-ttu-id="3048a-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="3048a-252">COLUMN_DEF</span></span>|<span data-ttu-id="3048a-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-253">String</span></span>|  
|<span data-ttu-id="3048a-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="3048a-255">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-255">Int16</span></span>|  
|<span data-ttu-id="3048a-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="3048a-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="3048a-257">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-257">Int16</span></span>|  
|<span data-ttu-id="3048a-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="3048a-259">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-259">Int32</span></span>|  
|<span data-ttu-id="3048a-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-261">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-261">Int32</span></span>|  
|<span data-ttu-id="3048a-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-262">IS_NULLABLE</span></span>|<span data-ttu-id="3048a-263">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-263">String</span></span>|  
|<span data-ttu-id="3048a-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3048a-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="3048a-265">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-265">String</span></span>|  
|<span data-ttu-id="3048a-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3048a-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="3048a-267">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-267">String</span></span>|  
|<span data-ttu-id="3048a-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="3048a-269">Byte</span><span class="sxs-lookup"><span data-stu-id="3048a-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="3048a-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="3048a-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="3048a-271">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-271">ColumnName</span></span>|<span data-ttu-id="3048a-272">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="3048a-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="3048a-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-274">String</span></span>|  
|<span data-ttu-id="3048a-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="3048a-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="3048a-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-276">String</span></span>|  
|<span data-ttu-id="3048a-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="3048a-278">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-278">String</span></span>|  
|<span data-ttu-id="3048a-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-279">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-280">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-280">String</span></span>|  
|<span data-ttu-id="3048a-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-281">COLUMN_TYPE</span></span>|<span data-ttu-id="3048a-282">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-282">Int16</span></span>|  
|<span data-ttu-id="3048a-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-283">DATA_TYPE</span></span>|<span data-ttu-id="3048a-284">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-284">Int16</span></span>|  
|<span data-ttu-id="3048a-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-285">TYPE_NAME</span></span>|<span data-ttu-id="3048a-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-286">String</span></span>|  
|<span data-ttu-id="3048a-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="3048a-287">COLUMN_SIZE</span></span>|<span data-ttu-id="3048a-288">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-288">Int32</span></span>|  
|<span data-ttu-id="3048a-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="3048a-290">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-290">Int32</span></span>|  
|<span data-ttu-id="3048a-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="3048a-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="3048a-292">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-292">Int16</span></span>|  
|<span data-ttu-id="3048a-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="3048a-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="3048a-294">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-294">Int16</span></span>|  
|<span data-ttu-id="3048a-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-295">NULLABLE</span></span>|<span data-ttu-id="3048a-296">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-296">Int16</span></span>|  
|<span data-ttu-id="3048a-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-297">REMARKS</span></span>|<span data-ttu-id="3048a-298">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-298">String</span></span>|  
|<span data-ttu-id="3048a-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="3048a-299">COLUMN_DEF</span></span>|<span data-ttu-id="3048a-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-300">String</span></span>|  
|<span data-ttu-id="3048a-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="3048a-302">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-302">Int16</span></span>|  
|<span data-ttu-id="3048a-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="3048a-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="3048a-304">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-304">Int16</span></span>|  
|<span data-ttu-id="3048a-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="3048a-306">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-306">Int32</span></span>|  
|<span data-ttu-id="3048a-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-308">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-308">Int32</span></span>|  
|<span data-ttu-id="3048a-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-309">IS_NULLABLE</span></span>|<span data-ttu-id="3048a-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-310">String</span></span>|  
|<span data-ttu-id="3048a-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3048a-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="3048a-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-312">String</span></span>|  
|<span data-ttu-id="3048a-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3048a-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="3048a-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-314">String</span></span>|  
|<span data-ttu-id="3048a-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="3048a-316">Byte</span><span class="sxs-lookup"><span data-stu-id="3048a-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="3048a-317">Pilote Microsoft Oracle ODBC</span><span class="sxs-lookup"><span data-stu-id="3048a-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="3048a-318">Le pilote Microsoft SQL Server Oracle ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="3048a-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="3048a-319">Tables</span><span class="sxs-lookup"><span data-stu-id="3048a-319">Tables</span></span>  
  
-   <span data-ttu-id="3048a-320">Columns</span><span class="sxs-lookup"><span data-stu-id="3048a-320">Columns</span></span>  
  
-   <span data-ttu-id="3048a-321">Procédures</span><span class="sxs-lookup"><span data-stu-id="3048a-321">Procedures</span></span>  
  
-   <span data-ttu-id="3048a-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="3048a-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="3048a-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="3048a-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="3048a-324">Vues</span><span class="sxs-lookup"><span data-stu-id="3048a-324">Views</span></span>  
  
-   <span data-ttu-id="3048a-325">Index</span><span class="sxs-lookup"><span data-stu-id="3048a-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="3048a-326">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="3048a-326">Tables and Views</span></span>  
  
|<span data-ttu-id="3048a-327">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-327">ColumnName</span></span>|<span data-ttu-id="3048a-328">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="3048a-330">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-330">String</span></span>|  
|<span data-ttu-id="3048a-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="3048a-331">TABLE_OWNER</span></span>|<span data-ttu-id="3048a-332">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-332">String</span></span>|  
|<span data-ttu-id="3048a-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-333">TABLE_NAME</span></span>|<span data-ttu-id="3048a-334">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-334">String</span></span>|  
|<span data-ttu-id="3048a-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-335">TABLE_TYPE</span></span>|<span data-ttu-id="3048a-336">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-336">String</span></span>|  
|<span data-ttu-id="3048a-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-337">REMARKS</span></span>|<span data-ttu-id="3048a-338">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="3048a-339">Columns</span><span class="sxs-lookup"><span data-stu-id="3048a-339">Columns</span></span>  
  
|<span data-ttu-id="3048a-340">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-340">ColumnName</span></span>|<span data-ttu-id="3048a-341">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="3048a-343">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-343">String</span></span>|  
|<span data-ttu-id="3048a-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="3048a-344">TABLE_OWNER</span></span>|<span data-ttu-id="3048a-345">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-345">String</span></span>|  
|<span data-ttu-id="3048a-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-346">TABLE_NAME</span></span>|<span data-ttu-id="3048a-347">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-347">String</span></span>|  
|<span data-ttu-id="3048a-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-348">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-349">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-349">String</span></span>|  
|<span data-ttu-id="3048a-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-350">DATA_TYPE</span></span>|<span data-ttu-id="3048a-351">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-351">Int16</span></span>|  
|<span data-ttu-id="3048a-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-352">TYPE_NAME</span></span>|<span data-ttu-id="3048a-353">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-353">String</span></span>|  
|<span data-ttu-id="3048a-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="3048a-354">PRECISION</span></span>|<span data-ttu-id="3048a-355">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-355">Int32</span></span>|  
|<span data-ttu-id="3048a-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-356">LENGTH</span></span>|<span data-ttu-id="3048a-357">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-357">Int32</span></span>|  
|<span data-ttu-id="3048a-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="3048a-358">SCALE</span></span>|<span data-ttu-id="3048a-359">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-359">Int16</span></span>|  
|<span data-ttu-id="3048a-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="3048a-360">RADIX</span></span>|<span data-ttu-id="3048a-361">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-361">Int16</span></span>|  
|<span data-ttu-id="3048a-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-362">NULLABLE</span></span>|<span data-ttu-id="3048a-363">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-363">Int16</span></span>|  
|<span data-ttu-id="3048a-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-364">REMARKS</span></span>|<span data-ttu-id="3048a-365">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-365">String</span></span>|  
|<span data-ttu-id="3048a-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-367">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="3048a-368">Procédures</span><span class="sxs-lookup"><span data-stu-id="3048a-368">Procedures</span></span>  
  
|<span data-ttu-id="3048a-369">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-369">ColumnName</span></span>|<span data-ttu-id="3048a-370">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="3048a-372">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-372">String</span></span>|  
|<span data-ttu-id="3048a-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="3048a-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="3048a-374">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-374">String</span></span>|  
|<span data-ttu-id="3048a-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="3048a-376">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-376">String</span></span>|  
|<span data-ttu-id="3048a-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="3048a-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="3048a-378">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-378">Int16</span></span>|  
|<span data-ttu-id="3048a-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="3048a-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="3048a-380">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-380">Int16</span></span>|  
|<span data-ttu-id="3048a-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="3048a-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="3048a-382">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-382">Int16</span></span>|  
|<span data-ttu-id="3048a-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-383">REMARKS</span></span>|<span data-ttu-id="3048a-384">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-384">String</span></span>|  
|<span data-ttu-id="3048a-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="3048a-386">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="3048a-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="3048a-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="3048a-388">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-388">ColumnName</span></span>|<span data-ttu-id="3048a-389">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="3048a-391">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-391">String</span></span>|  
|<span data-ttu-id="3048a-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="3048a-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="3048a-393">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-393">String</span></span>|  
|<span data-ttu-id="3048a-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="3048a-395">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-395">String</span></span>|  
|<span data-ttu-id="3048a-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-396">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-397">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-397">String</span></span>|  
|<span data-ttu-id="3048a-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-398">COLUMN_TYPE</span></span>|<span data-ttu-id="3048a-399">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-399">Int16</span></span>|  
|<span data-ttu-id="3048a-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-400">DATA_TYPE</span></span>|<span data-ttu-id="3048a-401">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-401">Int16</span></span>|  
|<span data-ttu-id="3048a-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-402">TYPE_NAME</span></span>|<span data-ttu-id="3048a-403">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-403">String</span></span>|  
|<span data-ttu-id="3048a-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="3048a-404">PRECISION</span></span>|<span data-ttu-id="3048a-405">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-405">Int32</span></span>|  
|<span data-ttu-id="3048a-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-406">LENGTH</span></span>|<span data-ttu-id="3048a-407">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-407">Int32</span></span>|  
|<span data-ttu-id="3048a-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="3048a-408">SCALE</span></span>|<span data-ttu-id="3048a-409">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-409">Int16</span></span>|  
|<span data-ttu-id="3048a-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="3048a-410">RADIX</span></span>|<span data-ttu-id="3048a-411">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-411">Int16</span></span>|  
|<span data-ttu-id="3048a-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-412">NULLABLE</span></span>|<span data-ttu-id="3048a-413">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-413">Int16</span></span>|  
|<span data-ttu-id="3048a-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-414">REMARKS</span></span>|<span data-ttu-id="3048a-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-415">String</span></span>|  
|<span data-ttu-id="3048a-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="3048a-416">OVERLOAD</span></span>|<span data-ttu-id="3048a-417">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-417">Int32</span></span>|  
|<span data-ttu-id="3048a-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-419">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="3048a-420">Pilote Microsoft Jet ODBC</span><span class="sxs-lookup"><span data-stu-id="3048a-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="3048a-421">Le pilote Microsoft Jet ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="3048a-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="3048a-422">Tables</span><span class="sxs-lookup"><span data-stu-id="3048a-422">Tables</span></span>  
  
-   <span data-ttu-id="3048a-423">Index</span><span class="sxs-lookup"><span data-stu-id="3048a-423">Indexes</span></span>  
  
-   <span data-ttu-id="3048a-424">Columns</span><span class="sxs-lookup"><span data-stu-id="3048a-424">Columns</span></span>  
  
-   <span data-ttu-id="3048a-425">Procédures</span><span class="sxs-lookup"><span data-stu-id="3048a-425">Procedures</span></span>  
  
-   <span data-ttu-id="3048a-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="3048a-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="3048a-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="3048a-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="3048a-428">Vues</span><span class="sxs-lookup"><span data-stu-id="3048a-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="3048a-429">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="3048a-429">Tables and Views</span></span>  
  
|<span data-ttu-id="3048a-430">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-430">ColumnName</span></span>|<span data-ttu-id="3048a-431">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="3048a-433">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-433">String</span></span>|  
|<span data-ttu-id="3048a-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="3048a-434">TABLE_OWNER</span></span>|<span data-ttu-id="3048a-435">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-435">String</span></span>|  
|<span data-ttu-id="3048a-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-436">TABLE_NAME</span></span>|<span data-ttu-id="3048a-437">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-437">String</span></span>|  
|<span data-ttu-id="3048a-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-438">TABLE_TYPE</span></span>|<span data-ttu-id="3048a-439">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-439">String</span></span>|  
|<span data-ttu-id="3048a-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-440">REMARKS</span></span>|<span data-ttu-id="3048a-441">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="3048a-442">Columns</span><span class="sxs-lookup"><span data-stu-id="3048a-442">Columns</span></span>  
  
|<span data-ttu-id="3048a-443">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-443">ColumnName</span></span>|<span data-ttu-id="3048a-444">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="3048a-446">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-446">String</span></span>|  
|<span data-ttu-id="3048a-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="3048a-447">TABLE_OWNER</span></span>|<span data-ttu-id="3048a-448">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-448">String</span></span>|  
|<span data-ttu-id="3048a-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-449">TABLE_NAME</span></span>|<span data-ttu-id="3048a-450">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-450">String</span></span>|  
|<span data-ttu-id="3048a-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-451">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-452">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-452">String</span></span>|  
|<span data-ttu-id="3048a-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-453">DATA_TYPE</span></span>|<span data-ttu-id="3048a-454">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-454">Int16</span></span>|  
|<span data-ttu-id="3048a-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-455">TYPE_NAME</span></span>|<span data-ttu-id="3048a-456">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-456">String</span></span>|  
|<span data-ttu-id="3048a-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="3048a-457">PRECISION</span></span>|<span data-ttu-id="3048a-458">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-458">Int32</span></span>|  
|<span data-ttu-id="3048a-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-459">LENGTH</span></span>|<span data-ttu-id="3048a-460">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-460">Int32</span></span>|  
|<span data-ttu-id="3048a-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="3048a-461">SCALE</span></span>|<span data-ttu-id="3048a-462">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-462">Int16</span></span>|  
|<span data-ttu-id="3048a-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="3048a-463">RADIX</span></span>|<span data-ttu-id="3048a-464">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-464">Int16</span></span>|  
|<span data-ttu-id="3048a-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-465">NULLABLE</span></span>|<span data-ttu-id="3048a-466">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-466">Int16</span></span>|  
|<span data-ttu-id="3048a-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-467">REMARKS</span></span>|<span data-ttu-id="3048a-468">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-468">String</span></span>|  
|<span data-ttu-id="3048a-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-470">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="3048a-471">Procédures</span><span class="sxs-lookup"><span data-stu-id="3048a-471">Procedures</span></span>  
  
|<span data-ttu-id="3048a-472">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-472">ColumnName</span></span>|<span data-ttu-id="3048a-473">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="3048a-475">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-475">String</span></span>|  
|<span data-ttu-id="3048a-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="3048a-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="3048a-477">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-477">String</span></span>|  
|<span data-ttu-id="3048a-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="3048a-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-479">String</span></span>|  
|<span data-ttu-id="3048a-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="3048a-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="3048a-481">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-481">Int16</span></span>|  
|<span data-ttu-id="3048a-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="3048a-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="3048a-483">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-483">Int16</span></span>|  
|<span data-ttu-id="3048a-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="3048a-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="3048a-485">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-485">Int16</span></span>|  
|<span data-ttu-id="3048a-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-486">REMARKS</span></span>|<span data-ttu-id="3048a-487">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-487">String</span></span>|  
|<span data-ttu-id="3048a-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="3048a-489">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="3048a-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="3048a-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="3048a-491">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-491">ColumnName</span></span>|<span data-ttu-id="3048a-492">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="3048a-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="3048a-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-494">String</span></span>|  
|<span data-ttu-id="3048a-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="3048a-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="3048a-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-496">String</span></span>|  
|<span data-ttu-id="3048a-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="3048a-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-498">String</span></span>|  
|<span data-ttu-id="3048a-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-499">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-500">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-500">String</span></span>|  
|<span data-ttu-id="3048a-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-501">COLUMN_TYPE</span></span>|<span data-ttu-id="3048a-502">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-502">Int16</span></span>|  
|<span data-ttu-id="3048a-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-503">DATA_TYPE</span></span>|<span data-ttu-id="3048a-504">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-504">Int16</span></span>|  
|<span data-ttu-id="3048a-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-505">TYPE_NAME</span></span>|<span data-ttu-id="3048a-506">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-506">String</span></span>|  
|<span data-ttu-id="3048a-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="3048a-507">PRECISION</span></span>|<span data-ttu-id="3048a-508">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-508">Int32</span></span>|  
|<span data-ttu-id="3048a-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-509">LENGTH</span></span>|<span data-ttu-id="3048a-510">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-510">Int32</span></span>|  
|<span data-ttu-id="3048a-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="3048a-511">SCALE</span></span>|<span data-ttu-id="3048a-512">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-512">Int16</span></span>|  
|<span data-ttu-id="3048a-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="3048a-513">RADIX</span></span>|<span data-ttu-id="3048a-514">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-514">Int16</span></span>|  
|<span data-ttu-id="3048a-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-515">NULLABLE</span></span>|<span data-ttu-id="3048a-516">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-516">Int16</span></span>|  
|<span data-ttu-id="3048a-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-517">REMARKS</span></span>|<span data-ttu-id="3048a-518">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-518">String</span></span>|  
|<span data-ttu-id="3048a-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="3048a-519">OVERLOAD</span></span>|<span data-ttu-id="3048a-520">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-520">Int32</span></span>|  
|<span data-ttu-id="3048a-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-522">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="3048a-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="3048a-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="3048a-524">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3048a-524">ColumnName</span></span>|<span data-ttu-id="3048a-525">Type de données</span><span class="sxs-lookup"><span data-stu-id="3048a-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="3048a-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="3048a-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="3048a-527">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-527">String</span></span>|  
|<span data-ttu-id="3048a-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="3048a-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="3048a-529">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-529">String</span></span>|  
|<span data-ttu-id="3048a-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="3048a-531">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-531">String</span></span>|  
|<span data-ttu-id="3048a-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-532">COLUMN_NAME</span></span>|<span data-ttu-id="3048a-533">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-533">String</span></span>|  
|<span data-ttu-id="3048a-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-534">COLUMN_TYPE</span></span>|<span data-ttu-id="3048a-535">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-535">Int16</span></span>|  
|<span data-ttu-id="3048a-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-536">DATA_TYPE</span></span>|<span data-ttu-id="3048a-537">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-537">Int16</span></span>|  
|<span data-ttu-id="3048a-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="3048a-538">TYPE_NAME</span></span>|<span data-ttu-id="3048a-539">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-539">String</span></span>|  
|<span data-ttu-id="3048a-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="3048a-540">COLUMN_SIZE</span></span>|<span data-ttu-id="3048a-541">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-541">Int32</span></span>|  
|<span data-ttu-id="3048a-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="3048a-543">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-543">Int32</span></span>|  
|<span data-ttu-id="3048a-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="3048a-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="3048a-545">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-545">Int16</span></span>|  
|<span data-ttu-id="3048a-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="3048a-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="3048a-547">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-547">Int16</span></span>|  
|<span data-ttu-id="3048a-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-548">NULLABLE</span></span>|<span data-ttu-id="3048a-549">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-549">Int16</span></span>|  
|<span data-ttu-id="3048a-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="3048a-550">REMARKS</span></span>|<span data-ttu-id="3048a-551">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-551">String</span></span>|  
|<span data-ttu-id="3048a-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="3048a-552">COLUMN_DEF</span></span>|<span data-ttu-id="3048a-553">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-553">String</span></span>|  
|<span data-ttu-id="3048a-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3048a-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="3048a-555">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-555">Int16</span></span>|  
|<span data-ttu-id="3048a-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="3048a-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="3048a-557">Int16</span><span class="sxs-lookup"><span data-stu-id="3048a-557">Int16</span></span>|  
|<span data-ttu-id="3048a-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="3048a-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="3048a-559">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-559">Int32</span></span>|  
|<span data-ttu-id="3048a-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="3048a-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="3048a-561">Int32</span><span class="sxs-lookup"><span data-stu-id="3048a-561">Int32</span></span>|  
|<span data-ttu-id="3048a-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="3048a-562">IS_NULLABLE</span></span>|<span data-ttu-id="3048a-563">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3048a-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3048a-564">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3048a-564">See Also</span></span>  
 [<span data-ttu-id="3048a-565">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="3048a-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
