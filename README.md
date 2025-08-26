#Project Report: Real Estate Web Application
1. Overview:
   
This project is a real estate web application built using Next.js and Tailwind CSS.
           Key Features:
                   Responsive Navbar with mobile menu.
                   
                   Residencies Section with a horizontal slider.
                   
                   Our Value Section featuring an FAQ accordion.

                   Contact Section with interactive call-to-action cards.

2. Technologies Used

Next.js – For server-side rendering and React components.

Tailwind CSS – Utility-first styling framework.

Lucide-react icons – Modern icons such as Menu, X, Phone, etc.

3. Tailwind CSS Usage

Tailwind is used to style components directly in HTML:

<nav className="bg-gray-900 text-white sticky top-0 z-50 shadow-md">


Responsive behavior is achieved using breakpoints:

<ul className="hidden md:flex items-center gap-8 font-medium">


Utility classes like rounded-lg, shadow-lg, overflow-x-scroll make styling easier and more consistent.

4. Functions and Logic
4.1 State Management with Hooks

Example for toggling the mobile menu:

const [open, setOpen] = useState(false);

4.2 Accordion Toggle

Controls opening and closing of FAQ answers:

onClick={() => toggleAccordion(index)}

4.3 Residencies Data Array

Dynamically renders property cards:

const residencies = [
  { id: 1, price: "$47,043", title: "Aliva Priva Jardin", img: "/images/Modern-Appartment.jpg" },
  ...
];

5. Key Sections
5.1 Navbar

Desktop links with hover effects.

Mobile menu controlled by a hamburger button.

5.2 Residencies Slider

Horizontal scroll using Tailwind’s overflow-x-scroll.

Cards rendered dynamically from the residencies array.

5.3 Our Value Section

Left: Feature image.

Right: FAQ accordion with toggle functionality.

5.4 Contact Section

Four interactive options: Call, Chat, Video Call, Message.

Each card contains:

Icon

Description

Action button

6. How to Upload and Host
6.1 Push the Project to GitHub

Create a new repository.

Commit and push all files.

6.2 Deploy on Vercel or Netlify

Ensure images are placed inside /public/images/.

6.3 Image Reference Example
<img src="/images/contact-house.png" alt="Contact" />
