# Pokémon Search App

## Project Overview

The Pokémon Search App is a simple web application built using **HTML, CSS, and JavaScript**. It integrates with the **PokéAPI** to fetch and display Pokémon information based on the user's input.

The application demonstrates API integration using the JavaScript `fetch()` method and dynamically displays Pokémon details on the webpage.

---

## Features

- Search Pokémon by **Name**
- Search Pokémon by **ID**
- Display Pokémon Image
- Display Name
- Display ID
- Display Height
- Display Weight
- Display Types
- Display Abilities
- Display Base Stats
- Loading Message
- Error Handling
- Input Validation

---

## Technologies Used

- HTML5
- CSS3
- JavaScript (ES6)
- Fetch API
- PokéAPI

---

## How to Run the Project

1. Download or clone the project.
2. Open the project folder.
3. Open **index.html** using Live Server in Visual Studio Code.
4. Enter a Pokémon name or ID.
5. Click the **Search** button.

---

# Testing the Application

## Search by Name

Enter

```
pikachu
```

Click **Search**

The application should display

```
Image

Name: Pikachu

ID: 25

Height: 4

Weight: 60

Type: electric

Abilities:
- static
- lightning-rod

Stats:
- HP
- Attack
- Defense
- Speed
- ...
```

---

## Search Another Pokémon

Enter

```
charizard
```

Click **Search**

The application should display Charizard's information.

---

## Search by Pokémon ID

Enter

```
150
```

Click **Search**

The application should display

```
Mewtwo
```

---

## Invalid Search

Enter

```
abcdxyz
```

Click **Search**

The application should display

```
Pokémon not found.
```

---

## Empty Input

Leave the textbox empty.

Click **Search**

The application should display

```
Please enter a Pokémon name or ID.
```

---

# How the Project Works

```
User enters:

pikachu
      │
      ▼
JavaScript reads input
      │
      ▼
fetch()
      │
      ▼
     API
      ▼
PokéAPI sends JSON data
      │
      ▼
JavaScript extracts:
- Name
- Image
- Height
- Weight
- Types
- Abilities
- Stats
      │
      ▼
Displays the data on the webpage
```

---

## JSON Data Used

The application extracts the following properties from the API response.

| Property | Description |
|----------|-------------|
| name | Pokémon name |
| id | Pokémon ID |
| sprites.front_default | Pokémon image |
| height | Pokémon height |
| weight | Pokémon weight |
| types | Pokémon types |
| abilities | Pokémon abilities |
| stats | Pokémon base statistics |

---

## Project Structure

```
pokemon-search-app/

│── index.html
│── style.css
│── script.js
│── README.md
```

---

## Learning Outcomes

This project demonstrates the following JavaScript concepts:

- DOM Manipulation
- Event Handling
- Fetch API
- API Integration
- JSON Parsing
- Template Literals
- Async/Await
- Error Handling
- Input Validation
- Dynamic API URL Generation

---

## Future Improvements

- Display Pokémon moves
- Display Pokémon evolution chain
- Display multiple Pokémon images
- Add dark mode
- Add search history
- Add responsive design improvements

---


**Dhanalaxmi Ravela**
