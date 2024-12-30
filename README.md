# Dark Jokes API Documentation

![alt text](https://github.com/qa-p1/Dark-Jokes-API/blob/main/Dark%20Jokes%20API.png?raw=true)

## Table of Contents

- [Introduction](#introduction)
- [API Endpoints](#api-endpoints)
  - [/](#-)
  - [/random](#random)
  - [/joke-by-id](#joke-by-id)
  - [/search](#search)
  - [/submit-joke](#submit-joke)
  - [/playground](#playground)
- [Contributing](#contributing)
- [Rate Limit](#rate-limit)

## Introduction

Welcome to the Joke API! This API provides a collection of dark jokes. You can access the jokes through various endpoints, which are described below. Rate limit **100 per hour**, These are just not meant to hurt anyone's emotion!!

## API Endpoints

### /

Root Page of the Dark Jokes API

**Response:**

```json
{
  "message": "Welcome to the Dark Jokes API. This api is created by none other than me. Visit our Github page for more Documentation: https://github.com/qa-p1/Dark-Jokes-API"
}
```

## /random

This endpoint returns a random selection of jokes. The 'limit' parameter specifies the maximum number of jokes to return. Maximum limit is 20.

**Example Request:**

```http
GET /random?limit=3
```

**Example Response:**

```json
[
  {
    "id": 26,
    "joke": "  What's the difference between baby's and onions? I cry when cutting onions!"
  },
  {
    "id": 119,
    "joke": "How much time does it takes to fill a hole on the road?    Decades Lol"
  },
  {
    "id": 129,
    "joke": "Any joke can be funny when delivered right. Except abortion jokes, cause there's no delivery. "
  }
]
```

## /joke-by-id

This endpoint returns a joke by its ID. If the ID is less than or equal to 0, an error message is returned. If the joke with the specified ID does not exist, an error message is returned.

**Example Request:**

```http
GET /joke-by-id?id=5
```

**Example Response:**

```json
{
    "joke": "Karate for amputees is called partial arts",
    "id": 5,
    "from": "reddit",
    "type": "dark"
}
```

## /search

This endpoint searches for jokes containing the specified query. If no jokes are found matching the query, an error message is returned.

**Example Request:**

```http
GET /search?query=black
```

**Example Response:**

```json
[
  {
    "id": 10,
    "joke": "Why do black people have white palms and white bottoms of there feet?  Because there's a little good in everyone."
  },
  {
    "id": 11,
    "joke": "Why do black men cry after sex?  The pepper spray."
  },
  {
    "id": 29,
    "joke": "Sir, this is a gloryhole. We're going black then."
  },
  {
    "id": 48,
    "joke": "Why is there only two handles on a black persons casket?   Have you ever seen a trash can with more than two handles?"
  },
  {
    "id": 101,
    "joke": "What's the difference between a black man and a tractor tyre? The tyre doesn't sing when you put chains on it."
  }
]
```

## /submit-joke

You can now submit your own jokes to the API! Use this endpoint to send a joke along with your details. All jokes are reviewed before being added to the database. Go Creative!!!


**Form Data:**

- `username`: Your name.
- `joke`: The joke you want to submit.
- `email`: Your email address.


## /playground

The playground is a web interface to test out the API and its endpoints interactively. You can use it to explore features, make API calls, and view responses directly in a GUI. 

###

# Contributing

We welcome contributions to the Dark Joke API! Majorly if you have any jokes available, submit them. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
