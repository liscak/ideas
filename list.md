1. Use GPT-2, GPT-3, BERT or other Transformer based models to convert/translate natural language to scripting language in games. 
Explanation: you write(or generate) a game script(the logic) in english(or other language) and the transformer based model converts/translate the english text to code that the game will execute.
For example: "The animal moved to the left." would move the animal on screen by one block(or some other unit) to the left(on the screen or map, etc)  
TEXT --> CODE(javascript, luascript, python, etc.) --> Execution.
Text would be used as input for the transformer based model and the output from the model would be the game script and the game script would be executed by the game.
2. Use GPT-2, GPT-3, BERT or other Transformer based models to convert/translate code from one programming language to another programming language.
For example convert/translate Python code to equivalent Javascript code, where the output and side effects of functions are identical.
3. Use GPT-2, GPT-3, BERT or other Transformer based models to convert/translate programming language code to binary code(executable) and vice versa(binary code to programming language code)
4. AI RPG where you write or select your actions in english and the game randomly generates a floating point number to indicate the chance of success.  
The random number indicates if the action taken is succesfull or not and the game would alter the story accordingly.  
Text --> ACTION --> RANDOM NUMBER GENERATION --> STORY ALTERATION.  
The game would generate the story with a Transformer based model and present you some choices(generated) of action or you would write your own.
The game would then generate the random number indicating the success represented either in binary ((0, fail), (1, success)) integer/text or more detailed form(float in range between 0 and 1 where the number 1 could represent critical success and 0 critical or deadly failure, 0.5 could represent some form of success 
The sucess rate would be either in integer floating point or text form.  
There could be two ways to implement this:1. Append the random number in number or text form to the action taken and use that as input for the transformer based model and let the transformer generate the outcome. 2. Use the random number in a game system to compute the outcome. 

5. Use IGPT other Transformer based models to generate game images(game props, backgrounds) from the story (text) generated by the transformer based model.  
First, generate the story(text) with a GPT-2 or other Transformer based model.  
Second, use the the text(one or multiple sentences or the whole text) as input into IGPT.  
Third, let IGPT generate the Image.  
Fourth, use the Image as the main Image in the game Window or as a Background?  
Or one could just detect the entities in the story/text and use those(the names and descriptions) as input into IGPT
6. Can GPT-2 or other Transformer based models be used to generate a fake dataset?  
I tried to use GPT-2 with the following input:  
NAME:HENRI,AGE:32,LOCATION:GERMANY;NAME:JAMES,AGE:64,LOCATION:RUSSIA;  
Output from GPT-2:  
NAME:HENRI,AGE:32,LOCATION:GERMANY;NAME:JAMES,AGE:64,LOCATION:RUSSIA;NAME:GARY,AGE:80,LOCATION:FRANCE;  
It looks like GPT-2 can generate a sequence based on a pattern.  
Link: <https://huggingface.co/gpt2?text=NAME%3AHENRI%2CAGE%3A32%2CLOCATION%3AGERMANY%3BNAME%3AJAMES%2CAGE%3A64%2CLOCATION%3ARUSSIA%3B>  
7. Generate Animation Data with GPT-2, GPT-3, BERT or other Transformer based models?  
Use a english description of movement as input into the GPT-2, GPT-3, BERT or other Transformer based model and let it compute the Animation Data.  
Example:  
* Input:
"Move the characters hands up"  
The output would be the animation data(a point cloud, voxels, or some other format)
8. Use GPT-2 or other Transformer based models to generate a video sequence, either by using a single or multiple frames(represented in text form) as input or by using a sentence, description(of an object), or a whole document/story in text form as input.  
It could be possible using the Longformer transformer based model.  
9. Use GPT-2 or other Transformer based models to generate a list of entities(characters with descriptions and stats) for games.  
The system could generate characters with names, descriptions, stats, and more(like relationships of characters, attitudes, moods and more.)  
Input:  
NAME:SANDRA,WEAPONS:KNIFE,MOOD:SAD,STRENGTH:MEELE WEAPONS,WEAKNES:FIRE;
10. Use roberta large or other transformer model for token classfication to find entities in descriptions,stories,text and use those in game.  
NAME:SANDRA,WEAPONS:KNIFE,MOOD:SAD,STRENGTH:MEELE WEAPONS,WEAKNES:FIRE;NAME:JAMES,WEAPONS:SHOTGUN,MOOD:CHEERFUL,STRENGTH:SHORT RANGE WEAPONS,WEAKNES:ICE;  
Link: <https://huggingface.co/xlm-roberta-large-finetuned-conll03-german?text=NAME%3ASANDRA%2CWEAPONS%3AKNIFE%2CMOOD%3ASAD%2CSTRENGTH%3AMEELE+WEAPONS%2C+WEAKNES%3AFIRE%3BNAME%3AJAMES%2CWEAPONS%3ASHOTGUN%2CMOOD%3ACHEERFUL%2CSTRENGTH%3ASHORT+RANGE+WEAPONS%2C+WEAKNES%3AICE%3B>  
The game would know that the story is about those entities, could show them on screen(load/display the sprites,images of those entities) or generate new images,sprites of those entities with a GAN network or IGPT.  
If the token classification network(like roberta,electra, etc) detects entities in text(like in a sentece or multiple sentences of a story, the game would load the images(or sprites) of those(said) entities, like for an example show the entities(characters) side by side to simulate with the text in the middle of ath the bottom of the screen to simulate a dialog.
The token classification network could be use to detect the environment(location) described in the sentence,story,text and show an image of the location on screen(like game screen),
if the location/environment would not be avaiable in memory the system could use similarity search to search for a similar image or generate a new one with GAN or IGPT.
Example:  
Input: "It is the year 1946 in Germany, the city of ... is rebuild. Frank and Thomas are looking a new job."  the three dots could be any name of a city.  
Output(TAGS) could be: YEAR:1946; LOCATION: GERMANY,CITY; CHARACTERS: FRANK,THOMAS;  and the game would load a picture of a German city in the year 1946 on the game screen. It could show images of those characters if avaiable or generate new ones, etc.
11. Use GPT-2, GPT-3, BERT or other Transformer based models to convert/translate game scripts(like actions) to natural language.  
Example(input could be any programming/scripting language or DSL):  
Input: "ENEMY1 ATTACK WIZZARD, DAMAGE:64, WIZZARD HEALTH:100-64"  
Output: "The enemy attacked the wizzard with his dagger. The wizzard could not evade the attack and took 64 DMG, but he is still alife!"
The game(transformer) could infer from the script that the wizzard is still alife.  
12. Use GPT-2, GPT-3, BERT or other Transformer based models to generate ASCII art/graphics, enter the name or description of an object and let the transformer generate a ASCII text string representing the ASCII art.
13. Use a transformer based AutoEncoder for video compression?  
Transformer Encoder:  
Input: Few Frames in High Resolution  
Output: Embedding (low dimensional)  
Transformer Decoder:  
Input: Embedding (low dimensional)  
Output: Few Frames in High Resolution  
The question is should the input be preprocessed with and convolutional neural network(CNN)?  
14. Use a transformer based model for foto/video upscaling?  
15. Use a transformer based model for audio noise cancelling?  
16. Use GPT-2, GPT-3, BERT or other Transformer based models to generate levels/maps/worlds for games.  
The input would be a description of a place and the transformer would generate a design for a level.  
The output could be a list of names of entities and objects with their respective coordinates(positions) that would be used to generate the level on screen.  
If the game would be a ascii roguelike game, the output could be directly the level itself, every character from the output could represent a part of the level, one character would represent an enemy, another character would represent an item, and another one the game character, a wall, etc.  
If the game would be a 2D or 3D the model output could represent the postion of entities and objects on the level.  
For example(in a 2D game) if the input for the transformer would be: "beach" and the level would be divided into tiles then the output could be: SANDTILE[X=0, Y=10], SEATILE[X=10, Y=30], ROCKTILE[X=20, Y=50] where each tile represents an object or entity and the values 'x' and 'y' the coordinates.  
A 3D game entity or object would have 3 coordinates -> x, y and z.  
The transformer could generate a minecraft style map, the output of the transformer would be the names and positions of entities and objects represented by voxels(or even by point clouds).  
17. Use GPT-2, GPT-3, BERT or other Transformer based models to detect events(actions), objects and entities in sentences, story, text and then try to call the event(name) as a function first by looking for the function in a list/array of functions or in a dictionary(hash table) of functions, if the function is found, then call it with the object and entities names as parameters/arguments.  
First detect the event(action), that is the function name. Then detect the objects and entities, now we  have the names of objects and entities. Call the function with the names of objects and entities as arguments/parameters.
Event(event name) ==> function name
Objects/Entities ==> function parameters.  
event(object_name, ..., entity_name, ...)  
18. Use Neural Video Compression for Game Streaming/Cloud Gaming. Either use and Auto-Encoder convolutional neural network to compress the stream and send out embeddings.  
Other ideas for Cloud Gaming/Game Stream video compression:  
Train convolutional autoencoder that takes as input an frame or frames and the output would be the original frame, frames or the same frame, frames in higher resolution. The server would use the encoder to encode the game stream frame or frames into an embedding in realtime and the decoder(from the convolutional autoencoder) on the client device would decode the embedding and create the frame, frames and the software would display the on the screen.  
Another way to do this would be to use a second network for meta learning the weights of the autoencoder or of a superresolution convolutional neural network and send those weights to the client device and the client would load the model with those weights.  
Game Stream frame,frames --> MetaLearning Convolutional Neural Network   
The metalearning CNN (CNN = convolutional neural network) would take a frame or multiple frames as input and the output would be the weights of a CNN that takes as input an frame, frames in lower resolution and creates a frame, frames in higher resolution(that would be a superresolution network) or the CNN would take as input an embedding and recreate the frame, frames from the embedding.  The server would use the metalerning network to create the weights from the game stream frame,frames and send the weights and low resolution frame,frames(created from the original frame, frames) to the client device. The client devices woudl load the CNN model withs those weights and the CNN would take as input the low resolution frame,frames and the low resolution frame,frames would be transformed by the CNN into higher resolution frames,frames.  
19. All transformer based models here mentioned would be trained either directly(with input output pairs) or in a one-shot or few-shot manner: by giving it examples as part of the input. (like openai mentioned in: https://arxiv.org/abs/2005.14165)  
20. Use continuous signed distance functions/ DeepSDF for game textures.  
Train an multilayer  perceptron(MLP) that outputs a RGB value for a (x,y) pixel.  
The input are the x and y coordiantes represented as floating point values between 0 and 1, both inclusive.
The output is the RGB value of the pixel, so 3 channels, an array of 3(three) values.
The game texture is compressed/represented as the weights of the neural network.  
The game texture is compressed(learned) beforehand.  
The original game texture is an image.  
For every pixel in the texture(or image) we get its coordinates and RGB value, we normalize the coordinate(x and y pair) as float values between 0 an 1, use  them as the neural network input(feed them into the network) and the output are is RGB value of the pixel at that coordinate. So the output is a array of 3 values (because we have 3 channels): Red Green and Blue.  The ground truth value(the pixel value of the original texture) is used in the optimizer to compute the mean squared error(or other type of erro signal, like MSA, etc).  After training and overfiting the neural network with the one texture represented as the dataset we recover the texture(or just concrete pixels of the texture) by looping over the coordinates(all of the x and y pairs).  The weights of the trained/overfited network represent on texture.  
The texture will be recovered when the game loads the texture.  
21. One-Shot SDF learing mesh geometry?  
22. Use NN trained with SDF for long term storage, use neural radiance field to learn an object and use that network(that learned the object or enironment) as long term memory.  
23. Use CNN on neural radiance field generated volumes or images for find object or for semantic segmentation.  
24. Saving a video/animation into a MLP(multi layer perceptron) neural network, where the input is the x and y coordinate in the floating point form(between 0 and 1 inclusive) for one pixel and a floating point value representing the continuous timestep/time, that is 0 represents the start(first frame) of the video/animation, 0.25 would represent the frame at the one fourth timestep/time of the full length of the video/animation ,0.5 the middle(frame) of the video/animation and 1 the end(last frame) of the vide/animation, other values represent their respective timesteps. And the output would be the one pixel RGB value(3 values: red green and blue all normalized and represented as floating point values between 0 and 1 both inclusive) at the queried timestep/time. This could be used to compress video files, video streams, game streams(game streaming), etc.  
Example: A video(file) would be 50 minutes long, that would be 3000 seconds(50 * 60), the first frame would be at time position 0( zero seconds) and represented as 0 float,  
the one fourth time position of the whole video/animation would be 750 seconds(3000 * 0.25) represented as 0.25 float.  
25. Use GPT-2, GPT-3, BERT or other Transformer based models to generate textures, shaders or meshes.  
A transformer model would be used to generate mesh data, or texture data or a shader.  
The input would be a description of the texture, shader or mesh and the output would be either the data: either the texture, shader or mesh.  
In games(ingame) a user would write a description of an objest/mesh/texture/shader and the game would send the query/text-string to an Transformer(or an API/transformer running on a server), the query would consist of either just the description or of two or more examples(description and data pairs) and the description the user wrote. The server/transformer would return the output/data(texture,shader or mesh). The game would load and display the data(texture,shader or mesh). So the system would generate new data based on the descriptions on the fly.  
26. A social/party online game where multiple people need to complete objectives in the game world by describing/naming objects that would spawn into the game world and could be used by the users/players to complete the objectives in creative ways. The descriptions/names of the objects would be send to a Transformer based model and that model would generate the object(game model[either a 2D sprite, 3D object with mesh, etc.]) data. The query could consist of either the description/name of the object or of two or more examples(description/name and data pairs) and the description/name itself. The data would be loaded into the game and the game would display the object. The object would have attached code or properties generated by the Transformer model that make the object interactive.  
27. A social/party online game where multiple people need to complete objectives in the game world by describing/naming objects word by word that would spawn into the game world and could be used by the users to complete the objectives in creative ways.  
All users/players would describe one(single) object to be spawned, each user would write one(single) word or each user would write a part of the description or of the name and all parts would be combined together as one(final) description or name of an object.
The descriptions/names of the objects would be send to a Transformer based model and that model would generate the object(game model[either a 2D sprite, 3D object with mesh, etc.]) data. The query could consist of either the description/name of the object or of two or more examples(description/name and data pairs) and the description/name itself. The data would be loaded into the game and the game would display the object. The object would have attached code or properties generated by the Transformer model that make the object interactive.  
28. A social/party online game where multiple people(the first group) need to gues what object was spawned/displayed in the game world by the other players(second group).  The second group describes/names objects word by word that would be spawn into the game world and the first group needs to gues the name of the object/objects that the second grounp spawned.  
All second group would describe one(single) object to be spawned, each user(of the second group) would write one(single) word or each user(of the second group) would write a part of the description or of the name and all parts would be combined together as one(final) description or name of an object.
The descriptions/names of the objects would be send to a Transformer based model and that model would generate the object(game model[either a 2D sprite, 3D object with mesh, etc.]) data. The query could consist of either the description/name of the object or of two or more examples(description/name and data pairs) and the description/name itself. The data would be loaded into the game and the game would display the object. The object would have attached code or properties generated by the Transformer model that make the object interactive.  
29. Use OpenNARS(https://github.com/opennars/opennars) with GPT-3(or a newer GPT version), where GPT-3 would be used to convert/translate natural language to Narsese and Narsese to natural language.(A parser??) Provide GPT-3 with english to Narsese pairs and Narsese to english pairs for few shot learning(learning without training,[https://arxiv.org/abs/2005.14165]). For english to Narsese: The input for GPT-3 would be english-Narsese pairs and the query in english and GPT-3 would output Narsese. And for Narsese to english the input for GPT-3 would be Narsese-english pairs and the query in Narsese and GPT-3 would output english(text).  
Example Narsese to english(few-shot version), ENGLISH and NARSESE represent tags or special tokens:
  (first the examples for few-shot learning, 2 or more pairs)  
  ENGLISH:Dog is a type of animal.;NARSESE:<dog --> animal>.;  
  ENGLISH:Cat is a type of animal.;NARSESE:<cat --> animal>.;  
  ENGLISH:Bear is a type of animal.;NARSESE:<bear --> animal>.;  
  (now the user input in the form: "ENGLISH:user-input", here the user input is: "Horse is a type of animal")  
  ENGLISH:Horse is a type of animal.;  
  (and then GPT3/transformer would output:)  
  NARSESE:<horse --> animal>.;
    
  The full query could look like this:  
  ENGLISH:Dog is a type of animal.;NARSESE:<dog --> animal>.;ENGLISH:Cat is a type of animal.;NARSESE:<cat --> animal>.;ENGLISH:Bear is a type of animal.;NARSESE:<bear --> animal>.;ENGLISH:Horse is a type of animal.;  
  And the output:  
  NARSESE:<horse --> animal>.;  
  (Or train a transformer model directly on Narsese-english pairs or english-Narsese pairs where the first thing is the input and the second is the desired output)  
30. Differentiable NARS/OpenNARS. It could be written in python with the pytorch library and would/could be GPU/TPU accelerated. It could be trained(with backpropagation/autodiff) to learn new rules. The differentiable NARS/OpenNARS could be combined with other models(neural networks) to build an end to end trainable model/system.  
31. Use DLSS(or similar technology) with "GeForce Now"(or other cloud gaming service) to upscale the game stream, it would lower the bandwidth requirements(and even the latency). Every game would have its own DLSS profile. The gaming service would stream the game in low resolution to the client, the client would load the correct DLSS profile and would use DLSS to upscale the game stream to a higher resolution. 
32. AI video file upscaler:
* the network/model would use similarity search to search over the whole video file for reference images that would be used as input
* the network/model would use multiple previous frames as input
* the network/model would output an upscaled frame that would be downsampled and the downsampled frame/image would be used as input for the loss function
* the network/model would use as loss the MSE or similar loss function.  
33. Realtime AI video upscaler:
* the network/model would use multiple previous frames as input
* the network/model would use motion vectors/optical flow as input
* the network/model would have a small buffer(of probably 1000 frames/images) of previous(older) frames/images for use as reference and would use similarity search to search for reference frames/images inside the buffer
* the network/model would output an upscaled frame that would be downsampled and the downsampled frame/image would be used as input for the loss function
* the network/model would use as loss the MSE or similar loss function.  
34. AI video upscaler that would use continous signed distance functions
35. AI video upscaler that would use the floating point coordinates(from Cartesian coordinate system) of a pixel as input?  
36. Realtime AI game upscaler:
* the network/model would use similarity search to search over all textures to be used as reference(the model would find one or more textures and use them as input), input for the model. The textures could have embedded metadata. The model could search for the right textures by learning to compare them opticaly(as images) and/or by the name(search by name/word embedding).  
Another way would be to find/classify the textures visible on the current frame and use the found/recognized textures as input for the model. So the model would recognize the used textures(textures visible on frame/frames), load the textures(in original/high resolution) and use them as input for the upscaler part of the model.
Another way would be to load the textures used in the current frame/scene direcly from the game engine.
* the network/model would use multiple previous frames as input
* the network/model would use motion vectors/optical flow as input
* the network/model would use depth data(if available) as input
* the network/model would output an upscaled frame that would be downsampled and the downsampled frame/image would be used as input for the loss function  
37. When users write in a natural language(like english) to NARS with GPT/transformer based parser(see 29.), let the users rate the quality of the output(for example english-narsese pairs) with numbers(0 to 1 float or 0 to 100 integer), store the input-output pair with the rating(for example into a database) and if the input-output pair gets a good enough rating use it for learning(few-shot learning) or training(train the whole transformer model on  those pairs)[the pairs would be used as part of the training dataset.]  
  The low/bad quality output could be used for analytics(where to improve the model, etc).  
38. Append for 29. and 37.
  If the used transformer would be a Longformer, use as many examples as possible for few-shot learning, the query would consist mostly out of example pairs(english-narse, narse-english)  
39. Append for 29. and 37.  
  For the English to Narsese(and backward) parser/translator: we could store the example pairs into a file and use the RetriBert(transformer model) as parser/translator,
  RetriBert would search for the most similar examples in the file and use them as reference/part of input for itself(use them as part of it's input).  
  Instead of RetriBert we could use a Retrieval-augmented generation model like "RAG".
40. A trasnformer based web scraper?  
41. Make a big dataset of narsese-english and english-narsese pairs and use them to train the parser/translator(see 29.)  
42. Use Resolution Dependant GAN Interpolation from https://arxiv.org/pdf/2010.05334.pdf to colorize old images and videos.  
  The first GAN would be trained to generate colored images.  
  The second GAN would be trained to generate black-white or gray images or old looking images.  
  And the weights would be swapped as in Resolution Dependant GAN Interpolation from https://arxiv.org/pdf/2010.05334.pdf  
43. Use Resolution Dependant GAN Interpolation from https://arxiv.org/pdf/2010.05334.pdf to change the age of people on photos and videos.
  This example would be to turn young people old on photos/images.
  The faces of young people would look old.
  The first GAN would be trained to generate images(faces) of young people.  
  The second GAN would be trained to generate images(faces) of old people.  
  And the weights would be swapped as in Resolution Dependant GAN Interpolation from https://arxiv.org/pdf/2010.05334.pdf  
44. Using T5 transformer to translate English to Narsese.  
  Example1:  
  Input:  
    translate English to Narsese: Wolf is a type of animal.  
  Output:  
  <wolf --> animal>.  
  Example2:  
  Input:  
    translate English to Narsese: Is wolf a type of animal?  
  Output:  
  <wolf --> animal>?  
  The model could translate any natural language string to narsese.(any language to narsese)  
  For example:  
  Input:  
    translate German to Narsese: Der Wolf ist grau.  
  Output:  
    <wolf --> [grau]>.  
45. Use a overfited transformer to compress enwik9 to maybe win the hutter prize.  
      Overfit a transformer model on the enwiki9 [dataset]  
46. AI image/video upscaling with a transformer model?  
47. Use a transformer to compress text or binary file.  
      INPUT:  
        ID: 12345  
      OUTPUT:  
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim.
      
      ID is a number representing the part/section that is compressed
      OUTPUT represents the text or binary numbers at that ID or section.
      
      Train the transformer until it overfits.  
      
48. Train and use a transformer based model to predict the output of a function or source code without executing it.  
Use source code as input for the transformer and the output from the transformer model would be the result/output of the source code or function as if it was executed.  
49. A transformer based Transpiller or Compiller that would take source code(text string) a input and output a binary string.  
50. A trasformer based model that would transpile/translate binart code to  binary code from one architecture to another like: from x64 to ARM64. Translate/convert code to code.  
The input would be a binary code(string) of a part or of the whole binary executable(of one architecture) and the output of the transformer would be the binary code of the target architecture.  
The transformer would be trained on input-output pairs, the first part of the pair would be the binary code of the input architecure and the second part would be the binary code of the target architecture.  
The T5 transformer model could be used:  
Example:  
  Input:  
    Translate x64 to ARM64: {here would be the x64 binary code }
    
  Output:
    {here would be the ARM64 binary code}
    
 Or the transformer model could translate binary code(of one architecture) to assembly code(of the targert architecture).  
 
 51.A transformer model that would translate assembly code of one architecture to assembly code of a target architecture.(from x64 assembly to AMR assembly, x64 assembly to RICS, etc.)  
 A T5 transformer model could be used:  
 Example:  
 Input:  
    "Translate x64 to ARM64: {here would be the x64 assembly code }"  
 Output:  
    "{here would be the ARM64 assembly code}"  
It would be trained on input-output pairs. The input would be the assembly code of the input architecture and output would be the assembly code of the target architecture.  

52. Compress textures into a transformer based model.  
A T5 transformer model could be trained to output textures when using input ids.  
The output could be a base64 string, binary string or RGB integer values in a text string.
Example:  
Input:  
  ID: 1545464  
Output(base64 image):
  iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAIAAAACUFjqAAAALElEQVR4nGJRS/RhQALV06SQuUwMeAFNpVmSHKOQ+VcDEulmNwFpQAAAAP//0JIEmh25QkkAAAAASUVORK5CYII=]

Output(RGB values):
  255,120,0,123,65,11
 
 The input would be a integer number/value in the form: "ID: integer-number-here" corresponding to the index number of the saved/learned image.
 Exaple: "ID: 12312412"
  
53. A crowdsourced app to stop waiting in lines, waiting in restaurants, theaters, to stop waiting everywhere where a crowd of people is.
It could be webapp or mobile app, after the user would start the app it would detect the user postion with satelites(GPS/GLONASS),
the app would show the neares businesses(pub, theater, etc.), spots, points of inteterest and the user could choose between them or enter/register a new point/spot.
After selecting the point/location/business the user would input the number of people waiting (like waiting in line, or people in crowd) and the time the user is waiting.
After the user confirms the input would send to the server.
The server would calculate the number of people/or crowds and show them on a google street or openstreet map. 
On the map the number of people or crowds would be shown as colored hotspots and after clicking on them the average waiting time would be shown and a history how bussy the spot is.
The server could analyse the data and predict the future waiting times.  
54. Neural network for video colorization where the input is a batch of frames and multiple reference images (not from the same video) found with similarity search( or similarity search and extraction network.)  
55. Compressing a image with a Neural Network by trying to learn rectangular parts of an image.  
The input of the neural network is the location/coordinates of the rectangle/window representing a part of the image. The input is four(4) floating point values X1,Y1,X2,Y2,  normalized in range from -1 to 1, they represent the location/coordinates of a rectangle/window(a part) inside the image. First we divide/partition the image into quadrants/rectangles/windows and then we get the integer coordinates of the quadrant/rectangle/window X1, Y1, X2, Y2 and normalize them so they are in range -1 to 1, by applying the following functions/formulas/formulae: for x values f(X) = (X/X_max * 2) -1 and for y values f(Y) = ((Y/Y_max) * 2) - 1 , where X_max represent the maximum value of the X axis of the image and the Y_max represent the maximum value of the Y axis of the image.
The output of the neural network is a rectangle/window array of pixel values representing the pixels of the image inside the rectangle at the input location.  
One neural network would learn one image.  
The weights of the neural network would represent the (compressed) image.  The image would be decompressed by loading the weights into the neural network and recovering all parts/rectangles/windows of the image and concatenating them together.  
56. Use a transformer model to convert EEG spectograms to images(frames)/videos.  
57. Combine neural dictionary with similarity search(for speedup) and when finding the most similar keys, return/use them in the neural dictionary computation.
Could even save stats/statistics/metadata on how many times the key/value was accesed/modified.
Have some guarantee that unused keys are probably not important enough/or not learned/initialized,,,,,
Use that meta data logging in classification tasks, where each key is a class and when you find/search for a key/class that hasn't been used or learned before you can tell the user that it's either not in memory, or learned or that the value is random/uninitialized
Could be used as uncertainty value.the count of how many times it was learned/accesed,
How the network is surprised, (suprised/uncertain like in Random Network Distillation)
When you access a key the first time then The network is surprised a the uncertainty is 100% and the value can't be used in classification or further processing without training (or pretraining).
If the key was accesed multiple times or trained/learned the the value cant be used as probability in classification or other processing.  
58. One way to have unlimited memory would be to use similarity search over all examples(the whole dataset). Every example tensor would be a key and the input tensor would be a query.That is have a input tensor/queyry and similarity search over examples/keys(the whole dataset) and either return the example/key or have values(tensors that are trainable or nontrainable parameters) associated to the examples/keys. For example in Reinforcement Learning a unique key/example could be associated with a action(one or multidimensional tensor, the input state/query would be compared with all keys/examples and the model would return the action(tensor) associated to the most similar key.   
Maybe it would be a good idea to group together multiple queries(tensors)/examples representing one class and learn one super key(parameter) or key-value pair representing that particular class.
Again: have a bunch of examples(tensors like images,states, etc.) of one class, create a learnable tensor/parameter as Key and train the key/paramter to be more(or most) similar to the examples of the class, that is compare all examples with the Key, compute the absolute difference(or mean squared error or use other loss or distance function) between the key and each example, sum up the differences/errors and use that as loss signal, compute the gradients and update the Key(trainable parameter) to lower the loss. The Key will be more similar to the examples and would represent that particular class. Then save the Key inside a list(or tensor) with other Keys, where every Key then represents a single class, when classifying an image/state(or other tensor) use the input as a query, similarity search the list with the query, that is compare all Keys with the query and depending on the task either return the Key that is most similar to the query or just return the index of the Key that is most similar to the query.(the index would represent that particular class).
59. A general way to upscale games with machine learning would be to let developers have access to a upscaling neural network(convolutional, transformer based or etc.) that would take as input the following things: the current frame, the last few frames the game displayed, scene depth data/information and high(or full) resolution versions of the textures used in the current frame(Game would use low resolution textures in the current frame and input/feed high resolution versions of the textures into the neural netwok/model).  
The game engine would provide all necesary thing, the most important ones are the last few frames and high resolution versions of the textures used in the current frame.  
Providing textures(texture data in high resolution) would prevent the network from using up its capacity to learn the high resolution details, it could be thought as a general way to upscale the game frame.  
The neural network(or model) would use similarity-search/retrieval and attention to retrieve the data from the most relevant texture from all as input provided textures.  
60. Break up an image(with a known class) into many smaller tiles(each tile would be shifted from the previous tile by a certain amount of pixels(defined by the stride value.)  
  Save every tile into the faiss index(or list) and every tiles class into a list or database.  
  Repeat this for every image in a dataset.  
  When classifying an image break up the image into many smaller tiles(where every tile is shifted from the previous).  
  Take the tile first tile from the image and similarity search for the most similar tile in the faiss index.  When the most similar tile is found save the (found) tiles known class into a list.(tldr. we will classify every tile of the image).
  Repeat for every tile in the image(until the last tile is classified).
  We ge an array/list of regions which have a class.(a list(or image) where every region is classified).  
  We can now tell to which class the whole image belongs(by looking at the most prevalent class in the list) or which part of the image belongs to a certain class.(or multiple classes if they overlap).  
70. Speed up a trained neural network/MLP(multi layer perceptron) by replacing every linear/dense layer with similarity search from the faiss library.  
Take one layer, make a new pytorch module, create a faiss index object, copy the weights from the old layer into the faiss index object. Write a new forward function that uses similarity searches for the most similar tensor/array/neuron in the faiss index object, the similarity search returns the distance between the input/query and saved tensors/arrays/neurons and the index value/position of the found(most similar) tensor/array.
Get 1 or more distance values and correspoding index values. Create a new array/tensor filled with zeros. Replace zeros with distance values of the found tensors at the correct index and return/feed the array/tensor into the next layer.
EXAMPLE:  When we have 4 arrays/tensors saved in the faiss index object and the similarity search returns the third tensor(at index 2) from the faiss index object with a distance value of 0.99.  
  We create a new array filled with zeros of length 4. [0,0,0,0] and replace the third value(at index 2) with the distance value 0.99, like this: [0,0, 0.99, 0].  
  We then feed the array [0,0, 0.99, 0] into the next layer.
