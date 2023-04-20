# WebApp for Blockchain oracle security Thesis

**Title of the Thesis**: Securing the bridges between two worlds: a Systematic Literature Review of Blockchain Oracles security
Institutions:
- Aalto University, Finland
- Tartu University, Estonia

**Student**: Alessandro Chiarelli

**Supervisors**:
- Prof. Raimundas Matulevicius
- PhD. Mubashar Iqbal
- Prof. Fabian Fagerholm

## Description
WebApp for the thesis project - it is the data source for the inbound oracles
For a detailed description of the use case, see the Thesis

The WebApp simulates a centralized data destination for an outbound blockchain oracle.
The webapp queries information from the blockchain and provides it to the user.
The scenario that is being simulated is that of a news/media company, that provides
flash news on its website through an API. A user of the blockchain oracle wants
to query the latest flash news.

The pieces of news in both the WebApp and design documents will be referred to as
"posts" or "articles" interchangeably.

An article is a json object defined as:
```
{
  title: String,
  description: String
}
```

The WebApp is a Proof of Concept that provides a very simple interface were it shows the last object present in the oracle and whether the generated signature is valid or not.

The thesis focuses on some of the security aspects for blockchain oracles, thus the WebApp
is barebones and has very limited functionality. This is because Web development and 
security of Web Applications is not part of the thesis, thus DO NOT USE this code in any
production environment.

For example, with the way the app is designed, anyone can submit new articles to the 
WebApp database. This is of course problematic, but it is not a concern for our 
purposes.

## Technologies

The technologies used for this WebApp are:
- Node.js / npm to create and manage the app
- Cors.js to allow interacting with the app form any IP
- Body-parser.js to parse the HTTP requests and responses
- Dotenv.js to deal with environment variables
- Nodemon.js to run the app in a test environment
- Web3.js
- Render.com to deploy the app and manage CI/CD
- This Github repository for CI/CD

## How to run

In order to run the app, you need to have Node.js and npm with the latest update available
at the time this document was written: `9.3.1`

You also need your own MongoDB database, otherwise you will not be able to use the API.

Once you download this repository, you need to run `npm install` and `npm start` to run it
in a test environment using Nodemon.

You need to add your Ethereum endpoint in the `app.js` file at line 4. 

The app will run on `localhost:3000`.

## Demo

One demo is available here: https://outbound-oracle.onrender.com
