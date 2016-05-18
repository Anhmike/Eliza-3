# Eliza
A JavaScript implementation of the ELIZA bot originally made by Joseph Weizenbaum in 1966.

## Usage

    var bot = new ElizaBot( true ) // the "true" argument controls whether the bot chooses phrases randomly (true) or not (false) [optional arg]
    bot.transform("Hello!") // the only argument allowed is a string; returns bot's response 
    bot.getInitial() // returns the a "hello" phrase
    bot.getFinal() // returns a "goodbye" phrase
    bot.reset() // resets the bot's cache & memory back to its initial state

## Example

    var Eliza   = new ElizaBot(),
        initial = Eliza.getInitial(),
        reply   = Eliza.transform("Hello, Eliza");
    
    console.log(initial); // returns hello
    console.log(reply); // returns a reply to user's "Hello"
    
    // to reproduce the example conversation given by J. Weizenbaum,
    // initialize with the optional random-choice argument
    var originalEliza = new ElizaBot(true);
