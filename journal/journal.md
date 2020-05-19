# 1701QCA Final project journal: *Insert your name here*

<!--- As for other assessments, fill out the following journal sections with information relevant to your project. --->

<!--- Markdown reference: https://guides.github.com/features/mastering-markdown/ --->

## Related projects ##
<!--- Find about 6 related projects to the project you choose. A project might be related through  function, technology, materials, fabrication, concept, or code. Don't forget to place an image of the related project in the appropriate folder and insert the filename in the appropriate places below. Copy the markdown block of code below for each project you are showing. --->

### *Insert name of related project here* ###

<!--- Modify code to insert image of related project below --->
![Image](missingimage.png)

<!--- Fill out name and link to related project in the code below. --->
[Name of related project](https://[URL of related project])

<!--- Include information about why this project is related to yours. --->

<!--- Repeat code above for a total of 6 related projects --->

## Other research ##
<!--- Include here any other relevant research you have done. This might include identifying readings, tutorials, videos, technical documents, or other resources that have been helpful. For each particular source, add a comment or two about why it is relevant or what you have taken from it. You should include a reference or link to each of these resources. --->

## Conceptual development ##

### Design intent ###
<!--- Include your design intent here. It should be about a 10 word phrase/sentence. --->
An interesting device that uses light detection to alert the user when it gets dark.

### Design ideation ###
<!--- Document your ideation process. This will include the design concepts presented for assessment 2. You can copy and paste that information here. --->

### Final design concept ###
<!--- This should be a description of your concept including its context, motivation, or other relevant information you used to decide on this concept. --->

### Interaction flowchart ###
<!--- Include an interaction flowchart of the interaction process in your project. Make sure you think about all the stages of interaction step-by-step. Also make sure that you consider actions a user might take that aren't what you intend in an ideal use case. Insert an image of it below. It might just be a photo of a hand-drawn sketch, not a carefully drawn digital diagram. It just needs to be legible. --->

![Image](missingimage.png)

## Process documentation ##
<!--- In this section, include text and images (and potentially links to video) that represent the development of your project including sources you've found (URLs and written references), choices you've made, sketches you've done, iterations completed, materials you've investigated, and code samples. Use the markdown reference for help in formatting the material.

This should have quite a lot of information! It will likely include most of the process documentation from assessment 2 which can be copied and pasted here.

Use subheadings to structure this information. See https://guides.github.com/features/mastering-markdown/ for details of how to insert subheadings.

There will likely by a dozen or so images of the project under construction. The images should help explain why you've made the choices you've made as well as what you have done. --->

## Final code ##

<!--- Include here screenshots of the final code you used in the project if it is done with block coding. If you have used javascript, micropython, C, or other code, include it as text formatted as code using a series of three backticks ` before and after the code block. See https://guides.github.com/features/mastering-markdown/ for more information about that formatting. --->

```javascript
let light = 0;
let lightThreshold = 20;
pins.analogSetPitchPin(AnalogPin.P2);

basic.forever(function () {
    checkLight();
})

function checkLight() {
    light = pins.analogReadPin(AnalogPin.P1)
    //if light level too dark play tone and turn LED on
    if (light < lightThreshold) {
        pins.digitalWritePin(DigitalPin.P0, 1);
        music.playTone(1200, 1000);
    } else {
        //otherwise turn led off
        pins.digitalWritePin(DigitalPin.P0, 0);
        return;
    }
}
```

## Design process discussion ##
<!--- Discuss your process used in this project, particularly with reference to aspects of the Double Diamond design methodology or other relevant design process. --->


## Reflection ##

<!--- Describe the parts of your project you felt were most successful and the parts that could have done with improvement, whether in terms of outcome, process, or understanding.

What techniques, approaches, skills, or information did you find useful from other sources (such as the related projects you identified earlier)?

What parts of your project do you feel are novel? This is IMPORTANT to help justify a key component of the assessment rubric.

What might be an interesting extension of this project? In what other contexts might this project be used? --->

The construction of the final model could definitely be of a higher standard but due to limited funds and resources the true concept of the project was not acheived. Ideally I would have used a 3D printing or metal CNC machining service to construct the parts out of a more sturdy, reliable, and aesthetic material. This would have saved time and stress by reducing manual labor and physical error, giving me more time to work on the functionality of the electronics. However the time spent working on the physical construction drew away from the overall effectiveness of the final product. 

Prior knowledge and assistance from the similary projects identified earlier allowed me to provide efficient and readable code to the microbit, increasing the level of usability and reasuability. The program is simple yet allows for the novel aspects of the device, such as its pseudo-personality to shine through in a performance optimised way.

Extending this product could turn it into a fully featured advanced alarm clock system that uses artificial intelligence to simulate a personality. This could be well marketed at children, especially those that have difficulty making friends, as the clock could provide some companionship. With more advanced technology like direction control and collision detection, the robot could move freely around the room performing tasks and holding conversations with the user. Conversation would not be an overly complicated feature to implement as chatbots have been in development [since the early 1960s](http://psych.fullerton.edu/mbirnbaum/psych101/Eliza.htm) and have only advanced in complexity and efficiency since then.

The device gains its novel aspect from its seemingly behavioural nature. When the ambient light in a room is too dark it screams, reminding the device's user to break away from common distractions that run into night when commitments and important tasks need to be fulfilled such as feeding pets, eating, and sleeping. The alarm system, meant to simulate screaming and distress from the robot, grabs the attention from the user and reminds them of the current time. This product would appeal mostly to gamers and people in the technology field, that already have an affinity for robots and technology, that have hobbies and occupations that often occupy them into the evening, letting them forget what time it actually is.  
