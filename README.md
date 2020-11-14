# React API Tutorial - Pokemon List
Step by Step commits of setting up a react app that consumes an API using Axios

**Based on this [video](https://www.youtube.com/watch?v=o3ZUc7zH8BE&list=PLZlA0Gpn_vH_NT5zPVp18nGe_W9LqBDQK&index=3&ab_channel=WebDevSimplified) by WebDevSimplified on YouTube**

# What the App does: 
The app consumes pokemon information from [pokeapi.co](https://pokeapi.co/), it fetches paginated data from the api and presents a list of pokemon names.
It also creates dynamic previous/next buttons to allow pagination through the list

# React tools used: 
* Destructuring props
* Mapping elements of array to render
* State variables - useState, useEffect
* Axios for fetching API data
* Using functions as props

# Development process 

* Start with npx create-web-app. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/0e41473a13a9ffa2ba5f7b6b9d5d069b29e46d37))
* Remove majority of boiler plate code. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/221dd46aba262c86a08743ff7493df873cec1605))
* Create initial state variable "pokemon" using the `useState` hook. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/61532256faa49f5f7822a639fec3b9784af6c4fd))
* Render the `PokemonList` component within the App using the pokemon state ([commit](https://github.com/blotty23/React_API_Tutorial/commit/681a055917954f0047ec1db5621905b7a40dd44a))
* Write map in `PokemonList` which loops over pokemon array and renders the names. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/4a9bad167c47e99a18d003b7f0683a56fd30266a))
* Prepare for API usage to populate State, installing axios. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/f2215870a81e6a810de5a02087aca58a69ade793))
* Use axios in a `useEffect` hook to call the API only when the page first renders - shows the first 20 names. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/aec6316304d48524aa98b51808634f34942c62ac))
* Create new state variable `currentPageUrl` and refactor useEffect hook to use it. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/a404aa053ad5def84ef8b9c807d65603387978d7))
* Create new state variables `nextPageUrl` and `prevPageUrl` which are then populated by the API call to `currentPageUrl`. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/e60a3920501ab745717849dc427359194a330fc4))
* Create a new state variable `loading` which shows the user when the api is being called. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/commitaddress))
* Add a cancel function into our useEffect hook so we can't have multiple calls going at the same time. ([commit](https://github.com/blotty23/React_API_Tutorial/commit/12a58c3e26100c6d54a30b275e25334f056a97d9))
* Create functions which change state of `currentPageUrl` to `next` or `prev` `PageUrl` ([commit](https://github.com/blotty23/React_API_Tutorial/commit/5f95ab3597ce26c51faba39f682ae37d370ec92e))
* Create buttons inside Pagination component which use the passed in functions ([commit](https://github.com/blotty23/React_API_Tutorial/commit/ac5c72d92f65926a763630e0c00e9b7ea30b48a4))
* Add conditions so buttons in Pagination only show up if there **is** a previous or next page ([commit](https://github.com/blotty23/React_API_Tutorial/commit/418ee814e341d297af19d96de463fa946d725bad))
* Add conditions to App.js so props passed into Pagination are either functions or null([commit](https://github.com/blotty23/React_API_Tutorial/commit/70e4fa8a94d71010da936a0b03a21e1cb4a9302d))


# Useful things 
* Plugin for Visual studio code - [ES7 React/Redux/GraphQL/React-Native snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets) - lets you type shortcuts to generate react components automatically


