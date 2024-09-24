# Common DITA Elements in Tasks

<main>

## `<shortdesc>` vs. `<context>`: 

 `<shortdesc>` follows the `<title>` element and gives a brief overview of the topic, covering perhaps benefits, importance, purpose. `<context>` appears in `<taskbody>` and provides background knowledge for the user to complete the task, including where and when to do the task.

## `<prereq>`: 

 information that users might need prior to getting started. Should precede the steps. Could contain needed materials or other pre-requisite states. Should write these are imperative statements. Will show up with the heading "before you begin"

## `<steps>`: 

 demarcates the start of a section of steps. The default is that the steps will be numbered within them.

## `<steps-unordered>`: 

 like the `<steps>` element but more for a parallel format of tasks. These will give a bullet list of steps.

## `<step>`: 

 contained in `<steps>` and contains `<cmd>`. All `<cmd>` should be imperative statements. Write one set of steps per significant action, combine small steps. Omit steps that are obvious from the interface. Buttons, menus, fields that users interact with are marked `<uicontrol>`.
•	Can take the attribute “importance" and set to “optional/required"

## `<substeps>` `<substep>`:
- Keep substeps to one sub-level if possible. Anything more and you should rethink whether your task is not really two or more tasks. DITA will allow up to two levels of substeps.

## `<image>`:
- can insert an image stored in your local folders `<image href="image.png"/>`

## `<stepsection>`: 

 used between steps, if you want to insert a comment or a brief introduction to the steps that follow. Must be in the `<step>` element.

## `<stepresult>`: 

 when you want to say what happens when a step is finished (e.g., “the log in menu appears"). Do this sparingly and only when needed for clarification.

## `<stepxmp>`: 

 for illustrating how a step can be carried out

## `<menucascade>`: 

 produces the effect of File >` New >` Template where each of the clickable options are `<uicontrol>` elements.
•	(e.g., `<menucascade>` `<unicontrol>`File > `</uicontrol>` `<uicontrol>`New > `</uicontrol>` `<uicontrol>`Template`</uicontrol>`

## `<choice>`: 

 contained in `<choices>` and is used for giving a list of bullet items

## `<choicetable>`: 

 for more complex choosing. Contains `<chhead>` (choptionhd, chdeschd) and `<chrow>` (choption, chdesc).

## `<info>`: 

 additional information following a step. Could be used for notes that warn or caution. Can take the attribute of “importance" and set to “high/low"

## `<hazardstatement>`: 

 can take a “type" attribute and used for including warnings, cautions, and other notices as needed for a step. Inserted in the `<step>` element and before the `<cmd>` element. Includes necessary child elements of `<typeofhazard>` and `<howtoavoid>`. Can be substituted more simply for a `<note>` element.

## `<result>`: 

 at the conclusion of the `<steps>` you can include a comment about the overall result of completing the task. Unlike `<stepresult>` the `<result>` element covers the entire task. Wrap content in a `<p>` element.

## `<example>`: 

 like the `<result>` element in that it speaks to the whole task and provides an example of how the task might have been carried out. Wrap content in a `<p>` element.

## `<object>`: 

 used for inserting media objects (e.g., sound and video) into a topic. Can be used in a variety of places, including concepts. Commonly appears in `<stepxmp>` and `<example>`.
•	Takes the attribute “data" for selecting a video file (e.g., `<object data="video.mp4">` `</object>`

## `<postreq>`: 

 anything that the user must do when finished with the task

## `<xref href="somefile.dita">`:
- links to a local dita file:
  - **Example**: `<xref href="http:www.whitehouse.gov" format="html" scope="external">`:
- allows a link to an outside html resource. If the resource is in the local file, then change scope to `<"internal">`
  - **Caution**: Do not use `<xref>` for related topics.

</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Abel&family=Exo+2:ital,wght@0,100..900;1,100..900&family=Roboto+Mono:ital,wght@0,100..700;1,100..700&display=swap');
  body {
    background: white;
    color: black;
    font-family: "Abel";
  }
  h1,h2,h3,h4,code { font-family: "Exo 2" }
  
  h1 {
    text-align: center;
  }
  h2, h2 > code {
    font-size: 1.5rem;
    margin: 3.5rem 0 1rem 0;
  }
  code {
    background: inherit;
    color: red;
    font-size: 1rem;
    font-weight: 600;
  }
  
  main {
    max-width: 700px;
    margin: auto;
    font-size: 1rem;
  }
</style>

