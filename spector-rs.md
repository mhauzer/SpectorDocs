
# Spector - Requirement Specification

v0.2, 2026-09-16

- [Spector - Requirement Specification](#spector---requirement-specification)
  - [Changelog](#changelog)
  - [Preamble](#preamble)
    - [Requirement Specification Writing Rules](#requirement-specification-writing-rules)
    - [Label Grammar](#label-grammar)
  - [(REQ1) General Requirements](#req1-general-requirements)
  - [(REQ2) Requirement](#req2-requirement)
    - [(REQ2.2) Requirement Label](#req22-requirement-label)
    - [(REQ2.3) Requirement Description](#req23-requirement-description)
  - [(REQ3:S2) Requirements Graph](#req3s2-requirements-graph)
  - [(REQ4) Requirements Specification Document](#req4-requirements-specification-document)
    - [(REQ4.2) Displaying a Requirement Specification](#req42-displaying-a-requirement-specification)
    - [(REQ4.3) Creating a New Requirement Specification](#req43-creating-a-new-requirement-specification)
    - [(REQ4.4) Saving the Current Requirement Specification Document to a File](#req44-saving-the-current-requirement-specification-document-to-a-file)
    - [(REQ4.5) Opening an Existing Requirement Specification from a File](#req45-opening-an-existing-requirement-specification-from-a-file)
    - [(REQ4.6) Closing a Requirement Specification Document](#req46-closing-a-requirement-specification-document)
    - [(REQ4.7) Editing Requirement Specification](#req47-editing-requirement-specification)

## Changelog

Date | Author | Version | Description
---- | ------ | ------- | -----------
2026-09-16 | Michał Hauzer | v0.1 | Initial version
2026-09-16 | Michał Hauzer | v0.2 | Requirement Specification Document Unsaved Changes flag added
2026-09-17 | Michał Hauzer | v0.3 | Document creation date should be set on new document creation event, not the saving one 

## Preamble

[GitHub Markdown documentation](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

### Requirement Specification Writing Rules

1. Requirements must be labelled.
2. Requirements must be context free.
3. Requirements must be atomic.

Supplemental:

1. Avoid technical and implementation details as much as possible but no more than that.
2. In the end, you decide what is a requirement. If you require something, then it is a requirement.

### Label Grammar

- **(P1)** - requirement definition
- **(P1.1)** - sub requirement definition
- **(P1:S2)** - project stage reference
- **(>P1)** - requirement reference
- **(>?)** - unknown / generic requirement reference

## (REQ1) General Requirements

**(REQ1.1)** The app should have a GUI.

**(REQ1.2)** The Users should be able to access the app from their desktops.

**(REQ1.3)** The Users should be able to access the app regardless of their work context, whether they are employed by the company, working on client projects, freelancing, or managing private projects.

**(REQ1.4)** The app should be easy to use.

**(REQ1.5)** The app should be user-friendly and resilient to mistakes.

**(REQ1.6)** User should be able to recover from mistakes easily.

## (REQ2) Requirement

**(REQ2.1)** A requirement consists of:

- **(REQ2.1.1)** (>REQ2.2) a label
- **(REQ2.1.2)** (>REQ2.3) a description
- **(REQ2.1.3:S2)** a set of relationships to other requirements
- **(REQ2.1.4:S2)** a status

### (REQ2.2) Requirement Label

**(REQ2.2.1)** A Requirement Label uniquely identifies a requirement.

**(REQ2.2.2)** A Requirement Label is composed of:

- **(REQ2.2.2.1)** a prefix
- **(REQ2.2.2.2)** a numeric identifier

*MHA: Label examples: (REQ1), (S2)*  

**(REQ2.2.3)** Requirement label identifier values should be managed automatically.

**(REQ2.2.4)** Users should be able to change the requirement label prefix on demand.

### (REQ2.3) Requirement Description

**(REQ2.3.1)** A Requirement Description is a textual explanation of the requirement.

- **(REQ2.3.1.1)** Maximum length of the requirement description should be limited to a reasonable number of characters to ensure clarity and conciseness.

## (REQ3:S2) Requirements Graph

**(REQ3.1:S2)** Requirements can be connected to each other by relationships.

## (REQ4) Requirements Specification Document

**(REQ4.1)** A Requirement Specification Document contains the following elements:

- **(REQ4.1.1)** document header:
  - **(REQ4.1.1.1)** document title
  - **(REQ4.1.1.2)** document author
  - **(REQ4.1.1.3)** document version
  - **(REQ4.1.1.4)** document creation date
  - **(REQ4.1.1.5)** document last modification date
- **(REQ4.1.2:S2)** change log
- **(REQ4.1.3)** a list of requirements
- **(REQ4.1.4)** document unsaved changes status

**(REQ4.4)** By default, the application should open with no active document.

### (REQ4.2) Displaying a Requirement Specification

**(REQ4.2.1)** The application should display the contents of the opened requirement specification document:

- **(REQ4.2.1.1)** (>REQ4.1.1) document header
- **(REQ4.2.1.2)** (>REQ4.1.3) list of requirements
- **(REQ4.2.1.3)** (>REQ4.1.4) document unsaved changes status

**(REQ4.2.2)** Every (>REQ2) requirement should be displayed with its:

- **(REQ4.2.2.1)** (>REQ2.2) label
  - **(REQ4.2.2.1.1)** (>REQ2.2) labels should be displayed in parentheses.
  - **(REQ4.2.2.1.2)** (>REQ2.2) labels should be displayed with bold text.
- **(REQ4.2.2.2)** (>REQ2.3) description

**(REQ4.2.3)** The requirements should be displayed in the order defined by their labels.

### (REQ4.3) Creating a New Requirement Specification

**(REQ4.3.1)** The User should be able to create a new requirement specification document.

**(REQ4.3.2)** The file name should be specified by the User in the moment of the first (>REQ4.4) save operation.

**(REQ4.3.3)** A new document should be treated as having unsaved changes.

### (REQ4.4) Saving the Current Requirement Specification Document to a File

**(REQ4.4.1)** The User should be able to save the current requirement specification document.

**(REQ4.4.2)** The User should be able to specify the file name and location when saving the requirement specification document for the first time.

**(REQ4.4.3)** If the requirement specification document is saved for the first time, the application should automatically set the following header fields:

- **(REQ4.4.3.1)** document last modification date

**(REQ4.4.4)** If the requirement specification document is saved after (>REQ4.4.3) the first time, the application should automatically update the document last modification date header field.

**(REQ4.4.5)** After the document is saved, the unsaved changes status should be set to false.

### (REQ4.5) Opening an Existing Requirement Specification from a File

**(REQ4.5.1)** The User should be able to open an existing requirement specification document from a file.

### (REQ4.6) Closing a Requirement Specification Document

**(REQ4.6.1)** The User should be able to close the current requirement specification document.

**(REQ4.6.2)** If there are unsaved changes, the application should prompt the User to save the document before closing it.

### (REQ4.7) Editing Requirement Specification

**(REQ4.7.1)** The User should be able to modify the following parts of the header:
  
- **(REQ4.7.1.1)** document title
- **(REQ4.7.1.2)** document author
- **(REQ4.7.1.3)** document version

**(REQ4.7.2)** The User should be able to do the following operations on requirements within the requirement specification document:

- **(REQ4.7.2.1)** add requirements
  - **(REQ4.7.2.1.1)** new requirements are appended to the end of the requirement list
- **(REQ4.7.2.2)** edit requirements
- **(REQ4.7.2.3)** remove requirements
- **(REQ4.7.2.4:S2)** reorder requirements
