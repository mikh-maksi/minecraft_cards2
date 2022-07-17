Робота із часом:  
loops.forever(function () {
    time = Math.idiv(gameplay.timeQuery(GAME_TIME), 100)
    mod = time % 10
    if (mod % 2 == 0) {
        if (active == 1) {
            player.say("Парні")
            active = 0
        }
    } else {
        if (active == 0) {
            player.say("Не парні")
            active = 1
        }
    }
})

Додавання води:

loops.forever(function () {
    time = Math.idiv(gameplay.timeQuery(GAME_TIME), 100)
    mod = time % 10
    if (mod % 2 == 0) {
        if (active == 1) {
            blocks.fill(
            AIR,
            world(0, 4, 0),
            world(0, 7, 0),
            FillOperation.Replace
            )
            active = 0
        }
    } else {
        if (active == 0) {
            blocks.fill(
            WATER,
            world(0, 4, 0),
            world(0, 7, 0),
            FillOperation.Replace
            )
            active = 1
        }
    }
})


