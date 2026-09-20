# Welcome to the OpenAPI Template Project

This project provides a guide to show Cisco teams how to start an API documentation project. Included is a structured outline with common documentation elements, tips for constructing robust documentation, and a checklist of steps to help focus the documentation effort. Along the way, links are offered to the API Style Guide to help expand details and recommendations for design and documentation efforts.

The [Cisco API Style Guide](https://developer.cisco.com/api-guidelines/) offers insights into defining your API product, along with recommendations that encourage a more consistent API design across Cisco. Links to various pages within the style guide are provided across the template to help you apply the style guide recommendations.

Use the ["Managing Your API Documentation Process"](https://developer.cisco.com/api-guidelines/#!apix-documentation/managing-your-api-documentation-process) and ["Documenting REST APIs"](https://developer.cisco.com/api-guidelines/#!rest-documentation), along with this project, to help you get started with your documentation efforts. 

[PubHub Local Preview](https://developer.cisco.com/docs/pubhub-user-guide/using-the-pubhub-local-preview-tool-for-windows/) allows authors to view their PubHub projects locally before committing to the repo, providing a seamless preview experience on [Windows](https://developer.cisco.com/docs/pubhub-user-guide/using-the-pubhub-local-preview-tool-for-windows/) and [Mac](https://wwwin-github.cisco.com/DevNet/PubHub-Preview) computers.

# Project Structure

The template project provides an overall structure along with placeholder elements to help jumpstart a new documentation effort. The template has five sections that are managed by the `config.json`:

| Section         | Description                                          |
|-----------------|------------------------------------------------------|
| __Overview__    | Provides an overview of the API to the reader, details on obtaining an API token, a quick start guide to help developers get started, and some examples to demonstrate common uses for the API. |
| __Guides__      | Various guides to help developers accomplish common tasks using the API. |
| __API Reference__ | Provides reference documentation for each API operation, along with an example using the OpenAPI Specification and/or SDKs. |
| __Developer Resources__   | Additional resources for developers, information about developer sandboxes, Learning Labs, Code Exchange, and more. |
| __Community and Support__   | Contains support information specifically for developers, including links to glossary, FAQ, blogs, and community. |

Each section contains its own folder/file structure for managing the individual pages in each section, as detailed below. 

## Overview Section

Provides an overview of the API to the reader, details on obtaining an API token, a quick start guide to help developers get started, and some examples to demonstrate common uses for the API.

See ["Overview Section"](https://developer.cisco.com/api-guidelines/#apix-documentation/overview-section) for more details on what should go into this section. 


| Page                            | Description    |
|---------------------------------|----------------|
| Introduction                    | Provides an overview of the API |
| Authentication                  | Describes the steps necessary to obtain an API token |
| Getting Started                 | Offers a step-by-step guide on how to get started quickly with the API |
| API Changelog                   | Provides a list of improvements with each new release |


## Guides Section

Various guides to help developers accomplish common tasks using the API. Guides should be task-oriented, helping developers find examples on how to use the API to accomplish different kinds of outcomes.

This project offers some examples, but it is important to remove any that aren't applicable and add new ones to meet the needs of your developers. See ["Guides Section"](https://developer.cisco.com/api-guidelines/#apix-documentation/guides-section) for more details on what should go into this section. 


| Page                            | Description    |
|---------------------------------|----------------|
| guide-template.md                       | An example how-to page with resources to inspire creating your own API-specific guides for common developer tasks. Multiple TOC entries point to this file as a method of showing how the guides will render in the table of contents. |
| Request and Response Formats    | A template for APIs that have to deal with multiple request/response formats |
| Versioning                    | Details how the API handles API versioning and sunsetting of an API version. |
| Content Compression and Encoding         | Additional information about the supported content types and encodings supported. |
| Browsing, Sorting, Filtering, and Rate Limits | A template for APIs that provide listing/browsing, sorting, filtering, and pagination support. |
| Errors and Troubleshooting | A template for helping developers understand and troubleshoot error messages. |


## API Reference Section

Provides reference documentation for each API operation, along with an example using the OpenAPI Specification. Each version of the API should be listed in descending order by version number.

See the API style guide's ["Reference Section"](https://developer.cisco.com/api-guidelines/#!apix-documentation/api-reference-section) for more details on what should go into this section. 

You can change PubHub to render the OpenAPI Specification (OAS) either interactively or non-interactively, depending on your sandbox environment. Interactive docs mean a developer can make a GET request in the docs and get back a real response. To learn more about setting up interactive docs, check out the [Guide for Interactive REST API Docs on DevNet](https://testing-developer.cisco.com/docs/interactive-api-doc-example/).

| Page                            | config.json setting    | Description  |
|---------------------------------|-------------------|-------------------|
|  OASv3           | "type": "oas3" | OpenAPI Specification v3 for interactive API reference |
|  OASv2           | "type": "oas" | OpenAPI Specification v2 for interactive API reference |
|  OAS (remote file example stored on GitHub.com)           | "content": "Enter URL of OAS" | Display the OpenAPI Specification from GitHub.com  |
| Download OpenAPI Document           | "type": "file" | Let developers download the raw OpenAPI Specification  |

>**Note**: If your API prefers the use of SDKs rather than direct API integration, you may wish to adjust this title in the `config.json` to "SDK Reference". 

## Developer Resources Section

Additional resources for developers, information about developer sandboxes, Learning Labs, Code Exchange, and more.

Many of the entries will link to other resources directly but may require adjusting the link to direct the reader to the landing page for your API product.

There are some pages that will require customization to fit the specific needs of your API product. 

Refer to the ["Supporting API" section of the API Style Guide](https://developer.cisco.com/api-guidelines/#!apix-support) for more information on the purpose of this section and resources that should be included. 


| Page                            | Description    |
|---------------------------------|----------------|
| Sandbox                         | Page that details the available developer sandboxes for this API |
| Learning Labs                   | External link to the DevNet Learning Labs for this API |
| Postman Collection              | Additional examples and Postman collections for common developer tasks |
| Code Exchange                   | External link to the Code Exchange where code examples and scripts may be found |



## Community and Support Section

Contains support information specifically for developers, including links to glossary, FAQ, blogs, and community.

Many of the entries will link to other resources directly but may require adjusting the link to direct the reader to the landing page for your API product.

There are some pages that will require customization to fit the specific needs of your API product. 

Refer to the ["Supporting API" section of the API Style Guide](https://developer.cisco.com/api-guidelines/#!apix-support/knowledge-base) for more information on the purpose of this section and resources that should be included. 


| Page                            | Description    |
|---------------------------------|----------------|
| Developer Support                         | Page that provides details on how to obtain support for your API product. |
| Glossary                        | Common terms and definitions important for understanding and using the API. |
| FAQ                             | Frequently Asked Questions (FAQ) about the API and the capabilities it offers. |
| Blogs                           | External link to the blog for your product |
| Community                       | External link to the Cisco Community discussion forums |
| Videos                       | External link to the developer-related videos for your API |


# Strategy for Version-Based Documentation

## Versioning API Documents in PubHub

API deployments will often have 1-3 active API versions available at any time: the current version, a previous version that is still supported for customers, and an upcoming version available as a preview release.

For these kinds of API deployments, use one PubHub project per major version of the API. This is more like the industry standard where each API version has its own set of dedicated documentation. Non-breaking changes, such as adding a new API operation, require updating the documentation set for that version of the API. Introducing a breaking change to the API requires:

1. Incrementing the API version number, e.g. v1->v2.
2. Producing a new documentation set to manage all related documentation.

A drop-down menu, included above the TOC on each PubHub project, allows developers to move between versions as necessary by redirecting the browser to the corresponding documentation. As an example, [Meraki offers drop-down selection](https://developer.cisco.com/meraki/api/#!introduction) between v0 and v1. Since v1 is the default and will be for some time, the default hash-bang URLs are all for the v1 API. 

For more information on versioning the API document, see [Versioning documentation](https://developer.cisco.com/docs/pubhub-user-guide/#!versioning).

# Tips for Site Management

## General Content Management

Modify or replace the example `.md` files with the content and explanations for your project. If you need to add more then one file to this repo we suggest using a version control system locally. 

## Table of Contents Auto-Expansion Config

For some documentation, it is better to start with some or all sections of the table of contents collapsed, sometimes referred to as compressed. Doing so allows readers to see the top-level headings first. This helps to answer questions such as, "Does this API offer an SDK?" without first being forced to collapse headings.

Add an "expand": 0 setting in the config.json file for each top-level TOC entry.

For example, to ensure the Overview section is expanded but the remaining sections are compressed:

```
{
  "items": [
      {
        "title": "Overview",
        "type": "config",
        "content": "overview/config.json"
      },
      {
        "title": "Guides",
        "type": "config",
        "content": "guides/config.json",
		"config": {
		  "expand": 0
		}
      },
      {
        "title": "API Reference",
        "type": "config",
        "content": "reference/config.json",
		"config": {
		  "expand": 0
		}
      },
      {
        "title": "Developer Resources",
        "type": "config",
        "content": "resources/config.json",
		"config": {
		  "expand": 0
		}
      }
    ]
}
```

## Using config.json

The `config.json` file contains the overall organization of the project, and you can add or remove references to files there. This file sets up the navigation for your documentation. [Click here to learn how to set up the config.json](https://developer.cisco.com/docs/pubhub-user-guide/#!table-of-contents/adding-items-to-the-navigation-pane-using-config-json-file).

## Using sub configs

To make it easier to group and manage the pages within each section, a dedicated subconfig JSON file can be added. 

For more information on using sub config files, see the [Creating Sub Config Files](https://developer.cisco.com/docs/pubhub-user-guide/#!table-of-contents/creating-sub-config-files) section of the PubHub User's Guide.

# Guidance for Creating API Documentation

## Inline Documentation Guidance

Throughout this sample project, there are notes such as the following:

_> Provide an overview of what Postman Collections are and how they can be used._

These comments guides you in the documentation process.

Additionally, there are resources offered at the bottom with links to the Cisco API Style Guide recommendations and existing Cisco API product documentation with more examples. Use these to guide your documentation efforts.

## OpenAPI Specification

We do prefer teams use the OpenAPI specification to document the reference information for their API project. The examples provided in this template project use the OpenAPI 3.0 specification, although an OAS v2.0 description example is also included for teams that depend upon older toolsets that are not OAS v3 compatible.

If your team is unfamiliar with OAS, refer to the [OpenAPI specification v3.0](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.3.md) for further study and reference.

The ["OpenAPI Support with PubHub"](https://developer.cisco.com/api-guidelines/#!rest-documentation/openapi-support-with-pubhub) section offers links to better understanding how OAS is supported within PubHub.

For more information and recommendations on offering an OpenAPI specification as part of your machine-readable API description offerings, see ["Machine-readable API definitions"](https://developer.cisco.com/api-guidelines/#apix-documentation/machine-readable-api-definition). 

## Using the Interactive API Explorer

DevNet Interactive API Documentation is a tool developed by the DevNet team to provide a better API learning experience. It parses the  OpenAPI specification JSON/YAML file and provides an interactive UI. This is similar to the interactive API reference documentation generated by swagger-ui, but tailored to the needs of Cisco APIs.

By setting the "type" value in a config.json to "oas3" or "oas", the API Explorer will be used to render an OpenAPI Specification (OAS) file. For more information on how to enable the API Explorer, see [PubHub API Explorer docs](https://developer.cisco.com/docs/interactive-api-doc-example/).

In addition to the API Explorer, it is recommended that the OpenAPI specification file should be offered as a raw download, for developers that wish to use it with code generators and other purposes directly. 

## SEO Best Practices

These template files have one tag you need to edit to produce the best search engine results for your documentation. For more information, see the [PubHub Best Practices documentation](https://developer.cisco.com/docs/pubhub-2-0-best-practices/#!optimizing-for-search-engines).

## Publishing: Use PubHub to Preview Changes and Submit for Final Review

Once you have your project where you want it, and have `committed` your files in source control, go to your project on PubHub. There you can preview your document and also submit it to go live on DevNet.

# Publishing Checklist

All new docs on DevNet will need to be reviewed by a DevNet Developer Advocate and DevNet Tech Writer prior to being published on DevNet. They will review and provide feedback over the course of 1 week.

A read-only version of the checklist used by DevNet Developer Advocates during the review is available as a [checklist](https://cisco.sharepoint.com/:x:/s/DevNetContent/EeNmGf86si9Pghjco4w0nzIBpUmuNVqiElMuTCB7UoUH5Q?e=lRNCwR&amp;CID=EE767ECA-4CF2-4244-BFB1-084782C5A0CB&amp;wdLOR=c45F377D2-8A16-4F2E-A8F0-43A9303AB7D2). Feel free to duplicate the sheet for your team and use it to track the documentation progress. You may also use it as a way to ensure that everything has been completed prior to the review. 

The DevNet team will create a GitHub issue for each item that needs to be fixed in the docs.  Only the items under the Required sections in the checklist need to be marked as Approved prior to being published.



