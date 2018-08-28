swagger: "2.0"
x-collection-name: Fire Browse
x-complete: 1
info:
  title: Fire Browse Beta API
  description: a-simple-and-elegant-way-to-explore-cancer-data
  version: 1.1.35 (2016-09-27 10:12:23 6a47e74011281b2aa
host: firebrowse.org
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Analyses/mRNASeq/Quartiles:
    get:
      summary: Returns RNASeq expression quartiles, e.g. suitable for drawing a boxplot.
      description: For a given gene compute quartiles and extrema, suitable e.g. for
        drawing a boxplot (Tukey 1977).  Results may be filtered by cohort, sample
        type, patient barcode  or characterization protocol, and are returned sorted
        by cohort.  Note that samples for which no expression value was recorded (e.g.
        the melanoma sample TCGA-GN-262) are removed prior to calculation.
      operationId: getAnalysesMrnaseqQuartiles
      x-api-path-slug: analysesmrnaseqquartiles-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: Exclude
        description: Comma separated list of TCGA participants, identified by barcodes
          such as TCGA-GF-A4EO, denoting samples to exclude from computation
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Enter a single gene name
      - in: query
        name: protocol
        description: Narrow search to one or more sample characterization protocols
          from the scrollable list
      - in: query
        name: sample_type
        description: For which type of sample(s) should quartiles be computed?
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - MRNASeq
      - Quartiles