Menu Breakpoint Configuration

PROBLEM:
The hybrid menu layout was switching to hamburger mode at 640px (sm breakpoint).

SOLUTION:
Modified the breakpoint from sm: (640px) to md: (768px) in the header template.

FILES CHANGED:
- layouts/partials/header/hybrid.html - Overrides the theme hybrid header template

HOW TO ADJUST THE BREAKPOINT:

The menu breakpoint is controlled by Tailwind CSS classes.

Current Configuration (768px / md breakpoint):
- Hamburger menu: class="block md:hidden" - visible below 768px
- Desktop menu: class="hidden list-none flex-row text-end md:flex" - visible at 768px and above

Available Tailwind Breakpoints:
- sm: 640px
- md: 768px (current)
- lg: 1024px
- xl: 1280px
- 2xl: 1536px

To Change the Breakpoint:
1. Edit layouts/partials/header/hybrid.html
2. Find and change these classes:
   - class="block md:hidden" -> change md: to your desired breakpoint
   - class="hidden list-none flex-row text-end md:flex" -> change md: to same breakpoint

Example for 1024px (lg):
   - Change to class="block lg:hidden"
   - Change to class="hidden list-none flex-row text-end lg:flex"

Testing:
After making changes, test at different screen sizes.

Technical Details:
The hybrid layout uses a checkbox input (#menu-controller) to toggle the hamburger menu and CSS classes to show/hide elements based on screen size.
