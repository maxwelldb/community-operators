# Writing Operator CSV descriptions for the OpenShift catalogue and OperatorHub.io

In OpenShift version 4.1 and greater, the Operator Lifecycle Manager (OLM) component reads an Operator’s ClusterServiceVersion (CSV) to determine how to run the Operator and present it to users. A CSV file comprises metadata that accompanies an Operator’s container image.

In a CSV's `spec` block, the `description` field contains a Markdown passage that describes the Operator's features, uses, and limitations. This content appears as the Operator's documentation in the OpenShift web console and the [OperatorHub.io](https://operatorhub.io/) catalogue.

A description has five sections:

| Section   |  Definition |
|-----------|---------------|
| Introduction | A brief paragraph or two about the application that the Operator creates. Unlike the other sections in a description, this one does not need a heading. |
| Core capabilities | An unordered list of the application's core capabilities and use cases. |
| Operator features | An unordered list of actions that the Operator is able to automate related to the application. |
| Before you start | _Optional_: An ordered list of steps that the end-user must take before deploying the application in their project. Only include steps that, if skipped, cause application creation to fail. Typically, these steps might be setting mandatory roles, bindings, or secrets. If your Operator requires a secret, include a cleanly formatted example that includes instructions to generate necessary information.|
| Troubleshooting | _Optional_: An ordered list of quick, common troubleshooting steps or an unordered list of links to the Troubleshooting section of external documentation. |

Other than the introduction, all of the sections have headings. All headings must be in sentence case and at level H3.

For more information about creating CSVs, see [Building a Cluster Service Version (CSV) for the Operator Framework](https://github.com/operator-framework/operator-lifecycle-manager/blob/master/Documentation/design/building-your-csv.md).

## Examples

TBD: Add 2-3 exemplary examples here.

## Language guidelines

When in doubt, defer to the IBM Style Guide.

## Operator description template

```markdown

<!-- Operator description template -->

<!-- Introduction -->
Insert text here.

### Core capabilities

* Insert an ordered list of items here.

### Operator features

* Insert an ordered list of items here. 

### Before you start

* If necessary, insert an ordered list of items here.

### Troubleshooting
<!-- If listing troubleshooting steps in the description-->

1. Insert an ordered list of steps here.

<!-- If linking to documentation -->

* Insert an unordered list of links here.


```
