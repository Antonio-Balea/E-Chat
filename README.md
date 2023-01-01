
# E-Chat

E-Chat is a chatbot that answers questions accordingly to his training data. 


## Features

- 700 lines of JSON Training Data
- Answers your questions accordingly to his training data
- Cross platform


## Usage/Examples

```
Start talking with E-Chat.
E-Chat: You can say bye to quit.
E-Chat: You can say search to search on internet.
You: hi
E-Chat: Hello there!  (Accuracy -> 18)
You: how are you
E-Chat: I am E-Chat, a Deep-Learning chatbot / an AI language model.  (Accuracy -> 0)
You: what are you doing
E-Chat: I wasn't programmed to do anything.  (Accuracy -> 11)
You: how's the weather
E-Chat: I don't have access to the internet.  (Accuracy -> 45)
```

"You: " is where you type your questions, after you enter them, E-Chat is gonna answer with one of his answers.


## Deployment

To deploy this project in your CMD:

```bash
  cd location (where you downloaded e-chat.py and intents.json)
  e-chat.py
```


## Modifications

If you want to make the E-Chat say that he doesn't understand some questions, here is the following code you should edit:

```
results = model.predict([bag_of_words(inp, words)])
results_index = numpy.argmax(results)
tag = labels[results_index]
if results_index > write here your accuracy number: (it says the accuracy when running the app)
    for tg in data["intents"]:
        if tg['tag'] == tag:
                responses = tg['responses']
    print(f"E-Chat: " + (random.choice(responses)) + f"  (Accuracy -> {results_index})")
            
    else: 
        print("I don't know what are you asking.")
```


## Lessons Learned

I made this project for learning AI. This is the first version of E-Chat so I'm gonna learn more along the way.
## Contact

You can contact me on Discord. 
```
Seven#1101 - My Discord
```
There you can make suggestions or leave feedbacks for my projects. I'll read them all.

## License

For this project we used MIT License.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)



## Authors

- [@Antonio-Balea](https://github.com/Antonio-Balea)

