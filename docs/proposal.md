# Pokémon "Vibe Check" Tournement
The goal of this website is to create a crowdsourced, uninformed, and incredibly biased ranking of pokemon based on vibes alone. The main page of the site displays a photo and name of two random pokemon and prompts the user to select which one "has better vibes," with what defines "better" and "vibes" purposefully left up to user's discretion.

## Web Services
- [Micro User Service](https://m3o.com/user) (apiKey)
    - POST /v1/user/Create
    - POST /v1/user/Login
    - POST /v1/user/ResetPassword
- [pokéapi](https://pokeapi.co/) (No Auth) (Used to generate Pokémon table)
    - GET /v2/pokemon/{id or name}

## Database Use
The first table, called <strong>PokémonData</strong>, statically stores the information of all pokémon that can be voted on and includes pokémonID (PK), name, and image. The second table, called <strong>Votes</strong>, is edited any time a user votes between two pokémon and includes userID, winningPokémonID (FK), losingPokémonID (FK), and the date and time the vote was made.

## Initial Design
![Page Layout](/pagelayout.png)
![Site Map](/sitemap.png)