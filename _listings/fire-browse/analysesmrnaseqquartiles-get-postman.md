{
  "info": {
    "name": "Fire Browse Beta API Returns RNASeq expression quartiles, e.g. suitable for drawing a boxplot.",
    "_postman_id": "37c693f9-e70d-48be-9f52-0237589f62fe",
    "description": "For a given gene compute quartiles and extrema, suitable e.g. for drawing a boxplot (Tukey 1977).  Results may be filtered by cohort, sample type, patient barcode  or characterization protocol, and are returned sorted by cohort.  Note that samples for which no expression value was recorded (e.g. the melanoma sample TCGA-GN-262) are removed prior to calculation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "d37b60f6-86ba-4d75-bee1-624adf3442bc",
          "name": "getAnalysesCopynumberGenesAll",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/All?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 all_data_by_genes.txt output data. This data is a gene-level table of copy number values for all samples. The returned copy number values are in units (copy number - 2) so that no amplification or deletion is 0, genes with amplifications have positive values, and genes with deletions are negative values. The data are converted from marker level to gene level using the extreme method: a gene is assigned the greatest amplification or the least deletion value among the markers it covers. Results may be filtered by cohort, gene, or barcode, but at least one gene or barcode must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6efe1837-68b6-4f44-8215-d01464dadc36"
            }
          ]
        },
        {
          "id": "ed23cb2d-cbb5-4ad6-8128-5f9470ac785f",
          "name": "getAnalysesCopynumberGenesAmplified",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/Amplified?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&q=%7B%7D&sort_by=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 amp_genes.conf_99.txt output data.  At least 1 gene or cohort must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "babe265b-871e-49ed-a95f-290b365ffcc3"
            }
          ]
        },
        {
          "id": "8f22f11b-bef7-4b68-8480-274ff53b7f38",
          "name": "getAnalysesCopynumberGenesDeleted",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/Deleted?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&q=%7B%7D&sort_by=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 del_genes.conf_99.txt output data.  At least 1 gene or cohort must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "670f13c2-9c15-4639-ba09-368c4711f1c9"
            }
          ]
        },
        {
          "id": "85e72e77-26c3-4638-b443-37d9ef635529",
          "name": "getAnalysesCopynumberGenesFocal",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/Focal?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 focal_data_by_genes.txt output data. This output is similar to the all_data_by_genes.txt output, but using only focal events with lengths greater than the  focal length cutoff. This data is a gene-level table of copy number values for all samples. The returned copy number values are in units (copy number - 2) so that no amplification or deletion is 0, genes with amplifications have positive values, and genes with deletions are negative values. The data are converted from marker level to gene level using the extreme method: a gene is assigned the greatest amplification or the least deletion value among the markers it covers. Results may be filtered by cohort, gene, and/or barcode, but at least one gene or barcode must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "51f35fea-6c64-4a2c-a5bb-375bd552006d"
            }
          ]
        },
        {
          "id": "0a0a3898-1f72-4e1e-9639-823ad612e65f",
          "name": "getAnalysesCopynumberGenesThresholded",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/Thresholded?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 all_thresholded_by_genes.txt output data. A gene-level table of discrete amplification and deletion indicators for all samples. A table value of 0 means no amplification or deletion above the threshold. Amplifications are positive numbers: 1 means amplification above the amplification threshold; 2 means amplifications larger to the arm level amplifications observed for the sample. Deletions are represented by negative table values: -1 represents deletion beyond the threshold; -2 means deletions greater than the minimum arm-level deletion observed for the sample. Results maybe filtered by cohort, gene or barcode, but at least one gene or barcode must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b5b18cae-533c-4bf2-b2e6-33e00e77f483"
            }
          ]
        },
        {
          "id": "06ec4b0b-b4b6-4f79-9b2a-a34dbe35de72",
          "name": "getAnalysesFeaturetable",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/FeatureTable?cohort=%7B%7D&column=%7B%7D&date=%7B%7D&format=%7B%7D&page=%7B%7D&page_size=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns part or all of the so-called feature table; which aggregates the most important findings across ALL pipelines in the GDAC Firehose analysis workflow into a single table for simple access.  One feature table is created per disease cohort.  Results may be filtered by date or cohort, but at least 1 cohort must be specified here. For more details please visit the online documentation.  Please note that the service is still undergoing experimental evaluation and does not return JSON format."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fda2e1e0-cc72-4808-8f8a-cb87526170bf"
            }
          ]
        },
        {
          "id": "561a12dc-c354-4482-a0a6-b6d3bd98bdcb",
          "name": "getAnalysesMutationMaf",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/Mutation/MAF?cohort=%7B%7D&column=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D&tool=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns columns from the MAF generated by MutSig. Results may be filtered by gene, cohort, tool, or barcode, but at least one gene OR barcode OR cohort must be given.  By default a subset consisting of the most commonly used columns will be returned, but that can be modified with the column parameter. Specifying 'all' in this parameter is a convenient way to return every column of the respective MAF, and has precedence over any any other column selection expression.  The complete list of column names that may be specified is given here.  For more information on the mutation data, and how it is processed by Firehose, please consult the pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8b8ba518-2e70-4c73-8083-73ba8254acf1"
            }
          ]
        },
        {
          "id": "81b79da6-a485-4d1c-a79b-213d033c5412",
          "name": "getAnalysesMutationSmg",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/Mutation/SMG?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&q=%7B%7D&rank=%7B%7D&sort_by=%7B%7D&tool=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides a list of significantly mutated genes, as scored by MutSig.  It may be filtered by cohort, rank, gene, tool and/or Q-value threshold, but at least one cohort or gene must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dc24d8cf-4936-49ca-aa3d-88b2db1fcfb2"
            }
          ]
        },
        {
          "id": "1776dbd0-a9ca-4f8f-8cde-3e4796133c50",
          "name": "getAnalysesReports",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/Reports?cohort=%7B%7D&date=%7B%7D&format=%7B%7D&name=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns URLs to the analysis result reports for runs of the Broad Institute GDAC Firehose analysis pipeline. At least one year of run reports are maintained in the database, but the reports from the latest run will be returned by default. The set of Nozzle reports returned may be filtered by disease cohort, report type and report name."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6930e1bc-3bec-4db7-a828-d19c6a042194"
            }
          ]
        },
        {
          "id": "14f0b18d-fe21-48fd-9471-c3af1495f076",
          "name": "getAnalysesMrnaseqQuartiles",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/mRNASeq/Quartiles?cohort=%7B%7D&Exclude=%7B%7D&format=%7B%7D&gene=%7B%7D&protocol=%7B%7D&sample_type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "For a given gene compute quartiles and extrema, suitable e.g. for drawing a boxplot (Tukey 1977).  Results may be filtered by cohort, sample type, patient barcode  or characterization protocol, and are returned sorted by cohort.  Note that samples for which no expression value was recorded (e.g. the melanoma sample TCGA-GN-262) are removed prior to calculation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1a75310e-fdb8-4b8f-85c6-a7af09368c13"
            }
          ]
        }
      ]
    }
  ]
}