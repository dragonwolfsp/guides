In this guide, you will learn how to use OBS Studio to monitor the output of any microphone that is connected to your computer, as well as route your audio, with no lag what soever!

<!--more-->

## Important disclaimers

This is only for Windows, and guides for Mac and Linux will most likely not be written, as I have no idea how to achieve this on those platforms.

This guide assumes you have OBS Studio and some routing solution already installed, and this topic will not be covered. If help is needed, feel free to contact me with the information found on the [contact page.](https://jonathanr.me/contact-information/)

## What you will need

You will need the [Audio Monitor plugin](https://obsproject.com/forum/resources/audio-monitor.1186/version/5987/download?file=109924) and the [win-capture-audio plugin](https://github.com/bozbez/win-capture-audio/releases/download/v2.2.3-beta/win-capture-audio-2.2.3-beta-setup.exe), as these plugins do most of the work when it comes to routing the audio.

As of OBS Studio 28 and later,  the windows audio capture is built in, but does not allow for us to click the checkbox to capture all audio except sessions from the selected executables. This is why you need the third party plugin that allows for this.

## Setting up the plugins

Extract the Audio Monitor archive, run the Audio Monitor setup, and go through the installer wizard.

Run the win-capture-audio setup, and go through the installer wizard.

## Creating the microphone and routing sources

Each microphone and your route needs their own sources, and creating those sources will be explained.

Once you create and configure the source and audio monitor for your first microphone, repeat the same process for each other microphone that you intend to use with this setup.

## Creating the first microphone source

Step 1: Press tab until you find sources window, list. If you are not seeing this, press tab until you find the unlabeled space after the scenes window.

Step 2: Press shift f10/applications, use your arrow keys until you find add collapsed, and press enter. Then press enter on audio input capture.

Step 3: Give the source a name of your choice. I would recommend naming it based on which microphone you are using with this source.

Step 4: Press enter to save your changes. If you forgot to name it, press tab or shift tab until you find sources list, window, or the unlabeled space after the scenes window, and press f2 on  the unlabeled source and give that source a new name.

### Configuring the first microphone source

Step 1: Press tab until you find sources window, list. If you are not seeing this, press tab until you find the unlabeled space after the scenes window.
  
Step 2: Use your arrow keys until you find the source you want to edit. If this is your first source, it will automatically be selected.

Step 3: Press tab until you find the device combo box, and use your arrow keys until you find the microphone you want to use with this source.

Step 4: Press tab or shift tab until you find sources list, window, or the unlabeled space after the scenes window. Once there, use your arrow keys until you find the source you want to edit. If you are not seeing your source name, you will be highlighted on the first source.

Step 5: Press shift F10/applications, use your arrow keys until you find filters, and press enter.

Alternatively, press tab until you find the properties for your source name button, press space, use your arrow keys until you find filters, and press enter.

Step 6: Press the tab key until you find the add button. Press space, and down arrow and press enter on audio monitor.

Step 7: Give the audio monitor a name, or leave it at its defaults.

### Configuring the audio monitor

Step 1: Press tab until you find sources window, list. If you are not seeing this, press tab until you find the unlabeled space after the scenes window.

Step 2: Use your arrow keys until you find the source you want to edit. If this is your first source, it will automatically be selected.

Step 3: Press shift F10/applications, use your arrow keys until you find filters, and press enter.

Alternatively, press tab until you find the properties for your source name button, press space, use your arrow keys until you find filters, and press enter.

If you are still in the same window from configuring the microphone source, don't worry about the steps above.

Step 4: Your system should focus on the list of filters, and the unlabeled list items are in order in which you created the filters. The first and only item is your monitor. Find the first and only unlabeled list item, and press tab until you find the combo box containing your sound devices. Use your arrow keys until you find your routing solution soundcard. VB cable and virtual audio cable are the most common.

Step 5: You should still be focused on the monitor filter, and press tab until you find the combo box that says not linked. Use your arrow keys until you find linked to deactivated from the main view (not visible on stream/recording). This means when you mute a source, it will show/hide, as well as mute the monitor since it is linked to the source. An example is the monitor gets muted when the source gets muted. We use show/hide because it reloads the source each time, avoiding sources getting out of sync.

Once done, press  enter or escape to save your changes.

## Configuring the ability to monitor your microphone through your headphones(optional)

Step 1: Press tab until you find the properties for your source name button, press space, use your arrow keys until you find advanced audio properties, and press enter.

Step 2: Press tab until you find the audio monitoring for source name combo box, and use your arrow keys until you find monitor and output.

Once done, press  enter or escape to save your changes.

## Creating the routing source

This source relies on the third-party win-capture-audio plugin, and only routes all applications. This does not route your whole system. An example is it won't route Windows UI sounds.

Step 1: Press tab until you find sources window, list. If you are not seeing this, press tab until you find the unlabeled space after the scenes window.

Step 2: Press shift f10/applications, use your arrow keys until you find add collapsed, and press enter. Then press enter on application audio output capture. Do not press enter on the one that says BETA.

Step 3: Give the source a name of your choice.

Step 4: Press enter to save your changes. If you forgot to name it, press tab or shift tab until you find the sources list, window, or the unlabeled space after the scenes window, and press f2 on the unlabeled source and give that source a new name.

### Configuring the routing source

Step 1: Press tab until you find the sources window, list. If you are not seeing this, press tab until you find the unlabeled space after the scenes window.

Step 2: Use your arrow keys until you find the routing source in the list.

Step 3: Press shift F10/applications,          use your arrow keys until you find properties, and press enter.

Alternatively, press tab until you find the button that says properties for your source name, press space, use your arrow keys until you find properties, and press enter.

Step 4: Press tab until you find the Capture all audio EXCEPT sessions from the selected executables checkbox. Press space to check this checkbox.

When you check this checkbox, it will route all applications except those that are excluded.

Step 5:: Press tab until you find the combo box that says add from currently active sessions, and add the applications you want excluded from the route. Make sure to exclude communication applications and OBS Studio to prevent loopback problems.

Once you are focused on the application you want excluded, press tab until you find the add executable button, and press space. You press the add executable button for each application you want added to the list.

Note: You will have to alt tab out and back into the window after each time you press the add executable button.

Once done, press  enter to save your changes.

### Creating and configuring the audio monitor

Step 1: Press tab or shift tab until you find the sources list, window, or the unlabeled space after the scenes window.

Step 2: Use your arrow keys until you find the routing source in the list.

Step 3: Press shift F10/applications, use your arrow keys until you find filters, and press enter.

Alternatively, press tab until you find the button that says properties for your source name, press space, use your arrow keys until you find filters, and press enter.

Step 4: Press the tab key until you find the add button. Press space, and down arrow and press enter on audio monitor.

Step 5: Give the audio monitor a name, or leave it at its defaults.

Step 6: Your system should focus on the list of filters, and the unlabeled list items are in order in which you created the filters. The first and only item is your monitor. Find the first and only unlabeled list item, and press tab until you find the combo box containing your sound devices. Use your arrow keys until you find your routing solution soundcard. VB cable and virtual audio cable are the most common.

Step 7: You should still be focused on the monitor filter, and press tab until you find the combo box that says not linked. Use your arrow keys until you find linked to deactivated from the main view (not visible on stream/recording). This means when you mute a source, it will show/hide, as well as mute the monitor since it is linked to the source. An example is the monitor gets muted when the source gets muted. We use show/hide because it reloads the source each time, avoiding sources getting out of sync.

Once done, press  enter or escape to save your changes.

Now, in any communication application, change the input device to the routing solution soundcard you used for your audio monitors in your microphone sources and your routing source.

## Configuring global hotkeys

It's recommended to configure global hotkeys, so you can easily show/hide your microphone and routing sources as needed.

Step 1: press the alt key to go to the OBS file menu, use your arrow keys until you find settings, and press enter.

Step 2: Once in the settings window, press tab until you find the list of items, and press down arrow until you find hotkeys.

Press tab until you find show source name, and hide source name, and you do the global hotkey gesture you want to assign to that action.

Keep pressing tab until you find the okay button, and press space to save your changes. Do not use shift tab or arrow keys, otherwise it will add those as hotkeys. Be careful!

## Miscellaneous settings

You can optionally have obs minimize to the system tray, so I will explain how to do this.

Step 1: press the alt key to go to the OBS file menu, use your arrow keys until you find settings, and press enter.

Step 2: Press tab until you find the always minimize to system tray instead of task bar checkbox. Press space to check this checkbox.

Step 3: Press tab until you find the okay button, and press space to save your changes.

## Extra notes

If you're listening to your microphone through the Windows sound control panel, this is not needed, as you can optionally monitor the output of your microphone using this setup.

If your microphone source or your routing source stop working, sometimes you need to switch the device on the microphone source and the audio monitors to the right devices to get it working again.

## Credits

I would like to give a huge thanks to Ethan Jones for discovering how to do this. Without him, I don't think this guide would be written, so thank you so much dude!

Enjoy!