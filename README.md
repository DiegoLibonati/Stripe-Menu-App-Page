# Stripe-Menu-App-Page

## Getting Started

1. Clone the repository
2. Join to the correct path of the clone
3. Install node_modules with npm install
4. Use npm start to run the app page

## Description

I made a web application that simulates a new style of navbar. It is not the traditional navbar, but it is a menu that will appear if we hover over the nav link. As you scroll through the different nav links, the menu will scroll as well.

## Technologies used

1. React JS
2. CSS3

## Galery

![Stripe-menu-App-Page](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/React/Imagenes/stripemenureact-0.jpg)

![Stripe-menu-App-Page](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/React/Imagenes/stripemenureact-1.jpg)

![Stripe-menu-App-Page](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/React/Imagenes/stripemenureact-2.jpg)

![Stripe-menu-App-Page](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/React/Imagenes/stripemenureact-3.jpg)

![Stripe-menu-App-Page](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/React/Imagenes/stripemenureact-4.jpg)

## Portfolio Link

`https://diegolibonati.github.io/DiegoLibonatiWeb/#/projects?q=Stripe%20Menu%20App%20Page`

## Video

https://user-images.githubusercontent.com/99032604/199617642-cbe53bbe-07a3-4e08-a153-0b75c1994920.mp4

## Documentation

In the `svgs` folder we have all the images.
In the `helpers/data.js` file we have all the information that we are going to use to render in the page as if it was the information of an API.
In the `helpers/context.js` file we find the context that we use for the whole application to handle states and functions:

This code block handles the system of opening or closing the navigation menu in the mobile version:

```
const [mobileMenu, setMobileMenu] = useState(false);

const handleMobileMenuOpen = () => {
    setMobileMenu(true);
};

const handleMobileMenuClose = () => {
    setMobileMenu(false);
};
```

This code block handles the system of opening or closing the navigation menu in the desktop version:

```
const [desktopMenu, setDesktopMenu] = useState(false);

const handleDesktopMenuOpen = (text, centerBtn) => {
    const page = sublinks.find((link) => link.page === text);
    setPage(page);
    setLocation(centerBtn);
    setDesktopMenu(true);
};

const handleDesktopMenuClose = () => {
    setDesktopMenu(false);
};
```

The `page` state is in charge of rendering the different links for each navLink:

```
const [page, setPage] = useState({ page: "", links: [] });
```
