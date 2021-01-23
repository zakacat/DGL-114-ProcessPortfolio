# DGL-114 Process Portfolio
## <ins> Intro to App Development </ins>
### By Zak (zakacat) Toews

#### :octocat: Activity 0101:

>_"Find one example of a mobile app that has an interface that you consider 'good', and one example of a mobile app that has an interface that you consider 'poor' (or, if not poor, at least 'difficult'). Take some screenshots that highlight the best and worst of each app and provide a short description in your Process Portfolio justifying your choices."_

###### Good Interface - Currency Plus

<img src = ".git\img\CurrencyPlus1.jpg" width = "200">

<img src = ".git\img\CurrencyPlus2.jpg" width = "200">


- I like how this app always has the number input  widget open.
- This app is really straight-forward. Choose the currency that corresponds with the flag of the country from the drop down list. Click the text field and input the amount, the other currencies update in real time. There is no need to press any button to get the computation.
- Near the top, there is information for when the values of the currencies were last updated which is important info for a currency conversion app.

###### Bad (confusing) Interface - Facebook

<img src = ".git\img\Facebook.jpg" width = "200">

- I find the Facebook and the Facebook app have become more and more cluttered and confusing over the years as they are trying to adopt features that their competitors have.
- I have confused the "What's on your mind?" text field with search on several occasions. Maybe because an open text field near the top of an app is usually for something specific or search?
- I do not want to see this room feature and I don't know an easy way to get rid of it.
- I prefer how the story feature works in other apps, where either it is hidden on a different screen or it is collapsed to just the icon representation of the person without a preview of their story.
- The app could maybe benefit from a builder tool that could quickly rid the UI of elements that the user doesn't want?

#### :octocat: Activity 0102:

>_"Consider what it means for a mobile interface to be 'usable'. What types of things do you expect to find in an app that is considered 'intuitive'? Make a list of as many 'usable' and 'intuitive' elements as you can think of (Hint: Don't restrict yourself only to buttons and widgets!)"_

- Items having to do with orientation should be at the very top (Home, About Us, Search, Help, etc.) or sometimes at the very bottom.
- Intuitive apps are designed in such a way that usually the first attempt by the user to do something is the correct way to carry out that action.
- Number fields should automatically open a num-pad or calculator.
- Text fields should accept a large range of input or at least warn the user that their input is not acceptable.
- Phone apps especially should avoid clutter. The screens are too small and our thumbs are too big to deal with small text/buttons/widgets.
- Apps should load quickly or inform the user in some way that it is loading so the user doesn't think that the app is broken or that it is frozen.
- Apps should be easily closeable.
- Apps should ask for permissions, and they should also avoid using any unnecessary permissions.
- An app should be easier and quicker to use than its web counterpart.
- I think for almost all software that we are interacting with these days, that giving feedback should be really easy to do (I like how easy it is to give feedback on our course on ZyBooks). There could be a list kept in the back-end for users who tend to give appropriate feedback.
- Activities or screens should be focused on one task.

#### :octocat: Activity 0201:

>_"Choose a mobile app (Android or iOS) that you use frequently. For this activity you will identify features and permissions associated with the app, as defined in section 2.1 of the textbook. Make a list of all features in your chosen app (if you don't know for sure, but try to be complete - you can see a full list of Android features here - scroll to the bottom), and a list of all permissions. For permissions you can check your app permission settings (whether iOS or Android) typically in the Apps or Permissions Manager section of the OS settings."_

###### Chosen App - Adidas Run

**Feature** | **Example**
-------------|-------------
android.hardware.multitouch | This app can recognize several types of gestures including swipes for scrolling and pinch to zoom.
android.hardware.screen.portrait | This app is always displayed in portrait mode.
android.hardware.camera.any | This app is able to exercise either camera as desired to take a picture after an exercise routine. The photo can then be saved to the phone or shared in social media.
android.hardware.camera.flash | This app allows the use of flash when pictures are taken.
android.hardware.audio.output | The app normally doesn’t have any sounds but when you are in an exercise, the app can inform you audibly for increments of time or distance with a pre-recorded voice (my “Voice Coach” is still in Spanish).
android.hardware.type.watch | As this is a fitness app, it is compatible with a smartwatch (preferably an Adidas smart watch).
android.hardware.wifi | This app can use WiFi for any function that requires network connectivity.
android.hardware.location.gps | This app will use GPS apparently; however, I noticed when my SIM card was disconnected, my location tracking became too unreliable to be useful.

