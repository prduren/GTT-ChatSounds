This script is used to give GoToTraining chat sounds (since GTT currently as of 11.18.21 does not have chat sounds).
The chat box is polled every second, and if a message comes in prior to when the check happens then a sound will go off.

	1. When in GoToTraining, Undock the Chat pane from the main GTT control center

	2. Once you have the chat pane where you want it, run the GTT_ChatSound.ahk script

	3. Press WindowsKey + P to pause and unpause the script. You'll almost definitely want to do this
		every time you're typing in the text box, otherwise the chat sound will go off every second.

Notes:
	- The script will be killed upon rebooting machine, or you can kill the process in Task Manager ("GTT_ChatSound.exe" or "AutoHotkey Unicode 64-bit" if you're running the .ahk instead)

	- The script is only checking the screen area where the chat box is, so if you pull up another window that covers up the chat box, the
	chat sounds will still go off. You'll need to just leave the chat box where it is without covering it up during training

If you want to edit the script:

	1. Obtain AutoHotkey (it's on a drive somewhere...)

	2. Edit .ahk file (Notepad/Notepad++(also on a drive somewhere))

	3. Either run the .ahk file instead of the .exe every time, or right-click .ahk file > Compile Script to make another .exe with your changes

	- If you would rather not pause the script every time you type in the chatbox, you can instead change the "Sleep 1000" (1 second)
	on line 65 to "Sleep 10000" (10 seconds), or any other amount of milliseconds. Although this will still make the chat noise
	every 10 seconds when you're typing in the GTT chat box, it'll be less annoying than every 1 second. This will still check 
	for chat messages, but it'll just check every 10 seconds instead of every second. 

	- Since the sound that plays is just a .wav in C:/Windows/Media (path should be the same on your machine), you can switch 
	"Speech Sleep.wav" out on line 66  in the .ahk with any other sound you like in that Media folder.