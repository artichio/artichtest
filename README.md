# ArtichTest

[Getting started](#getting-started) | [Exercises](#exercises) | [Developer tools](#developer-tools)

This is a fork of Shopify's Dawn theme and will be used for our technical test.

---

## Getting started

### Prerequisites

To get started with this test, you need the following:

- A Shopify Partner account
- A development store (if you don't have one, create one for free [here](https://www.shopify.com/partners))
- [Shopify CLI](https://shopify.dev/docs/api/shopify-cli/theme) installed on your machine
- [Theme Check](https://github.com/shopify/theme-check) (Optional, but recommended for linting and best practices)

### Setup

1. Fork and clone this repository to your local machine.
   
2. Navigate to the project directory in your terminal and run the Shopify CLI command to serve the theme locally:

    ```bash
    shopify theme dev
    ```

    This will open the local development server where you can preview your changes in real-time.

3. Open the project in Visual Studio Code (or your preferred code editor). If you're using VS Code, you should be prompted to install the [Theme Check extension](https://marketplace.visualstudio.com/items?itemName=Shopify.theme-check-vscode).

4. Start developing by following the exercises below.

---

## Objective

The goal of this exercise is to demonstrate your understanding of Shopify’s templating language (Liquid) and your ability to implement a clean and user-friendly UI.

---

### Exercices
## Exercise 1 : Add Custom "Icon + Text" Blocks to the Product Section

1. **Extend the product section**:  
   - Locate the existing `main-product.liquid` section file in the theme.  
   - Add a new custom block that represents a pair consisting of an **icon (image)** and **text**.

2. **Create the block**:  
   - The block should allow a store admin to:
       - Upload an image (icon).
       - Input a short text description associated with the icon.  
   - Each block represents **one "icon + text" pair**.

3. **Multiple blocks**:  
   - Ensure that multiple blocks can be added, so the store admin can create a list of "icon + text" pairs.

4. **UI**:  
   - Ensure that the layout of the "icon + text" pairs is responsive and visually appealing.  
   - Style the icons and text to align nicely, either using existing Dawn styles or adding custom styles if necessary.

---

## Exercise 2 : Create a Custom Section with Multiple "Image + Text" Blocks

1. **Create a new custom section**:  
   - In the theme, create a new section file called `custom-image-text.liquid`.

2. **Add custom blocks**:  
   - In this section, allow the store admin to add multiple blocks.  
   - Each block should represent a pair of:
       - An **image** (uploadable by the admin).
       - A **text** field (editable by the admin).

3. **Single vs multiple lines layout**:  
   - Add a setting in the section that lets the store admin choose between displaying the blocks in:
       - **Single line (row)**: All blocks are displayed in a single row, with images and text aligned horizontally.
       - **Multiple lines (rows)**: Blocks are displayed in multiple rows, where each row contains a set number of blocks (e.g., 2 or 3 per row).

4. **UI**:  
   - Ensure the layout is responsive, so that the blocks look good on both desktop and mobile.  
   - Style the text and image pairs to align nicely, providing sufficient spacing between each block for a clean visual presentation.

5. **Optional Bonus**:  
   - Allow the store admin to control the number of blocks per row when multiple lines are selected.  
   - Provide an option to adjust the spacing between blocks.

---

### Submission

When you're done, ensure your code is clean and well-commented. Push your changes to your forked repository and share the link with us.

---

## Developer tools

There are a number of really useful tools that the Shopify Themes team uses during development. Dawn is already set up to work with these tools.

### Shopify CLI

[Shopify CLI](https://github.com/Shopify/shopify-cli) helps you build Shopify themes faster and is used to automate and enhance your local development workflow. It comes bundled with a suite of commands for developing Shopify themes—everything from working with themes on a Shopify store (e.g., creating, publishing, deleting themes) or launching a development server for local theme development.

You can follow this [quick start guide for theme developers](https://shopify.dev/docs/themes/tools/cli) to get started.

---

### Theme Check

We recommend using [Theme Check](https://github.com/shopify/theme-check) as a way to validate and lint your Shopify themes.

We've added Theme Check to Dawn's [list of VS Code extensions](/.vscode/extensions.json), so if you're using Visual Studio Code as your code editor of choice, you'll be prompted to install the [Theme Check VS Code](https://marketplace.visualstudio.com/items?itemName=Shopify.theme-check-vscode) extension upon opening VS Code after you've forked and cloned Dawn.

You can also run it from a terminal with the following Shopify CLI command:

```bash
shopify theme check
