# Gopher Telephone

![rainbow sparkles gopher]({{site.baseurl}}/images/rainbow-sparkles-gopher.png)

## Rules
* All gophers get in a line.
* The first gopher thinks up a really special message and tells it to the next gopher.
* Each gopher repeats the message to the next gopher in line.
* When the last gopher receives the message, she tells everyone the message.

If every gopher faithfully repeats the message, then the game isn't terribly fun. However, when each gopher has a slightly different personality, altering the message in unique ways, then the final message can be quite different from the original. Haha, things that are different from what we expect are funny! Get it?! 😎

## Gophers

* **Default**: This gopher is quite boring and repeats the message exactly as received. Everyone starts out with this gopher so that they have a working game to play with.
* **Emoji Gopher**: This gopher ❤️ emoji, and replaces well-known words with their emoji equivalent. For example, it replaces the word `love` with ❤️.
* **Chuck Norris Gopher**: This gopher is obsessed with Chuck Norris, and instead of relaying the message received, sends [Chuck Norris quotes](norris).
* **Data Science Gopher**: Data is awesome! This gopher queries the [SQLite](sqlite) database provided in this repository and sends interesting gopher facts.
* **CSI Cyber Gopher**: Lookout criminals, CSI gopher can read the files on your computer, searching for clues to solve the case. Pick words from the message received, and use it to lookup relevant text from the sample files in this repository.

[norris]: http://api.icndb.com/jokes/random
[sqlite]: https://github.com/mattn/go-sqlite3
[aciitext]: http://artii.herokuapp.com/make?text=gophers

✅ You can find solutions for the gophers in the [solutions branch](https://github.com/ladygogo/telephone/tree/solutions/gophers).

# Get the Game

```
go get -u github.com/ladygogo/telephone
cd ${GOPATH:-~/go}
cd src/github.com/ladygogo/telephone
go build
```

# Play Telephone
```
# open a terminal and run the following
./telephone -name gopher1
# open another terminal in the same directory and run the following
./telephone -name gopher2
```

Once the game is running, you can type messages into the console and it should be repeated to the other connected game instances.

To stop the game, press `CTRL + C`.

Once you have implemented a gopher, you can reload the game as that gopher with `-gopher` flag

```
./telephone -gopher GOPHERTYPE
```

The pre-defined gopher types are:

    * `emoji`
    * `norris`
    * `csi`
    * `data`

# Run Tests

Some of the gophers come with tests which verify your implementation.

**Run a single test**
```
go test -v -run TestEmoji ./gophers
```

**Run all tests**
```
go test -v ./gophers
```
