# ClinicalProfile FHIR Model

This repository carries the changes that need to be made to the FHIR R5 build to include the ClinicalProfile resource 
definition.  These changes were last applied April 15, 2019.

## Details
* [implementations](implementations)
  * [translations.xml](implementations/translations.xml) - adds a english translation for "Clinical Profile"
  
* [source](source)
  * [clinicalprofile](source/clinicalprofile) - clinical profile model, documentation and examples
  * [compartments.xml](source/compartments.xml) - Excel Spreadsheet that associates patient / provider / links with resource.  
  * [fhir.ini](source/fhir.ini) - basic information about Clinical Profile resource (maturity level, committee, etc.)
  * [modules-fragment.html](source/modules-fragment.html) - Include ClinicalProfile under home page Clinical Reasoning section
  * [newnavbar.html](source/newnavbar.html) - Adds header to FHIR navigation bars
  * [resourcelist.html](source/resourcelist.html) - Add clinical profile to Evidence-Based Medicine resources listing
  * [status-codes.xml](source/status-codes.xml) - map Clinical Profile status entries to status code semantics
  
* [tools/html/assets/imags/jhulogo.png](tools/html/assets/imags/jhulogo.png) - JHU logo for navigation bar
  
 
 # Building
 1) Clone a copy of the [latest FHIR R5 image](https://github.com/HL7/fhir)
 2) Copy `source/clinicalprofile` directory into fhir/source directory
 3) Copy `tools/html/assets/imags/jhulogo.png` into corresponding path in HL7 FHIR directory
 4) Copy `implementations/translations.xml` into corresponding path in HL7 FHIR directory
 3) Merge `compartments.xml`, `fhir.ini`, `modules-fragment.html`, `resourcelist.html` and `status-codes.xml` with directory content
 4) in the HL7/fhir root directory:
    * . publish.sh
 