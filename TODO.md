## URL STRUCTURE

https://neural.fm

https://neural.fm/bitcoin

https://neural.fm/music

https://neural.fm/synfonaut@moneybutton.com


- run calculation up to X most recent entries
- run longer full data calculations in background
- before updating predictions, reset all back to 0

## SCALING PROBLEM
- There's just too many rows...you need to classify a smaller data set while iterating and then do the full one in the background
- Clear Twitter dataset....only grab recent 50 tweets?
- Do a little more testing on what is actually slow.... mysql streaming? normalization? prediction? all of it?
- What else is causing the slow down?
- Could cache trainingInputData if that is slow...might make DB big bug oh well....
- MongoDB batch size....see if faster ways to stream data in
- btw streaming data doesn't even seem to be working...it's not calling 'done' which means promise is hanging.....
- what's a way we could hack it so that we could ship tomorrow? my vote right now? make data set smaller... goodnight. and good luck

## TODO
- [ ] Editor mode
- [ ] Classify it
- [ ] Train it


- [ ] Image mode
- [ ] Classification mode

## BONUS ROUND
- [ ] title tags
- [ ] snapshot hashes of data models on chain
- [ ] paymail integration
- [ ] tonicpow integration

## BEFORE GOING LIVE
- [ ] SSL certificate
- [ ] Error boundary
- [ ] Copywriting

## NICE TO HAVE
- [ ] Performance optimzations on normalizer...iterative so doesn't need entire data set in memory
- [ ] Performance optimzations on prediction updater....bulk writer
- [ ] Performance optimzations on model input size
- [ ] Performance optimzations on training...it takes a really long time...likely just do load soure dat
    - [ ] Is there a move to make training a lot more lightweight but only using partial data?
    - [ ] Is there a move to make training a lot more lightweight but only using partial data?
- [ ] Update all throw "strings" into throw new Error("string")...it makes stack traces nicer
- [ ] Custom Colors ...just something a little unique
- [ ] A few icons here and there would make a big different ("like on the create button")
- [ ] Loading spinner before side loads (with timout and error message)
- [ ] training with callback to provide UI updates
- [ ] cancel training in middle

- [ ] model is getting detached when server resets or client closes website....need to wake up socket automatically when client reconnects

## INSANE MODE
- [ ] implement twetch source to start testing multi data normalization
- [ ] scrape a lot of twitter history
- [ ] sometimes caldera is crashing


## AFTER
- [ ] Thorough review of data model and indexes. Don't need to index entire normalization field just to check if it exists...probably need a separate field

## ON CHAIN HASHES
https://www.bitpaste.app/tx/0f1c503d83d4e05ffffaaa81fa039187ba8f895a44e0bc8e9dc6c82079bd2562

## BONUS POINTS
- [ ] create your own channel should work
- [ ] ideally create 2 other channels just to have some variance


## TAGLINES
- Neural Network Radio Stations
- Intelligence For Your Life
- Intelligent Neural Networks For your Life
- AI-powered information channels, be your own DJ
- Intelligent Information Channels
- AI-powered information channels
