# Pokédex - portfolio app

This is a portfolio app made with [React Native](https://reactnative.dev) and
[Expo](https://expo.dev).

## Goal

To demonstrate ideas and good practices to implement an efficient and user
friendly React app. I'm also registering the thinking process below.

In a real world project, the team would usually iterate on the problem and
solution, create mockups, implement a prototype and test it with real users.
This demo will focus on the implementation part alone, using an existing mockup.

## Journal

### Day 1

For the mockup, I picked
[Pokédex App by Saepul Nahwan](https://dribbble.com/shots/6540871-Pokedex-App).
There's a complete version for purchase, but I'll take just those 3 screens.

For the data, I'll be using [PokéAPI](https://pokeapi.co/). It's free and has
most data required in the mockup, such as stats, images and physical attributes.

Before any coding, I can plan ahead some work.

#### React components

I start by breaking down the mockup into relevant React components.
If I don't plan this upfront, the app will likely need refactoring very soon.
For example, it's very common that you implement a fixed-size component that
displays text, but later realize the same component occurs in different sizes
and that it can also display an image or sub-component. Planning saves time.

![pokedex-components](https://user-images.githubusercontent.com/5458658/132126766-ce07e8fb-e1e8-44fb-b2c0-7e637227c5cc.png)

#### Routes

I like to think of navigation like website URLs, some are nested, some are flat.
It's how React navigation libraries work and it's helpful for Universal Links.

- `/` - Pokémon List Screen
  - `/pokemon/:id` - Pokémon Detail Screen
    - `/about` - About Tab (default)
    - `/base-stats` - Base Stats Tab
    - `/evolution` - Evolution Tab
    - `/moves` - Moves Tab
