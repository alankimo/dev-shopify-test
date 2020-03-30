# Development Test for Shopify
## Tools
- Shopify Theme Kit - [Shopify Theme Kit] (https://shopify.github.io/themekit/)
- Liquid Reference - [Liquid reference · Shopify Help Center] (https://help.shopify.com/en/themes/liquid)
- Shopify Theme Layouts Reference - [Theme layouts · Shopify Help Center] (https://help.shopify.com/en/themes/development/layouts)
- Shopify Theme Templates - [Theme templates · Shopify Help Center] (https://help.shopify.com/en/themes/development/templates)
- Shopify Theme Sections - [Theme sections · Shopify Help Center] (https://help.shopify.com/en/themes/development/sections)

## Tips
- It is recommended to read the documentation in detail to understand the Shopify template design structure.
- Theme Kit documentation is provided, the tool to work locally that connects to the Shopify server.
- To achieve this test pay special attention to: ** Shopify Theme Templates, Shopify Theme Sections, Liquid Reference. **


## Brief
A blank template is provided, without design of any kind, but with the basic structure detailed in [Building themes · Shopify Help Center] (https://help.shopify.com/en/themes/development). ** The test consists of the development of the visual part and some technical characteristics of the home page of a Shopify store ** considering only the following:

- Static Section - Header
- Dynamic Section - Collection List
- Dynamic Section - Featured Product
- Static Section - Footer

> Important: only the main page will be made, the other sections must remain without design. Consider that the Header and Footer retain their style throughout the site.

The visual reference is provided but the adjustment of spaces for the different resolutions is free to interpretation, we do not look for perfect pixel, we look for responsive design.

The mockup to follow for desktop and mobile version is as follows:
[Sketch Cloud - Mockup] (https://sketch.cloud/s/D84ne)

You find the assets in this same repository.

## Requirements
The following list of requirements must be met for us to consider the test completed and ready for review:

### Github and development environment
You need to fork this repository so that you have it in your GitHub account and there work on branches each requirement.

The environment you are going to work in is development.

### Source
The entire site must have https://fonts.google.com/specimen/Raleway

### Icons
All icons must be used in SVG snippet format.


### Static Section - Header

- The hamburger must work in the same way on desktop as on mobile, in addition to displaying the menu selected in the * Section Header * configuration.
- The logo must be able to be changed with the * image-picker * available in the * Section Header * configuration.


### Dynamic Section - Collection list
- The title, as well as the collections, must respond to the dynamic blocks of the section.
- By using the template grid, if there are 5 blocks, the distribution should be: First Row of 3 columns | Second row of 2 columns.


### Dynamic Section - Featured product
- The title, as well as the complete product, must respond to the control of the section.
- Display the featured image `{{product.featured_image}}` of the product.
- Create a component that allows to increase / decrease the amount of the input taking into account the following:
- It should not be possible to write 0
- The maximum number to write must be the amount of inventory available `{{variant.inventory_quantity}}`
- In case of reaching the maximum, throw a message with an alert.
- By clicking on * Add to cart * you must add it to the cart and take me to the / cart page.


### Static Section - Footer
- Follow design guidelines for the model.


### Delivery
Once you have the settings ready, you should fully deploy your version of the theme to the development environment.

`theme deploy --env = dev`

After this, make a pull request to our original repository on the `test` branch.

Finally send an email to confirm that you finished the test and it is ready for review.