# Program the lever to blow up the Helden in IT logo!

## Step 1
Voeg een ``||forever||`` toe.

```blocks
loops.forever(function () {})
```

## Step 2
Voeg een ``||if||`` toe in de ``||forever||``.

```blocks
loops.forever(function () {    if(true)  })
```

## step 3
Voeg een ``||testForBlock||`` toe waar de waarde true nu staat.

```blocks
loops.forever(function () {
    if (blocks.testForBlock(GRASS, pos(0, 0, 0))) {
    	
    }
})
```

## step 4
Voeg een ``||blockWithData||`` toe op de plek van de grassblock in de ``||if||``.

```blocks
loops.forever(function () {
    if (blocks.testForBlock(blocks.blockWithData(GRASS, 0), pos(0, 0, 0))) {
    	
    }
})
```

## step 5
Plaats een ``||world||`` op de tweede positie van de ``||if||``. Verander hierna de grassblock naar een lever en zet de datavalue op 9. De wereldcoördinaten moeten 244, 74, -110 worden.

```blocks
loops.forever(function () {
    if (blocks.testForBlock(blocks.blockWithData(LEVER, 9), world(244, 74, -110))) {
    	
    }
})
```
## step 6
voeg een ``||execute||`` met de tekst "function blowup" toe in de ``||if||``.

```blocks
loops.forever(function () {
    if (blocks.testForBlock(blocks.blockWithData(LEVER, 9), world(244, 74, -110))) {
        player.execute(
        "function blowup"
        )
    }
})
```

## step 7
Voeg een ``||place||`` toe onder de ``||execute||``.

```blocks
loops.forever(function () {
    if (blocks.testForBlock(blocks.blockWithData(LEVER, 9), world(244, 74, -110))) {
        player.execute(
        "function blowup"
        )
        blocks.place(GRASS, pos(0, 0, 0))
    }
})
```

## step 8
Voeg een ``||leverOnBlock||`` toe op de plek van de grassblock en voeg een ``||world||`` toe op de tweede plaats.

```blocks
loops.forever(function () {
    if (blocks.testForBlock(blocks.blockWithData(LEVER, 9), world(244, 74, -110))) {
        player.execute(
        "function blowup"
        )
        blocks.place(blocks.lever(BLOCK_BOTTOM_EAST_WHEN_OFF), world(0, 0, 0))
    }
})
```

## step 9
Verander de bottom pointing west naar East side en zet de coördinaten op 244, 74, -110.

```blocks
loops.forever(function () {
    if (blocks.testForBlock(blocks.blockWithData(LEVER, 9), world(244, 74, -110))) {
        player.execute(
        "function blowup"
        )
        blocks.place(blocks.lever(BLOCK_SIDE_FACING_EAST), world(244, 74, -110))
    }
})
```
