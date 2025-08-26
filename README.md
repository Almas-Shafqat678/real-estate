Project Report: Homyz Real Estate Website
1. Overview

This project is a responsive real estate website built with Next.js/React and styled using Tailwind CSS.
Key features:

Modern responsive navigation bar with mobile toggle.

Residencies section with horizontal slider to showcase properties.

Our Value section with image and FAQ accordion.

Contact section with interactive cards and responsive layout.

Fully mobile-friendly using Tailwind's utility classes.

2. Tailwind CSS Usage

Tailwind CSS is used as the primary styling framework. It allows utility-first CSS, meaning you style components directly using class names instead of writing separate CSS files.

Examples in the code:

Layout and spacing:

<div class="flex flex-col md:flex-row items-center gap-12"></div>


flex flex-col md:flex-row → Flexbox layout; column on mobile, row on medium+ screens.

gap-12 → Adds uniform spacing between items.

Typography and colors:

<h2 class="text-3xl md:text-4xl font-bold text-blue-900 mt-2"></h2>


text-3xl md:text-4xl → Responsive font sizes.

text-blue-900 → Custom color from Tailwind palette.

Responsive Images:

<img class="rounded-t-full overflow-hidden border shadow-lg object-cover w-full h-auto" />


object-cover → Maintains aspect ratio.

w-full h-auto → Makes images responsive.

3. Main Components & Functions
Navbar

useState Hook:

const [open, setOpen] = useState(false);


Used to toggle the mobile menu on and off.

Lucide-react Icons:

import { Menu, X } from "lucide-react";


Used to show hamburger icon and close icon.

Sticky Positioning:

<nav class="bg-gray-900 text-white sticky top-0 z-50 shadow-md"></nav>


Keeps the navbar fixed at the top when scrolling.

Residencies Section

Uses a horizontal slider created with overflow-x-scroll and flex items.

Data is stored in an array of objects:

const residencies = [
  { id: 1, price: "$47,043", title: "Aliva Priva Jardin", img: "/images/Modern-Appartment.jpg" },
  ...
];


Each item is dynamically rendered inside a card component.

Our Value Section

Accordion with useState:

The toggleAccordion function tracks which FAQ is open.

Icons rotate using conditional class names:

className={`${openIndex === index ? "rotate-180" : ""}`}


Flex Layout:

Left side: image inside a rounded container.

Right side: accordion list.

Contact Section

Interactive Cards:
Each card has an icon (Phone, Chat, Video, Mail) and a call-to-action button.

Responsive grid layout using:

<div class="grid grid-cols-2 gap-4 mt-8"></div>


Buttons styled with Tailwind:

<button class="bg-blue-100 text-blue-600 py-1.5 rounded-md"></button>

4. How It Works

Navbar allows smooth navigation across sections with mobile support.

Residencies shows a scrolling list of properties for easy exploration.

Our Value section educates the user with expandable FAQs.

Contact Section provides multiple ways to reach the team.

Images and static assets can be stored locally or hosted on GitHub and accessed via raw URLs.

5. Future Enhancements

Add form validation and submission in Contact section.

Connect backend for property data (e.g., Firebase, Neon).

Add animations using Framer Motion.
