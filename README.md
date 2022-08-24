# Digital Audio Workstation (DAW)

![image](https://user-images.githubusercontent.com/73859429/186344505-053d4501-46f0-4160-ad5a-c8f6296bb79d.png)

## Code Working Functions:

* The user can upload an audio input file (eg., wav) from the computer's file system.
	- Name of Selected Audio file is displayed and plotting on graph	
	- Length of input audio file is displayed (in seconds)
  
* The user can apply the following to an input audio signal:
	- Fade-in/Fade-Out effect or both Fade-in & Fade-Out 
	  effects for default or specific time periods
	- Tremolo Effect with user selectable depth of amplitude
  	and frequency range with an option of choosing between 
  	different wave types (sine, square, sawtooth/triangle)
	- Rhythmic Auto Panning Effect with user selectable amplitude 
  	and frequency alongside a panning type (Linear, Square-Law, Sine-law)
  	and choice between left to right or right to left panning
	- Echo effect (Feedback Echo) with user selectable Echo Tempo (BPM)
  	and Note Division (length/division of echo)
	- Reverb effect with static/predetermined Impluse Response Audio 
  	used for convolution
* The user can save the modified audio with a user-defined file name
  (User cannot save file if the name is invalid or no input audio is present)
* User can apply effects and play the updated sound data, undo the last
  effect, tune the effect parameters, and reapply the effect algorithm
  (plot will show modified audio signal)
* User can click reset button to return all buttons/sliders and audio effects to default values
* User can stop the audio signal that is being played


## Code Limitations:

* Some of the effects are limited by their slider, limitations are set by us (range of slider values)
* Need the signal to have one column with all the data for us to apply the audio effects (size error if input is a 2D matrix/array)
  (some files contain layered audio, 2+ rows in input signal, we convert to 1 column signal before applying any effects)
* Need to apply the effects in a certain order in order for the code to work (need to maintain a certain number of columns to apply certain effects)
* The noteDIV is limited to only 5 different values to apply the echo effect (4 = whole, 2 = half, 1 = quarter, 0.5 = eighth, 0.25 = sixteenth)
* There are only 3 types of waves used to modulate the input signal, applying the tremolo effect (sine, square and triangle)
* Only three different type of panning available for auto-panning in the signal, which include linear, square-root and sine
* Two different type of fading choices provided, linear and exponential fading (S-curve & logrithmic fade is not included)
- The amplitude of the echo effect is set as a constant value
- Reverb has only 1 impulse response, pre-determined by us (hard coded)


## Suggested Future Work:

* Make a seperate function for all the audio effects for better presentation and simplicity of code representation
  * Add an undo button to go back to the previously selected/saved and played audio effect
	  (made a matrix to save all changes one by one and revert by calling previously saved column(s) of audio)
* Add an undo button to go back to the last saved setting/effects (when save button is clicked, all effect settings are saved until new audio file is saved)
* Be able to possibly identify effects applied to an uploaded audio signal 
* Add more effects and more variation to current effects such as sliders/text input for constant hard coded values and further variation in modulation waves
* Create user option to input impulse response if they want to test a different impulse for reverb effect on the input audio signal
* Look into possiblity of real-time signal processing user-interface
