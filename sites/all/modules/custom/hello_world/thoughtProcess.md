# My Approach

* Identify dependencies
* Identify requirements
* Formulate implementation plan
* Execute plan

## Identify Dependencies

This project requires Drupal to be in a known state in order to be able to full fill the dependencies. My first 
requirement will be to put Drupal into the defined state by creating the required content, and setting the default
theme. I'll also be declaring the content_type_vocab_hello_world as a dependency so that when the hello_world module
is enabled the content types and vocabularies will be created.

## Identify Requirements

* Set Drupal to known state
  * Create vocab terms
    * About Us
    * Misc
    * News
  * Create 4 Hello World Article Nodes
    * 2 tagged with the "News" Vocab term
    * 1 tagged with "About Us"
    * 1 tagged with "Misc"
  * Set Bartik as the default theme
* Hello World Block
  * Title should be "Hello World!" in Bold typeface
  * linked titles to all nodes that are of Hello World Article type, and are tagged with "Enabled" terms from the 
  Sections vocabulary
  * Should only appear only on Node Overview pages of Hello World Articles
* Theme customization to Hello World Articles
  * the phrase "Content starts here!" should appear in an italic typeface as the first line of content on the page.
  
## Formulate Plan

* Satisfy all dependencies during module installation viz hook_install
* Create a custom block, satisfying the dependencies listed above
* Implement theme customization 