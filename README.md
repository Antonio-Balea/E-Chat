1. If you are planning on launching this AI in your cmd, you should use cd on your location with the intents and the .py file.
2. Here is a model for copy paste in intents.json:

 {       
	        "tag": "",
            "patterns": [
                ""
            ],
            "responses": [
                ""
			         ]
       }
       
3. Have in mind that if you add more training data (in intents.json), it will take longer to load it.
4. It doesn't have a lot of training data so it can't answer everything. If you want to answer with: "I don't know what are you asking.", edit the code like this:

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

Enjoy!
