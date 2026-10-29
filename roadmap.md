# Spector Roadmap

- [Spector Roadmap](#spector-roadmap)
  - [v0.1](#v01)
  - [v0.2](#v02)
  - [v0.3](#v03)
  - [v0.4](#v04)
  - [v0.5](#v05)
  - [v0.6](#v06)
  - [v0.7](#v07)
  - [Backlog](#backlog)

## v0.1

- [x] Simple lists of requirements
- [x] Adding, editing and removing requirements

## v0.2

- [x] Tool bar
- Labels:
  - [x] Define the internal structure for labels:
    - prefix: str
    - number: int
  - [x] setting prefixes for labels
  - [x] updating prefixes for labels
  - [ ] autonumeration
  - [ ] autonumeration option
  - [ ] Relabelling
- [ ] User Options
- [ ] Drag & drop
- [ ] Undo

## v0.3

- [ ] Requirement trees
- [ ] Persistent view state (collapsed and expanded nodes in the tree view)
- [ ] References
- [ ] Exporting requirements to Markdown files.
- [ ] Import requirements from Markdown files.
- [ ] [Markdown files editor](https://doc.qt.io/qtforpython-6/examples/example_webenginewidgets_markdowneditor.html)
- [ ] New help menu item: Requirement Specification Writing Rules
- [ ] New help menu item: Label Grammar

## v0.4

- [ ] Search
- [ ] Select all, add to the selection, remove from the selection
- [ ] Dictionaries
- [ ] Automatic linking to a dictionary item
- [ ] Automatic linking to a referred requirement
- [ ] User Support:
  - [ ] Displaying Requirement Specification Writing Rules as a tool property window
  - [ ] Displaying Label Grammar as a tool property window
  - [ ] Contextual Help
  - [ ] Manual
  - [ ] FAQ
  - [ ] Reporting Bugs

## v0.5

- [ ] Project stage as a part of a requirement
- [ ] Sections
- [ ] Non-requirement items:
  - [ ] Paragraphs
  - [ ] Comments
- [ ] Requirement Graphs [Graph Databases for Python](https://www.reddit.com/r/Python/comments/x376eg/do_you_use_python_in_combination_with_some_graph/?rdt=62766), ([2](https://www.reddit.com/r/KnowledgeGraph/comments/1qcpqj3/i_built_a_graph_database_in_python/)), CogDb
- [ ] Detecting Redundant Requirements
- [ ] Detecting Requirement Conflicts
- [ ] Specification Review against the 3 rules
- [ ] Marking requirements as implemented

## v0.6

- [ ] Requirements Library
- [ ] Domain areas
- [ ] Composing specifications from the requirements library.
- [ ] Specification Templates
- [ ] Requirement mapping across multiple specifications

## v0.7

- [ ] Planning
- [ ] Versioning, automatic changelog
- [ ] Comparing specifications

## Backlog

- UI:
  - Toolbar customization
  - Shortcuts customization
  - Requirement details as a part of the view, rather than a dialog form
  - Smart Markdown file editor
- Business Features:
  - Converting Documentation to Specification
  - Converting Code to Specification
  - Generating Tests
  - Generating Code