**Permission** | **Severity** | **Example**
----------------|--------------|-------------
Location | Potentially Dangerous | I solely use this app to track my km’s when running, so this is a necessary permission.
Microphone/ Record Audio | Potentially Dangerous | I am not sure why this app wants this permission. It is not required and I have it deselected.
Contacts | Potentially Dangerous | I am not too sure why the app needs my contacts, but some apps will generate friends or recommendations from the contact list. I also have this deselected.
Camera | Potentially Dangerous | This one makes sense as I use it sometimes to pair a photo with my workout.
Storage * | Potentially Dangerous| The app can alter my storage and store photos and workouts.

*As a note, the read/write storage permission is an almost mandatory permission for all apps and has only been enforced since API 19 ([Reference](https://developer.android.com/reference/android/Manifest.permission#READ_EXTERNAL_STORAGE)).

#### :octocat: Activity 0202:

>_"Choose a mobile app (Android or iOS) that you use frequently. Pick one screen in the app and identify elements of the Model, View and Controller in that screen. In other words, list out all View elements (i.e. everything you can see on screen), all Model elements (i.e. all data relevant to that screen) and all Controller elements (i.e. all the possible interactions on that screen that may modify the Model or View)."_

###### Chosen App - Voice Recorder

**View**

<img src = ".git\img\Screenshot_20210122-070301_Voice Recorder.jpg" width = "600">

* Primary color is Grey
* Secondary color is Black
* Text color is White

**Controller**

*Some of these points are speculation.

* Record/ Stop button starts or stops the recording of the audio file when button is pressed. Button alternates. It becomes a record button when the user opens the app or after a recording has been stopped. When a recording is taking place, the button becomes a stop button.

* All Text fields are adjusted accordingly for the user as the recording continues. Storage decreases while elapsed time and file size increase.

* Pause/ Play button pauses the current recording or plays the last recorded file when button is pressed. When the record button is pressed, the pause button appears on the right side, when the stop button is pressed, a play button appears on the left side.

* Navigation buttons switch screens accordingly and also display as a red button when the navigation button ¬matches the accompanying screen.

* Visualizer displays a live visual representation of the audio wave intensities being received (could be pseudo, but it is believable).

* Controller must call a new instance of a record file object every time the record button is pressed.
There are no extra preliminary input fields… so probably no parameters for the record file object… though I am not certain.

* Controller requests info (calls getter methods) from the model so it can update the text fields.

**Model**

*All these points are assumptions.

*I wrote this as a computation flow, not as a description of the class contents.

* A record file object is instantiated.

* Variables are instantiated for file size and duration of recording.

* A method is called that uses the microphone to listen.

* Duration and file size increments in real time.

* Empty storage value is retrieved from somewhere and updated against the current audio file size (As audio files are quite small, and my storage in quite large (to only 1 decimal place), I am not sure if this value is updated in real time or not, but I imagine it is).

* A stop button selection reported from controller will call a method to stop the recording.

*I suppose the file size, duration, and storage info could be handled in the controller and it might be easier to use a recording class from the library and only have to make the controller from scratch.

#### :octocat: Activity 0203:
*I understand that only two activities per week are necessary, but I would like to do three if I can when I have the time.

>_"Visit material.io and examine some aspects of Material Design. Scroll through the site and take a look at one page/article that interests you in more detail. Summarize what you learn from the article in your Process Portfolio."_"

The article that I chose was Text Fields ([Source](https://material.io/components/text-fields/android)). I chose the implementation section instead of the design section as that is what I am more concerned with. Although I know design is important for a polished, highly-usable app, I feel I should focus on how to use the feature first.

###### Summary of Text Fields Implementation

* Firstly, apparently, a dependency needs to be made.
* The API supports both label text and helper text in addition to the edit text and the use of both is recommended.
* You can set descriptions of icons and errors so that apps that read the screen can interpret what is being displayed. (I am thinking like apps designed for the visually impaired or maybe a translator).
* If you are using a Custom edit text, you can define accessibilities (I am not too certain what that means).
* You can add start and end icons into the text field. They can be strictly visual or they can increase functionality. The example is the hide/show password icon that can be selected to hide the text as the user types it into the text field.
* You can also create custom icons and use them. There are more directions on the website on how to modify the behaviour of the custom icon.
* You can add a character counter to the text field.
* You can add errors to the text field (which look to display in the helper text by default)
* You can add prefixes and suffixes to the text field.
* There are two types of text fields, filled and outlined
* You can also apply themes to the text fields.

*There is soooooo much useful information in here. I will definitely be back here, probably for the final assignment or maybe past that if I decide to continue with app building. 
