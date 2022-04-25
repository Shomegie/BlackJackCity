<script>
    


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

    /* vv card shuffler vv */
    var deck = []
    let card;
    let shuffleDeck = () => {
        for (let i=1; i<=52; i++){
            card = {id:i,value:cardValue(i),face:cardFace(i)}
            deck.push(card)
        }
    }
    shuffleDeck()
    /* ^^ card shuffler ^^ */



    let draw = ()=> {
        let length = deck.length
        let draw_pick = Math.floor((Math.random()*length))

        return  deck.splice(draw_pick,1)

    }


    let draws = []
    for (let i=0; i<52; i++){
        draws.push(draw())
    }

//console.log(draws)

</script>


<div class="app-container h-full bg-contain bg-origin-border" style= "background-image: url(images/web.png)" >

    
    <!-- <img src="images/bg2.png" alt="background image" /> -->

</div>


<!-- <ul>
    <li>Player(s) card 1</li>
    <li>Dealer card 1 face down</li>
    <li>Player(s) card 2</li>
    <li>Dealer card 2 face up</li>
</ul> -->

<!-- 
{deck[27].id}
{deck[27].value}
{deck[27].face} -->

<!-- {#each draws as card, index }
   <p class="text-red-400"> {index+": "} {Object.entries(card[0]).map(x=>x.join(": ")).join("\n")} </p>
{/each} -->





