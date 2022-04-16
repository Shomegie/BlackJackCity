<script>
var deck = []

var cardValue = (i)=> i%13>10?10:i%13

var cardFace = (face)=> {
    if (face>39)
        return "clubs"
    else if (face>26)
        return "spades"
    else if (face>13)
        return "diamonds"
    else
        return "hearts"
}

let card;
for (let i=1; i<=52; i++){
    card = {id:i,value:cardValue(i),face:cardFace(i)}
    deck.push(card)
}


// for (var i =1; i<=52; i++){
//     deck.push(
//        // {id:i,value:cardValue(i),face:cardFace(i)}
//        {"id":i}
//     )
// }



</script>


<ul>
    <li>Player(s) card 1</li>
    <li>Dealer card 1 face down</li>
    <li>Player(s) card 2</li>
    <li>Dealer card 2 face up</li>
</ul>

{deck[27].id}
{deck[27].value}
{deck[27].face}

