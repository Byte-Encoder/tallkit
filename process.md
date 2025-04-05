# Guide for Junior Frontend Engineer: Using Tailwind CSS

## 1. Research Similar Category Websites on Design Sites (e.g., Dribbble)
- **Objective**: To understand industry trends, best practices, and gather inspiration for your design.
- **Action**:
    - Browse websites on design platforms like [Dribbble](https://dribbble.com/) or [Behance](https://www.behance.net/).
    - Look for websites that share a similar purpose or style to the one you're building.
    - Focus on layout structure, typography, color schemes, and overall user interface design.
    - Take notes on specific patterns that might help inform your design decisions, such as spacing, button styles, card designs, or navigation patterns.

    **Tip**: Take screenshots or make mood boards of components and layouts that stand out to you and align with the project goals.

---

## 2. Prepare Layout and Plan Pages & Components
- **Objective**: To define the overall structure of the site and identify reusable components.
- **Action**:
    - Sketch out the main layout of the page, including header, footer, and content sections.
    - Break down the pages into components that can be reused across multiple pages. For example:
        - Navbar
        - Hero section
        - Cards (product/service displays)
        - Forms (login, contact, etc.)
        - Footer with links and social icons
    - Organize the layout into clear sections like "Header," "Main Content," "Sidebar," and "Footer" to ensure the design is modular and scalable.

    **Tip**: Use wireframing tools (e.g., Figma, Adobe XD) to quickly prototype layouts before jumping into Tailwind CSS development.

---

## 3. Prepare Color Variables in Tailwind's `app.css` File
- **Objective**: To set up a custom color palette to maintain consistency across your design.
- **Action**:
    - Open the `tailwind.config.js` file and extend the default theme with custom colors under the `extend` key. You can define colors for various design states like:
        - `primary`: Main brand color (e.g., blue).
        - `secondary`: A complementary color (e.g., light gray or secondary branding color).
        - `accent`: A color used for highlights or buttons.
        - `base`: Default background or text color.
        - `warning`: Used for alerting users (e.g., yellow or orange).
        - `error`: Colors to indicate errors (e.g., red).
    - Example:
    ```css
    @theme {
    --font-poppins: "Poppins";
    --font-inter: "Inter";
    --color-base-100: oklch(98% 0.001 106.423);
    --color-base-200: oklch(97% 0.001 106.424);
    --color-base-300: oklch(92% 0.003 48.717);
    --color-base-content: oklch(21% 0.006 56.043);
    --color-primary: oklch(78% 0.115 274.713);
    --color-primary-content: oklch(25% 0.09 281.288);
    --color-secondary: oklch(0% 0 0);
    --color-secondary-content: oklch(100% 0 0);
    --color-accent: oklch(86% 0.005 56.366);
    --color-accent-content: oklch(14% 0.004 49.25);
    --color-neutral: oklch(14% 0.004 49.25);
    --color-neutral-content: oklch(98% 0.001 106.423);
    --color-info: oklch(62% 0.214 259.815);
    --color-info-content: oklch(97% 0.014 254.604);
    --color-success: oklch(72% 0.219 149.579);
    --color-success-content: oklch(98% 0.018 155.826);
    --color-warning: oklch(76% 0.188 70.08);
    --color-warning-content: oklch(98% 0.022 95.277);
    --color-error: oklch(65% 0.241 354.308);
    --color-error-content: oklch(97% 0.014 343.198);
    --radius-selector: 2rem;
    --radius-field: 0.5rem;
    --radius-box: 1rem;
    --size-selector: 0.25rem;
    --size-field: 0.25rem;
    --border: 1px;
    --depth: 1;
    --noise: 1;
}
    ```

    **Tip**: Keep the color palette simple and balanced. Too many colors can make your UI feel cluttered. Stick to a few primary colors and use lighter/darker shades where needed.


## 4. Start from the Navbar
- **Objective**: The navbar is a critical part of the site’s layout and user experience, so starting with it can help set the tone for the rest of the design.
- **Action**:
    - Begin by creating a responsive navbar using Tailwind CSS utilities for layout and positioning.
    - Use flexbox or grid utilities to structure the navbar elements like logo, navigation links, and any buttons.
    - Example basic navbar:
    ```html
    <nav class="bg-primary p-4">
      <div class="max-w-7xl mx-auto flex justify-between items-center">
        <a href="#" class="text-white font-bold">Brand</a>
        <div class="hidden md:flex space-x-4">
          <a href="#" class="text-white">Home</a>
          <a href="#" class="text-white">About</a>
          <a href="#" class="text-white">Contact</a>
        </div>
      </div>
    </nav>
    ```
    - For responsiveness, use Tailwind’s breakpoint classes to hide/show the navigation menu on different screen sizes.
        - For example, a hamburger menu on mobile:
    ```html
    <div class="md:hidden">
      <button class="text-white">☰</button>
    </div>
    ```

    **Tip**: Keep your navbar simple and focus on usability. Make sure it's responsive, ensuring good accessibility on all devices. Tailwind’s utility-first approach allows you to quickly adjust the navbar’s layout for small, medium, and large screens.

---
