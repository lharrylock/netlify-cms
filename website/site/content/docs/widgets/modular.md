---
label: "Modular"
target: "modular"
type: "widget"
---

### Modular

The modular widget allows you to a list of different content types item in the UI which saves as a list of widget values. Map a user-provided string with a comma delimiter into a list. You can choose any widget as a child of a modular widget.

* **Name:** `modular`
* **UI:** `types` is a list of widgets (modular content types) available to the user from the modular content dropdown. User selects a (or multipe) widgets to add to a list. Child widget is added to the list, with controls for adding, deleting, and re-ordering the child widgets;
* **Data type:** list of widget values
* **Options:**

  * `types`: a one-dimensional list of multiple widget types to be included in the dropdown

* **Example**

  ```yaml
  - label: "Modular Content Chunks"
        label_singular: "Modular Content Chunk"
        name: "chunk"
        widget: "modular"
        types:
          - {label: "Text", name: "text", widget: "text"}
          - {label: "String", name: "string", widget: "string"}
          - {label: "Boolean", name: "boolean", widget: "boolean"}
          - {label: "Number", name: "number", widget: "number"}
          - {label: "Markdown", name: "markdown", widget: "markdown"}
          - {label: "Datetime", name: "datetime", widget: "datetime"}
          - {label: "Date", name: "date", widget: "date"}
          - {label: "Image", name: "image", widget: "image"}
          - {label: "File", name: "file", widget: "file"}
          - {label: "Select", name: "select", widget: "select", options: ["a", "b", "c"]}
          - {label: "Select (Object)", name: "select_object", widget: "select", options: [{ label: "Chicago", value: "ORD" },{ label: "Paris", value: "CDG" },{ label: "Tokyo", value: "HND" }]}
          - {label: "Related Post", name: "relation", widget: "relationKitchenSinkPost", collection: "posts", searchFields: ["title", "body"], valueField: "title"}
          - label: "Profile"
            name: "profile"
            widget: "object"
            fields:
              - {label: "Public", name: "public", widget: "boolean", default: true}
              - {label: "Name", name: "name", widget: "string"}
              - label: "Birthdate"
                name: "birthdate"
                widget: "date"
          - label: "List"
            name: "list"
            widget: "list"
            fields:
              - {label: "String", name: "string", widget: "string"}
              - {label: "Boolean", name: "boolean", widget: "boolean"}
              - {label: "Text", name: "text", widget: "text"}
  ```