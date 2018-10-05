# Watchfaces

AndroidAPS is designed to be *controlled* by Android Wear watches. To achieve this you needed to select the build variant "fullRelease" when [building the APK](../Installing-AndroidAPS/Building-APK.md) (or "pumpRelease" will allow you to just remote control the pump without looping). Within AndroidAPS, in the ConfigBuilder you need to enable Wear. You can access the setting by clicking on the cog. If you want to bolus etc from the watch then within Wear Setting you need to enable "Controls from Watch".

There are several watchfaces to choose from that include average delta, IOB, currently active temp basal rate and basal profiles + CGM readings graph. You can also use the AAPS app on the watch to set a temporary target, administer a bolus, use the bolus wizard, prime/fill, and check the status of loop and pump. Ensure notifications from AndroidAPS are not blocked on the watch. Confirmation of action (e.g. bolus, tempt target) comes via notification which you will need to swipe and tick. To get faster to the AAPS menu, do a double tap on your BG. When doing a double tap onto the BG curve, it will show older/ just newer BG's.

## Troubleshooting the wear app:

* On Android Wear 2.0 the watch screen does not install by itself anymore. You need to go into the playstore on the watch (not the same as the phone playstore) and find it in the category apps installed on your phone, from there you can activate it. Also enable auto update. 
* Sometimes it helps to re-sync the apps to the watch as it can be a bit slow to do so itself: Android Wear > Cog icon > Watch name > Resync apps.
* Enable ADB debugging in Developer Options (on watch), connect the watch via USB and start the Wear app once in Android Studio.

## Legend AndroidAPSv2 watchface

![Legend AndroidAPSv2 watchface](../images/AAPSv2_Watchface_legend.png)

A - time since last loop run

B - CGM reading

C - minutes since last CGM reading

D - change compared to last CGM reading (in mmol or mg/dl)

E - average change CGM reading last 15 minutes

F - phone battery

G - BGI (blood glucose interaction) -> the degree to which BG “should” be rising or falling based on insulin activity alone.

H - actual basal rate

I - carbs (carbs on board | e-carbs in the future)

J - insulin on board (from bolus | from basal)

## View Nightscout data

If you are using another looping system and want to *view* your looping detail on an Android Wear watch, or want to watch your child's looping, then you can build/download just the NSClient APK. To do this follow the [build APK instructions](../Installing-AndroidAPS/Building-APK.md) selecting the build variant "NSClientRelease". There are several watchfaces to choose from that include average delta, IOB, currently active temp basal rate and basal profiles + CGM readings graph.

## Pebble

Pebble users can use the [Urchin watchface](https://github.com/mddub/urchin-cgm) to *view* looping data (if uploaded to nightscout), but you will not be able to interact with AndroidAPS through the watch. You can choose fields to display such as IOB and currently active temp basal rate and predictions. If open looping you can use [IFTTT](https://ifttt.com/) to create an applet that says if Notification received from AndroidAPS then send either SMS or pushover notification.