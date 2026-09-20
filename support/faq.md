<seotitle>Top keywords and FAQ terms for your API, 50–60 chars</seotitle>

_> Frequently Asked Questions (FAQ) is a dedicated page to answer common questions that are related to using the API. FAQ entries may offer new content or offer a short answer along with a link to other areas of the documentation for obtaining further details. Incorporating FAQ entries should be a standard part of building a [knowledge base](https://apistyleguide.cisco.com/#apix-support/knowledge-base) during the developer support process._

# Frequently Asked Questions

_> The following TOC allows the reader to see each FAQ, linking to the specific entry. Each FAQ entry has a title that is wrapped in an H3 tag with a name that is used as the anchor for the link from the TOC. Following this structure makes for the best developer experience._

1. <a href="#finesse">What is Finesse?</a>
1. <a href="#developer">What can a developer do with Finesse?</a>
1. <a href="#documentation">Where can I find the Finesse documentation?</a>

<h3 name="finesse">1: What is Finesse?</h3>
Finesse is a next-generation agent desktop that is designed to provide the optimal user experience for agents. It is 100% browser based so agent client machines do not need any contact center-specific applications. [Finesse Overview](##finesse-overview) for more info.

<h3 name="developer">2. What can a developer do with Finesse?</h3>
Finesse is built for developers. It provides two types of APIs, the [Finesse REST API](##rest-api-dev-guide) and the [Finesse JavaScript Library API](##javascript-library).

There are three paths for customization:

1. Use the [Finesse REST APIs](https://developer.cisco.com/docs/finesse/#!cisco-finesse-rest-apis).
    * Integrate Finesse into your existing application (whether it is thick or thin)
    * Create a custom agent desktop.
1. Use the [Finesse JavaScript Library APIs](https://developer.cisco.com/docs/finesse/#!javascript-library) to create gadgets to be added to the Finesse out of the box agent desktop. These gadgets do not have to be Finesse or Cisco specific.
1. Create gadgets of existing applications to be added to the Finesse out of the box agent desktop without using any Finesse specific APIs.

<h3 name="documentation">3. Where can I find the Finesse documentation?</h3>
The documentation for the latest version of Finesse can be found on the [Finesse DevNet](https://developer.cisco.com/site/finesse) site under Docs -> Guides:

* The Finesse REST API: [Finesse Web Services Developer Guide](https://developer.cisco.com/docs/finesse/#!rest-api-dev-guide)
* The Finesse JavaScript Library API: [Finesse JavaScript Library API Reference](https://developer.cisco.com/docs/finesse/#!javascript-library)
* For Finesse versions 10.6(1) or higher, the Finesse JavaScript Library API documentation can be referenced directly from the Finesse server via URL:
`http(s)://<FQDN>:<port>/desktop/assets/js/doc/index.html`

Documentation for older versions of Finesse can be found in the [Previous Documentation](##previous-documentation-pdfs) section under Docs -> Downloads -> Previous Documentation (PDFs).
