Open ai can be used to create an api key just go on there website and get an api key.

a new open ai object can be created using new OpenAi()

the .chat.completions.create() can be used to get a message from open ai

you need to pass in an object with the model property corresponding to the model and a messages property with the value being an array

the array should contain a role property and a content property and at least 2 objects with this property the first role is system the second one is user and the content in the first one decides what the ai should do and the second content is the user prompt

the max_tokens property can be used to determine how many tokens to be used per output

the playground in open ai can be used to check what the outputs might be

the temperature property can be used to control predictability of the output default is 1 can range between 0 and 2

the examples can also be given in a prompt

the stop property can be used to stop an output stop:["word"] if the output were to include word it would stop right before rendering word "\n" could also be used to make it only one line paragraph

presence_penalty property is between -2 and 2 and as it increases it increases the likelihood of starting a new topic

frequency_penalty does the same with repeated phrases

fine tuning is basically a process in which data is sent to the ai model to give desired results. It is easier to do on the open ai website and get the model name and use that model name when setting up the model


openai.images.create({}) can be used to create images. the object takes in a model a prompt a size a n(number) style and reference property

If the reference is url the url it generates is only valid for an hour