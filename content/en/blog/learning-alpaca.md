+++
title = "Learning to automate my investing with the Alpaca API. Part 1."
# subtitle =
tags = ['learning', 'finance']
date = 2021-01-13
description = "Learning how to use an API using examples from the Alpaca paper trading API. This blog series starts from step 0, authenticating yourself to the API server."
# banner = 'img/pf/gme-stock.jpg'
+++

# Who this is for

You want to learn about using an Application Program Interface (API) with a topic that is something other than the weather. If you already know how to use APIs. This is definitely not meant for you.

# What's an API?

An API is 

We're going to focus on **RE**presentational **S**tate **T**ransfer **R**EST (REST) APIs. Want to dive deeper into the actual tech behind REST? Read more [here](https://blog.postman.com/rest-api-definition/).

# What's Alpaca?

Alpaca is a  commission free trading platform like Robinhood. Unlike Robinhood, it's less focused on making investing a game. Instead, it's major selling point is being able to automate your investing using their Application Program Interface (API). 

An API is the definition that programs use to communicate (interface) with each other and request/perform actions. This is why you may also hear about things like API contracts, which explicitly lay out how an API behaves.

# Requirements

This guide is written with MacOS and the bash shell in mind, so some basic familiarity with the MacOS command line (Terminal) is really going to help here. When I say basic, I really do mean basic like how to open a hidden file and running commands. My aim is to explain anything more than that sufficiently so that you always know what's going on.

You'll also need an [Alpaca account](https://app.alpaca.markets/brokerage/new-account), specifically the "paper" money account. We are definitely not playing with real money here.

# Gathering information

To use the Alpaca API, you need to be able to verify who you are so that Alpaca knows you're allowed to do what you want to do. When you log in to a website, you use a username and password. APIs often use an API Key ID and Secret Key.

The recommended way of doing this is to start with configuring environment variables for your machine. Creating environment variables help you provide the same input consistently. 

> What's an environment variable?
>
> An environment variable is a variable that exists for your environment, independent of any program. You can refer to them by name in scripts or command-line programs. This way, you're not storing things like passwords where everyone can see, such as in a source control system like GitHub.

These are the environment variables that you are going to need to configure:

- **`APCA_API_BASE_URL`**

   The base URL is essentially where the API endpoints live. Endpoints are the actions you can take with an API. For Alpaca, this is the base URL: `https://paper-api.alpaca.markets`. Endpoints show up at the end of the base URL and are usually versioned. Here's an example of one: `https://paper-api.alpaca.markets/v2/orders`. The `/orders/` endpoint is the one you use to perform actions like buying.

- **`APCA_API_KEY_ID`**

   Think of this like your username. It's a an identifier for the Alpaca servers to know who you are.

- **`APCA_API_SECRET_KEY`**

   Keep this somewhere safe. This is the API equivalent of a password. If you lose it or let someone see it, you have to generate a new one.

Go to your [Alpaca paper dashboard](https://app.alpaca.markets/paper/dashboard/overview) to get the values for these variables. Have this open in a browser tab so that you can refer to these values later. Alternatively, you can take an extra secure step and store them in a password manager.

# Setting up your environment

Edit your `~./bash_profile` with your favorite plaintext editor, such as Atom or VSCode. (The default shell for MacOS is bash, which is why you're editing this particular file. It'll be a different file if you're not using bash.) You might notice other entries in the file, but you can safely ignore those for this lesson. 

Add the following lines to the file:

```
export APCA_API_BASE_URL=https://paper-api.alpaca.markets
export APCA_API_KEY_ID=<Random string of characters unique to you>
export APCA_API_SECRET_KEY=<Random string of characters you need to keep secret>
```

Replace `<Random string of characters unique to you>` and `<Random string of characters you need to keep secret>`

By putting it into your bash profile, these environment variables are available every time you open a Terminal window. 

Since you modified your bash profile, you have to load it again for the variables to be available. Do one of the following:

* Quit and reopen the Terminal. If it wasn't open and running, you can open it now.
* Manually load it by running `source ~/.bash_profile`.

# Checking your work

If you enter the following command, Terminal should return the values you assigned to the variable. For example, if you enter

```
echo $APCA_API_BASE_URL
```

You should get the following response:

```
https://paper-api.alpaca.markets
```

Repeat this for the other two variables you set.

# Putting it all together

Now that you've set all the variables, it's time to take it for a spin.

Run the following command:

```
curl  --request GET "$APCA_API_BASE_URL/v2/account" \
--header "APCA-API-KEY-ID: $APCA_API_KEY_ID" \
--header "APCA-API-SECRET-KEY: $APCA_API_SECRET_KEY"
```

Let's break this command down one piece at a time:

* **`curl`**

   This is the utility you are using to send your request to Alpaca.

* **`--request GET`**

   What action you want to take. `GET` means we are getting information from Alpaca.

   > Here are all the actions you can take with REST APIs: GET, POST, PUT, and DELETE.

* **`"$APCA_API_BASE_URL/v2/account"`**

## Dive deeper

Learning