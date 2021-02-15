# DGL-114 Process Portfolio
## <ins> Intro to App Development </ins>
### By Zak (zakacat) Toews

### :octocat: Activity 0101:

>_"Find one example of a mobile app that has an interface that you consider 'good', and one example of a mobile app that has an interface that you consider 'poor' (or, if not poor, at least 'difficult'). Take some screenshots that highlight the best and worst of each app and provide a short description in your Process Portfolio justifying your choices."_

###### Good Interface - Currency Plus

<img src = "img\CurrencyPlus1.jpg" width = "200">

<img src = "img\CurrencyPlus2.jpg" width = "200">


- I like how this app always has the number input  widget open.
- This app is really straight-forward. Choose the currency that corresponds with the flag of the country from the drop down list. Click the text field and input the amount, the other currencies update in real time. There is no need to press any button to get the computation.
- Near the top, there is information for when the values of the currencies were last updated which is important info for a currency conversion app.

###### Bad (confusing) Interface - Facebook

<img src = "img\Facebook.jpg" width = "200">

- I find the Facebook and the Facebook app have become more and more cluttered and confusing over the years as they are trying to adopt features that their competitors have.
- I have confused the "What's on your mind?" text field with search on several occasions. Maybe because an open text field near the top of an app is usually for something specific or search?
- I do not want to see this room feature and I don't know an easy way to get rid of it.
- I prefer how the story feature works in other apps, where either it is hidden on a different screen or it is collapsed to just the icon representation of the person without a preview of their story.
- The app could maybe benefit from a builder tool that could quickly rid the UI of elements that the user doesn't want?

### :octocat: Activity 0102:

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

### :octocat: Activity 0201:

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

### :octocat: Activity 0202:

>_"Choose a mobile app (Android or iOS) that you use frequently. Pick one screen in the app and identify elements of the Model, View and Controller in that screen. In other words, list out all View elements (i.e. everything you can see on screen), all Model elements (i.e. all data relevant to that screen) and all Controller elements (i.e. all the possible interactions on that screen that may modify the Model or View)."_

###### Chosen App - Voice Recorder

**View**

<img src = "img\Screenshot_20210122-070301_Voice Recorder.jpg" width = "600">

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

### :octocat: Activity 0203:
*I understand that only two activities per week are necessary, but I would like to do three if I can when I have the time.

>_"Visit material.io and examine some aspects of Material Design. Scroll through the site and take a look at one page/article that interests you in more detail. Summarize what you learn from the article in your Process Portfolio."_

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

### :octocat: Activity 0301:

>_"Choose a mobile app (Android or iOS) that you use frequently. Do your best to identify all the activities (or 'screens') in the app and write them down in your Process Portfolio. See if you can come up with some meaningful way to categorize all screens. (Note that some screens in some apps may have tabs and menus, etc. I'm looking here just for the screens themselves - so any time there is a clear full screen change in the app. Additionally, note that in iOS we do not refer to these as 'activities', but more commonly as 'views'. For the purposes of this activity the distinction is not too important)."_

###### Chosen App - Adidas Run

<img src = "img\AdidasMainActivity.jpg" width = "200">

###### Activity

The main activity is called Activity and it shows that it is selected at the bottom on the navigation bar. This activity includes a simple set-up to start recording your work out. It also displays information about the work like duration and GPS location.

<img src = "img\AdidasMusic.jpg" width = "200">

###### Music & Story Running

Clicking the music icon brings up an activity to modify settings related to music that you can listen to while you workout.

<img src = "img\AdidasSettings.jpg" width = "200">

###### Activity Setup (General Settings)

Clicking the sprocket icon (as usual) brings up the general settings activity. This is where you can change the activity type, imperial to metric, voice coach, and many other settings.

<img src = "img\AdidasCommunity.jpg" width = "200">

###### Community

Clicking the community button in the navigation bar opens the activity for interacting with the social media aspects of the app. There is also and option to connect with Facebook friends which might open up a certain activity in the Facebook app.

<img src = "img\AdidasNewsFeed.jpg" width = "200">

###### News Feed

