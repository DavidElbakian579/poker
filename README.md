# poker
The game of poker

// The Poker Game

let player1 = [];
let player2 = [];
let player3 = [];
let player4 = [];
let player5 = [];
let board = [];

let deckOfCards = [
    "D2", "C2", "H2", "S2", 
    "D3", "C3", "H3", "S3", 
    "D4", "C4", "H4", "S4", 
    "D5", "C5", "H5", "S5", 
    "D6", "C6", "H6", "S6",
    "D7", "C7", "H7", "S7", 
    "D8", "C8", "H8", "S8", 
    "D9", "C9", "H9", "S9",
    "D10", "C10", "H10", "S10", 
    "DQ", "CQ", "HQ", "SQ", 
    "DJ", "CJ", "HJ", "SJ", 
    "DK", "CK", "HK", "SK", 
    "DA", "CA", "HA", "SA"
];

// carteri master
let diamond = 'D';
let spade = 'S';
let heart = 'H';
let club = 'C';

// cart points for 'HighCard' combination
let two = {Name:'2', number:0};
let three = {Name:'3', number:1};
let four = {Name:'4', number:2};
let five = {Name:'5', number:3};
let six = {Name:'6', number:4};
let seven = {Name:'7', number:5};
let eight = {Name:'8', number:6};
let nine = {Name:'9', number:7};
let ten = {Name:'10', number:8};
let jalet = {Name:'J', number:9};
let queen = {Name:'Q', number:10};
let king = {Name:'K', number:11};
let tuz = {Name:'A',number:12};

// combinations
let HighCard = {Name:'HighCard', number:0};
let Pair= {Name:'Pair', number:1};
let TwoPair= {Name:'TwoPair', number:2};
let Trips= {Name:'Trips', number:3};
let Straight= {Name:'Straight', number:4};
let Flush = {Name:'Flush', number:5};
let FullHouse={Name:'FullHouse', number:6} ;
let Quads= {Name:'Quads', number:7};
let StraightFlush= {Name:'StraightFlush', number:8};
let RoyalFlush= {Name:'Royal Flush', number:9};

// method for get new card from the deck and return new array without pop cart
let getNewCard = deckOfCards => {
    let rand = Math.round(Math.random() * (deckOfCards.length-1));
    let cart = deckOfCards[rand];
    console.log(cart); // for debug
    deckOfCards.splice(rand, 1);
    return cart;
};


// metod razdachi kart igrokam - 1 krug po 1 karte kajdomu
let distributionOfCards = () => {
    player1.push(getNewCard(deckOfCards));
    player2.push(getNewCard(deckOfCards));
    player3.push(getNewCard(deckOfCards));
    player4.push(getNewCard(deckOfCards));
    player5.push(getNewCard(deckOfCards));
};
// razdacha po 2 karty kajdomu igroku
distributionOfCards()
distributionOfCards()


// "Sexanin piti skzbuc 3 qart lini"
board.push(getNewCard(deckOfCards));
board.push(getNewCard(deckOfCards));
board.push(getNewCard(deckOfCards));


// Here we should write code for the programm
