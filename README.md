Android Intents
===============

A small library which will save you from writing the same intent creation code again and again for the most simple tasks. I found myself writing my own 
library to create some common intents I was using across projects, so we decided to push that code to a project everyone could contribute to.

You can find a comprehensive list of all intents that can be used in the sample application. Here are some sample methods to show you how to do some 
simple things:

- Email intents:

    `EmailIntents.newEmailIntent( "me@example.com", "My subject", "Hey there!" )`

- Phone intents:

    `PhoneIntents.newDialNumberIntent(null)`

    `PhoneIntents.newCallNumberIntent("+123456789")`

    `PhoneIntents.newDialNumberIntent("+123456789")`

    `PhoneIntents.newSmsIntent("+123456789", "this is a test SMS")`

    `PhoneIntents.newSmsIntent("this is a test SMS")`

    `PhoneIntents.newPickContactIntent()`

    `PhoneIntents.newPickContactWithPhoneIntent()`
	
- Geo intents:

    `GeoIntents.newMapsIntent( "Musée du Louvre 75058 Paris", "Le Louvre" )`

    `GeoIntents.newMapsIntent( 43.481055f, -1.561959f, "My label for that place" )`

    `GeoIntents.newStreetViewIntent( 43.481055f, -1.561959f )`

    `GeoIntents.newNavigationIntent( "1 rue du Louvre 75058 Paris, France" )`
	
- System intents:

    `SystemIntents.newMarketForAppIntent( getApplicationContext() )`

- Media intents:

    `MediaIntents.newPlayYouTubeVideoIntent("b_yiWIXBI7o")`

	`MediaIntents.newPlayImageIntent("http://upload.wikimedia.org/wikipedia/commons/thumb/a/a9/Biarritz-Plage.JPG/1920px-Biarritz-Plage.JPG")`

    `MediaIntents.newPlayAudioIntent("http://www.stephaniequinn.com/Music/Allegro%20from%20Duet%20in%20C%20Major.mp3")`

    `MediaIntents.newPlayVideoIntent("https://www.youtube.com/watch?v=b_yiWIXBI7o")`

    `MediaIntents.newOpenWebBrowserIntent("http://vincentprat.info")`

    `MediaIntents.newTakePictureIntent(Environment.getExternalStorageDirectory().toString() + "/temp.jpg")`

    `MediaIntents.newSelectPictureIntent()`
	
This project has now been initiated with a few intents but we are looking forward to integrating your own intents to ease each developer's life.

Some rules for contributors: 

- If the intent you are creating does not fit into any of the provided utility classes (EmailIntents, GeoIntents, ...), do not hesitate to create your own. 
Those classes are meant to be simple factories with only static methods.
- If the intent you are creating is specific to an application (like a particular Twitter client), please put the utility class in a sub-package named after 
that application.

