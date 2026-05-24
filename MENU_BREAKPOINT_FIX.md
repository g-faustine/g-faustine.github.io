Menu Breakpoint Fix

PROBLEM:
The menu was switching to hamburger mode at 640px (sm breakpoint), causing multi-line display on medium screens.

SOLUTION:
Created custom header template with breakpoint at 1024px (lg).

FILES CHANGED:
- layouts/_partials/header/hybrid.html - Custom header template overriding Congo theme

HOW TO ADJUST:

The breakpoint is controlled by Tailwind CSS classes in layouts/_partials/header/hybrid.html:

1. Hamburger button (line ~8):
   class="block lg:hidden"
   
2. Desktop menu (line ~90):
   class="hidden list-none flex-row text-end lg:flex"

Change "lg:" to your desired breakpoint:
- sm: 640px
- md: 768px  
- lg: 1024px (current)
- xl: 1280px
- 2xl: 1536px

Example for 1280px:
- Change to: class="block xl:hidden"
- Change to: class="hidden list-none flex-row text-end xl:flex"

TESTING:
1. git checkout fix-menu-breakpoint-v2
2. hugo server -D
3. Test at different screen sizes