Clicking the news feed button in the navigation bar opens an Instagram-like post scroller for your activities and activities of friends or people you follow.

<img src = "img\AdidasProgress.jpg" width = "200">

###### Progress

Clicking the progress button in the navigation bar opens the activity for goal setting and stats.

<img src = "img\AdidasProfile.jpg" width = "200">

###### Profile

Clicking the profile button in the navigation bar opens the activity for adjusting the information in your profile and image.

###### Re-Categorization

If I were to generally Categorize these, I would separate them into 2 sections of settings (or customizability) and function. It could be maybe 3 categories as settings, function, and social media. I think this might be more appropriate as the main function of this app is to record work outs, but a secondary function is to be able to share it.

### :octocat: Activity 0302:

>_"Choose a mobile app (Android or iOS) that you use frequently and consider some of the more common Android event types are discussed in chapter 3.1 of the textbook. Which of these events does your app use? List a few different instances for each event in your app. Can you think of other events that your app might use that are not discussed in chapter 3.1?"_

###### Chosen App - Adidas Run

*Events used :*

onClick()
* this app uses the click to navigate thru almost the whole app

onLongClick()
* long clicking on the output values for the exercise allow the user to customize which information is displayed.

onTouch()
* After the GPS is selected and expanded to take up the whole screen, the user can use the pinch gesture to zoom in or out of the map



### :octocat: Activity 0303:

>_"After reading chapter 3.5 - Table, Grid and Frame Layouts visit material.io and do a search for one of 'table', 'grid' or 'frame'. Choose one of the articles in the search results that most closely relate to what you learned about tables, grids or frames from chapter 3.5 and read through it. Summarize what you've learned in your Process Portfolio."_

I chose the article about spacing methods ([Source](https://material.io/design/layout/spacing-methods.html)). Hopefully, this will explain a bit about what the jargon represents and how spacing affects the display on different devices.

* All components align to a 8dp square baseline grid
* Icons, type, and some elements within a component align with a 4dp grid.
* Type (Text) aligns to a 4dp baseline grid, but this can easily be overridden if the type is within
any components
* Spacing methods
	* Padding = the space between elements in a component
		- measured in increments of 4dp or 8dp
		- measured vertically and horizontally
		- does not need to span the whole height of the layout
	* Dimensions = describe the width and height of a component
		- Some components only have a height dimension as they are designed to fit the width of a view port.
		- Component dimensions tend to follow the 8dp grid baseline
	* Alignments = the placement of elements in a component
		- Keylines are established when elements are placed out of the 8dp grid
		- Keylines can be used to consistently line up other elements
		- Keylines can be adjusted to create more or less space between elements
* Containers are adjustable shapes that are used to hold UI elements like text or buttons.
* To maintain consistency of the layout, try to use consistent aspect ratios .
* Flexible ratios can be used with containers to match columns and image height.
* Touch targets (is the interaction area of a touch UI element) should be 48 x 48dp with 8dp padding to make it easier to press the item, I suppose.

### :octocat: Activity 0401:
>_"Choose a mobile app (Android or iOS) that you use frequently. Characterize the app's navigational model by examining how the user traverses through different activities (i.e. 'screens') in the app. Is the navigational model flat? (Meaning all activities have the same level of importance, perhaps each activity is accessible by swiping left or right?) Is there a hierarchical relationship between activities? (Meaning, is there a central, or main screen from which all other activities are accessed?) Discuss your findings in your Process Portfolio."_

###### Chosen App - Meme Generator Free

<img src = "img\MemeGeneratorMainScreen.jpg" width = "200">

* The Main Activity displays the meme formats in a tile display. Though the user can swipe left and right, it does not start new activities, instead it cycles through different organizations of the memes. New is automatically displayed onCreate(), and the User can swipe through Favorite, Popular, etc.

* The Memes Activity IS the Main Activity and from there the other activities can be selected, and it is a two step process. The user must click the Navigation Drawer and then they must click which activity they would like to open. This is probably a good plan when design is less of a concern than functionality and the large majority of the actions in the app will be started in the Main Activity.

<img src = "img/MemeGeneratorNavigationBar.jpg" width = "200">

* The Navigation Drawer directs the user to different activities which are organized into two categories, Create Memes and Other.

* The Create Memes category is positioned higher in the overflow list, so it appears to have a higher importance or at least a higher relevance.

<img src = "img/MemeGeneratorIThinkIAmFunny.jpg" width = "200">

* It should be noted that when a meme is selected, a new activity is opened that has a larger version of the meme with various edit options.


### :octocat: Activity 0402:
>_"After reading chapters 4.3 - Multiple activities and intents and 4.4 - Implicit intents of the textbook choose a mobile app (Android or iOS) that you use frequently and characterize all possible uses of intents in the app. Which other apps can be opened from your chosen app? Be thorough, and make sure you identify all possibilities. (Note that we do not refer to these as intents in iOS, but the distinction is not important here)."_

###### Chosen App - Meme Generator Free

<img src = "img/MemeGeneratorNavigationBar.jpg" width = "200">

* Categorically, the Create Memes options in the Navigation Drawer call internal intents (explicit intents for other activities in the same application).

<img src = "img/MemeGeneratorSavedMemes.jpg" width = "200">
<img src = "img/MemeGeneratorEditableTemplates.jpg" width = "200">
<img src = "img/MemeGeneratorVideoMemes.jpg" width = "200">
<img src = "img/MemeGeneratorBackgrounds&Grids.jpg" width = "200">

* Saved/Memes/ Combine, Editable Templates, Video Memes, Background & Grids, and Custom Memes all start their appropriate in-app activities.
*	In the Other section of the Navigation Drawer is where many actions that use intents for external applications can be found.
*	There are several examples of implicit intents or actions that attempt to open activities in other already installed applications:

<img src = "img/MemeGeneratorEmailIntent.jpg" width = "200">
<img src = "img/OutlookWriteEmailActivity.jpg" width = "200">


* The email option recommends several applications in which to complete the action and, as expected, extra information is include. With the intent is included, the to address and subject.
(This extra information is called Activity Startup Data and it can be added as a URI in the Intent constructor parameter or it can be added to the intent with the .putExtra method)

<img src = "img/GooglePlayRateMemeGenerator.jpg" width = "200">

*	The Rate App option is an example of explicit intent as it directly opens the google play store activity for rating this app. It appears that the Activity Startup Data contains the exact information for finding this app in the google play store.

*	Share App option is an implicit intent that generates several different social media messaging app options that are available to complete the action.
*	The GIF (pronounced with a hard G) Memes (Pronounced not like a crazy person) option in the Create Memes Category has an explicit intent which opens the Tenor gifs activity, but I am not sure if this is part of the Meme Generator app or if it is external.


### :octocat: Activity 0403:
>_"After reading chapter 4.5 - App Bar visit material.io and read the article App bars: Bottom. After reading the article summarize the differences between the use of top and bottom app bars in your Process Portfolio."_

**TOP** | **BOTH** | **BOTTOM**
--------|----------|-----------
Top Bars are considered with the principles of Persistent, Guiding, and Consistent| Both bars should locate the navigation drawer on the far left (but only on one of the bars at a time if the app is using a top bar and a bottom bar such as Instagram)| Bottom Bars are considered with the principles of Actionable, Flexible, and Ergonomic
There are two _types_ of top bars to consider, regular bars and contextual bars (bars that pop up to help execute certain actions based on context)| Both bars can contain an Overflow Menu and Action Items which are normally located on the right (while using a FAB on a secondary screen, the action icons are on the left and the navigation drawer disappears)|It is common to have a Floating Action Button (FAB) on a bottom bar.
A top bar can contain a title (or an action name in the case of a contextual bar)|Both bars can be hidden in relation to scrolling (where scroll direction affects when and how the bar is hidden)|When debating which action buttons should be placed where, most common actions should be placed where they are the easiest to access… at the bottom
Two heights are available for mobile. Regular and Prominent| The overflow menu should be the last option on the right whether it is a top bar or a bottom bar| Bottom bars should be covered by temporary surfaces
It is common to display images in a Prominent style top bar background as long as they don’t interfere with the visibility of the icons or text|:octocat:|:octocat:
When debating which action buttons should be placed where, destructive actions should be harder to reach and thus on the top bar|:octocat:|:octocat:

### :octocat: Activity 0501:
>_"Choose a mobile app (Android or iOS) that you use frequently. For this activity you will characterize the app's navigational model (similar to activity 0401), but in this case you will draw a diagrammatic representation of the navigation. You may use the same app chosen for activity 0401. Include an image of your drawing in your Process Portfolio and briefly describe what you have learned from this activity."_
###### Chosen App - Meme Generator Free
<img src = "img\MemeGeneratorMainScreen.jpg" width = "200">

Refer to Activity 0401 for more images of the app.

**Figure 0501.1 Meme Generator Navigation Logic**
![Meme Generator Navigation Logic](img/MemeGeneratorNavigationLogic.jpg)

I have learned through this exercise, that this app is a bit difficult to follow. The categories make sense but only after speculation. This app could/could’ve probably benefit/ed from more layout design. There are a couple way that I would improve the layout.  I think I would try to organize the activities that lead to the Meme Editor together and in their own category. They could have used tabs, but the tabs are used to scroll horizontally through the different orderings of the meme lists (Top, popular, new, etc.). This app is not as clean overall as I would like it. The “Merch Store”, “Email”, “Rate App”, “More Apps”, and “Share App” would probably be better suited hidden away in “About” with “About” having a child activity as opposed to a dialog. “Video Memes” and “GIF Memes” are better suited in an extra category as they don’t quite fit with the other activities of similar importance.

### :octocat: Activity 0502:
>_"After reading chapters 5.5 -Handling touch and 5.6 -Touch gestures choose a mobile app (Android or iOS) that you use frequently and list all touch events and touch gestures used in the app. Be thorough and make sure you consider testing events and gestures you might not commonly use. Feel free to check your app's 'how to' manual (if such a thing exists). Summarize your findings in your Process Portfolio."_

###### Chosen App - Adidas Run
<img src = "img\AdidasMainActivity.jpg" width = "200">

**TOUCH EVENTS**| **EXAMPLE**
----------------|-------------
Tap | Tap is equivalent to a mouse button click and is the basis for all user interaction in mobile apps.
Double Tap | N/A :octocat:
Long Press | This event is usable on the text views that display the workout stats. It allows the user to change the metric this is displayed in each text view.
Scroll | This is used to scroll vertically through any of the activities that need to be scrolled through. For example, “Activity Setup”.
Pinch & Spread | These two events are used to zoom in and zoom out of the map that displays the user’s location.
Drag | This event is used to move that map. It a useful gesture as the user does not need to zoom out again to see other areas of the map.
Fling | N/A :octocat:

### :octocat: Activity 0503:
>_"After reading chapter 5.3 -Dialogs visit material.io and read the article Dialogs. As you read carefully consider when the use of dialogs is appropriate. Summarize your findings in your Process Portfolio."_

Dialogs in general are designed to force the attention of the user to critical information. The term used in the article for dialogs is modal window as the dialog is a child of the activity behind it.

There are four categories of dialogs according to the material.io:

* Alert Dialogs are meant to be used when information is important and the user should be interrupted from continuing. Alert dialogs should be used sparingly as they are meant to convey the most crucial of information. Overusing the alert dialog format might cause the user to ignore alert dialogs over time.

* Simple Dialogs are meant to display a list of items that will affected by the user’s recent/current decisions. This a good alternative to an alert dialog as it simply informs the user of the changes that have or are about to occur.

* Confirmation Dialogs are meant for decisions. They can replace in-screen selectors like radio buttons. A choice should be confirmed before the dialog disappears. Confirmation dialogs are similar to simple dialogs but require a confirmation button to be pressed. A negative action button should also be included.

* Full Screen Dialogs are meant for a series of tasks. Full screen dialogs are the only type of dialogs that can display another type of dialog. Full screen dialogs take up the full screen, and they should be used with dialogs that use a keyboard or when the changes aren’t instantly saved. In my opinion, Full Screen Dialogs look like a great alternative to new activities.
